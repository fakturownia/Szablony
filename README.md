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
{{document_type}}
{{kind}} - typ
{{number}} - numer
{{title}} - tytuł
{{issue_date}} - data wystawienia
{{issue_place}}
{{print_option}}
{{sell_date}} - data sprzedaży
{{company}}
{{post_code}}
{{place}} - miejsce wystawienia
{{street}}
{{tax_no}} - nip
{{country}}
{{www}}
{{email}}
{{fax}}
{{phone}}
{{bank}}
{{person}}
{{bank_account}}
{{buyer}} - nabywca
{{buyer_post_code}} - kod pocztowy
{{buyer_place}}
{{buyer_street}} - ulica i nr
{{buyer_country}} - kraj
{{buyer_tax_no}} - nip
{{buyer_person}} - imię i nazwisko odbiorcy
{{buyer_company}}
{{total_price_net}} - wartość netto
{{total_price_net_with_currency}}
{{total_price_gross}} - wartość brutto
{{total_price_gross_with_currency}}
{{tax_value}}
{{tax_value_with_currency}}
{{notes}}
{{outstanding}}
{{outstanding_in_words}}
{{all_in_words}}
{{payment_to}} - termin płatności
{{type_of_payment}}
{{paid}} - kwota opłacona
{{logo_url}}
{{stamp_url}}
{{token}}
{{oid}} - nr zamówienia
{{description_long}} - dodatkowe uwagi (drukowane na drugiej stronie)
{{description_footer}} - dodatkowe uwagi (drukowane na dole strony)
{{view_url}}
{{payment_url}}
{{tax_name}}
{{currency}} - waluta
{{currency_symbol}}
{{currency_short}}
{{exchange_currency}} - przeliczanie na walutę
{{use_delivery_address}} - inny adres korespondencyjny
{{delivery_address}} - adresat
{{lang}} - język
{{discount}} - rabat
{{show_discount}}
{{income}} - przychód
{{exchange_rate}} - kurs
{{total_price_net_in_main_currency}}
{{total_price_gross_in_main_currency}}
{{additional_info}}
{{department}} - dział / oddział firmy - dostępne są pola id, name, kind ... np {{department.id}} {{department.name}}

{{#each positions}} :
  {{no}}
  {{item}} - nazwa produktu/usługi
  {{additional_info}} - dodatkowe pole na pozycjach faktury
  {{discount}}
  {{quantity}} - ilość
  {{unit_price_net}}
  {{unit_price_net_with_discount}}
  {{unit_price_gross}}
  {{total_price_net}} - wartość netto
  {{total_price_gross}} - wartość brutto
  {{tax}} - stawka vat
  {{tax_value}} - wartość vat
{{/each}}

{{#each summary}} :
  {{total_price_net}}
  {{total_price_gross}}
  {{tax}}
  {{tax_value}}
{{/each}}

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
  tt
  include
  include_in_col
  in
  not_in
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

{{#mt val1 17 }}
  >17
{{else}}
 <17
}}

{{#eq department_id "123"}}
  info dla danego departamento
{{else}}
  info dla innych departamentow
{{/eq}}


{{#for size_from size_to}}
    no: {{no}}
{{/for}}
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

