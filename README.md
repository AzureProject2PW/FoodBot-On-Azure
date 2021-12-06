# Dietetyczny Bot
Projekt realizowany w ramach przedmiotu *Wprowadzenie do aplikacji i rozwiązań opartych o Sztuczną Inteligencję i Microsoft Azure* prowadzonym na Politechnice Warszawskiej.

## Opis i cel projektu
Światowa Organizacja Zdrowia ogłosiła, że 800 milionów osób zmaga się z otyłością. Liczba osób chorujących wśród dorosłych wzrosła od 1975 roku prawie trzykrotnie. Chorujący są w każdym wieku, w każdej grupie społecznej oraz w krajach o różnym poziomie rozwinięcia. Szacuje się, że do 2025 roku na walkę z otyłością zostanie przeznaczone ponad bilion dolarów. Natomiast na zaburzenia odżywiania, które są przypadłościami psychosomatycznymi cierpi około 70 milionów osób na całym świecie. Około 6% przypadków tych zaburzeń kończy się śmiercią, zarówno spowodowanej skutkami zdrowotnymi, jak i samobójstwem. Dlatego w ramach projektu chcieliśmy stworzyć bota, który zwiększy świadomość na temat zaburzeń odżywiania, ale również będzie podawał przydatne informacje na temat zdrowego sposobu odżywiania. Powstały bot potrafi na podstawie podanych przez użytkownika danych wyliczyć wskaźnik masy ciała (BMI), zapotrzebowanie kaloryczne oraz zwrócić informacje na temat kaloryczności i zawartości odżywczych poszczególnych produktów spożywczych. Z naszym botem można komunikować się w języku angielskim.

<a href="https://pulsmedycyny.pl/who-otylosc-to-choroba-ktora-dotyka-800-mln-ludzi-na-swiecie-1110168" target="_blank">Link do danych na temat otyłości</a>

<a href="https://psychologiawpraktyce.pl/artykul/zaburzenia-odzywiania-wsrod-dzieci-i-mlodziezy" target="_blank">Link do danych na temat zaburzeń odżywiania</a>

## Skład zespołu
* Kinga Kocoł – <a href="https://github.com/kingakocol" target="_blank">Link do konta</a>
* Aleksandra Kowalczyk – <a href="https://github.com/Olakow" target="_blank">Link do konta</a>
* Martyna Jakubowska – <a href="https://github.com/mjakubowska" target="_blank">Link do konta</a>
* Aleksander Wodnicki – <a href="https://github.com/AleksanderWodnicki" target="_blank">Link do konta</a>

## Opis funkcjonalności
*Dietetyczny Bot* zawiera rozbudowaną bazę wiedzy związaną z tematyką zdrowego odżywiania oraz zaburzeń odżywiania. Dzięki tej bazie użytkownik ma możliwość komunikacji z botem poprzez zadawanie zróżnicowanych pytań.

Poniżej zostały opisane funkcjonalności *Dietetycznego Bota*:
- wyświetlanie informacji dotyczących zaburzeń odżywiania (czym są, opis kilku zaburzeń odżywiania (anoreksja, bulimia, ortoreksja, zaburzenia z napadami objadania się), objawy (zmiany w zachowaniu, psychiczne, fizyczne), skutki chorobowe, sposoby leczenia),
- przekazywanie informacji dotyczących zdrowego odżywiania i aktywności fizycznej,
- wyświetlanie informacji dotyczących najpopularniejszych diet,
- bot oprócz odpowiedzi w formie tekstowej, zwraca również odpowiedzi ze zdjęciami oraz linkami do stron zewnętrznych, które zawierają więcej informacji związanych z tematyką bota,
- obsługa *follow-up prompts*, które zwracają przykładowe pytania bądź hasła, które nawiązują do tematyki udzielonej odpowiedzi,
- wyświetlanie informacji dotyczącej kaloryczności i zawartości odżywczych podanych przez użytkownika składników odżywczych,
- wyliczanie wskaźnika masy ciała (BMI) na podstawie danych podanych przez użytkownika,
- wyliczanie zapotrzebowania kalorycznego na podstawie danych podanych przez użytkownika.

