# ROADMAP

## Obiettivo

Personalizzare questo repository `al-folio` per trasformarlo nel sito accademico personale di Enrico Martini, facendo in modo che il sito rifletta in modo coerente il curriculum, la produzione scientifica e le attivita` professionali.

## Stato attuale del repository

Prima di modificare i contenuti, conviene partire da cio` che e` gia` presente:

- `_pages/about.md` e` gia` parzialmente personalizzato con nome, foto e un breve profilo.
- `_config.yml` contiene nome e URL corretti, ma titolo, descrizione, contatti e metadata sono ancora molto vicini al template.
- `_pages/cv.md` esiste, ma punta ancora a `example_pdf.pdf`.
- `_data/cv.yml` e` ancora il CV demo di Albert Einstein e va completamente sostituito.
- `_data/socials.yml` contiene ancora email, Scholar ID e link custom di esempio.
- `_bibliography/papers.bib` contiene gia` pubblicazioni reali, ma richiede pulizia, arricchimento metadata e deduplica di alcune voci.
- `_news/`, `_projects/`, `_teachings/`, `_posts/`, `_pages/profiles.md` e `_pages/repositories.md` contengono ancora materiale demo o semi-demo.

## Fase 0: Estrarre il curriculum in struttura dati

### Obiettivo

Trasformare il PDF del curriculum in un elenco strutturato di dati da distribuire nel sito.

### Input da ricavare dal CV

- intestazione: nome completo, ruolo, affiliazione, localita`, email, link principali
- bio breve: 4-6 righe per homepage
- interessi di ricerca: parole chiave e aree principali
- esperienza: ruoli, istituzioni, date, attivita`
- formazione: titoli, universita`, anni
- pubblicazioni: selezione delle piu` importanti e collegamenti a PDF/codice se disponibili
- progetti: linee di ricerca, software, dimostratori, collaborazioni
- teaching/service: corsi, supervisione, attivita` didattiche o di mentoring
- premi, certificazioni, invited talks, visiting positions, servizi editoriali se presenti

### Output atteso

Un foglio di lavoro unico, anche provvisorio, da usare come sorgente per i file YAML e Markdown del sito.

## Fase 1: Definire identita` e configurazione globale del sito

### File da modificare

- `_config.yml`
- `_data/socials.yml`

### Attivita`

- impostare un titolo del sito piu` professionale oppure lasciarlo vuoto se si vuole mostrare direttamente il nome completo
- riscrivere `description` con una tagline coerente con il CV
- aggiornare `keywords` con aree reali di ricerca
- verificare `lang` e decidere se tenere il sito in inglese o renderlo bilingue
- sostituire i placeholder nei contatti social con email, Google Scholar, GitHub, LinkedIn, ORCID, sito del laboratorio, ecc.
- collegare il PDF reale del CV tramite `cv_pdf`
- rivedere le feature globali: search, latest posts, social in search, repo trophies, Open Graph

### Criterio di completamento

Homepage, metadata e footer devono identificare chiaramente il profilo professionale senza riferimenti al template.

## Fase 2: Sistemare homepage e profilo personale

### File da modificare

- `_pages/about.md`
- `assets/img/emartini.jpg`

### Attivita`

- riscrivere il sottotitolo con ruolo, affiliazione e focus di ricerca
- aggiornare `more_info` con ufficio, dipartimento o contatti essenziali
- sostituire il testo bio con una presentazione piu` forte e allineata al CV
- decidere se mostrare o no `selected_papers`, `announcements` e `latest_posts`
- mantenere la pagina iniziale molto leggibile: chi sei, cosa fai, su cosa lavori, come contattarti

### Nota operativa

La homepage deve riassumere il CV in 30 secondi: ruolo, expertise, ambiti applicativi, contesto accademico/industriale e link rapidi alle sezioni importanti.

## Fase 3: Costruire una pagina CV fedele al PDF

### File da modificare

- `_data/cv.yml`
- `_pages/cv.md`
- `assets/pdf/`

### Attivita`

- sostituire completamente il contenuto demo di `_data/cv.yml` con i dati reali del curriculum
- mantenere una struttura pulita almeno per queste sezioni:
  - Education
  - Experience
  - Publications o Selected Publications
  - Awards / Honors
  - Teaching / Supervision
  - Skills / Methods / Tools
  - Service / Collaborations / Projects
