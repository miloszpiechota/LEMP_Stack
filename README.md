# Labolatorium 11 
# Miłosz Piechota IO 6.7


W pliku docker_compose.yml dodałem:
1.Konfiguracje servera PHP, gdzie definiowany jest obraz i tworzony kontener php. Następnie mapuję lokalny katalog ./html do katalogu /var/www/html w kontenerze, co powinno umożliwić dostęp do plików PHP. Na konieć dołączam server PHP do sieci backend.

2.Konfiguracje servera MySQL, gdzie definiowany jest obraz i tworzony kontener mysql. Ustawiane są zmienne środowiskowe jak hasło dla użytkownika root i dane do bazy. Następnie mapuję wolumin mysql_data do katalogu /var/lib/mysql w kontenerze, aby zachować trwałość danych bazy danych MySQL. Na koniec dołączam server do backend.

3.W sekcji phpMyAdmin tworzę kontener phpmyadmin, ustawiam zmienne takie jak adres hosta i port bazy oraz hasło root, kieruję port 6001 hosta na port 80 kontenera, umożliwiając dostęp do phpMyAdmin z przeglądarki. Na koniec dołączam do sieci backend.

4.Definiuję server Nginx wraz z kontenerem nginx. Mapuję lokalne konfiguracje Nginx (./nginx/conf.d) i katalog HTML (./html) do odpowiednich katalogów w kontenerze. Przekierowuję port 4001 hosta na port 80 kontenera aby działało na przeglądarce. Na koniec Dołącza serwer Nginx do sieci backend i frontend.

W pliku default.conf zawarta jest konfiguracja servera Nginx, gdzie znajduje się nasłuchiwanie na porcie 80, określam katalog główny /usr/share/nginx/html z plikami indeksowymi. 

## Wyniki działania aplikacji:

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/9ed88f99-b894-4f30-8bbd-e89325433a3f)

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/72636ca7-9178-4e66-a6f2-169b6567bf03)


## Zalogowanie się do bazy danych 

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/079fcbf2-a77d-4b19-863f-207d551a5912)


## Dostepna baza danych "test_db" 

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/52a6ce3f-f237-476e-ab41-84308cfc23f7)


## Nieudana próba połączenia z http://localhost:4001 -> "File not found"

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/33237e74-2903-4253-bea4-aa99046518aa)

## Sprawdzenie logów php i nginx:

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/26e7bbac-1247-4706-94d6-fb1c71bbff44)

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/c05f51dd-ea2e-464c-ade7-6e93a824f789)

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/1279e78e-d8d2-43a8-b587-3e9279a98522)

## Błąd 404 wskazuje na brak odnalezienia pliku index.php.

## Sprawdzenie uprawnień:

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/e349cc1c-76db-45a9-937f-49407f9e5025)

## Uruchomienie powłoki Bash w celu dostepu do kontenera:

![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/590edbca-c40d-421f-8c0e-7cfc745eddba)


![image](https://github.com/miloszpiechota/LEMP_Stack/assets/161620373/c0a9b849-5a69-4eca-9d79-65ab066b8821)










