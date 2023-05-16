# Integracja ETL C hash oraz procedury TSQL
Integracje Pipedrive oraz ClickMeeting
    1. Aplikacje konsolowe .NET Framework:
    Kod pobierające dane w formacie JSON z bramki API platformy ( w tym definiowanie head`ersów). Dane są następnie deserializowane z zastosowaniem biblioteki Newtonsoft i zapisywane na serwer MS SQL (ADO.NET).
    Jeżeli tabela docelowa nie istnieje na serwerze, jest tworzona poprzez aplikację osobną metodą.
    Poprzez LINQ następuje połączenie z tabelą na MS SQL, zawierającą aktualne dane i przypisanie zmiennej, określającej moment rozpoczęcia pobierania dancyh.
    Na końcu wyzwalane są procedury zapisujące na serwerze status operacji oraz aktualizację tabeli systemowo-wersjonowanej na MS SQL.
2. Procedury TSQL:
    Przykładowe procedury TSQL współpracujące z aplikacjami .NET Framework.

