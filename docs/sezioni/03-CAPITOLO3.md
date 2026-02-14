# CAPITOLO 3 - L'IMPRONTA ECOLOGICA DELL'INTELLIGENZA ARTIFICIALE: COSTI NASCOSTI E CONTRADDIZIONI

## 3.1 Introduzione: il lato oscuro dell'AI

Questo capitolo esamina l'intelligenza artificiale non come *soluzione* alla crisi climatica, ma come *parte del problema* – un'infrastruttura tecnologica con un'impronta ecologica significativa e in rapida crescita.

### 3.1.1 La materialità nascosta dell'"immateriale"

La metafora della "nuvola" (*cloud*) per descrivere l'infrastruttura computazionale dell'AI è profondamente fuorviante. Come documenta [@Crawford2021] in *The Atlas of AI*, ciò che appare come eterea computazione digitale è in realtà radicato in catene materiali estremamente concrete: miniere di litio nel deserto di Atacama, estrazione di terre rare in Mongolia, data center che consumano milioni di litri d'acqua, cavi sottomarini che attraversano gli oceani, server raffreddati 24 ore su 24, chip semiconduttori prodotti in impianti che richiedono acqua ultrapura.

L'AI non è immateriale: è profondamente *terrestre*. Ogni query a ChatGPT, ogni raccomandazione di Netflix,  ogni predizione di un modello climatico richiede elettricità generata da qualche parte, hardware costruito con minerali estratti da qualche parte, calore dissipato attraverso sistemi di raffreddamento che consumano risorse. La "leggerezza" dell'interfaccia utente nasconde il peso dell'infrastruttura sottostante.

Questa materialità nascosta ha conseguenze ambientali che devono essere analizzate sistematicamente per comprendere il paradosso dell'AI: una tecnologia che promette di essere lo strumento della transizione ecologica, ma la cui crescita esponenziale sta generando pressioni ambientali sempre più significative. Come vedremo nelle sezioni seguenti, queste pressioni si manifestano lungo molteplici dimensioni: energia, acqua, materiali, rifiuti elettronici – ciascuna con le proprie implicazioni per la giustizia ambientale e per la sostenibilità dei sistemi socio-tecnici contemporanei.

## 3.2 Il consumo energetico dell'AI

### 3.2.1 L'energia per l'addestramento dei modelli

Il processo di addestramento di modelli di machine learning – in particolare dei grandi modelli di linguaggio (*Large Language Models*, LLM) e dei sistemi di deep learning – richiede quantità straordinarie di energia computazionale. Come ha documentato il pionieristico studio di [@Strubell2019], l'addestr amento di un singolo grande modello di elaborazione del linguaggio naturale può generare emissioni di CO₂ equivalenti a quelle prodotte da **cinque automobili durante l'intero ciclo di vita** – dalla produzione allo smaltimento.

I dati empirici sono impressionanti. [@Strubell2019] hanno calcolato che l'addestramento di un modello transformer con ricerca dell'architettura neurale (*neural architecture search*) emette circa **284.000 kg di CO₂e** (CO₂ equivalente). Per contestualizzare: questo corrisponde alle emissioni di 125 voli andata-ritorno tra New York e San Francisco, o al consumo energetico di una famiglia americana media per 57 anni. Anche modelli più piccoli generano impronte significative: un singolo modello BERT base emette circa 652 kg di CO₂e, equivalente a un volo transatlantico [@Strubell2019].

**GPT-3: un caso di studio emblematico.** Il modello GPT-3 di OpenAI, alla base di ChatGPT, rappresenta un esempio particolarmente illuminante dell'intensità energetica dell'AI contemporanea. Secondo le stime riportate da [@Patterson2021] e [@Li2023], l'addestramento di GPT-3 ha consumato **1.287 MWh** (megawattora) di elettricità e generato circa **552 tonnellate di CO₂e**. Per dare un ordine di grandezza: 1.287 MWh potrebbero alimentare circa 120 abitazioni americane medie per un anno intero [@Patterson2021].

È cruciale sottolineare che questi calcoli si riferiscono a un *singolo* ciclo di addestramento. Nella pratica dello sviluppo di modelli AI, i ricercatori raramente addestrano un modello una volta sola. Il processo tipico coinvolge:

1. **Sperimentazione con iperparametri**: testare decine o centinaia di configurazioni diverse per trovare quella ottimale
2. **Ablation studies**: addestrare versioni ridotte del modello per comprendere il contributo di diverse componenti
3. **Ri-addestramento**: quando arrivano nuovi dati o si correggono errori nel dataset
4. **Modelli ensemble**: addestrare multipli modelli per poi combinare le loro predizioni

[@Strubell2019] hanno documentato che il costo computazionale effettivo di sviluppare un modello NLP all'avanguardia può essere **78.000 volte superiore** al costo di un singolo addestramento, una volta inclusi tutti gli esperimenti di tuning. Questo significa che l'impronta di carbonio totale del processo di ricerca e sviluppo può raggiungere dimensioni astronomiche.

**La crescita esponenziale del compute.** Un trend particolarmente preoccupante riguarda la crescita esponenziale della potenza computazionale (*compute*) utilizzata per addestrare modelli AI. Come documentano [@Patterson2021], la quantità di compute necessaria per i modelli all'avanguardia è cresciuta di un fattore **10 ogni anno** dal 2012 al 2021. Questa crescita segue una curva esponenziale molto più ripida della Legge di Moore (che prevedeva un raddoppio ogni due anni).

Ciò che sta emergendo nella comunità del machine learning è quella che [@Schwartz2020] chiamano la cultura del **"compute maximalism"** o "Red AI": l'idea che modelli più grandi, addestrati con più dati e più compute, siano sempre migliori. Questa cultura privilegia l'accuratezza e le prestazioni a scapito dell'efficienza energetica. [@Schwartz2020] hanno analizzato gli articoli pubblicati nelle principali conferenze di machine learning e hanno trovato che circa il **90% degli articoli** riporta solo metriche di accuratezza, ignorando completamente il costo computazionale e l'impronta energetica dei metodi proposti.

Questo rappresenta un'inversione delle priorità rispetto al trend storico dell'informatica, dove l'efficienza – fare di più con meno – era considerata un valore fondamentale. Nel contesto dell'AI contemporanea, invece, prevale la logica opposta: fare di più richiede necessariamente *più* risorse, e questo viene accettato come inevitabile piuttosto che come un problema da risolvere [@Schwartz2020].

### 3.2.2 Il consumo energetico per l'inferenza (uso dei modelli)

Se l'addestramento dei modelli AI genera titoli allarmanti per la sua intensità energetica, è l'*inferenza* – l'uso quotidiano dei modelli già addestrati – a rappresentare la quota maggiore del consumo energetico totale dell'intelligenza artificiale. Come osserva [@deVries2023], mentre l'addestramento è un evento unico (o quantomeno occasionale) che genera picchi di consumo, l'inferenza è un processo continuo che avviene ogni volta che un utente interagisce con un sistema AI.

**Il predominio dell'inferenza nel bilancio energetico.** Secondo le stime riportate da [@deVries2023], l'inferenza rappresenta tra l'**80% e il 90%** del computing AI totale in termini di energia consumata. Questo perché, sebbene una singola query richieda ordini di grandezza meno energia di un addestramento completo, il numero di query è astronomico: milioni di utenti che interrogano quotidianamente ChatGPT, Alexa, Google Assistant, sistemi di raccomandazione, filtri antispam, riconoscimento facciale su smartphone.

Per contestualizzare: [@Li2023] stimano che una singola conversazione con ChatGPT (circa 10-50 query) consumi tra **0.01 e 0.05 kWh** di elettricità – una quantità relativamente piccola. Ma se moltiplichiamo questo per i 100 milioni di utenti attivi mensili che ChatGPT ha raggiunto nei primi mesi dopo il lancio, e consideriamo che ciascun utente fa multiple query giornaliere, arriviamo a consumi complessivi enormi. Secondo le proiezioni di [@deVries2023], se Google integrasse l'AI generativa in tutte le sue ricerche (attualmente circa 9 miliardi al giorno), il consumo energetico aggiuntivo sarebbe paragonabile al consumo annuale di interi paesi come l'Irlanda.

