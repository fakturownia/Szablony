[Fakturownia.pl](http://fakturownia.pl/) - faktury online
===========

Szablony faktur
---------------

Korzystając z naszego systemu do fakturownia, masz dostęp do kilku wzorów faktur. Jeśli któryś z nich nie spełnia twoich oczekiwań możesz
przygotować własny szablon. Wystarczy zalogować się do swojego konta (jeśli go jeszcze nie masz to
[tu możesz założyć darmowe konto](https://app.fakturownia.pl/signup) ) i wejść w Ustawienia > Ustawienia konta > Szablony. Następnie kliknij "dodaj nowy szablon" i otworzy się okno do edycji kodu, dzięki któremu możesz przygotować indywidualny szablon.



Przykładowe szablony Faktur:

HTML: https://github.com/fakturownia/szablony/blob/master/default.hbs.html

CSS: https://github.com/fakturownia/szablony/blob/master/default.css

Szablony są tworzone przy wykorzystaniu znaczników  [Handlebars](http://handlebarsjs.com/)

Zmienne których można używać w szablonach:

```htmlbars
{{absolute_outstanding}}
{{absolute_outstanding_in_exchange_currency}}
{{absolute_outstanding_in_words}}
{{absolute_outstanding_in_words_in_exchange_currency}}
{{accounting_doc}}
{{accounting_note_kind}} - podtyp
{{additional_address_seller_name}}
{{additional_field_name}}
{{additional_field_value}}
{{additional_info}}
{{additional_info_desc}} - dodatkowe pole na pozycjach faktury
{{address}}
{{advanced}}
{{advanced_num}}
{{advanced_total_price_gross}}
{{all_in_words}}
{{all_in_words_in_exchange_currency}}
{{bank}}
{{bank_account}}
{{bilangual}}
{{buyer}} - nabywca
{{buyer_address}}
{{buyer_bank_account}} - konto
{{buyer_company}} - firma
{{buyer_country}} - kraj
{{buyer_country_code}}
{{buyer_email}} - e-mail klienta
{{buyer_first_name}} - imię
{{buyer_last_name}} - nazwisko
{{buyer_mobile_phone}} - telefon komórkowy
{{buyer_note}} - dodatkowy opis
{{buyer_person}} - imię i nazwisko odbiorcy
{{buyer_phone}} - telefon klienta
{{buyer_place}}
{{buyer_post_code}} - kod pocztowy
{{buyer_register_number}} - regon
{{buyer_street}} - ulica i nr
{{buyer_tax_no}} - nip
{{buyer_tax_no_kind}} - rodzaj numeru identyfikacyjnego nabywcy
{{cancel_reason}} - powód anulowania faktury
{{canceled}}
{{client_external_id}}
{{{client_panel_view_link}}}
{{{client_panel_view_link_unpaid}}}
{{client_panel_view_url}}
{{client_url}}
{{company}}
{{corrected_content_after}} - treść prawidłowa
{{corrected_content_before}} - treść korygowana
{{corrected_issue_date}}
{{corrected_kind}}
{{corrected_number}}
{{correction}} - dokument korygowany
{{correction_reason}} - przyczyna korekty
{{country}}
{{created_at}} - utworzenie
{{currency}} - waluta
{{currency_short}}
{{currency_symbol}}
{{delivery_address}} - adresat
{{delivery_address_name}}
{{description_footer}} - dodatkowe uwagi (drukowane na dole strony)
{{description_long}} - dodatkowe uwagi (drukowane na drugiej stronie)
{{discount}} - rabat
{{discount_kind}}
{{document_type}}
{{email}}
{{exchange_currency}} - przeliczanie na walutę
{{exchange_currency_rate}} - kurs
{{exchange_date}}
{{exchange_note}} - notatka do kursu
{{exchange_tax}}
{{exempt_tax_kind}}
{{fax}}
{{final}}
{{footer}} - {:generated_in=>"wygenerowano w %{domain}", :page=>"strona", :page_of=>" z "}
{{forced_payment_to}}
{{from_recurring_payment}}
{{global_discount_gross}}
{{global_discount_gross_with_currency}}
{{global_discount_net}}
{{global_discount_net_with_currency}}
{{gocardless_subscription}} - włącz możliwość ustawienia płatności cyklicznej gocardless
{{gtu_codes_list}}
{{gtu_codes_note}}
{{has_corrected_content}}
{{hide_tax}} - ukryj podatek i cenę netto
{{id}}
{{income}} - przychód
{{internal_note}} - notatka prywatna (niewidoczna na wydruku)
{{invoice_category}}
{{issue_date}} - data wystawienia
{{issue_place}}
{{issuer}}
{{kind}} - typ
{{kpir_col}} - numer kolumny w księdze
{{kpir_pos}} - numer pozycji w księdze
{{lang}} - język
{{legal_cost_compensation}}
{{locale}}
{{logo_url}}
{{long_exchange_note}}
{{long_exchange_note_for_tax}}
{{negative_outstanding}}
{{notes}}
{{number}} - numer
{{oid}} - nr zamówienia
{{outstanding}}
{{outstanding_in_exchange_currency}}
{{outstanding_in_words}}
{{outstanding_in_words_in_exchange_currency}}
{{overdue}}
{{paid}} - kwota opłacona
{{paid_date}} - data płatności
{{paid_mark_url}}
{{payment_button_url}}
{{{payment_link}}}
{{payment_reference_number}} - numer polecenia zapłaty
{{payment_to}} - termin płatności
{{payment_url}}
{{payments}} - {:header=>"płatności", :by=>"przez"}
{{person}}
{{phone}}
{{place}} - miejsce wystawienia
{{positions_total_price_gross}}
{{positions_total_price_net}}
{{positions_total_quantity}}
{{positions_total_quantity_separated}}
{{positions_total_tax}}
{{positions_total_weight}}
{{positons_total_tax}}
{{post_code}}
{{prepayment_required}} - wymagana przedpłata (%)
{{prepayment_required_exact_amount}} - dokładna wartość
{{print_option}}
{{procedure_designations_list}}
{{procedure_designations_note}}
{{product_cache}}
{{proforma}}
{{qrcode_img}}
{{receipt}}
{{recipient_address}}
{{recipient_city}} - miejscowość
{{recipient_country}} - kraj
{{recipient_name}} - odbiorca
{{recipient_note}} - dodatkowy opis
{{recipient_phone}} - telefon
{{recipient_post_code}} - kod pocztowy
{{recipient_present}}
{{recipient_street}} - ulica i nr
{{recipient_url}}
{{reminder_no}} - liczba wysłanych przypomnień o niepłaconej fakturze
{{reminder_number}}
{{reverse_charge_code}} - kod transakcji
{{reverse_charge_cz}}
{{sales_code}}
{{sec_stamp_url}}
{{sell_date}} - data sprzedaży
{{sell_date_MY}}
{{sell_date_kind}}
{{seller_register_number}} - regon
{{seller_tax_no_kind}}
{{seller_trade_register_cz}} - informacje dotyczące wpisu do rejestru handlowego
{{should_print_gtu_codes}}
{{should_print_procedure_designations}}
{{show_buyer_note}}
{{show_date_and_sign}}
{{show_discount}}
{{show_empty_buyer_person}}
{{show_empty_seller_person}}
{{show_links}}
{{show_paid_date}}
{{show_paid_logo}}
{{show_paid_when_zero}}
{{show_payments_on_invoice}}
{{show_product_description}}
{{show_sell_date}}
{{show_tax_split}}
{{show_totals}}
{{show_unit_price_gross}}
{{sign_document_url}}
{{signature_date}}
{{signature_url}}
{{split_payment}} - mechanizm podzielonej płatności
{{split_payment_note}}
{{stamp_below_sign_url}}
{{stamp_url}}
{{status_paid}}
{{street}}
{{subscription_count}}
{{subscription_day_of_month}}
{{subscription_month}}
{{swift}}
{{tax2_details}}
{{tax2_name}}
{{tax2_visible}}
{{tax_in_exchange_currency}}
{{tax_name}}
{{tax_no}} - nip
{{tax_value}}
{{tax_value_in_exchange_currency}}
{{tax_value_in_exchange_currency_with_currency}}
{{tax_value_name}}
{{tax_value_with_currency}}
{{tax_visible}}
{{title}} - tytuł
{{today_date}}
{{token}}
{{total_discount}}
{{total_discount_in_exchange_currency}}
{{total_discount_in_exchange_currency_with_currency}}
{{total_discount_with_currency}}
{{total_price_gross}} - wartość brutto
{{total_price_gross_in_exchange_currency}}
{{total_price_gross_in_exchange_currency_with_currency}}
{{total_price_gross_in_main_currency}}
{{total_price_gross_with_currency}}
{{total_price_gross_without_discount}}
{{total_price_gross_without_discount_with_currency}}
{{total_price_net}} - wartość netto
{{total_price_net_in_exchange_currency}}
{{total_price_net_in_exchange_currency_with_currency}}
{{total_price_net_in_main_currency}}
{{total_price_net_with_currency}}
{{total_price_net_without_discount}}
{{total_price_net_without_discount_with_currency}}
{{total_tax_inscription}}
{{transaction_id}}
{{type_of_payment}}
{{use_barcodes}}
{{use_delivery_address}} - inny adres korespondencyjny
{{use_paid_dates}}
{{use_product_code}}
{{{view_link}}}
{{view_url}}
{{www}}
{{zero_with_currency}}
{{zero_with_currency_in_exchange_currency}}

{{#each final_summary}} :
{{tax}}
{{tax_value}}
{{tax_value_with_currency}}
{{total_price_gross}}
{{total_price_gross_with_currency}}
{{total_price_net}}
{{total_price_net_with_currency}}
{{/each}}

{{#each positions}} :
{{accounting_activity_code}}
{{accounting_code_expenses}}
{{accounting_code_income}}
{{accounting_code_sales}}
{{accounting_code_tax_purchase}}
{{accounting_code_tax_sale}}
{{additional_info}} - wartość dodatkowego pola na pozycjach faktury
{{additional_info_desc}}
{{barcode}}
{{code}} - kod produktu
{{description}} - opis
{{discount}} - kwota rabatu
{{discount_amount_gross}}
{{discount_amount_net}}
{{ean_code}}
{{gtu_code}} - kod gtu
{{has_discount}}
{{image_url}}
{{item}} - nazwa produktu/usługi
{{item_url}}
{{kind}} - rodzaj pozycji
{{no}}
{{quantity}} - ilość
{{quantity_number}}
{{quantity_unit}} - jednostka
{{supplier_code}}
{{tax}} - stawka vat
{{tax1_value_name}}
{{tax2}} - stawka vat
{{tax2_name}}
{{tax2_value_name}}
{{tax_name}}
{{tax_value}} - wartość vat
{{tax_value_name}}
{{total_price_gross}} - wartość brutto
{{total_price_gross_without_discount}}
{{total_price_net}} - wartość netto
{{total_price_net_without_discount}}
{{unit_price_gross}}
{{unit_price_gross_with_discount}}
{{unit_price_net}}
{{unit_price_net_with_discount}}
{{/each}}

{{#each summary}} :
{{tax}}
{{tax_value}}
{{tax_value_with_currency}}
{{total_price_gross}}
{{total_price_gross_with_currency}}
{{total_price_net}}
{{total_price_net_with_currency}}
{{/each}}

{{additional_fields}} :
{{additional_fields.seller_bank_swift}}
{{additional_fields.tax_name}}
{{additional_fields.tax_name_type}}

{{client}} :
{{client.accounting_id}} - identyfikator w programie księgowym
{{client.additional_accounting_id}}
{{client.discount}} - domyślny rabat %
{{client.email}} - e-mail
{{client.first_name}} - imię
{{client.last_name}} - nazwisko
{{client.name}} - nazwa firmy
{{client.panel_link}}
{{client.panel_link_unpaid}}
{{client.panel_url}} - link do panelu klienta

{{department}} :
{{department.bank_account}} - konto bankowe
{{department.bank_iban}} - iban
{{department.bank_name}}
{{department.bank_swift}} - swift
{{department.capital}}
{{department.capital_currency}}
{{department.capital_kind}} - kapitał zakładowy
{{department.footer_content}} - treść stopki
{{department.footer_kind}}
{{department.id}}
{{department.kind}} - forma prawna
{{department.name}} - nazwa firmy lub działu
{{department.own_footer}} - własna treść stopki
{{department.tax_kind}} - nr nip
{{department.tax_no}} - numer nip

{{subscription_interval_unit}} :
{{subscription_interval_unit.monthly}} - co miesiąc
{{subscription_interval_unit.weekly}} - co tydzień
{{subscription_interval_unit.yearly}} - co rok

{{footer}}
```




Szablony e-maili
---------------
Można tworzyć szablony e-maili które będą wysyłane do klientów. Są 2 szablony dla standardowego wysyłania faktury oraz
do wysyłania przypomnień o niezapłaconych fakturyach. Tworząc szablony używa się tych samych zmiennych co przy szablonach
faktrur i korzysta się także z [Handlebars](http://handlebarsjs.com/).

Domyślne szablon wysyłania faktur:
```htmlbars
Dzień dobry,

dziękujemy za skorzystanie z naszych usług.
Załączam dokument {{document_type}} {{number}} na kwotę {{total_price_gross}} brutto.

Link do podglądu {{view_url}}


{{footer}}
```

Domyślne szablon przypomnienia o niezapłaconej fakturze:
```htmlbars
Dzień dobry,

przypominamy o zaległej płatności za {{document_type}} {{number}} na kwotę {{total_price_gross}} brutto.

Link do podglądu: {{view_url}}

{{footer}}
```


Funkcje dostępne w szablonach faktur i e-maili
---------------

w szablonach dostepne są następujące funkcje:

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

Przykład wywołania funkcji:

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
  info dla danego departamentu
{{else}}
  info dla innych departamentow
{{/eq}}

{{#for size_from size_to}}
    no: {{no}}
{{/for}}

{{inline_partial "partial1" "{{document_type}} {{number}}: {{total_price_gross_with_currency}} {{tt 'invoice.gross'}}<br>"}}
{{>partial1}}

{{#inline_partial "partial2"}}
  {{#eq lang "pl"}}
    Dzień dobry,
  {{else}}
    Hello,
  {{/eq}}
  {{>partial1}}
{{/inline_partial}}
{{>partial2}}
```


Import danych
---------------

Możliwy jest import danych z dowolnych programów które zapiszą dane do plików  .TXT, .CSV, .XLS, .ODS, .XLSX, .TSV, .XML
Podczas importu samodzienie można ustawiać jakie kolumny i wiersze są importowane.

Można importować Faktury, Klientów, Produkty

Dodatkowo dostępne są opcje importu: Sprzedaż na ALLEGRO.PL (XML), Zakupy w ACTION S.A. (CSV), Zakupy w ABC DATA S.A. (XML), Faktury, klienci i produkty z CDN optima


API
---------------

Opis API znajduje się tu: [Fakturownia API](https://github.com/radgost/fakturownia-api)

