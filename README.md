# Dietetyczny Bot
Projekt realizowany w ramach przedmiotu *Wprowadzenie do aplikacji i rozwiązań opartych o Sztuczną Inteligencję i Microsoft Azure* prowadzonym na Politechnice Warszawskiej.

## Opis i cel projektu
Światowa Organizacja Zdrowia ogłosiła, że 800 milionów osób zmaga się z otyłością. Liczba osób chorujących wśród dorosłych wzrosła od 1975 roku prawie trzykrotnie. Chorujący są w każdym wieku, w każdej grupie społecznej oraz w krajach o różnym poziomie rozwinięcia. Szacuje się, że do 2025 roku na walkę z otyłością zostanie przeznaczone ponad bilion dolarów. Natomiast na zaburzenia odżywiania, które są przypadłościami psychosomatycznymi cierpi około 70 milionów osób na całym świecie. Około 6% przypadków tych zaburzeń kończy się śmiercią, zarówno spowodowanej skutkami zdrowotnymi, jak i samobójstwem. Dlatego w ramach projektu chcieliśmy stworzyć bota, który zwiększy świadomość na temat zaburzeń odżywiania, ale również będzie podawał przydatne informacje na temat zdrowego sposobu odżywiania. Powstały bot potrafi na podstawie podanych przez użytkownika danych wyliczyć wskaźnik masy ciała (BMI), zapotrzebowanie kaloryczne (BMR) oraz zwrócić informacje na temat kaloryczności i zawartości odżywczych poszczególnych produktów spożywczych. Z naszym botem można komunikować się w języku angielskim.

<a href="https://pulsmedycyny.pl/who-otylosc-to-choroba-ktora-dotyka-800-mln-ludzi-na-swiecie-1110168" target="_blank">Link do danych na temat otyłości</a>

<a href="https://psychologiawpraktyce.pl/artykul/zaburzenia-odzywiania-wsrod-dzieci-i-mlodziezy" target="_blank">Link do danych na temat zaburzeń odżywiania</a>

## Skład zespołu
* Kinga Kocoł – <a href="https://github.com/kingakocol" target="_blank">Link do konta</a>
* Aleksandra Kowalczyk – <a href="https://github.com/Olakow" target="_blank">Link do konta</a>
* Martyna Jakubowska – <a href="https://github.com/mjakubowska" target="_blank">Link do konta</a>
* Aleksander Wodnicki – <a href="https://github.com/AleksanderWodnicki" target="_blank">Link do konta</a>

## Opis funkcjonalności

## Architektura
<p align="center">
  <img src="https://user-images.githubusercontent.com/64069048/144723367-8dfed661-4a9c-414f-b923-1bacd1e96b69.png"/>
</p>

## Wybrany stos technologiczny
- Azure:
  - Active Directory –
  - App Service –
  - App Service Editor –
  - Bot Service –
  - Cognitive Service – serwis ten umożliwił stworzenie *Knowledge Base* korzystając z QnA Maker, z bazy wiedzy korzysta utworzony przez nas bot,
  - LUIS (Language Understanding) –
- nie jestem pewna jak nazwać tę kategorię:
  - Bot Framework Composer –
  - Bot Framework Emulator –
- Język:
  - C# –

## Opis działania rozwiązania
Aby uruchomić dietetycznego bota należy skożystać z tego linku. Następnie zostaniemy przekierowani do Web Chatu.

--dodać zdjęcie--

Od tego momentu możliwe jest komunikowanie się z botem. Tworząc bazę wiedzy wybraliśmy, aby nasz bot zawierał chit-chat (friendly), oznacza to, że po stworzeniu bazy zawierała ona już część pytań, które użytkownik może zadać i odpowiedzi bota na nie. Poniżej zostały wypisane przykładowe pytania z różnych kategorii, które możemy zadać:
- chit chat
  - Who are you?
  - Are you old?
  - Could you ask me something?
  - Do you eat pancakes?
- pytania dotyczące zaburzeń odżywiania
  - What are eating disorders?
  - What should I say to someone with an eating disorder? 
  - What is anorexia?
  - What are behavioural signs of bulimia?
  - How can I treat orthorexia?
  - What are effects of binge eating disorder?
- pytania odnośnie zdrowego odżywiania
  - How to put on weight safely?
  - Tell me about tips which can help me lose weight.
  - What is the healthy eating pyramid?
  - How many calories are in alcohol?
  - How much should I drink evary day?
  - How to read food labels?
  - What are calories?
  - What is BMI?
  - What is basal metabolic rate?
- pytania dotyczące diet
  - What is diet?
  - What is vegetarianism?
  - What is veganism?
  - Tell me about most popular diets.
  - What is the 5:2 diet?
- pytania dotyczące aktywności fizycznej
  - Tell me examples of exercises.
  - Tell me examples of exercises for childrean under 5 years old.
  - Tell me examples of exercises for older adults.

W ramach niektórych pytań bot zwraca nie tylko odpowiedź, ale również link do strony na której można uzyskać więcej informacji na wybrany temat. Przykładem jest pytanie dotyczące ilości płynów, które należy wypić każdego dnia.

--dodać zdjęcie--

W przypadku, niektórych pytań możliwe jest prowadzenie dłuższej konwersacji z botem. Przykładem jest pytanie o bulimię.

--dodać zdjęcie--

Bot umożliwia wyliczenie wskaźnika masy ciała (BMI) oraz zapotrzebowanie kaloryczne (BMR) na podstawie podanych przez użytkownika danych.

--dodać zdjęcie--

Nasz bot daje również możliwość zwracania informacji o kaloryczności i zawartości składników odżywczych produktu spożywczego podanego przez użytkownika.

--dodać zdjęcie--

W przypadku podanych błędnych danych przez użytkownika, bot o tym poinformuje.

--dodać zdjęcie--

W przypadku pytań, na które bot nie zna odpowiedzi zostanie wyświetlona odpowiedź domyślna.

--dodać zdjęcie--

## Demo
W celu obejrzenia dema projektu opisanego powyżej, należy skorzystać ze zdjęcia załączonego poniżej:

--dodać filmik--