**Le proiezioni dell'International Energy Agency.** Nel report "Electricity 2024: Analysis and Forecast to 2026", l'International Energy Agency [@IEA2024] ha documentato come l'esplosione dell'AI stia contribuendo a un'impennata senza precedenti nel consumo elettrico dei data center a livello globale. Le proiezioni indicano che il consumo elettrico dei data center **raddoppierà entro il 2026**, raggiungendo circa **945 TWh** (terawattora) annui – equivalente al consumo elettrico combinato di Giappone e Germania [@IEA2024].

Non tutto questo aumento è attribuibile all'AI – anche il mining di criptovalute e l'espansione generale dei servizi cloud contribuiscono – ma l'AI rappresenta il fattore di crescita più rapido. Come riporta [@Kaack2022], le grandi aziende tech come Google e Microsoft hanno registrato aumenti del **20-34% anno-su-anno** nel consumo energetico dei loro data center dal 2018 al 2022, con l'AI identificata come il principale driver di questa crescita.

**Query apparentemente innocue, impatto cumulativo significativo.** Un aspetto particolarmente insidioso del consumo energetico da inferenza è la sua invisibilità per l'utente finale. Quando facciamo una domanda a ChatGPT o chiediamo a Siri di impostare una sveglia, non percepiamo alcun costo energetico – l'interazione appare istantanea e immateriale. Eppure, dietro ogni query si attivano server che processano miliardi di parametri, sistemi di raffreddamento che dissipano il calore generato, reti che trasmettono dati.

Secondo i calcoli di [@Li2023], ogni interazione con GPT-3 consuma tra **0.01 e 0.05 kWh** di elettricità a seconda della complessità della query. Moltiplicato per decine o centinaia di milioni di query giornaliere, questo si traduce in un'impronta energetica paragonabile a quella di intere città. E con l'integrazione sempre più pervasiva dell'AI in applicazioni quotidiane – dalle e-mail che si scrivono automaticamente ai filtri fotografici, dalle traduzioni istantanee ai suggerimenti di acquisto personalizzati – questo consumo "di sottofondo" è destinato a crescere esponenzialmente.

### 3.2.3 Data center e infrastruttura computazionale

**La spina dorsale energivora dell'AI.** I data center – le enormi strutture che ospitano i server su cui girano i modelli AI – rappresentano già oggi tra l'**1% e il 2% del consumo elettrico globale** [@Kaack2022; @IEA2024]. Questa percentuale può sembrare piccola, ma in termini assoluti corrisponde a centinaia di terawattora all'anno, più dell'intero consumo elettrico di molti paesi. E la quota è in rapida crescita.

Come documentato da [@IEA2024], l'espansione dell'AI sta mettendo sotto pressione le reti elettriche nazionali in modi senza precedenti. In alcune regioni degli Stati Uniti – in particolare Virginia, Oregon e Iowa, dove si concentrano i maggiori data center – le utilities elettriche stanno lottando per soddisfare la domanda crescente. Questo crea un paradosso perverso: mentre le società tech dichiarano impegni verso il 100% di energia rinnovabile, l'esplosione della domanda richiede la costruzione di nuova capacità elettrica che, almeno nel breve termine, viene spesso soddisfatta con centrali a gas naturale per la loro maggiore flessibilità e rapidità di costruzione rispetto alle rinnovabili [@Kaack2022].

**Il caso Google e Microsoft: crescita insostenibile.** I report di sostenibilità delle grandi tech company forniscono evidenza diretta di questa dinamica. Google, che aveva raggiunto l'obiettivo di operare al 100% con energia rinnovabile su base annuale, ha visto le sue **emissioni totali aumentare del 48% tra il 2019 e il 2022**, con l'espansione dell'AI identificata come principale causa [@Li2023]. Microsoft ha registrato un aumento ancora più marcato: **+34% di emissioni tra il 2020 e il 2022**, nonostante gli impegni pubblici verso la carbon neutrality entro il 2030 [@Li2023].

