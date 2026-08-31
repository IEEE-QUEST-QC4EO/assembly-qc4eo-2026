# AQCEO Workshop Site

## Deploy su GitHub Pages
1. Crea un repo GitHub, carica tutti questi file.
2. Settings → Pages → Source: branch `main`, cartella `/root`.
3. Il sito sarà live su `https://<username>.github.io/<repo>/`.

## Come editare i contenuti
Tutti i dati principali (date, speaker, organizzatori, topics, link registrazione)
sono in **`_config.yml`** — modifica quello, non serve toccare HTML/CSS.

Il testo della sezione "About" e la struttura delle sezioni sono in **`index.md`**.

## Placeholder da sostituire
- `[ACRONYM]` → acronimo evento (in `_config.yml`)
- `[GOOGLE_FORM_LINK]` → link Google Form registrazione
- `[CONTACT_EMAIL]` → email di contatto
- `[AFFILIATION]` / `[EMAIL]` → dati organizzatori e speaker
- `[SPEAKER_NAME]` / `[TALK_TITLE]` / `[SHORT_BIO]` → aggiungi uno speaker per ogni relatore invitato
- `[ACCOMMODATION_PDF_LINK]` → link PDF alloggi
- Foto: sostituisci i file in `assets/img/speakers/` e `assets/img/logos/`
  mantenendo lo stesso nome file, oppure aggiorna il path in `_config.yml`
- Agenda: sostituisci i blocchi `.agenda-placeholder` in `index.md` con le righe
  `.agenda-row` (vedi esempio già presente per la Domenica)

## Test locale (opzionale, richiede Ruby + Jekyll)
```
bundle exec jekyll serve
```
