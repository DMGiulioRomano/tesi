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

