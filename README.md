# IntegracjaPipedriveChash
Aplikacja konsolowa .NET Framework. 
Kod pobierające dane w formacie JSON z bramki API platformy Pipedrive. Dane są następnie deserializowane z zastosowaniem biblioteki Newtonsoft i zapisywane na serwer MS SQL (ADO.NET).
Jeżeli tabela docelowa nie istnieje na serwerze, jest tworzona poprzez aplikację osobną metodą.
Poprzez LINQ następuje połączenie z tabelą na MS SQL, zawierającą aktualne dane. Ostatnia wartość (MAX() z kolumny UpdateTime oznacza punkt, od którego pobieramy dane z API (ostatnie zapisy).
Na końcu wyzwalane są procedury zapisujące na serwerze status operacji oraz aktualizację tabeli systemowo-wersjonowanej na MA SQL.