Questi dati rivelano un problema strutturale: anche quando i data center sono alimentati da energia rinnovabile *sulla carta* (attraverso l'acquisto di crediti di energia rinnovabile o Power Purchase Agreements), la crescita della domanda è così rapida che richiede l'espansione della capacità di generazione complessiva. E poiché le rinnovabili come solare ed eolico sono intermittenti e richiedono anni per essere costruite su larga scala, nel breve-medio termine questa domanda aggiuntiva viene inevitabilmente soddisfatta con fonti fossili, vanificando parzialmente gli sforzi di decarbonizzazione [@Kaack2022].

**Pressione sulle reti elettriche locali.** Un aspetto spesso trascurato riguarda l'impatto locale dei data center sulle comunità che li ospitano. Come documenta [@Crawford2021], la costruzione di grandi data center – che possono richiedere decine o centinaia di megawatt di potenza continua – crea tensioni significative con le reti elettriche locali. In alcune aree rurali degli Stati Uniti, un singolo data center può consumare più elettricità dell'intera città circostante, causando aumenti nelle tariffe elettriche per i residenti e ritardi nell'elettrificazione di altre infrastrutture [@Crawford2021].

Inoltre, i data center richiedono alimentazione elettrica estremamente affidabile – anche pochi minuti di blackout possono causare perdite di dati e interruzioni di servizio costose. Questo significa che le utilities devono mantenere capacità di riserva significative specificamente per servire i data center, riducendo l'efficienza complessiva del sistema elettrico e aumentando i costi per tutti gli utenti [@Kaack2022].

La prossima sezione esamina un impatto ambientale dell'AI ancora meno visibile ma altrettanto preoccupante: il consumo di acqua dolce per il raffreddamento dei data center.

## 3.3 Il consumo d'acqua: la "sete" dell'AI

### 3.3.1 Acqua per il raffreddamento dei data center

Mentre il dibattito pubblico sull'impronta ambientale dell'AI si è concentrato principalmente sulle emissioni di carbonio, un impatto altrettanto significativo ma molto meno discusso riguarda il **consumo di acqua dolce**. Come documentano [@Li2023] nel loro studio pionieristico "Making AI Less 'Thirsty'", l'addestramento e l'uso di modelli AI su larga scala richiedono quantità impressionanti di acqua per raffreddare i server dei data center.

**GPT-3: 700.000 litri di acqua evaporata.** Applicando la metodologia di lifecycle assessment ai data center di Microsoft dove è stato addestrato GPT-3, [@Li2023] hanno stimato che l'addestramento di questo singolo modello abbia consumato circa **700.000 litri di acqua dolce** direttamente evaporata nei sistemi di raffreddamento. Per contestualizzare: questa quantità basterebbe a produrre circa 370 automobili o 320 tonnellate di acciaio [@Li2023].

E questo calcolo si riferisce solo al consumo diretto (*scope 1*) – l'acqua effettivamente evaporata nelle torri di raffreddamento del data center. Se includiamo il consumo indiretto (*scope 2*) – l'acqua utilizzata nelle centrali elettriche per generare l'elettricità che alimenta il data center – i numeri diventano molto più grandi. [@Li2023] stimano che il consumo totale di acqua per addestrare GPT-3, includendo sia scope 1 che scope 2, varia tra **4 e 5,4 milioni di litri** a seconda della localizzazione del data center e del mix energetico regionale.

**Come funzionano i sistemi di raffreddamento.** Per comprendere perché l'AI è così "assetata", dobbiamo capire come funzionano i data center. I server che eseguono computazioni AI generano enormi quantità di calore – quasi tutta l'energia elettrica consumata viene convertita in calore che deve essere dissipato per evitare il surriscaldamento delle componenti. Esistono due principali sistemi di raffreddamento [@Li2023]:

1. **Torri di raffreddamento (*cooling towers*)**: usano un circuito aperto dove l'acqua assorbe il calore dai server e poi viene raffreddata in una torre attraverso l'evaporazione. Lungo questo processo, parte dell'acqua evapora e viene "consumata" (ossia non può essere recuperata). In media, i data center che usano torri di raffreddamento evaporano circa **1-9 litri di acqua per ogni kWh** di energia dei server, con una media globale di circa 1,8 L/kWh per Google e 9 L/kWh per grandi data center commerciali in Arizona durante l'estate [@Li2023].

2. **Raffreddamento ad aria esterna (*outside air cooling*)**: quando le condizioni climatiche lo permettono, alcuni data center usano direttamente aria esterna per raffreddare i server, evitando o riducendo l'uso di acqua. Tuttavia, questo è possibile solo in climi freschi e secchi, e comunque richiede acqua per il controllo dell'umidità quando l'aria esterna è troppo secca [@Li2023].

**Scale aggregate: miliardi di litri.** A livello aggregato, i numeri diventano astronomici. Google ha riportato di aver **prelevato 25 miliardi di litri di acqua** nel 2022 solo per i suoi data center proprietari – questo esclude i data center in cloud affittati a terzi [@Li2023]. Microsoft ha registrato un aumento del **34% nel consumo d'acqua tra il 2021 e il 2022**, attribuendo questa crescita principalmente all'espansione dell'infrastruttura AI [@Li2023].

Per dare un senso a questi numeri: 25 miliardi di litri potrebbero riempire circa 10.000 piscine olimpioniche, o soddisfare il fabbisogno annuale di acqua potabile di circa 250.000 persone nei paesi sviluppati [@Li2023].

### 3.3.2 Conflitti idrici e giustizia ambientale

Il consumo massiccio di acqua da parte dei data center non è solo una questione di quantità aggregate, ma solleva problemi acuti di **giustizia ambientale** e conflitti territoriali. Come documentano [@Li2023], i data center vengono spesso costruiti in regioni che stanno già affrontando stress idrico, creando tensioni con le comunità locali e compromettendo la sicurezza idrica di popolazioni vulnerabili.

**Il caso Uruguay: proteste popolari contro i data center.** Un esempio emblematico riguarda il progetto di Google per costruire un grande data center in Uruguay, un paese che ha attratto investimenti tech grazie alla disponibilità di energia rinnovabile a basso costo. Quando è emerso che il data center avrebbe consumato milioni di litri d'acqua al giorno in una regione già soggetta a siccità periodiche, le comunità locali hanno organizzato proteste e raccolte firme [@Li2023]. I residenti hanno denunciato che stavano già razionando l'acqua per uso domestico durante i periodi di siccità, mentre un'azienda straniera avrebbe avuto accesso illimitato alla risorsa per operazioni commerciali.

Questo caso rivela una dinamica di potere asimmetrica: le grandi tech companies negoziano accordi direttamente con i governi nazionali, spesso con incentivi fiscali e accesso prioritario alle risorse, mentre le comunità locali che subiscono gli impatti ambientali hanno scarso potere decisionale. Come osserva [@Crawford2021], questa è una manifestazione del colonialismo estrattivista applicato alle risorse digitali: regioni del Sud globale forniscono risorse materiali (acqua, energia, minerali) per sostenere infrastrutture che servono principalmente utenti del Nord globale.

**La crisi idrica globale e la scelta dei siti.** Il problema diventa ancora più grave se consideriamo le proiezioni sulla scarsità idrica futura. Secondo i dati citati da [@Li2023], si stima che circa il **50% della popolazione mondiale vivrà in aree water-scarce entro il 2050**. Eppure, come documenta il loro studio, una quota significativa dei data center esistenti e pianificati si trova già oggi in regioni caratterizzate da stress idrico.

[@Li2023] hanno analizzato la localizzazione dei data center di Microsoft e Google e hanno scoperto che molti sono situati in zone già classificate come *drought-prone* (soggette a siccità). Ad esempio, alcuni dei più grandi data center si trovano in Arizona, una regione desertica dove le città stanno già affrontando deficit idrici cronici e restrizioni all'uso dell'acqua. Altri si trovano in Texas e California, stati che hanno sperimentato siccità prolungate negli ultimi decenni [@Li2023].

La logica che porta a queste scelte di localizzazione apparentemente controintuitive riguarda altri fattori: vicinanza ai mercati, disponibilità di terra a basso costo, incentivi fiscali, connettività di rete, costi energetici. La disponibilità di acqua dolce, pur essendo critica per le operazioni, sembra pesare meno nelle decisioni di investimento [@Crawford2021].

**Scope 2: l'acqua nascosta nella generazione elettrica.** Un aspetto che rende il problema ancora più complesso riguarda il consumo idrico *indiretto*. Come spiegato nella sezione precedente, oltre all'acqua evaporata direttamente nei sistemi di raffreddamento dei data center (*scope 1*), c'è l'acqua consumata nelle centrali termoelettriche che generano l'elettricità per alimentare i data center (*scope 2*).

La generazione termoelettrica – da carbone, gas naturale o nucleare – richiede enormi quantità di acqua per il raffreddamento. Negli Stati Uniti, la media nazionale è di circa **43,8 litri prelevati e 3,1 litri consumati per ogni kWh** generato [@Li2023]. Questo significa che un data center che consuma 100 MWh di elettricità all'ora causa indirettamente il prelievo di circa 4,4 milioni di litri d'acqua nelle centrali elettriche, di cui circa 310.000 litri vengono effettivamente consumati (evaporati o inquinati e non restituibili all'ambiente) [@Li2023].

[@Li2023] sottolineano che le aziende tech tipicamente *non riportano* il consumo di acqua scope 2 nei loro sustainability report, concentrandosi solo sull'acqua usata direttamente nei loro data center. Questo crea una sottostima significativa dell'impronta idrica reale dell'AI. Quando si include lo scope 2, l'impronta idrica totale può essere **3-5 volte superiore** a quella riportata ufficialmente [@Li2023].

**Disuguaglianze globali nell'accesso all'acqua.** Il problema assume una dimensione di giustizia globale quando consideriamo che 2,2 miliardi di persone nel mondo non hanno ancora accesso ad acqua potabile sicura, e che la scarsità idrica è una delle principali cause di conflitti e migrazioni forzate [@Li2023]. In questo contesto, destinare miliardi di litri di acqua dolce per addestrare modelli AI che servono principalmente popolazioni benestanti solleva questioni etiche profonde.

Come osserva [@Luccioni2025] nella loro analisi degli effetti di secondo ordine dell'AI, questa è un'altra manifestazione del pattern generale: i benefici dell'AI (migliore efficienza, nuovi servizi, profitti aziendali) si concentrano in alcune regioni e classi sociali, mentre i costi ambientali (emissioni, consumo d'acqua, estrazione di minerali) ricadono sproporzionatamente su comunità vulnerabili e paesi del Sud globale.

## 3.4 Materiali e rifiuti elettronici

### 3.4.1 Estrazione di terre rare e minerali critici

L'infrastruttura fisica dell'intelligenza artificiale – GPU, TPU, server, sistemi di storage, reti di trasmissione – richiede una vasta gamma di **minerali critici e terre rare** la cui estrazione genera impatti ambientali e sociali devastanti. Come documenta [@Crawford2021] in *The Atlas of AI*, ogni componente dell'hardware AI nasconde una lunga catena di estrazione che attraversa il pianeta, dalle miniere di litio nel deserto di Atacama alle raffinerie di terre rare in Mongolia, dalle miniere di cobalto nella Repubblica Democratica del Congo agli impianti di produzione di semiconduttori a Taiwan.

**I materiali critici per l'AI.** Le GPU (Graphics Processing Units) e le TPU (Tensor Processing Units) – i chip specializzati che eseguono le computazioni di machine learning – richiedono una combinazione complessa di materiali [@Crawford2021; @Luccioni2025]:

- **Terre rare**: neodimio, disprosio, terbio, cerio, ittrio, gadolinio – usati per le loro proprietà magnetiche ed elettroniche uniche
- **Metalli di transizione**: litio, cobalto, nichel – per batterie di backup e sistemi di alimentazione
- **Semiconduttori**: silicio ultrapuro, gallio, germanio, arseniuro di gallio – per i chip
- **Metalli preziosi**: oro, argento, platino, palladio – per connessioni e conduttori
- **Altri metalli critici**: tungsteno, tantalio (coltan), indio, stagno – per condensatori e altri componenti

La produzione di questi materiali è altamente concentrata geograficamente. Come riporta [@Crawford2021], la **Cina controlla circa il 95% della produzione mondiale di terre rare**, non tanto per ragioni geologiche – questi minerali sono relativamente abbondanti nella crosta terrestre – quanto per la disponibilità del paese ad accettare i devastanti costi ambientali della loro estrazione e raffinazione.

**Baotou: il lago tossico della modernità digitale.** [@Crawford2021] descrive in dettaglio il caso di Baotou, in Mongolia Interna, sede del più grande deposito di terre rare del pianeta. Il processo di estrazione e raffinazione delle terre rare richiede l'uso massiccio di acidi solforici e nitrici per dissolvere i minerali dalla roccia. Secondo la Chinese Society of Rare Earths citata da [@Crawford2021], la raffinazione di una singola tonnellata di terre rare produce **75.000 litri di acque acide reflue e una tonnellata di residui radioattivi**.

Questi rifiuti tossici si accumulano in un enorme lago artificiale vicino a Baotou – un bacino di contenimento dove vengono scaricati i residui dell'industria mineraria. [@Crawford2021] descrive questo lago come "riempito con quello che la studiosa ambientale Myra Hird chiama 'i rifiuti che vogliamo dimenticare'" – una discarica di sostanze tossiche e radioattive che rappresenta il costo nascosto e invisibile della nostra economia digitale.

Il rapporto tra materiale utile e scarto è estremo. [@Crawford2021] riporta che nell'estrazione di disprosio e terbio nella provincia di Jiangxi, solo lo **0,2% dell'argilla estratta** contiene effettivamente elementi di terre rare utilizzabili. Questo significa che il **99,8% del materiale rimosso** viene scartato come rifiuto (*tailings*), scaricato nelle colline e nei corsi d'acqua, creando nuovi inquinanti come ammonio e compromettendo gli ecosistemi locali.

**Geopolitica dell'estrazione e territori indigeni.** Come documentano [@Luccioni2025], i minerali critici vengono estratti in modo sproporzionato da territori indigeni e da zone già soggette a stress ambientale. Il loro studio evidenzia che circa il **54% dei materiali critici** utilizzati nell'industria tech globale proviene da territori indigeni, spesso senza il consenso informato delle comunità locali e con impatti devastanti sui loro modi di vita tradizionali [@Luccioni2025].

Inoltre, il **62% dell'estrazione di minerali critici** avviene in zone classificate come *drought-prone* (soggette a siccità) [@Luccioni2025]. Questo crea un doppio problema: l'estrazione mineraria richiede grandi quantità di acqua per il processing, competendo con le necessità delle comunità locali e dell'agricoltura; e la contaminazione delle falde acquifere riduce ulteriormente la disponibilità di acqua potabile in regioni già idricamente vulnerabili.

### 3.4.2 E-waste e ciclo di vita dell'hardware

Oltre agli impatti dell'estrazione mineraria, l'infrastruttura AI genera un flusso crescente di **rifiuti elettronici** (*e-waste*) dovuto ai cicli di aggiornamento sempre più rapidi dell'hardware e all'obsolescenza programmata dei componenti. Come documentano [@Crawford2021] e [@Luccioni2025], i rifiuti elettronici rappresentano la frazione di rifiuti solidi in più rapida crescita a livello globale, con implicazioni ambientali e sanitarie gravi.

**La scala del problema e-waste.** Secondo i dati citati da [@Luccioni2025], nel 2022 sono stati generati circa **62 milioni di tonnellate (Mt)** di rifiuti elettronici a livello globale. Di questi, solo circa il **22% viene formalmente raccolto e riciclato** attraverso sistemi certificati. Il restante 78% finisce in discariche, viene incenerito, o – nel peggiore dei casi – viene esportato illegalmente verso paesi del Sud globale dove viene smaltito in modo informale con tecniche pericolose per la salute umana e l'ambiente [@Luccioni2025].

L'industria AI contribuisce a questo flusso in modi specifici e accelerati. Le GPU e le TPU utilizzate per il machine learning hanno cicli di vita molto più brevi rispetto all'hardware consumer standard. Come osserva [@Crawford2021], mentre un computer personale può rimanere funzionale per 5-10 anni, l'hardware specializzato per l'AI viene spesso sostituito ogni **2-3 anni** o anche più frequentemente per rimanere al passo con le esigenze computazionali dei modelli sempre più grandi.

**La corsa all'hardware e l'obsolescenza accelerata.** Questa dinamica è guidata da quella che [@Luccioni2025] chiamano la "corsa agli armamenti computazionali". Ogni nuova generazione di modelli AI richiede hardware più potente: più memoria, maggiore larghezza di banda, capacità di calcolo parallelo più elevate. Le aziende sono quindi costrette ad aggiornare costantemente i loro data center per rimanere competitive, generando montagne di hardware "obsoleto" che tecnicamente funziona ancora ma non è più abbastanza performante per i carichi di lavoro contemporanei.

Questo crea un paradosso particolarmente evidente: mentre l'AI viene presentata come strumento per l'economia circolare e l'ottimizzazione delle risorse (come discusso nella sezione 2.4), l'infrastruttura stessa dell'AI segue una logica profondamente lineare e estrattivista – estrai, produci, usa brevemente, scarta – che è l'antitesi dei principi dell'economia circolare [@Crawford2021].

**Tossicità e rischi sanitari.** I componenti elettronici contengono una miscela complessa di materiali, molti dei quali tossici. Come documenta [@Crawford2021], quando i rifiuti elettronici vengono smaltiti in modo improprio – bruciati a cielo aperto per recuperare i metalli preziosi, o scaricati in discariche dove i composti chimici filtrano nel terreno e nelle falde acquifere – rilasciano sostanze pericolose:

- **Metalli pesanti**: piombo, mercurio, cadmio, cromo esavalente – neurotossici e cancerogeni
- **Ritardanti di fiamma**: composti bromati e clorurati – interferenti endocrini e persistenti nell'ambiente
- **Plastiche**: quando bruciate, rilasciano diossine e furani – tra le sostanze più tossiche conosciute
- **Acidi e solventi**: usati nel processing, contaminano suolo e acqua

[@Crawford2021] descrive le comunità del Sud globale – in particolare in Ghana, Nigeria, India, Pakistan, Cina – dove i rifiuti elettronici del Nord vengono "riciclati" informalmente. Bambini e adulti bruciano circuiti stampati per estrarre rame e oro, respirando fumi tossici; immergono componenti in bagni acidi per recuperare metalli preziosi, senza protezioni adeguate. Studi sanitari in queste aree hanno documentato livelli allarmanti di piombo nel sangue, danni neurologici, malattie respiratorie e tassi elevati di cancro [@Crawford2021].

**Il "commercio tossico" globale.** Anche se esistono convenzioni internazionali – come la Convenzione di Basilea che dovrebbe limitare il trasferimento di rifiuti pericolosi dai paesi sviluppati a quelli in via di sviluppo – [@Crawford2021] documenta come enormi quantità di e-waste continuino a fluire dal Nord al Sud globale attraverso canali legali e illegali. 

I rifiuti elettronici vengono spesso esportati con l'etichetta di "equipaggiamento usato" o "donazioni per il riuso", aggirando le restrizioni. Una volta arrivati a destinazione, gran parte di questo materiale risulta non funzionante o non riparabile e finisce smaltito in modo informale [@Crawford2021]. Questo rappresenta un trasferimento di costi ambientali e sanitari: i paesi ricchi godono dei benefici dell'innovazione tecnologica accelerata, mentre i paesi poveri subiscono i costi dello smaltimento dei rifiuti tossici.

**Limiti strutturali del riciclo.** Anche quando l'e-waste viene riciclato formalmente, il processo è tutt'altro che perfetto. [@Luccioni2025] sottolineano che il tasso del 22% di riciclo formale nasconde il fatto che molti materiali non vengono effettivamente recuperati. Il riciclo di componenti elettronici è tecnicamente complesso e costoso: richiede processi di separazione sofisticati per estrarre i diversi metalli dalla matrice composita dei circuiti stampati.

Alcuni materiali – come le terre rare – sono particolarmente difficili da recuperare. [@Crawford2021] osserva che il costo economico ed energetico di riciclare terre rare da vecchi dispositivi è spesso superiore al costo di estrarre minerale vergine, creando un disincentivo economico al riciclo. Il risultato è che, nonostante la retorica dell'economia circolare, la maggior parte delle terre rare utilizzate nell'elettronica vengono estratte ex novo e poi perse quando i dispositivi diventano rifiuti.

**Verso una prospettiva di lifecycle completo.** Questi dati evidenziano la necessità di valutare l'impatto ambientale dell'AI attraverso un'analisi completa del ciclo di vita (*lifecycle assessment*), che includa:
- L'estrazione e raffinazione dei minerali
- La produzione dei componenti (chip, server, storage)
- Il trasporto e l'assemblaggio
- L'uso operativo (energia, acqua, raffreddamento)
- Lo smaltimento a fine vita

Come argomenteranno [@Luccioni2025] nella loro analisi del paradosso di Jevons applicato all'AI, concentrarsi solo sull'efficienza energetica operativa – pur importante – rischia di oscurare questi impatti "upstream" (estrazione, produzione) e "downstream" (smaltimento) che sono ugualmente significativi dal punto di vista ambientale e di giustizia sociale.

La prossima sezione integra questi diversi impatti materiali ed energetici attraverso la lente teorica del paradosso di Jevons, mostrando come i guadagni di efficienza nell'AI possano paradossalmente portare a un aumento del consumo totale di risorse.

## 3.5 Il paradosso di Jevons applicato all'AI

### 3.5.1 Cos'è il paradosso di Jevons

Il **paradosso di Jevons**, o effetto rimbalzo (*rebound effect*), rappresenta una delle critiche empiriche più potenti alla fiducia ingenua nell'efficienza tecnologica come soluzione ai problemi ambientali. Come discusso nel Capitolo 1 (sezione 1.2.3), questo fenomeno – identificato dall'economista britannico William Stanley Jevons nel XIX secolo nel contesto delle macchine a vapore – descrive come i guadagni di efficienza possano paradossalmente portare a un *aumento* anziché a una diminuzione del consumo totale di risorse.

Il meccanismo è apparentemente controintuitivo ma empiricamente ben documentato: quando una tecnologia diventa più efficiente, i suoi costi d'uso diminuiscono, rendendone l'utilizzo più economico e accessibile. Questo stimola un maggiore utilizzo della tecnologia stessa, l'espansione delle sue applicazioni, e talvolta la crescita economica complessiva che aumenta la domanda di risorse a livello sistemico. Il risultato netto può essere un *aumento* del consumo totale, nonostante i guadagni di efficienza per unità di output [@Luccioni2025].

Come ricordato nel Capitolo 1, [@Luccioni2025] identificano tre tipi di effetti rimbalzo:

1. **Effetto rimbalzo diretto**: l'efficienza riduce il costo d'uso, stimolando maggiore utilizzo della stessa tecnologia (es: automobili più efficienti → si guida di più)

2. **Effetto rimbalzo indiretto**: il risparmio economico viene speso per altri beni/servizi ad alta intensità di risorse (es: risparmi sul carburante → volo aereo)

3. **Effetto rimbalzo sistemico**: l'efficienza stimola crescita economica complessiva, aumentando la domanda totale di risorse (es: interi settori economici si espandono grazie alle nuove tecnologie efficienti)

L'applicazione di questo framework all'intelligenza artificiale, come dimostrano [@Luccioni2025] nel loro recente studio, rivela dinamiche preoccupanti che minano le narrative ottimistiche sulla sostenibilità dell'AI.

### 3.5.2 L'effetto rimbalzo nell'AI

L'intelligenza artificiale manifesta tutti e tre i tipi di effetto rimbalzo identificati da [@Luccioni2025], in modi che sono allo stesso tempo tecnicamente sofisticati e strutturalmente prevedibili. La loro analisi dimostra come i guadagni di efficienza computazionale – spesso celebrati come "Green AI" – possano paradossalmente accelerare la crescita complessiva dell'impronta ambientale del settore.

**Effetti rimbalzo diretti: modelli più grandi, training più frequente.** Il primo e più evidente effetto rimbalzo nell'AI riguarda il rapporto tra efficienza e scala dei modelli. Come documentano [@Luccioni2025], ogni volta che viene sviluppata una tecnica che rende l'addestramento più efficiente – algoritmi migliori, hardware specializzato, ottimizzazioni software – questa efficienza non si traduce in una riduzione del consumo totale, ma piuttosto viene "reinvestita" in modelli ancora più grandi e computazionalmente intensivi.

Ad esempio, quando [@Patterson2021] hanno dimostrato che modelli *sparse* (con attivazione parziale dei parametri) possono consumare meno di 1/10 dell'energia di modelli densi equivalenti mantenendo prestazioni simili, la risposta del settore non è stata "usiamo meno energia mantenendo modelli della stessa dimensione", ma piuttosto "costruiamo modelli 10 volte più grandi allo stesso costo energetico". Il risultato: il consumo energetico rimane costante o aumenta, mentre la complessità e la capacità computazionale crescono esponenzialmente [@Luccioni2025].

[@Luccioni2025] documentano che il numero di parametri nei modelli all'avanguardia è cresciuto di oltre **10.000 volte** tra il 2018 e il 2023 (da BERT con 340 milioni di parametri a GPT-4 con centinaia di miliardi). Questa crescita è stata resa possibile proprio dai guadagni di efficienza hardware e algoritmica, che hanno abbassato la "barriera all'ingresso" per addestrare modelli giganteschi.

Inoltre, i modelli più efficienti rendono economicamente sostenibile un addestramento più frequente. Invece di addestrare un modello una volta e usarlo per anni, le aziende ora ri-addestrano continuamente i modelli su dati aggiornati, eseguono esperimenti multipli, creano varianti specializzate per diversi task. [@Luccioni2025] citano il caso di DeepSeek-R1, un modello che richiede ri-addestramento frequente per mantenere le prestazioni, moltiplicando l'impronta energetica totale nonostante l'efficienza per singola iterazione.

**Effetti rimbalzo indiretti: democratizzazione e proliferazione.** Il secondo tipo di effetto rimbalzo opera attraverso l'espansione dell'accesso. Come osservano [@Luccioni2025], quando l'AI diventa più efficiente e quindi più economica, il suo utilizzo si espande a nuove applicazioni e nuovi utenti che prima non potevano permettersela.

Questo è particolarmente evidente con l'avvento di API pubbliche e modelli as-a-service. ChatGPT, Claude, Gemini e altri LLM sono ora accessibili gratuitamente o a costi molto bassi a centinaia di milioni di utenti. Ogni utente genera centinaia o migliaia di query, creando un carico computazionale aggregato enorme. [@deVries2023], come menzionato nella sezione 3.2.2, stima che se Google integrasse l'AI generativa in tutte le sue ricerche, il consumo energetico aggiuntivo sarebbe paragonabile al consumo annuale dell'Irlanda.

Ma l'effetto indiretto va oltre l'uso consumer. [@Luccioni2025] documentano come l'AI più accessibile stimoli la creazione di applicazioni che prima erano impossibili: chatbot personalizzati per ogni sito web, assistenti virtuali integrati in ogni app, sistemi di raccomandazione sempre più sofisticati, filtri AI per foto e video, traduzione in tempo reale, generazione di contenuti multimediali. Ciascuna di queste applicazioni, individualmente modesta, contribuisce al carico computazionale complessivo.

Un esempio citato da [@Luccioni2025] riguarda gli strumenti di "AI writing assistants" integrati in software di produttività. Tools come Grammarly, Notion AI, Microsoft Copilot eseguono continuamente inferenze AI mentre gli utenti scrivono, controllando grammatica, suggerendo riformulazioni, completando frasi. Ogni keystroke può potenzialmente triggerare una chiamata API. Moltiplicato per milioni di utenti che usano questi strumenti quotidianamente per ore, il consumo energetico aggregato diventa significativo – ma invisibile all'utente finale.

**Effetti rimbalzo sistemici: l'AI al servizio di industrie estrattive.** Il terzo e più preoccupante tipo di effetto rimbalzo riguarda l'uso dell'AI per espandere e ottimizzare settori economici ad alta intensità di carbonio. [@Luccioni2025] documentano numerosi casi dove l'AI viene applicata non per ridurre le emissioni, ma per *aumentare l'efficienza di industrie fossili*, portando paradossalmente a maggiori emissioni totali.

**Il caso Microsoft-ExxonMobil.** L'esempio più emblematico citato da [@Luccioni2025] riguarda la partnership tra Microsoft e ExxonMobil per l'uso dell'AI nell'esplorazione petrolifera. Microsoft ha sviluppato algoritmi di machine learning per analizzare dati geologici e identificare giacimenti petroliferi con maggiore precisione, permettendo a ExxonMobil di aumentare la produzione di **50.000 barili al giorno** nel bacino Permiano in Texas.

[@Luccioni2025] hanno calcolato che le emissioni di CO₂ derivanti da questo aumento di produzione petrolifera superano di **640 volte** le emissioni che Microsoft dichiara di aver evitato attraverso i suoi progetti di carbon removal (cattura e sequestro del carbonio). In altre parole: mentre pubblicamente Microsoft si impegna per la neutralità carbonica e investe in tecnologie di rimozione della CO₂, privatamente vende servizi AI che causano emissioni centinaia di volte superiori a quelle che dichiara di rimuovere.

Questo non è un caso isolato. [@Kaack2022] documentano l'uso diffuso dell'AI in:
- **Esplorazione petrolifera e di gas**: ottimizzazione delle trivellazioni, identificazione di giacimenti, riduzione dei costi di esplorazione
- **Agricoltura intensiva**: ottimizzazione di allevamenti industriali che generano enormi emissioni di metano
- **Logistica di merci**: rendendo più efficiente il trasporto di beni materiali, stimola l'aumento del commercio globale e quindi delle emissioni da trasporto
- **Fast fashion**: sistemi di raccomandazione che accelerano il ciclo di consumo di abbigliamento

In ciascuno di questi casi, l'AI rende le industrie problematiche più *efficienti* – ma questa efficienza si traduce in maggiore *volume* di attività, non in riduzione dell'impatto ambientale totale. Questo è precisamente il meccanismo del paradosso di Jevons operante a livello sistemico [@Luccioni2025].

**Quantificare il rimbalzo: oltre il 100%?** In alcuni casi, l'effetto rimbalzo può essere così forte da superare completamente i guadagni di efficienza – quello che gli economisti chiamano "backfire" (controeffetto). [@Luccioni2025] citano studi che suggeriscono che in certi settori tecnologici, per ogni miglioramento dell'1% nell'efficienza energetica, il consumo totale aumenta dello 0,5-1,5%, a seconda del contesto e delle dinamiche di mercato.

Nel caso dell'AI, [@Luccioni2025] argomentano che siamo probabilmente già in una situazione di backfire: i miglioramenti nell'efficienza computazionale (misurata come operazioni per watt) sono stati drammatici negli ultimi 10 anni, ma il consumo energetico totale dell'industria AI è *aumentato* ancora più rapidamente. Le proiezioni dell'IEA sul raddoppio del consumo dei data center entro il 2026 (discusse nella sezione 3.2.2) confermano questa dinamica [@IEA2024].

**Implicazioni per le politiche "Green AI".** Queste evidenze sollevano seri dubbi sull'efficacia delle iniziative "Green AI" che si concentrano esclusivamente sull'efficienza tecnica. Come argomentano [@Luccioni2025], migliorare l'efficienza energetica dell'addestramento e dell'inferenza è certamente importante – sarebbe peggio se i modelli fossero *anche* inefficienti. Ma in assenza di limiti assoluti sulla scala e sull'uso dell'AI, l'efficienza da sola non garantisce riduzioni nell'impronta ambientale totale, e può anzi facilitare un'espansione ancora più rapida del settore.

[@Kaack2022] arrivano a conclusioni simili, sostenendo che le politiche per l'AI sostenibile devono andare oltre l'efficienza tecnica e affrontare le dinamiche economiche e istituzionali che guidano la crescita del settore: incentivi al profitto, competizione tra aziende, mancanza di regolamentazione, esternalizzazione dei costi ambientali.

La sezione successiva esamina il dibattito "Green AI vs Red AI" per contestualizzare queste dinamiche nella cultura della ricerca in machine learning.

### 3.5.3 Il dibattito "Green AI vs Red AI"

Il fenomeno degli effetti rimbalzo nell'AI si interseca con un dibattito metodologico che ha iniziato a emergere all'interno della comunità di machine learning: la distinzione tra **"Red AI"** e **"Green AI"**. Questa distinzione, introdotta da [@Schwartz2020], rappresenta un tentativo di reindirizzare le priorità della ricerca AI verso una maggiore sostenibilità, ma rivela anche le resistenze culturali e istituzionali che rendono difficile questo cambiamento.

**Red AI: la cultura del "compute maximalism".** [@Schwartz2020] usano il termine "Red AI" per descrivere l'approccio dominante nella ricerca di machine learning: massimizzare l'accuratezza dei modelli a prescindere dal costo computazionale. In questa paradigma, l'efficienza energetica è considerata secondaria o irrilevante; ciò che conta è ottenere le migliori prestazioni possibili sul benchmark, anche se questo richiede addestrare modelli sempre più grandi su hardware sempre più potente.

Questa cultura è profondamente radicata negli incentivi della ricerca accademica e industriale. I paper che raggiungono lo "state-of-the-art" (le migliori prestazioni) su dataset standardizzati hanno maggiori probabilità di essere accettati alle conferenze prestigiose, di ottenere citazioni, di portare a carriere accademiche di successo. Le aziende competono per sviluppare i modelli più capaci, perché questo genera attenzione mediatica, attira investimenti, e crea vantaggio competitivo nel mercato [@Schwartz2020].

**Green AI: efficienza come metrica primaria.** In contrasto, [@Schwartz2020] propongono il concetto di "Green AI": ricerca che considera l'efficienza computazionale non come vincolo secondario ma come obiettivo primario. Questo significa:

1. **Riportare costi computazionali**: tutti i paper dovrebbero includere non solo l'accuratezza raggiunta, ma anche il tempo di addestramento, il numero di operazioni in virgola mobile (FLOPs), il consumo energetico stimato, le emissioni di CO₂

2. **Valorizzare l'efficienza nelle valutazioni**: le conferenze e i journal dovrebbero dare credito a metodi che raggiungono prestazioni competitive con meno risorse, anche se non ottengono il punteggio assoluto più alto

3. **Sviluppare benchmark di efficienza**: oltre ai tradizionali benchmark di accuratezza, creare competizioni che premiano il miglior rapporto prestazioni/energia

4. **Democratizzare la ricerca**: metodi più efficienti permettono a ricercatori con meno risorse computazionali di contribuire, riducendo la concentrazione della ricerca AI nelle grandi corporation

**La resistenza al cambiamento.** Nonostante queste proposte, [@Schwartz2020] documentano che il cambiamento è stato lento. Nella loro analisi degli articoli pubblicati nelle principali conferenze di machine learning, hanno trovato che circa il **90% degli articoli** continua a riportare solo metriche di accuratezza, omettendo completamente informazioni su costi computazionali ed energetici.

Questo non è solo pigrizia o disattenzione. [@Luccioni2025] argomentano che esistono incentivi strutturali che rendono difficile l'adozione della Green AI:

- **Competizione per il prestigio**: in un campo altamente competitivo, dedicare risorse computazionali all'ottimizzazione dell'efficienza piuttosto che al miglioramento dell'accuratezza può significare perdere la "corsa" per pubblicare il modello migliore

- **Accesso asimmetrico alle risorse**: le grandi aziende tech hanno data center così vasti che il costo energetico di addestrare modelli enormi è marginale rispetto al loro budget; per loro, l'efficienza è meno critica che per laboratori universitari con budget limitati

- **Mancanza di dati pubblici**: senza dati standardizzati sui consumi energetici dei diversi modelli e sistemi, è difficile fare confronti significativi e premiare l'efficienza

- **Assenza di regolamentazione**: a differenza di settori come l'automotive o l'edilizia, dove esistono standard di efficienza energetica obbligatori, l'industria AI opera in un vuoto regolatorio pressoché completo

**Oltre la dicotomia Red/Green.** [@Luccioni2025] suggeriscono che la distinzione Red AI/Green AI, pur utile pedagogicamente, rischia di essere eccessivamente semplicistica. Il vero problema non è scegliere tra efficienza e prestazioni, ma riconoscere che *l'efficienza da sola non basta* in presenza di effetti rimbalzo sistemici.

Anche se tutta la ricerca AI diventasse "Green" nel senso di [@Schwartz2020] – modelli più efficienti, hardware ottimizzato, algoritmi parsimoniosi – fintanto che gli incentivi economici premiano la crescita e l'espansione, il consumo totale continuerebbe ad aumentare. Come dimostrato nella sezione precedente sul paradosso di Jevons, modelli più efficienti rendono l'AI più accessibile e quindi ne amplificano l'uso, potenzialmente annullando i guadagni di efficienza a livello aggregato [@Luccioni2025].

Questo suggerisce che una vera AI sostenibile richiede non solo innovazione tecnica (Green AI) ma anche cambiamenti nelle strutture di governance, negli incentivi economici, e nelle priorità sociali – temi che esploreremo nella sezione 3.7 sull'interpretazione sociologica critica.

## 3.6 Opacità e mancanza di trasparenza

### 3.6.1 I dati mancanti

Uno degli ostacoli più significativi alla comprensione e alla regolamentazione dell'impronta ambientale dell'AI è la **mancanza di trasparenza** da parte delle aziende che sviluppano e deployano questi sistemi. Come documentano [@Crawford2021] e [@Li2023], le grandi tech companies trattano i dati sui consumi energetici e idrici dei loro modelli AI come informazioni proprietarie e commercialmente sensibili, rendendo estremamente difficile una valutazione indipendente dei loro impatti.

**Il problema delle "AI model cards" incomplete.** Negli ultimi anni, sotto pressione della comunità di ricerca e della società civile, alcune aziende hanno iniziato a pubblicare "model cards" – documenti che descrivono le caratteristiche dei modelli AI, incluse informazioni sul loro addestramento e performance. Tuttavia, come criticano [@Li2023], queste model cards raramente includono dati completi sull'impronta ambientale.

In particolare, [@Li2023] evidenziano che le model cards tipicamente *omettono completamente* i dati su:

- **Consumo d'acqua scope 1** (acqua evaporata direttamente nei data center durante l'addestramento)
- **Consumo d'acqua scope 2** (acqua usata nelle centrali elettriche per generare l'energia consumata)
- **Emissioni scope 3** (emissioni nella supply chain: produzione di chip, costruzione di data center, trasporti)
- **Localizzazione geografica specifica** dell'addestramento (che determina il carbon intensity del mix energetico e la disponibilità idrica locale)

