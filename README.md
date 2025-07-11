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
{{absolute_outstanding}} - do zapłaty
{{absolute_outstanding_in_exchange_currency}} - do zapłaty po przeliczeniu wg kursu
{{absolute_outstanding_in_words}} - do zapłaty słownie
{{absolute_outstanding_in_words_in_exchange_currency}} - do zapłaty słownie po przeliczeniu wg kursu
{{absolute_outstanding_without_currency}} - do zapłaty bez waluty
{{accounting_doc}} - typ dokumentu
{{accounting_expense_discount_code}} - kod księgowy rabatu w wydatkach
{{accounting_income_discount_code}} - kod księgowy rabatu w przychodach
{{accounting_note_kind}} - podtyp
{{act_of_acceptance}} - protokół zdawczo-odbiorczy
{{additional_address_seller_name}} - nazwa wyświetlana na fakturze zamiast "wystawca" (sprzedawca)
{{additional_field_name}} - nazwa dodatkowego pola na fakturze
{{additional_field_value}} - wartość dodatkowego pola na fakturze
{{additional_info}} - dodatkowe pole na pozycjach faktury
{{additional_info_desc}} - dodatkowe pole na pozycjach faktury
{{address}} - adres sprzedawcy
{{advance_compact_look}}
{{advance_compact_name_colspan}}
{{advance_compact_pos_name}}
{{advanced_num}} - ilość powiązanych faktur zaliczkowych dla faktury końcowej
{{advanced_total_price_gross}} - suma brutto powiązanych zaliczek
{{all_in_words}} - suma brutto słownie
{{all_in_words_in_exchange_currency}} - suma brutto słownie po przeliczeniu
{{arr_due_amount}} - należna stopa zwrotu
{{arr_due_msg}} - wiadomość do należnej stopy zwrotu
{{bank}} - bank (nazwa banku)
{{bank_account}} - numer konta bankowego
{{bank_account_name_uk}} - nazwa konta bankowego w uk
{{bank_account_payment_url}} - url płatności na konto bankowe
{{bank_iban}}
{{bdo_no}} - bdo
{{bilangual}} - dwujęzyczna faktura
{{bm_bank_account_link}} - ink do konta bankowego bm
{{buyer}} - nabywca
{{buyer_address}} - adres nabywcy
{{buyer_bank_account}} - konto
{{buyer_company}} - firma
{{buyer_country}} - kraj
{{buyer_country_code}} - oznaczenie kraju nabywcy
{{buyer_email}} - e-mail klienta
{{buyer_first_name}} - imię
{{buyer_full_name}} - imię i nazwisko nabywcy
{{buyer_last_name}} - nazwisko
{{buyer_mobile_phone}} - telefon komórkowy
{{buyer_note}} - dodatkowy opis
{{buyer_person}} - imię i nazwisko odbiorcy
{{buyer_phone}} - telefon klienta
{{buyer_place}} - miejscowość nabywcy
{{buyer_post_code}} - kod pocztowy
{{buyer_register_number}} - regon
{{buyer_street}} - ulica i nr
{{buyer_tax_no}} - nip
{{buyer_tax_no_kind}} - rodzaj numeru identyfikacyjnego nabywcy
{{cancel_reason}} - powód anulowania faktury
{{canceled}} - faktura anulowana
{{client_external_id}} - id klienta z karty klienta
{{{client_panel_view_link}}} - link do panelu klienta
{{{client_panel_view_link_unpaid}}} - link do panelu klienta (tylko nieopłacone faktury)
{{client_panel_view_url}} - adres url do panelu klienta
{{client_url}} - id klienta w systemie
{{company}} - nazwa sprzedawcy
{{conditional_notes}} - uwagi warunkowe
{{corrected_content_after}} - treść prawidłowa
{{corrected_content_before}} - treść korygowana
{{corrected_issue_date}} - data wystawienia korygowanego dokumentu
{{corrected_kind}} - typ dokumentu korygowanego
{{corrected_number}} - numer dokumentu korygowanego
{{corrected_sell_date}} - data sprzedaży dokumentu korygowanego
{{correction}} - dokument korygowany
{{correction_reason}} - przyczyna korekty
{{country}} - kraj sprzedawcy
{{created_at}} - utworzenie
{{currency}} - waluta
{{currency_short}} - skrócona nazwa waluty
{{currency_symbol}} - symbol waluty
{{delivery_address}} - adresat
{{delivery_address_filled}} - adres dostawy
{{delivery_address_name}} - adres korespondencyjny
{{description_footer}} - dodatkowe uwagi (drukowane na dole strony)
{{description_long}} - dodatkowe uwagi (drukowane na drugiej stronie)
{{discount}} - rabat
{{discount_kind}} - rodzaj rabatu
{{document_type}} - rodzaj dokumentu
{{email}}
{{estimates}} - zaliczki
{{estimates_first}}
{{estimates_first_no}}
{{estimates_first_url}}
{{estimates_size}} - liczba zaliczek
{{exchange_currency}} - przeliczanie na walutę
{{exchange_currency_rate}} - kurs
{{exchange_date}} - data kursu przeliczenia
{{exchange_note}} - notatka do kursu
{{exchange_rate}} - internal field!!!
{{exchange_tax}} - przeliczona kwota vat
{{expense_payment_url}}
{{fax}}
{{final}} - faktura końcowa
{{final_summary_table}} - faktura końcowa tabela z podsumowaniem
{{footer}} - {:generated_in=>"wygenerowano w %{domain}", :page=>"strona", :page_of=>" z "}
{{forced_payment_to}} - wymuszony termin zapłaty
{{from_recurring_payment}} - autopłatność z faktury cyklicznej
{{global_discount_gross}} - rabat od sumy brutto
{{global_discount_gross_with_currency}} - rabat od sumy brutto z oznaczeniem waluty
{{global_discount_net}} - rabat od sumy netto
{{global_discount_net_with_currency}} - rabat od sumy netto z oznaczeniem waluty
{{gtu_codes_list}} - lista kodów gtu
{{gtu_codes_note}} - nazwa + lista kodów gtu
{{has_corrected_content}} - treść korygowana
{{hide_tax}} - ukryj podatek i cenę netto
{{id}}
{{income}} - przychód
{{internal_note}} - notatka prywatna (niewidoczna na wydruku)
{{invoice_act_of_acceptance}} - numer faktury bazowej
{{invoice_category}} - kategoria faktury
{{issue_date}} - data wystawienia
{{issue_place}} - miejsce wystawienia
{{issuer}} - wystawca dokumentu
{{issuers}} - wystawcy
{{issuers_header}}
{{kind}} - typ
{{kpir_col}} - numer kolumny w księdze
{{kpir_pos}} - numer pozycji w księdze
{{ksef_enabled}}
{{ksef_if_below_qr}}
{{ksef_qrcode_img}}
{{lang}} - język
{{legal_cost_compensation}} - rekompensata kosztów prawnych
{{locale}} - ustawienia regionalne
{{logo_url}} - adres url logo
{{long_exchange_note}} - notatka o kursie przeliczenia
{{long_exchange_note_for_tax}} - notatka o kursie przeliczenia
{{many_qrs}}
{{multiple_delivery_addresses}} - adresy dostawy
{{negative_outstanding}} - wartość do zapłaty ujemna
{{notes}} - uwagi
{{number}} - numer
{{number_text}} - słownie
{{oid}} - nr zamówienia
{{outstanding}} - do zapłaty
{{outstanding_in_exchange_currency}} - do zapłaty po przeliczeniu
{{outstanding_in_words}} - do zapłaty słownie
{{outstanding_in_words_in_exchange_currency}} - do zapłaty słownie po przeliczeniu
{{overdue}} - zaległość
{{paid}} - kwota opłacona
{{paid_date}} - data płatności
{{paid_fr}}
{{paid_mark_url}} - adres url znaku opłacono
{{payment_button_url}} - adres url przycisku "kliknij i zapłacić online"
{{{payment_link}}} - link do bezpośredniej płatności online
{{payment_reference_number}} - numer polecenia zapłaty
{{payment_to}} - termin płatności
{{payment_type_sym}} - typ płatności
{{payment_url}} - link do płatności
{{payments}} - {:header=>"płatności", :by=>"przez"}
{{payments_providers}}
{{person}} - imię i nazwisko wystawcy
{{phone}} - telefon sprzedawcy
{{place}} - miejsce wystawienia
{{positions_correction_after_total_price_gross}}
{{positions_correction_before_total_price_gross}}
{{positions_total_price_gross}} - suma brutto
{{positions_total_price_net}} - suma netto
{{positions_total_quantity}} - suma z rubryki ilość
{{positions_total_quantity_separated}} - suma ilości z jednostką
{{positions_total_tax}} - wartość podatku
{{positions_total_weight}} - waga produktu
{{positons_total_tax}} - całkowity podatek od pozycji
{{post_code}} - kod pocztowy sprzedawcy
{{prepayment_required}} - wymagana przedpłata (%)
{{prepayment_required_exact_amount}} - dokładna wartość
{{price_offer_no_catalogue}} - pokaż ofertę bez informacji o produktach
{{print_ean_codes}}
{{print_option}} - wydruk faktury
{{procedure_designations_list}} - oznaczenia dotyczące procedur
{{procedure_designations_note}} - oznaczenia dotyczące procedur z opisem
{{product_cache}} - pamięć podręczna produktu
{{proforma}} - numer proformy do faktury
{{qrcode_img}} - oznaczenie kodu qr
{{receipt}} - numer paragonu do faktury
{{recipient_address}} - adres odbiorcy
{{recipient_city}} - miejscowość
{{recipient_country}} - kraj
{{recipient_country_code}} - oznaczenie kraju odbiorcy
{{recipient_email}} - e-mail
{{recipient_name}} - odbiorca
{{recipient_note}} - dodatkowy opis
{{recipient_phone}} - telefon
{{recipient_post_code}} - kod pocztowy
{{recipient_present}} - odbiorca
{{recipient_street}} - ulica i nr
{{recipient_tax_no}} - nip
{{recipient_url}} - id odbiorcy w systemie
{{recipients}} - odbiorcy
{{recipients_header}}
{{reject_button_text}}
{{reminder_no}} - liczba wysłanych przypomnień o niepłaconej fakturze
{{reminder_number}} - numer kolejnego przypomnienia o nieopłaconej fakturze
{{reverse_charge}} - odwrotne obciążenie
{{reverse_charge_code}} - kod transakcji
{{reverse_charge_cz}} - odwrotne obciążenie cz
{{rr_declaration}} - deklaracja rr
{{sales_code}} - kod sprzedaży
{{sec_stamp_url}} - adres url dodatkowej pieczęci na fakturze
{{sell_date}} - data sprzedaży
{{sell_date_MY}} - data sprzedaży w formacie mm/yyyy
{{sell_date_kind}} - oznaczenie czasu sprzedaży
{{seller_register_number}} - regon
{{seller_tax_no_kind}} - rodzaj numeru identyfikacyjnego sprzedawcy
{{seller_trade_register_cz}} - informacje dotyczące wpisu do rejestru handlowego
{{sent_at}} - data i godzina wysłania dokumentu
{{should_print_gtu_codes}} - wstaw kody gtu
{{should_print_procedure_designations}} - wstaw oznaczenie dotyczące procedur
{{show_buyer_note}} - wstaw dodatkowy opis nabywcy
{{show_client_phone_on_invoice}} - pokaż numer telefonu klienta na fakturze
{{show_date_and_sign}} - pokaż datę i podpis
{{show_discount}} - widoczna rubryka rabat
{{show_discount_as_net_amount}} - zawsze pokazuj rabat w postaci netto
{{show_empty_buyer_person}} - wstaw puste pole na podpis wystawcy
{{show_empty_seller_person}} - wstaw puste pole na podpis odbiorcy
{{show_links}} - linki na podglądzie dokumentu
{{show_paid_date}} - wstaw datę płatności
{{show_paid_logo}} - pokaż logo "zapłacono"
{{show_paid_when_zero}} - kwota opłacona …
{{show_payments_on_invoice}} - pokaż płatności na fakturze
{{show_price_offer_summary}} - pokaż z podsumowaniem
{{show_product_description}} - opis produktu na pozycjach faktury
{{show_reject_button}}
{{show_related_estimates_on_invoice}} - pokaż powiązane zaliczki na fakturze
{{show_rr_declaration}} - oświadczenie dostawcy produktów rolnych
{{show_sell_date}} - pokazuj datę sprzedaży
{{show_tax_split}} - wyświetlaj podsumowanie podatku
{{show_totals}} - pokaż sumy
{{show_unit_price_gross}} - wyświetlaj cenę jednostkową brutto
{{sign_button_text}}
{{sign_document_url}} - link do podpisu elektronicznego
{{signature_date}} - data podpisania elektronicznego
{{signature_url}} - link do podpisu elektronicznego
{{signers_full_name}} - imie i nazwisko
{{skonto_active}} - skonto
{{skonto_date}} - skonto termin płatności
{{skonto_price}} - suma rabatu za wcześniejszą płatność
{{skonto_value}} - % przyznanego upustu
{{sort_code_uk}} - kod sortowania w uk
{{split_payment}} - mechanizm podzielonej płatności
{{split_payment_note}} - notatka o metodzie podzielonej płatności
{{stamp_below_sign_url}} - adres url pieczęci na fakturze
{{stamp_url}} - adres url pieczęci na fakturze
{{status}} - status
{{status_accepted}} - status zaakceptowano
{{status_paid}} - status opłacona
{{street}} - ulica i nr sprzedawcy
{{swift}} - kod swift
{{tax2_details}} - drugi podatek
{{tax2_name}} - nazwa drugiego podatku
{{tax2_visible}} - drugi podatek (widoczność)
{{tax_based_on_debits}}
{{tax_in_exchange_currency}} - wartość podatku po przeliczeniu
{{tax_name}} - nazwa podatku
{{tax_no}} - nip
{{tax_value}} - wartość podatku
{{tax_value_in_exchange_currency}} - wartość podatku po przeliczeniu
{{tax_value_in_exchange_currency_with_currency}} - wartość podatku po przeliczeniu z określoną walutą
{{tax_value_name}} - nazwa wartości podatku
{{tax_value_with_currency}} - wartość podatku z oznaczeniem waluty
{{tax_visible}} - widoczność podatku na dokumencie
{{title}} - tytuł
{{today_date}} - aktualna data
{{token}}
{{total_discount}} - suma rabatu
{{total_discount_in_exchange_currency}} - suma rabatu po przeliczeniu
{{total_discount_in_exchange_currency_with_currency}} - suma rabatu po przeliczeniu z oznaczeniem waluty
{{total_discount_with_currency}} - suma rabatu z oznaczeniem waluty głównej dokumentu
{{total_price_gross}} - wartość brutto
{{total_price_gross_in_exchange_currency}} - wartość brutto po przeliczeniu
{{total_price_gross_in_exchange_currency_with_currency}} - wartość brutto po przeliczeniu z oznaczeniem waluty
{{total_price_gross_in_main_currency}} - wartość brutto przeliczona na walutę główną konta
{{total_price_gross_with_currency}} - wartość brutto z oznaczeniem waluty dokumentu
{{total_price_gross_without_discount}} - wartość brutto bez rabatu
{{total_price_gross_without_discount_with_currency}} - wartość brutto bez rabatu z oznaczeniem waluty dokumentu
{{total_price_net}} - wartość netto
{{total_price_net_in_exchange_currency}} - wartość netto po przeliczeniu
{{total_price_net_in_exchange_currency_with_currency}} - wartość netto po przeliczeniu z oznaczeniem waluty
{{total_price_net_in_main_currency}} - wartość netto po przeliczeniu na walutę główną konta
{{total_price_net_with_currency}} - wartość netto z oznaczeniem waluty dokumentu
{{total_price_net_without_discount}} - wartość netto bez rabatu
{{total_price_net_without_discount_with_currency}} - wartość netto bez rabatu z oznaczeniem waluty dokumentu
{{total_tax_inscription}} - opis wartości vat
{{transaction_id}} - id powiązanej z fakturą transakcji
{{transaction_type}} - typ transakcji
{{type_of_payment}} - rodzaj płatności
{{use_arr_due}} - użyj należnej stopy zwrotu
{{use_barcodes}} - kod ean przy produkcie
{{use_delivery_address}} - inny adres korespondencyjny
{{use_iban}}
{{use_paid_dates}} - używaj dat opłacenia na fakturach
{{use_prime_cee}} - użyj prime cee
{{use_product_code}} - kod produktu
{{valid_till_date}} - ważna do
{{vat_created_from_act_of_acceptance}}
{{verifactu_enabled}}
{{{view_link}}} - link do dokumentu
{{view_url}} - bezpośredni link do dokumentu
{{warehouse_document_numbers}} - numer powiązanego dokumentu magazynowego
{{www}} - adres strony www sprzedawcy
{{zero_with_currency}} - zero z walutą dokumentu
{{zero_with_currency_in_exchange_currency}} - zero po przeliczeniu z oznaczeniem waluty