- copiare il PDF reale in `assets/pdf/` con un nome stabile, ad esempio `enrico-martini-cv.pdf`
- aggiornare `_pages/cv.md` per mostrare il PDF corretto e una descrizione coerente

### Decisione importante

Se il PDF contiene molte sezioni non adatte al web, conviene sintetizzarle nella pagina CV e lasciare il PDF completo come versione scaricabile.

### Criterio di completamento

La pagina `/cv/` deve raccontare lo stesso profilo del PDF e offrire un download funzionante del CV.

## Fase 4: Allineare e rafforzare la sezione pubblicazioni

### File da modificare

- `_bibliography/papers.bib`
- `_pages/publications.md`
- `_data/coauthors.yml`
- `_data/venues.yml`
- `assets/pdf/`
- `assets/img/publication_preview/`

### Attivita`

- rivedere tutte le entry BibTeX gia` presenti
- eliminare duplicati o record quasi duplicati
- aggiungere campi utili come `doi`, `pdf`, `code`, `html`, `selected`, `preview`
- marcare come `selected={true}` i lavori piu` rappresentativi da mostrare anche in homepage
- completare `coauthors.yml` per dare link ai collaboratori ricorrenti
- completare `venues.yml` per normalizzare conferenze e journal

### Osservazione utile

Nel file attuale risultano gia` pubblicazioni reali e abbastanza numerose: questa sezione puo` diventare uno dei punti forti del sito con poco sforzo strutturale e molta cura editoriale.

### Criterio di completamento

La pagina `/publications/` deve essere coerente, senza duplicati evidenti, e ogni lavoro principale dovrebbe avere almeno un link utile.

## Fase 5: Trasformare i progetti demo in linee di ricerca reali

### File da modificare

- `_projects/*.md`
- `_pages/projects.md`
- `assets/img/`

### Attivita`

- rimuovere o sovrascrivere i progetti demo esistenti
- creare 3-6 schede progetto reali, per esempio:
  - human motion analysis
  - human pose estimation
  - multimodal / visual-inertial sensing
  - gait analysis and telemedicine
  - human-robot interaction
  - optimization and filtering for motion estimation
- per ogni progetto aggiungere:
  - titolo chiaro
  - descrizione breve
  - contesto applicativo
  - eventuali paper, codice, demo, immagini

### Criterio di completamento

La pagina `/projects/` deve spiegare le linee di ricerca anche a chi non legge il CV completo.

## Fase 6: Decidere cosa fare con teaching, news, blog e repositories

### File da valutare

- `_pages/teaching.md`
- `_teachings/*.md`
- `_pages/news.md`
- `_news/*.md`
- `_pages/blog.md`
- `_posts/*.md`
- `_pages/repositories.md`
- `_data/repositories.yml`
- `_pages/profiles.md`
- `_pages/about_einstein.md`

### Attivita`

- teaching:
  - se hai contenuti reali, sostituire i corsi demo
  - se non hai ancora materiale sufficiente, togliere la pagina dalla navigazione
- news:
  - convertire eventi reali del CV in news brevi
  - esempi: paper accepted, invited talk, visiting period, award, release software
- blog:
  - disattivarlo se non prevedi di usarlo nel breve
- repositories:
  - sostituire i repo demo con repository reali oppure nascondere la pagina
- profiles / people:
  - questa pagina e` chiaramente demo e va rimossa dalla navigazione o eliminata

### Criterio di completamento

La navbar deve contenere solo sezioni reali, curate e coerenti con il posizionamento professionale del sito.

## Fase 7: Pulizia contenuti demo e consistenza editoriale

### Attivita`

- cercare ed eliminare tutti i riferimenti a:
  - Albert Einstein
  - torvalds / alshedivat nei repository
  - email e link fake
  - immagini, descrizioni o testi generici del template
- uniformare lingua, stile e capitalizzazione delle pagine
- verificare che titoli e permalink siano coerenti

### Comando utile

Usare una ricerca globale per trovare i residui del template prima della pubblicazione.

## Fase 8: Rifinitura grafica minima ma professionale