Quando vengono forniti dati sul carbon footprint, questi sono spesso calcolati usando il metodo *market-based* piuttosto che *location-based*. La differenza è cruciale: il metodo market-based permette alle aziende di "compensare" le emissioni acquistando crediti di energia rinnovabile o certificati verdi, anche se l'elettricità effettivamente consumata proviene da centrali fossili. Il metodo location-based, invece, calcola le emissioni reali basandosi sul mix energetico effettivo della rete elettrica dove opera il data center [@Li2023].

**Asimmetria informativa strutturale.** [@Crawford2021] argomenta che questa opacità non è accidentale ma riflette una strategia deliberata di controllo dell'informazione. Le aziende tech hanno un interesse diretto a mantenere vaghi i dettagli sull'impronta ambientale dei loro sistemi, per diverse ragioni:

1. **Vantaggio competitivo**: rivelare i costi energetici dettagliati dei modelli potrebbe dare informazioni utili ai competitori sulla scala e l'efficienza delle loro infrastrutture

2. **Rischio reputazionale**: dati precisi potrebbero alimentare critiche pubbliche e campagne di pressione da parte di attivisti ambientali

3. **Evitare regolamentazione**: maggiore trasparenza potrebbe catalizzare richieste di regolamentazione obbligatoria sui consumi energetici e idrici

