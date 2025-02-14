# n8n Trivia Quiz

Dit project is een interactieve trivia quiz gebouwd in n8n, waarbij Discord-gebruikers een quiz kunnen starten en hun antwoorden kunnen zien in Discord. De quizvragen worden opgehaald via de Open Trivia Database (OpenTDB).

## 📌 Functionaliteiten
- Start de quiz in Discord door "start quiz" te sturen.
- Ontvang een Discord-bericht met een link naar het quizformulier.
- Vul je naam in en beantwoord de trivia-vraag.
- Na het beantwoorden word je teruggestuurd naar Discord.
- Ontvang een bericht met jouw antwoord en het correcte antwoord.

## 🛠️ Workflow Overzicht
Het project bestaat uit twee workflows:

### **Workflow 1: Start de quiz**
1. **Discord Trigger**: Activeert wanneer een gebruiker "start quiz" typt in Discord.
2. **HTTP Request**: Haalt een trivia-vraag op van OpenTDB.
3. **Code (JS Node)**: Formatteert de quizvraag en antwoordopties.
4. **Discord Webhook**: Stuurt een bericht in Discord met een link naar het quizformulier.

### **Workflow 2: Verwerk quiz antwoorden**
1. **Form Trigger**: Wacht op gebruikersinvoer (naam + antwoord).
2. **HTTP Request**: Haalt opnieuw de quizvraag op.
3. **Code (JS Node)**: Verwerkt het antwoord en vergelijkt het met het correcte antwoord.
4. **Form Node**: Stelt het quizformulier samen met de vraag en mogelijke antwoorden.
5. **Discord Webhook**: Stuurt een bericht naar Discord met de naam van de deelnemer, hun gekozen antwoord en het correcte antwoord.
6. **Finale Form Node**: Geeft een "Ga terug naar Discord"-link.

## 📋 Installatie en Configuratie
1. Zorg ervoor dat **n8n** is geïnstalleerd en draait.
2. Voeg een **Discord Bot** toe met de juiste rechten voor webhooks en berichten.
3. Stel **n8n webhooks** correct in en zorg ervoor dat deze toegankelijk zijn.
4. Configureer de juiste webhook-URL’s in je Discord webhook nodes.
5. Start beide workflows in n8n.

## 🚀 Gebruik
1. Ga naar Discord en stuur het bericht **"start quiz"**.
2. Klik op de link in het bericht van de bot.
3. Vul je naam in en kies een antwoord op de quizvraag.
4. Klik op verzenden en ga terug naar Discord.
5. Bekijk het resultaat in Discord!

## 🔧 Mogelijke Verbeteringen
- Meerdere vragen per quizronde.
- Score bijhouden per gebruiker.
- Meerdere moeilijkheidsgraden toevoegen.
- UI verbeteren met aangepaste styling in het formulier.

## 📄 Breakpoints
1. Beter plannen
2. Beter onze concentratie erbij houden
3. Hulp vragen als we hulp nodig hebben