{{#each advanced}} :
{{currency}} - waluta zaliczki
{{issue_date}} - data wystawienia zaliczki
{{kind}}
{{no}} - liczba porządkowa powiązanej zaliczki
{{number}} - numer systemowy zaliczki
{{price}} - wartość zaliczki
{{price_gross}} - wartość brutto zaliczki
{{price_gross_with_currency}} - wartość brutto zaliczki z oznaczeniem waluty
{{price_net}} - wartość netto zaliczki
{{price_net_with_currency}} - wartość netto zaliczki z oznaczeniem waluty
{{price_tax}} - wartość vat zaliczki
{{price_tax_with_currency}} - wartość vat zaliczki z oznaczeniem waluty
{{/each}}

{{#each final_summary}} :
{{tax}} - stawka podatku vat
{{tax_value}} - wartość podatku
{{tax_value_with_currency}} - wartość podatku z oznaczeniem waluty
{{total_price_gross}} - cena całkowita brutto
{{total_price_gross_with_currency}} - cena całkowita brutto z oznaczeniem waluty
{{total_price_net}} - cena całkowita netto
{{total_price_net_with_currency}} - cena całkowita netto z oznaczeniem waluty
{{/each}}

{{#each positions}} :
{{accounting_activity_code}} - kod działalności księgowej
{{accounting_code_expenses}} - kod księgowy wydatków
{{accounting_code_income}} - kod księgowy przychodów
{{accounting_code_sales}} - kod księgowy sprzedaży
{{accounting_code_tax_purchase}} - kod księgowy podatku od zakupów
{{accounting_code_tax_sale}} - kod księgowy podatku od sprzedaży
{{additional_info}} - wartość dodatkowego pola na pozycjach faktury
{{additional_info_desc}} - nazwa dodatkowego pola na pozycjach faktury
{{barcode}} - kod kreskowy produktu
{{code}} - kod produktu
{{description}} - opis
{{discount}} - kwota rabatu
{{discount_amount_gross}} - rabat brutto dla jednej sztuki
{{discount_amount_net}} - rabat netto dla jednej sztuki
{{dummy_position}} - rodzaj pozycji bez produktu
{{ean_code}} - kod ean produktu
{{gtu_code}} - kod gtu
{{has_discount}} - dokument zawiera rabat
{{image_url}} - adres url zdjęcia produktu
{{invoice_created_at}} - data utworzenia faktury
{{item}} - nazwa produktu/usługi
{{item_url}} - id produktu z adresu url
{{kind}} - rodzaj pozycji
{{no}} - numer pozycji na dokumencie
{{product}} - dane o produkcie na pozycji faktury
{{quantity}} - ilość
{{quantity_number}} - ilość produktu
{{quantity_unit}} - jednostka
{{supplier_code}} - kod u dostawcy
{{tax}} - stawka vat
{{tax1_value_name}} - nazwa podatku
{{tax2}} - stawka vat
{{tax2_name}} - nazwa drugiego podatku na fakturze
{{tax2_value_name}} - nazwa wartości drugiego podatku na fakturze
{{tax_name}} - nazwa podatku
{{tax_value}} - wartość vat
{{tax_value_name}} - nazwa wartości podatku na fakturze
{{total_price_gross}} - wartość brutto
{{total_price_gross_without_discount}} - wartość brutto bez rabatu
{{total_price_net}} - wartość netto
{{total_price_net_without_discount}} - wartość netto bez rabatu
{{unit_price_gross}} - cena jednostkowa brutto
{{unit_price_gross_with_discount}} - cena jednostkowa brutto z rabatem
{{unit_price_net}} - cena jednostkowa netto
{{unit_price_net_with_discount}} - cena jednostkowa netto z rabatem
{{/each}}

{{#each summary}} :
{{tax}} - stawka vat
{{tax_value}} - wartość podatku
{{tax_value_with_currency}} - wartość podatku z oznaczeniem waluty
{{total_price_gross}} - wartość brutto
{{total_price_gross_with_currency}} - wartość brutto z oznaczeniem waluty
{{total_price_net}} - wartość netto
{{total_price_net_with_currency}} - wartość netto z oznaczeniem waluty
{{/each}}

{{additional_fields}} :
{{additional_fields.seller_bank_swift}} - kod swift sprzedającego
{{additional_fields.seller_bdo_no}}
{{additional_fields.tax_name}} - nazwa podatku na fakturze
{{additional_fields.tax_name_type}} - rodzaj podatku na fakturze

{{client}} :
{{client.accounting_id}} - identyfikator w programie księgowym
{{client.additional_accounting_id}} - dodatkowy kod księgowy klienta
{{client.discount}} - domyślny rabat %
{{client.email}} - e-mail
{{client.first_name}} - imię
{{client.id}} - id
{{client.last_name}} - nazwisko
{{client.name}} - nazwa firmy
{{client.panel_link}} - link do panelu klienta
{{client.panel_link_unpaid}} - link do panelu klienta z nieopłaconymi fakturami
{{client.panel_url}} - link do panelu klienta

{{department}} :
{{department.bank_account}} - konto bankowe
{{department.bank_iban}} - iban
{{department.bank_name}} - nazwa banku
{{department.bank_swift}} - swift
{{department.capital}} - kapitał
{{department.capital_currency}} - waluta kapitału
{{department.capital_kind}} - kapitał zakładowy
{{department.footer_content}} - treść stopki
{{department.footer_kind}} - rodzaj stopki
{{department.id}}
{{department.kind}} - forma prawna
{{department.name}} - nazwa firmy lub działu
{{department.own_footer}} - własna treść stopki
{{department.shortcut}} - nazwa skrócona
{{department.tax_kind}} - nr nip
{{department.tax_no}} - numer nip
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