4. **Proteggere le narrative di sostenibilità**: numeri concreti potrebbero contraddire le dichiarazioni pubbliche di impegno ambientale

Questa asimmetria informativa rende estremamente difficile per ricercatori indipendenti, regolatori, e la società civile valutare accuratamente l'impatto dell'AI. Gli studi come quelli di [@Strubell2019], [@Patterson2021], [@Li2023] e [@Luccioni2025] devono basarsi su stime, assunzioni ragionevoli, e i pochi dati parziali disponibili – un processo che introduce inevitabilmente incertezza e margini di errore significativi.

### 3.6.2 Greenwashing e narrative corporate

La mancanza di trasparenza discussa nella sezione precedente si intreccia con pratiche sistematiche di **greenwashing** – la presentazione pubblica di un'immagine di sostenibilità ambientale che maschera o contraddice le pratiche effettive dell'azienda. Come documentano [@Crawford2021] e [@Luccioni2025], le grandi tech companies hanno sviluppato narrative sofisticate che enfatizzano selettivamente gli aspetti "green" dell'AI mentre minimizzano o occultano gli impatti negativi.

**Le dichiarazioni di "carbon neutrality" e i loro limiti.** Molte aziende tech – incluse Google, Microsoft, Amazon – hanno annunciato impegni ambiziosi verso la "carbon neutrality" o addirittura la "carbon negativity" (rimuovere più CO₂ di quanto emesso). Tuttavia, come osservano [@Crawford2021] e [@Luccioni2025], questi impegni si basano prevalentemente su meccanismi di *compensazione* (carbon offsets) piuttosto che su riduzioni effettive delle emissioni.

