Perfetto! Procediamo con ordine. Prima analizzo l'indice della tesi, poi leggo i capitoli già scritti, e infine preparo i primi paragrafi del capitolo 3 basandomi esclusivamente sul materiale presente nel project knowledge.Ora accedo al repository GitHub per vedere esattamente cosa avete già scritto nei capitoli precedenti:Perfetto! Ho analizzato l'indice e letto i capitoli già scritti. Ora cerco le informazioni necessarie per scrivere il Capitolo 3 sul project knowledge.Perfetto! Ho analizzato l'indice e letto i capitoli già scritti. Ora inizio a scrivere i primi paragrafi del Capitolo 3, attingendo esclusivamente dalle fonti presenti nel project knowledge e usando la sintassi di citazione pandoc.

---

# CAPITOLO 3 - L'IMPRONTA ECOLOGICA DELL'INTELLIGENZA ARTIFICIALE: COSTI NASCOSTI E CONTRADDIZIONI

## 3.1 Introduzione: il lato oscuro dell'AI

Nel Capitolo 2 abbiamo esplorato la narrativa più ottimista sul rapporto tra intelligenza artificiale e ambiente, documentando come l'AI venga presentata e utilizzata come strumento di transizione ecologica. Abbiamo visto applicazioni promettenti nelle smart grid, nella previsione meteorologica, nel monitoraggio degli ecosistemi – tutte incarnazioni della promessa della modernizzazione ecologica informazionale: risolvere i problemi ambientali attraverso maggiore efficienza, ottimizzazione e governance basata sui dati.

Questo capitolo rovescia la prospettiva. Esaminiamo ora l'intelligenza artificiale non come *soluzione* alla crisi climatica, ma come *parte del problema* – un'infrastruttura tecnologica con un'impronta ecologica significativa e in rapida crescita. Come osservano [@Luccioni2025], il dibattito sull'AI e l'ambiente è diventato profondamente polarizzato: da un lato, i sostenitori ne enfatizzano il potenziale per accelerare la transizione energetica e la scoperta di materiali sostenibili; dall'altro, i critici sottolineano il crescente consumo di carbonio, acqua e risorse materiali. Questa polarizzazione, tuttavia, ha concentrato l'attenzione principalmente sugli *impatti diretti* – energia e acqua nei data center, rifiuti elettronici – senza affrontare adeguatamente gli effetti indiretti e sistemici.

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

