[VosFactures](https://vosfactures.fr/) - Logiciel de Facturation en ligne
===========

## Menu
+ [Formats des factures (et autres documents de facturation)](#templates)  
     + [Principe](#main)
     + [Documentation](#more)
     + [Variables Handlebars](#variables)
+ [Formats des Emails](#emails)
+ [Fonctions disponibles dans les formats](#fct)
+ [Importations de données](#import)
+ [API](#api)

<a name="templates"/>

## Formats (templates) des factures
---------------
<a name="main"/>

## Principe
En utilisant notre logiciel de facturation, vous avez accès à un certain nombre de formats (mises en page) de factures et devis, que vous pouvez personnaliser via l'ajout de codes CSS. </br>
Toutefois, si l'un d'eux ne répond pas à vos attentes, <b>vous pouvez créer votre propre modèle</b>.</br></br> 
Pour cela, il vous suffit de vous connecter à votre compte (si vous n'êtes pas encore inscrit : https://app.vosfactures.fr/signup pour un essai gratuit), de cliquer sur Paramètres > Paramètres du compte > Formats des documents, puis de cliquer sur le bouton "Ajouter un nouveau format". Vous pouvez choisir le format par défaut que vous souhaitez modifier, comme expliqué ici: https://aide.vosfactures.fr/8631976-Cr-er-un-format-personnalis-

<a name="more"/>

## Documentation 

Vous trouverez sur Github la documentation de chacun des formats par défaut, c'est-à-dire la partie HTML et la partie CSS de chaque format. Les formats sont créés en HTML et CSS en utilisant [Handlebars](https://handlebarsjs.com/)

Les formats utilisent des fichiers partiels, représentés dans le code HTML par un tag {{>fichier_partiel}}. Ces fichiers partiels sont accessibles ici: https://github.com/vosfactures/Formats/tree/master/partials.

<a name="variables"/>

## Variables handlebars

Vous pouvez visualiser les données d'une facture en handlebars en ajoutant le suffixe <b>.handlebars</b> à l'url (ex: moncompte.vosfactures.fr/invoices/232342321.handlebars). <br/>
Les principales variables qui peuvent être utilisées dans les formats sont:
 
```htmlbars
{{document_type}} Type de document
{{kind}} - Type : "vat" pour facture, "estimate" pour devis, "proforma" pour facture proforma, "correction" pour avoir, "client_order" pour bon de commande de client, "maintenance_request" pour les bons d'intervention, "payment_receipt" pour les reçus de paiement, "advance" pour facture d'acompte", "final" pour facture de solde, "receipt" pour les reçus, "invoice_other" pour autre type de document comptable, "kw" pour versements en espèces, "kp" pour reçus en espèces.
{{number}} - Numéro du document
{{title}} - titre
{{created_at}}
{{issue_date}} - Date de création du document
{{issue_place}} - Lieu de création du document
{{today_date}}
{{print_option}} 
{{sell_date}} - Date additionnelle
{{sell_date_kind}} - Intitulé de la date additionnelle
{{today_date}} - Date du jour
{{invoice_category}} - Catégorie du document
{{lang}} - Langue du document
{{bilangual}} - Langues du document
{{currency}} - Devise du document
{{currency_symbol}} - Devise (symbole)
{{currency_short}} - Devise (abrégé)
{{cancel_reason}} - Raison de l'annulation
{{canceled}}
{{corrected_issue_date}}
{{corrected_kind}}
{{corrected_number}}
{{correction}} - Document corrigé
{{correction_reason}} - Motif de l'avoir
{{corrected_content_after}} - contenu avant correction
{{corrected_content_before}} - contenu après correction

* Concernant le département vendeur :
{{department}} - département/compagnie - les champs sont id, nom, type ... par ex: 
{{department.id}} - ID du département
{{department.kind}} - Forme juridique
{{department.name}} - Nom du département
{{company}} - Nom de la compagnie/département vendeur
{{department.tax_kind}} - type de n° fiscal (ex : "TVA")
{{seller_tax_no_kind}} - Type de numéro d'immatriculation (TVA, SIREN, CIF...)
{{department.tax_no}} - Numéro d'immatriculation (ex: n° TVA)
{{department.footer_kind}}
{{department.footer_content}} - contenu du bas de page
{{department.own_footer}} - bas de page personnalisé
{{department.capital}}
{{department.capital_kind}} - Capital social
{{department.capital_currency}} - Devise du Capital social
{{post_code}} - Code postal
{{street}} - Rue (numéro et nom)
{{place}} - Ville
{{country}} - Pays
{{address}} - adresse complète
{{www}} - Adresse internet
{{email}} - Adresse email
{{fax}} - Numéro de fax
{{phone}} - Numéro de téléphone
{{department.bank_account}} - Numéro de compte bancaire (RIB ou IBAN)
{{department.bank_iban}} - iban
{{department.bank_swift}} - Numéro BIC
{{department.bank_name}} - Domiciliation bancaire (nom de la banque)
{{bank}} - Domiciliation bancaire et numéro de compte
{{person}} - Nom/Prénom du vendeur

* Concernant le contact (client) :
{{buyer}} - Nom de l'acheteur
{{buyer_person}} - Nom (et prénom) de l'acheteur
{{buyer_company}} - Nom de la compagnie de l'acheteur professionnel
{{client.email}} - e-mail
{{client.first_name}} - Prénom
{{client.last_name}} - Nom
{{client.name}} - Nom de la compagnie
{{buyer_post_code}} - Code postal de l'acheteur
{{buyer_place}} - Ville de l'acheteur
{{buyer_street}} - Rue (numéro et nom) de l'acheteur
{{buyer_country}} - Pays de l'acheteur
{{buyer_tax_no}} - Numéro d'immatriculation (ex: n° TVA) de l'acheteur professionnel
{{buyer_tax_no_kind}} - Type de numéro d'immatriculation (TVA, SIREN, CIF...) de l'acheteur professionnel
{{buyer_phone}} - Numéro de tel de l'acheteur (correspond au champ "Téléphone" du contact)
{{buyer_mobile_phone}} - Numéro de tel portable de l'acheteur (correspond au champ "Tél. portable" du contact)
{{client.external_id}} - Réf/code de l'acheteur
{{use_delivery_address}} - Afficher l'adresse supplémentaire (ex: adresse de livraison)
{{delivery_address}} - Adresse supplémentaire
{{delivery_address_name}} - Nom de l'Adresse supplémentaire
{{show_buyer_note}} - Afficher la description additionnelle
{{buyer_note}} - Description additionnelle
{{client.accounting_id}} - compte comptable général
{{client.additional_accounting_id}}  - compte comptable auxiliaire
{{client.discount}} - Taux de réduction par défaut (en %)
{{{client_panel_view_link}}} - Espace Facturation
{{{client_panel_view_link_unpaid}}} - Espace Facturation (factures impayées)
{{client.panel_url}} - lien de l'espace facturation
{{show_client_phone_on_invoice}} - afficher le numéro de téléphone du client


* Concernant le tableau des produits/services :
{{use_product_code}} - Afficher la colonne Référence
{{show_product_description}} - afficher la description des produits
{{show_unit_price_gross}} - afficher le prix unitaire TTC
{{additional_info}} - Colonne additionnelle
{{additional_info_desc}} - Titre de la colonne additionnelle
{{discount}} - Réduction (montant)
{{total_discount}} - Réduction globale (montant)
{{global_discount_percent}} - Réduction globale (en %)
{{show_discount}} - Afficher la colonne réduction
{{hide_tax}} - Afficher les montants TTC uniquement 
{{tax_visible}} - Afficher la colonne taxe
{{tax_name}} - Nom de la Taxe
{{tax2_visible}} - Afficher deuxième colonne taxe
{{tax2_name}} - Nom de la deuxième Taxe
{{tax_value_name}} - Total des Taxes 
{{#each positions}}  - ligne des tableaux :
  {{no}} - Numéro de ligne
  {{kind}} - Type de ligne (ligne de produit ou ligne de texte)
  {{code}} - Référence du produit
  {{supplier_code}} - Référence fournisseur du produit
  {{barcode}} - code-barre du produit
  {{ean_code}} - code ean  du produit
  {{item}} - Nom du produit
  {{item_url}}
  {{description}} - Description du produit
  {{image_url}} - Photo du produit
  {{additional_info}} - Colonne additionnelle 
  {{discount}} - Réduction
  {{has_discount}}
  {{discount_amount_gross}} - Réduction montant TTC
  {{discount_amount_net}} - - Réduction montant TTC
  {{quantity}} - Quantité
  {{quantity_number}}
  {{quantity_unit}}  - Unité
  {{positions_total_quantity}} - Total des quantités
  {{unit_price_net}} - Prix unitaire ht
  {{unit_price_gross}} - Prix unitaire ttc
  {{unit_price_net_with_discount}} - Prix unitaire ht après réduction
  {{unit_price_gross_with_discount}} - Prix unitaire ttc après réduction
  {{positions_total_price_net}} - Total HT de la ligne
  {{positions_total_price_gross}} - Total TTC de la ligne
  {{positons_total_tax}} - Total taxe de la ligne
  {{tax}} - taux de taxe
  {{tax2}} - taux de la deuxième taxe
{{accounting_activity_code}} - Code Activité du produit 
{{accounting_code_expenses}} - Compte comptable du produit (charges)
{{accounting_code_sales}} - Compte comptable du produit (produits)
{{accounting_code_income}}
{{accounting_code_tax_purchase}} - Compte comptable taxe achat 
{{accounting_code_tax_sale}} - Compte comptable taxe vente
{{/each}}



* Concernant les Totaux :
{{#each summary}} - résumé des totaux :
  {{total_price_net}} - Total HT du document
  {{total_price_gross}} - Total TTC du document
  {{tax}} - Taux de taxe
  {{tax2}} - taux de la deuxième taxe
  {{tax_name}} - Nom de la taxe
 {{tax2_name}} - Nom de la 2ème taxe
  {{tax_value}} - Montant total des Taxes du document
  {{tax_value_name}} 
  {{tax1_value_name}} - Montant total de la 1ere Taxe du document
  {{tax2_value_name}} - Montant total de la 2ème Taxe du document
  {{total_price_net_without_discount}} - Total HT avant réduction
  {{total_price_gross_without_discount}} - Total TTC avant réduction
  {{global_discount_net}} - Montant total HT de la réduction
  {{global_discount_gross}} - Montant total TTC de la réduction
{{/each}}
{{{positions_total_quantity_separated}}} - Quantité totale (distinguée par unité différente) du document
{{total_price_net_with_currency}} - Total HT avec devise du document
{{total_price_gross_with_currency}} - Total TTC avec devise du document
{{tax_value_with_currency}} - Montant des Taxes avec devise du document
{{show_totals}} - Afficher un résumé du total net, brut et de la taxe
{{show_tax_split}} - afficher le résumé des différents taux de taxe
{{exchange_currency}} - Convertir en
{{exchange_currency_rate}} - Taux de change du document
{{exchange_note}} - Note sur le taux personnalisé
{{exchange_date}} - Date de la conversion
{{exchange_rate}} - Taux de change (utilisé dans les rapports)
{{long_exchange_note}} - Taux de change appliqué
{{total_price_net_in_main_currency}} - Total HT avec devise principale
{{total_price_gross_in_main_currency}} - Total TTC avec devise principale
{{total_price_net_in_exchange_currency}} - Total HT avec devise de conversion
{{total_price_gross_in_exchange_currency}} - Total TTC avec devise de conversion
{{tax_value_in_exchange_currency}} - Montant de taxe avec devise de conversion
{{outstanding}} - Montant total à payer (en chiffres)
{{outstanding_in_exchange_currency}} - Montant total converti à payer (en chiffres)
{{outstanding_in_words}} - Montant total à payer (en lettres)
{{outstanding_in_words_in_exchange_currency}} - Montant total converti à payer (en lettres)
{{all_in_words}} - Montant Total à payer (en lettres)
{{all_in_words_in_exchange_currency}} - Montant total à payer converti (en lettres)
{{negative_outstanding}} - Solde en votre faveur (en chiffres)
{{absolute_outstanding}} -  Montant total à payer en valeur absolue (en chiffres)
{{absolute_outstanding_in_words}} - Montant total à payer en valeur absolue (en lettres)
{{absolute_outstanding_in_exchange_currency}} - Montant total à payer converti
{{absolute_outstanding_in_words_in_exchange_currency}} - Montant total à payer converti (en lettres)

* Concernant les modalités de paiement :
{{paid}} - Montant payé
{{status_paid}} - Etat Payé ou non du document
{{oid}} - Numéro de commande du document
{{payment_to}} - Date limite de règlement
{{type_of_payment}} - Mode de règlement
{{show_paid_date}} - afficher la date de paiement
{{paid_date}} - date de paiement
{{payment_link}} - Lien vers Paiement en ligne (lien direct permettant au client de payer en ligne la facture)
{{payment_button_url}} - 
{{transaction_id}} - ID de la transaction
{{token}} - Code du paiement en ligne
{{show_paid_logo}} - afficher le tampon "Payé"
{{paid_mark_url}} - url du tampon vert "Payé"

* Concernant les autres éléments du document :
{{notes}} - informations spécifiques
{{conditional_notes}} - notes conditionnelles
{{additional_field_name}} - titre du champ additionnel
{{additional_field_value}} - contenu du champ additionnel
{{logo_url}} - Url du logo
{{stamp_url}} - Url du tampon
{{stamp_below_sign_url}} - Url du tampon sous le nom du vendeur
{{show_date_and_sign}} - Afficher la mention " Date et signature du client..."
{{description_long}} - Texte additionnel (imprimé sur la page suivante du document)
{{description_footer}} - Bas de page du document
{{view_url}} - URL du lien vers l'aperçu du document
{{view_link}} - Lien vers l'aperçu du document
{{final}} - Facture de Solde
{{advanced}} - Facture d'Acompte
{{advanced_num}} - Nombre de factures d'acompte liées à une facture finale
{{income}} - Revenu
{{footer}} - Bas de page (des emails)
{{client}} 
{{sales_code}}
{{locale}}

```


<a name="emails"/>

## Format des emails
---------------
Le système propose par défaut un contenu pour l'envoi des documents de facturation, et un contenu pour l'envoi de relances en cas de factures impayées. Vous pouvez personnaliser le contenu des e-mails envoyés aux clients. Le texte des emails utilisent les mêmes variables que les formats (voir ci-dessus) et utilise aussi [Handlebars](http://handlebarsjs.com/).

Contenu par défaut de l'email accompagnant l'envoi des factures:
```htmlbars
Bonjour, 

Veuillez trouver en pièce jointe le document suivant: 
{{{document_type}}} numéro {{number}} d’un montant total de {{total_price_gross_with_currency}}. 

Vous pouvez également visualiser le document en cliquant sur le lien suivant: {{{view_link}}}  

{{footer}}
```

Contenu par défaut de l'email de relance en cas de factures impayées:
```htmlbars
Bonjour, 

Veuillez trouver en pièce jointe la {{{document_type}}} numéro {{number}} d’un montant de {{outstanding}} qui {{#if overdue}}reste à ce jour impayé.{{else}}arrive à échéance le {{payment_to}}.{{/if}}

Vous pouvez visualiser la {{{document_type}}} en cliquant sur le lien suivant: {{{view_link}}}

Dans l’attente de votre prompt règlement,

Bien cordialement,

{{footer}}
```

Vous pouvez également utiliser les variables suivantes pour vos emails de relance: 
```shell
{{inc reminder_no}} - numéro de la relance que vous envoyez, ie. N
{{reminder_no}} - nombre de relances jusque là envoyées, ie. N-1 par rapport à la relance que vous allez envoyer
{{dec reminder_no}} - nombre de relances jusque là envoyées, ie. N-2 par rapport à la relance que vous allez envoyer
```

<a name="fct"/>

Fonctions disponibles dans les formats de factures et des e-mails
---------------

Les formats peuvent inclure les fonctions suivantes:

```htmlbars
 if
  for
  eq
  not_eq
  lt
  gt
  or
  and
  tt
  include
  include_in_col
  in
  not_in
  to_uppercase
  replace
  inc
  dec
  abs
  if_created_after_date
  inline_partial
```

Exemple:

```htmlbars  
{{#if val1 }}
  ok
{{else}}
  not ok
}}

{{#lt val1 17 }}
  <17
}}

{{#gt val1 17 }}
  >17
{{else}}
 <17
}}

{{#eq department_id "123"}}
  info sur le département
{{else}}
  info sur les autres départements
{{/eq}}


{{#for size_from size_to}}
    numéro: {{no}}
{{/for}}

{{inline_partial "partial1" "{{document_type}} {{number}}: {{total_price_gross_with_currency}} {{tt 'invoice.gross'}}<br>"}}
{{>partial1}}

{{#inline_partial "partial2"}}
  {{#eq lang "fr"}}
    Bonjour,
  {{else}}
    Hello,
  {{/eq}}
  {{>partial1}}
{{/inline_partial}}
{{>partial2}}

```

<a name="import"/>

Importation de données
---------------

Il vous est possible d'importer dans votre compte VosFactures des données existantes depuis n'importe quel programme si celles-ci sont dans un fichier .TXT, .CSV, .XLS, .ODS, XLSX, .TSV, .XML.</br></br> L'importation de fichiers se fait depuis l'onglet Paramètres > Importation.</br> Vous pouvez importer des documents de facturation (factures, devis, dépenses...), des clients et fournisseurs, vos catalogues produits, et des relevés bancaires.</br> Durant l'importation, vous pouvez choisir quelles colonnes et lignes importer. Vous pouvez consulter les sujets d'aide dédiés: [Etapes de l'importation]( https://aide.vosfactures.fr/410101-Principe-et-tapes-de-l-importation) et [Conseils avant d'importer](https://aide.vosfactures.fr/748672-Export-Importation-de-vos-fichiers-vers-VosFactures-Quelques-conseils). 


<a name="api"/>

API
---------------

Consultez notre documentation [API de VosFactures](https://github.com/vosfactures/API).  