I carbon offsets funzionano così: un'azienda che genera emissioni può "compensarle" finanziando progetti che dovrebbero rimuovere o evitare emissioni equivalenti altrove – piantare alberi, investire in energie rinnovabili, proteggere foreste. Sulla carta, il bilancio netto risulta zero o negativo. Ma questo approccio presenta problemi strutturali ben documentati dalla letteratura scientifica [@Luccioni2025]:

1. **Addizionalità incerta**: molti progetti di offset sarebbero avvenuti comunque senza il finanziamento, quindi non rappresentano riduzioni *aggiuntive* di emissioni

2. **Permanenza dubbia**: gli alberi piantati potrebbero morire, bruciare in incendi, o essere tagliati nei decenni successivi, rilasciando nuovamente la CO₂

3. **Problemi di quantificazione**: calcolare esattamente quanta CO₂ un progetto rimuove o evita è estremamente complesso e soggetto a incertezze

4. **Giustizia ambientale**: molti progetti di offset avvengono nel Sud globale e possono avere impatti negativi su comunità locali (es: espropriazione di terre per piantagioni)

Soprattutto, come criticano [@Luccioni2025], gli offset permettono alle aziende di continuare ad *aumentare* le loro emissioni assolute mentre dichiarano di essere "carbon neutral" – un paradosso contabile che non risolve il problema fisico dell'accumulo di CO₂ in atmosfera.