## Architektura
<p align="center">
  <img src="https://user-images.githubusercontent.com/64069048/144723367-8dfed661-4a9c-414f-b923-1bacd1e96b69.png"/>
</p>

## Wybrany stos technologiczny
- Azure:
  - Active Directory – nasz domyślna organizacja `Politechnika Warszawska` nieumożliwia nam korzystania ze wszystkich serwisów, między innymi z *Bot Service*, dlatego postanowiliśmy stworzyć nową organizację `DietBot-On-Azure`. Po utworzeniu nowej organizacji i przeniesieniu do niej subskrypcji mogliśmy korzystać z wymienionych serwisów niezbędnych do stworzenia projektu.
  - App Service – serwis ten został wykorzystany w przypadku *Bota Aplikacji Internetowej* oraz *QnA Maker*.
  - App Service Editor – dzięki niemu możliwe było edytowanie plików.
  - Bot Service – serwis ten umożliwił stworzenie *Bot Aplikacji Internetowej* DietBotOnAzure-Bot.
  - Cognitive Service – serwis ten umożliwił stworzenie *Knowledge Base* korzystając z *QnA Maker*, z bazy wiedzy korzysta utworzony przez nas bot.
  - LUIS (Language Understanding) – dzięki tej usłudze możliwe było dodanie funkcjonalności związanych z wyliczaniem wskaźnika masy ciała, zapotrzebowania kalorycznego oraz informowania o kaloryczności i zawartości odżywczych poszczególnych produktów spożywczych.
- środowisko programistyczne:
  - Bot Framework Composer – środowisko to umożliwiło lokalne tworzenie bota, a następnie opublikowanie go na platformie Azure.
  - Bot Framework Emulator – środowisko to umożliwiło przetestowanie powstałego bota lokalnie.
- Język:
  - C# – język wykorzystywany do edycji plików wspomnianych przy opisie usługi *Azure App Service Editor*.

## Opis działania rozwiązania
Aby uruchomić dietetycznego bota należy skożystać z tego linku. Następnie zostaniemy przekierowani do Web Chatu.

![bot_1](https://user-images.githubusercontent.com/64069048/144845276-dcf82e16-f600-43b5-ba89-3c316ac0fea6.png)

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
![website_1](https://user-images.githubusercontent.com/64069048/144846347-c9c2f40d-dd00-4d05-bb90-448402d70556.png)

W przypadku, niektórych pytań możliwe jest prowadzenie dłuższej konwersacji z botem. Przykładem jest pytanie o bulimię.

--dodać zdjęcie--

Bot umożliwia wyliczenie wskaźnika masy ciała (BMI) oraz zapotrzebowanie kaloryczne na podstawie podanych przez użytkownika danych. Jeżeli chcemy poznać swoje BMI należy poinformowac o tym bota - Calculate BMI., a następnie należy wykonywać polecenia bota. Podobnie jest w przypadku zapotrzebowania kalorycznego - Calculate DCR.

--dodać zdjęcie--

Nasz bot daje również możliwość zwracania informacji o kaloryczności i zawartości składników odżywczych produktu spożywczego podanego przez użytkownika. Najpierw należy poinformować bota o tym, że chcemy poznać kaloryczność produktu poprze wpisanie słowa food. Następnie należy podać nazwę produktu. Pojawiają się informacje o kaloryczności, zawartości węglowodanów, białka, tłuszczy i błonnika.

--dodać zdjęcie--

W przypadku podanych błędnych danych przez użytkownika, bot o tym poinformuje.

--dodać zdjęcie--

## Demo
W celu obejrzenia dema projektu opisanego powyżej, należy skorzystać ze zdjęcia załączonego poniżej:

--dodać filmik--
