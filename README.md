# Algoritmer og datastrukturer - Oblig1
Oppgave 1
I oppgave 1 gikk jeg frem ved å bruke boblesortering, som sammenligner to naboverdier og bytter plass dersom de danner en inversjon (ved hjelp av bytt-metoden). Trenger kun at man går gjennom for-løkka en gang, for da vil det største elementet være på siste plassen, så det er sisteplassen som blir returnert.
For å finne antall ombyttinger la jeg på en teller som øker for hvert bytte.

a) Det blir n-1 sammenligninger. if-testen sammenligner én gang per runde i løkka, og ettersom for-løkka går fra 0 til lengden-1 blir det n-1 og ikke bare n.
b) Det blir færrest ombyttinger når arrayet er sortert stigende, altså ingen ombyttinger.
c) Det blir flest ombyttinger når arrayet er sortert omvendt, dvs. største tallet først og minste sist.
d) I gjennomsnitt blir det n(n-1)/4 ombyttinger.

Denne maks-metoden er dårligere enn de tidligere maks-metodene, fordi den gjør flere operasjoner enn nødvendig ved at den bytter plass på verdiene i arrayet for å finne den største.

Oppgave 2
I oppgave 2 gikk jeg frem ved å bruke to for-løkker, for å unngå å endre på tabellens innhold. Sjekker først om arrayet er sortert med erSortert-metoden og om arrayet er tomt. Hvis den er sortert og ikke tom går man videre. Telleren starter på 1, fordi det første tallet er unikt. Dermed starter også for-løkka på 1 og if-testen sammenligner nåværende verdi med forrige. Antallet økes dersom verdiene ikke er like.

Oppgave 3
I oppgave 3 har jeg også brukt to for-løkker. Den ytre for-løkka går gjennom hvert element, og antar at hvert element er unikt. Setter da boolean erUnik lik true. Den indre løkka starter på i + 1, for å unngå tidligere sammenligninger. If-testen sjekker om det nåværende verdien i den ytre løkka finnes igjen senere i tabellen. Hvis den finner igjen elementet settes erUnik lik false og man bryter ut av løkka. Når man har gått gjennom indre løkke sjekker man om om erUnik fortsatt er true, og hvis den er det økes telleren (antall) med én.

Oppgave 4
I oppgave 4 har jeg brukt partisjonering og kvikksortering.
I "hovedmetoden" har jeg brukt partisjonering for å dele tabellen inn i oddetall og partall. While-løkken fortsetter så lenge v er mindre eller lik h. if-testen sjekker om det er et oddetall med en modulusoperator som gir ut resten etter divisjon med 2. Hvis det ikke er 0, indikerer dette oddetall. Venstre peker flyttes da videre til høyre. Dersom det er 0, indikerer dette partall og v og h-verdi bytter plass. Når arrayet er delt opp, sorteres oddetallene og partallene hver for seg ved hjelp av kvikksortering.

Oppgave 5
I oppgave 5 har jeg brukt en form for rotasjon som lagrer verdien til siste posisjon i arrayet, forskyver alle elementene et steg til høyre, og deretter legger siste verdien først i arrayet.

Oppgave 7
I oppgave 7a har jeg brukt en flettemetode. Den oppretter et tomt array som er like langt som begge strengene, som lagrer resultatet av flettingen. Den første while-løkka går så lenge det er tegn igjen i begges strengene. Så legger den inn tegn fra s og tegn fra t annenhver gang. Dersom det er forskjellig lengde på de to strengene, vil en av de to siste while-løkkene brukes. Til slutt konverteres arrayet tilbake til streng.

I oppgave 7b starter jeg metoden med å finne totale lengden på alle strengene, for å vite hvor lang hjelpetabellen skal være. Deretter finner jeg lengden på den lengste strengen, så man vet når den ytre for-løkka skal stoppe. Metoden har to for-løkker, hvor den ytre løkka går gjennom bver bokstav i strengene (starter med første bokstav, så andre osv.). Den indre løkka går gjennom hvert "ord" og sjekker at den ikke er tom og at man er innenfor lengden på "ordet". Dersom if-testen er i orden legges tegnet til i arrayet. Til slutt konverteres arrayet til en ny streng.