**Il caso Microsoft: contraddizioni tra dichiarazioni e pratiche.** Un esempio particolarmente emblematico analizzato da [@Luccioni2025] riguarda Microsoft. Pubblicamente, l'azienda si è impegnata a diventare "carbon negative" entro il 2030, rimuovendo più carbonio di quanto ne emette. Ha investito miliardi in progetti di carbon removal e pubblica report di sostenibilità dettagliati che enfatizzano questi impegni.

Tuttavia, come documentato nella sezione 3.5.2 sul paradosso di Jevons, contemporaneamente Microsoft vende servizi AI a ExxonMobil per ottimizzare l'estrazione petrolifera, contribuendo a un aumento di produzione di 50.000 barili al giorno. [@Luccioni2025] calcolano che le emissioni derivanti da questo petrolio aggiuntivo superano di **640 volte** le emissioni che Microsoft dichiara di rimuovere attraverso i suoi progetti di carbon capture.

Questa contraddizione rivela un problema strutturale: le aziende tech definiscono la loro "responsabilità ambientale" in modo estremamente selettivo, includendo solo le emissioni dirette delle loro operazioni (scope 1 e 2) e alcuni aspetti limitati della supply chain (scope 3), ma escludendo completamente le emissioni *abilitate* dall'uso dei loro prodotti e servizi. Come osserva [@Crawford2021], è come se un'azienda di armi dichiarasse la propria sostenibilità calcolando solo le emissioni delle fabbriche, ignorando quelle delle guerre combattute con le armi prodotte.

**AI "per il bene" vs AI "per il profitto".** Un altro pattern di greenwashing identificato da [@Kaack2022] riguarda la presentazione selettiva delle applicazioni AI. Nei materiali di marketing, nei report di sostenibilità, e nelle conferenze pubbliche, le aziende tech enfatizzano le applicazioni "AI for Good" – modelli climatici, monitoraggio della deforestazione, ottimizzazione delle energie rinnovabili – come discusso nel Capitolo 2.

Tuttavia, come documentano [@Kaack2022], queste applicazioni climate-positive rappresentano una **frazione minuscola** dell'uso totale dell'AI da parte delle stesse aziende. La maggior parte della capacità computazionale viene dedicata ad applicazioni commerciali: advertising personalizzato, sistemi di raccomandazione per aumentare il consumo, ottimizzazione di supply chain per fast fashion, strumenti per industrie estrattive.

