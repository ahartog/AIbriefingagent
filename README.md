# AI Briefing Agent

Een geplande Claude-taak die **elke ochtend om 06:44 (Amsterdamse tijd)** je agenda en mail doorneemt en een briefing naar hartogarie@gmail.com stuurt: wat je vandaag moet doen en op welke binnengekomen mails je actie moet nemen.

- Instructies voor de agent: [`BRIEFING_PROMPT.md`](BRIEFING_PROMPT.md)
- Connectors: Gmail + Google Calendar (account hartogarie@gmail.com)
- De agent doet alleen lezen. Hij stuurt geen antwoorden, verwijdert niets en wijzigt niets.

## Drie mailboxen
De Gmail-connector is gekoppeld aan **hartogarie@gmail.com**. Laat de andere twee adressen hun mail daarheen doorsturen:

1. **hartoghasnje@gmail.com**: Gmail → Instellingen → *Doorsturen en POP/IMAP* → *Een doorstuuradres toevoegen* → `hartogarie@gmail.com`, bevestig de code en kies "een kopie in de inbox bewaren".
2. **arie.hartog@key2control.nl**: bij Microsoft 365/Outlook: Instellingen → E-mail → *Doorsturen* → `hartogarie@gmail.com` (en "kopie bewaren" aanvinken). Lukt dat niet, vraag dan je IT-beheerder om een doorstuurregel. Let op: in je mail komt het adres ook voor als `ariehartog@key2control.nl` (zonder punt).

De agent herkent aan de oorspronkelijke ontvanger voor welke mailbox een mail bedoeld was en zet er een label bij: [Privé], [Hasnje] of [Key2Control].