### File da modificare

- `_config.yml`
- eventuali file in `_sass/` solo se necessario
- immagini in `assets/img/`

### Attivita`

- scegliere icona/favicon coerente
- valutare una foto profilo definitiva e immagini per progetti/pubblicazioni
- migliorare tagline, descrizioni, anteprime social e testo delle pagine
- intervenire sul CSS solo se serve migliorare leggibilita`, spaziature o gerarchie tipografiche

### Criterio di completamento

Il sito deve sembrare personale e professionale anche senza una grossa customizzazione grafica.

## Fase 9: Validazione finale

### Checklist tecnica

- eseguire `npx prettier . --write`
- eseguire `docker compose up --build`
- controllare:
  - homepage
  - CV
  - publications
  - projects
  - social links
  - immagini
  - download del PDF
  - dark mode
  - assenza di errori YAML o BibTeX

### Checklist contenutistica

- il profilo raccontato in homepage coincide con il CV?
- i ruoli e le date sono consistenti tra about, cv e publications?
- ci sono ancora pagine demo visibili?
- il sito aiuta un visitatore a capire rapidamente expertise, risultati e contatti?

## Ordine di esecuzione consigliato

1. Fase 0: estrazione dati dal CV
2. Fase 1: configurazione globale
3. Fase 2: homepage
4. Fase 3: CV e PDF
5. Fase 4: pubblicazioni
6. Fase 5: progetti
7. Fase 6: pulizia navigazione e sezioni opzionali
8. Fase 7: rimozione residui demo
9. Fase 8: rifinitura visiva
10. Fase 9: test finale

## Agenti consigliati

Se lavori con piu` agenti in parallelo, questa e` la combinazione piu` efficace.

### 1. Explorer per audit iniziale

- tipo: `explorer`
- modello consigliato: `gpt-5.4-mini`
- compito: mappare dove sono ancora presenti placeholder, contenuti demo e sezioni non allineate al CV

### 2. Worker principale per identita`, homepage e CV

- tipo: `worker`
- modello consigliato: `gpt-5.4`
- ownership:
  - `_config.yml`
  - `_data/socials.yml`
  - `_pages/about.md`
  - `_pages/cv.md`
  - `_data/cv.yml`
  - `assets/pdf/`
- motivo: e` il blocco piu` delicato per coerenza narrativa e accuratezza dei dati

### 3. Worker pubblicazioni

- tipo: `worker`
- modello consigliato: `gpt-5.4-mini` oppure `gpt-5.4` se vuoi molta cura editoriale
- ownership:
  - `_bibliography/papers.bib`
  - `_data/coauthors.yml`
  - `_data/venues.yml`
  - `assets/pdf/`
  - `assets/img/publication_preview/`
- motivo: e` un task molto strutturato, perfetto per un agente dedicato

### 4. Worker per progetti, news e pulizia demo

- tipo: `worker`
- modello consigliato: `gpt-5.4-mini`
- ownership:
  - `_projects/`
  - `_news/`
  - `_teachings/`
  - `_pages/blog.md`
  - `_pages/repositories.md`
  - `_pages/profiles.md`
  - `_pages/about_einstein.md`
  - `_data/repositories.yml`
- motivo: puo` avanzare in parallelo mentre il worker principale sistema CV e homepage

### 5. Agente coordinatore finale

- tipo: `default`
- modello consigliato: `gpt-5.4`
- compito: integrare le modifiche, fare review finale, lanciare test, verificare consistenza tra sezioni

## Strategia di parallelizzazione consigliata

1. usare un `explorer` per l'audit iniziale
2. avviare in parallelo:
   - un `worker` per CV/homepage/config
   - un `worker` per publications
   - un `worker` per projects/news/demo cleanup
3. lasciare al coordinatore finale il merge logico delle scelte editoriali e la validazione completa

## Definizione di "finito"

Il lavoro puo` considerarsi concluso quando:

- il sito non mostra piu` contenuti demo
- homepage, CV e publications raccontano lo stesso profilo
- il PDF del CV e` scaricabile
- la navbar contiene solo sezioni utili
- i contenuti principali sono allineati al curriculum reale
- il build locale funziona senza errori
