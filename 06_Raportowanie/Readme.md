## Raport z testów aplikacji Mr Buggy 3

#### 1. Wprowadzenie 

  Dokument ma na celu opisanie czynności wykonanych w ramach testowania aplikacji Mr Buggy 3.
  
---  

#### 2. Zakres testów

W zakres zaplanowanych i przeprowadzonych testów wchodziło:
   
  - wymagania niefunkcjonalne zebrane na podstwie specyfikacji aplikacji (wydajności i bezpieczeństwa)
  - zgodność interfejsu  części klienckiej z wymaganiami
  - wymagania funkcjonalne części klienckiej (w wersji końcowej)

    Napisano 25 test casów, które zostały podzielone na 4 Test runy:
    - Działnie aplikacji (6 TC)
    - Wymagania (7 TC)
    - Bezpieczeństwo (6 TC)
    - Exploracyjne (6 TC)

---  
    
####  3. Analiza statusów testów
 
Podczas przeprowadzania testów nie można było przeprowadzić testów dotyczących części serwerowej aplikacji, wersja demnostracyjnej oraz trybu drużynowego aplikacji z powodu braku dostępu. Testy te mają status "Blocked" w raportach (5 TC).
  
Testy ze statusem "Passed" (11 TC) mają zgodny rezultat faktyczny z rezultatem oczekiwanym wynikającym ze specyfikacji.
   
Testy ze statusem "Failed" (9 TC) mają inny rezultat faktyczny niż rezultat oczekiwany wynikający ze specyfikacji.
    
Raport [testrail-report-10](https://github.com/aleksandram13/MrBuggy3/blob/69feecd440595f21148a394d9b3c41022cd6b164/06_Raportowanie/testrail-report-10.pdf) pokazuje pokrycie testów, w podziale na TestRuny.


---
    
####  4. Znalezione błędy
 
 
 TC ID | Oczekiwany rezultat | Faktyczny rezultat
--- | --- | ---
*T23* | Menu boczne zawiera element "czas" | **W oknie aplikacji nie wyświetla się czas**
*T24* | Menu boczne zawiera element "zaraportuj defekt" | **W oknie aplikacji wyświetla się "Zgłoś defekt"**
*T82* | W aplikacji znajduje się 15 zadań, każde z 1 błędem | **W aplikacji jest zaimplementowane 24 zadania, z czego 6 zawiera kilka błędów**
*T46* | Login spełniający wymagania | **Aplikacja nie zezwala na podanie loginu ze znakiem specjalnym**
*T47* | Hasło spełniające wymagania | **Aplikacja wyświetla komunikat, że minimum znaków w haśle to 6**
*T48* | Login niespełniający wymagań | **Aplikacja zezwala na rejestrację z loginem bez wymaganych znaków**
*T56* | Zmiana ilości produktu w koszyku | **Możliwe jest dodanie większej ilości produktów, niż dostępnych na magazynie**
*T60* | Kwota przelewu | **Po zapisaniu, kwota przelewu zwiększa się o 1zł**
*T76* | Stoper można zatrzymać w dowolnym momencie | **Przycisk 'stop' nie działa po upływie 1 minuty**
*T80* | Możliwe jest wprowadzenie danych tylko z listy rozwijanej | **Można wpisać dowolną wartość z klawiatury**


---
    
#### 5. Sugerowane zmiany
Przede wszystkim należałoby ustalić, jak powinny wyglądać ostateczne wymagania dotyczące loginu i hasła. Komunikat w aplikacji o wymaganiach hasła (minimum 6 znaków) wydaje się bardziej przystępny, niż ten ze specyfikacji (minimum 20 znaków). Należy dopasować interfejs do podanych wymagań, brakuje kilku elementów, które są podane w specyfikacji. Ważną kwestią jest też doprecyzowanie ilości zadań oraz ich szczegółów. W specyfikacji jest mowa o 15 zadaniach, każde z zaimplementowanym jednym błędem. W aplikacji znajduje się 13 pojedynczych zdań, z czego 6 ma przynajmniej 2 błędy, co w sumie daje 24 problemy do rozwiązania. 
Poza tymi wymienionymi powyżej, w aplikacji występują błędy, które są porządane w działaniu aplikacji przygotowanej na Mistrzostwa Polski w Testowaniu.
