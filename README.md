# Tidrapportskalkylator Handel Sverige

---

Detta är en enkel webbaserad tidrapportskalkylator designad för att hjälpa anställda inom Handelsområdet i Sverige att beräkna sin lön, inklusive OB-tillägg och skatteavdrag. Kalkylatorn tar hänsyn till specifika regler för OB-ersättning som är vanliga inom handel.

## Funktioner

* **Enkel inmatning:** Lägg enkelt till rader för varje arbetsdag med datum, start- och sluttid, samt rast.
* **Automatisk OB-beräkning:** Beräknar OB-tillägg automatiskt baserat på angivna tider och veckodagar/helgdagar.
    * **Vardagar:** 50% efter kl. 18:15, 70% efter kl. 20:00.
    * **Lördagar:** 100% efter kl. 12:00.
    * **Söndagar och Helgdagar:** 100% hela dagen.
    * **Viktigt:** Raster dras i första hand **före** klockan 18:15 på vardagar, för att säkerställa korrekt OB-beräkning.
* **Helgdagshantering:** Identifierar automatiskt helgdagar (via `holidays.json`) och dagar som räknas som lördag (Påskafton, Midsommarafton, Julafton, Nyårsafton) för korrekt OB-beräkning. Möjlighet att manuellt markera en dag som helgdag.
* **Lönesummering:** Ger en tydlig sammanfattning av totala arbetstimmar, totala OB-timmar, bruttolön, skatteavdrag och utbetald nettolön.
* **Anpassningsbara inställningar:** Justera enkelt timlön och skattesats.
* **Lagra data lokalt:** Dina inmatade tider och inställningar sparas automatiskt i din webbläsares lokala lagring.
* **Import/Export:** Möjlighet att exportera tidrapporten till en CSV-fil samt importera tidigare sparad data.
* **Responsiv design:** Fungerar bra på både datorer och mobila enheter.

## Hur man använder den

1.  **Öppna kalkylatorn:** Klona repot och öppna `index.html` i din webbläsare, eller använd den live-versionen om det finns en.
2.  **Ange inställningar:** Fyll i din ordinarie timlön och din skattesats i procent i fälten under "Generella Inställningar".
3.  **Lägg till dagar:** Kalkylatorn startar med en tom rad. Använd knappen "Lägg till dag" för att lägga till fler rader för dina arbetspass.
4.  **Fyll i arbetspass:** För varje rad:
    * Välj **Datum**.
    * Ange **Starttid** och **Sluttid** (HH:MM-format).
    * Ange **Rast (min)** i minuter. Observera att rast på vardagar alltid antas tas före kl 18:15.
    * Markera "Helgdag?" om dagen är en särskild helgdag, eller om du vill tvinga 100% OB för hela passet (kalkylatorn markerar automatiskt söndagar och vissa andra helgdagar).
5.  **Se resultat:** Kalkylatorn uppdaterar automatiskt beräkningarna för varje rad och summerar totalerna längst ner.
6.  **Spara/Ladda:**
    * Dina data sparas **automatiskt** i din webbläsare.
    * Använd "Exportera data" för att spara en CSV-fil med din tidrapport.
    * Använd "Importera data" för att ladda en tidigare exporterad CSV-fil.
    * Använd "Rensa allt" för att nollställa kalkylatorn och ta bort all sparad data.

## Installation (för utvecklare/lokal körning)

1.  **Klona repot:**
    ```bash
    git clone [https://github.com/ditt-användarnamn/tidrapportskalkylator.git](https://github.com/ditt-användarnamn/tidrapportskalkylator.git)
    ```
2.  **Navigera till projektkatalogen:**
    ```bash
    cd tidrapportskalkylator
    ```
3.  **Öppna i webbläsaren:**
    Öppna filen `index.html` direkt i din webbläsare. Du behöver ingen webbserver för att köra denna kalkylator lokalt.

## Bidrag

Välkomna bidrag! Om du har förslag på förbättringar, buggfixar eller nya funktioner, vänligen skapa ett "issue" eller skicka in en "pull request".

## Licens

Detta projekt är licensierat under MIT-licensen. Se filen `LICENSE` för mer information.