[@Kaack2022] hanno analizzato il portfolio di progetti AI delle grandi tech companies e hanno trovato che meno del **5% della capacità computazionale** viene dedicata ad applicazioni esplicitamente orientate alla sostenibilità climatica. Il restante 95% serve applicazioni che al meglio sono neutrali rispetto al clima, e spesso contribuiscono attivamente ad aumentare consumi ed emissioni attraverso gli effetti rimbalzo discussi nella sezione 3.5.

**L'invisibilità strategica degli impatti.** [@Crawford2021] argomenta che la retorica della "nuvola" (*cloud*) e dell'AI "immateriale" serve una funzione ideologica precisa: rendere invisibili le catene materiali di estrazione, produzione, consumo e smaltimento che sostengono l'infrastruttura digitale. Quando l'AI viene presentata come pura "intelligenza software" slegata dalla fisicità, diventa più facile ignorare o minimizzare i suoi impatti ambientali concreti.

Questa invisibilità è particolarmente evidente nei consumer-facing products. Quando un utente fa una domanda a ChatGPT o chiede a Siri di impostare un promemoria, non c'è alcun feedback sul costo ambientale dell'interazione. L'interfaccia è pulita, istantanea, apparentemente gratuita. La materialità – i server che si scaldano, l'acqua che evapora, l'elettricità consumata, i minerali estratti per produrre l'hardware – rimane nascosta nei data center remoti, nelle miniere del Congo e della Mongolia, nelle discariche di e-waste in Ghana [@Crawford2021].

**Verso una trasparenza obbligatoria?** Di fronte a queste dinamiche, [@Li2023] e [@Luccioni2025] argomentano che la trasparenza volontaria ha fallito e che servono meccanismi di **reporting obbligatorio** regolato per legge. Propongono che:

1. Ogni modello AI deployato commercialmente dovrebbe includere una "environmental model card" standardizzata con dati verificabili su consumi energetici, idrici, emissioni (scope 1, 2 e 3), e materiali

2. Le aziende dovrebbero essere obbligate a usare metodologie *location-based* piuttosto che *market-based* per il calcolo delle emissioni, fornendo un'immagine più accurata dell'impatto reale

3. I dati dovrebbero essere resi pubblici in formato machine-readable per permettere audit indipendenti e ricerca scientifica

4. Le dichiarazioni di sostenibilità dovrebbero includere non solo le emissioni dirette ma anche quelle "abilitate" dagli usi downstream dei sistemi AI

Senza questo tipo di trasparenza obbligatoria, concludono [@Luccioni2025], il greenwashing continuerà a dominare il discorso pubblico sull'AI e ambiente, ostacolando la comprensione dei reali trade-off e delle scelte necessarie per una transizione ecologica genuina.

## 3.7 Interpretazione critica dalla prospettiva sociologica

Come discusso nella sezione 1.2, i teorici critici della modernizzazione ecologica hanno evidenziato i limiti strutturali della versione "debole": la subordinazione della razionalità ecologica a quella economica, la sottovalutazione delle dinamiche capitaliste di crescita e profitto, il paradosso di Jevons che vanifica i guadagni di efficienza [@Foster2012; @Ewing2017].

**Il caso empirico dell'AI conferma queste critiche teoriche.** L'evidenza documentata in questo capitolo mostra che:

- I guadagni di efficienza computazionale si traducono in modelli più grandi e deployment più diffuso, non in riduzioni assolute (paradosso di Jevons empiricamente verificato)
- Le logiche di profitto prevalgono sistematicamente: l'AI viene venduta a industrie fossili mentre si proclama "green", i data center vengono costruiti dove l'energia è economica (non dove è pulita)
- I costi ambientali vengono esternalizzati su comunità vulnerabili (Sud globale, territori indigeni) mentre i benefici si concentrano nel Nord globale
- L'opacità delle aziende tech impedisce accountability democratica

Verso una modernizzazione ecologica "riflessiva" che incorpori governance democratica, trasparenza obbligatoria, giustizia distributiva e internalizzazione dei costi nascosti nel calcolo economico [@Beck1992].


## 3.8 Sintesi del capitolo

Questo capitolo ha rovesciato la prospettiva ottimista del Capitolo 2, esaminando l'intelligenza artificiale non come soluzione alla crisi climatica ma come *parte del problema* – un'infrastruttura tecnologica con un'impronta ecologica significativa e in rapida espansione.

**I costi ambientali documentati.** Abbiamo documentato quattro dimensioni principali dell'impatto ambientale dell'AI:

1. **Consumo energetico** (sezione 3.2): L'addestramento di grandi modelli genera emissioni equivalenti a quelle di automobili durante l'intero ciclo di vita [@Strubell2019]; l'inferenza rappresenta l'80-90% del computing totale [@deVries2023]; i data center globali consumeranno circa 945 TWh entro il 2026, raddoppiando rispetto a pochi anni fa [@IEA2024]

2. **Consumo idrico** (sezione 3.3): L'addestramento di GPT-3 ha consumato circa 700.000 litri di acqua direttamente evaporata [@Li2023]; i data center vengono costruiti in regioni già water-scarce, creando conflitti con comunità locali; il 50% della popolazione mondiale vivrà in aree a stress idrico entro il 2050 [@Li2023]

3. **Materiali e rifiuti** (sezione 3.4): L'estrazione di terre rare genera 75.000 litri di acque acide per tonnellata raffinata [@Crawford2021]; il 54% dei minerali critici proviene da territori indigeni, il 62% da zone drought-prone [@Luccioni2025]; 62 milioni di tonnellate di e-waste nel 2022, solo 22% riciclato formalmente [@Luccioni2025]

4. **Effetti sistemici e rimbalzo** (sezione 3.5): I guadagni di efficienza portano a modelli più grandi e uso più diffuso, non a riduzioni assolute; l'AI viene usata per espandere industrie fossili (es: Microsoft-ExxonMobil: +50.000 barili/giorno, +640% emissioni rispetto ai target di carbon removal) [@Luccioni2025]

**Il paradosso rivelato.** L'evidenza empirica rivela un paradosso profondo: l'AI è simultaneamente presentata come *strumento della transizione ecologica* (Capitolo 2) e manifesta come *vettore di intensificazione del metabolismo industriale* (Capitolo 3). Questo non è una contraddizione superficiale che possa essere risolta con semplici aggiustamenti tecnici, ma riflette le tensioni strutturali tra le logiche del capitalismo (crescita, profitto, competizione) e gli imperativi ecologici (limiti planetari, sostenibilità, giustizia).

**Le implicazioni teoriche.** Dal punto di vista della teoria sociologica (sezione 3.7), il caso dell'AI conferma le critiche alla modernizzazione ecologica "debole": la subordinazione della razionalità ecologica a quella economica [@Foster2012; @Ewing2017], il "treadmill of production" che impone crescita indipendentemente dalle conseguenze [@Foster2012], il paradosso di Jevons che vanifica i guadagni di efficienza [@Luccioni2025], l'illusione della dematerializzazione digitale [@Crawford2021].

Verso una modernizzazione ecologica "forte" e riflessiva che incorpori governance democratica, trasparenza obbligatoria, internalizzazione dei costi ambientali, attenzione alla giustizia distributiva, e possibilmente limiti assoluti alla crescita di settori particolarmente impattanti [@Li2023; @Luccioni2025; @Kaack2022].

**Domanda aperta per le Conclusioni.** La domanda che emerge da questa analisi dialettica – l'AI come alleata (Cap. 2) e come problema (Cap. 3) – non è semplicemente "l'AI è buona o cattiva per l'ambiente?" ma piuttosto: **sotto quali condizioni istituzionali, economiche e politiche l'intelligenza artificiale potrebbe effettivamente contribuire a una transizione ecologica giusta e sostenibile, piuttosto che riprodurre e intensificare le contraddizioni del capitalismo verde?**

Questa domanda guiderà la sintesi finale nelle Conclusioni, dove integreremo le evidenze empiriche e le riflessioni teoriche di entrambi i capitoli per offrire una valutazione sociologicamente informata del ruolo dell'AI nella modernizzazione ecologica contemporanea.

