# Analisi dataset relativo all'inquinamento dell'aria

## Il dataset
Il dataset che andremo ad utilizzare è un dataset molto ricco di informazioni, ogni file, eccetto l’anno 2018, contiene oltre 200.000 righe. Quindi, abbiamo deciso di lavorare su una porzione dei file, prendendo in considerazione l’intervallo temporale che va dal 2008 al 2018. I campi che compongo il dataset sono:

<table>
<tr>
<td><b>Date:</b></td>
<td> questo campo contiene la data relativa al momento in cui è stato fatto il rilevamento. Il formato della data è composto dall’anno, il mese, il giorno, e l’ora.</td>
</tr>
<tr>
<td><b>BEN:</b></td>
<td> questo campo contiene il rilevamento del benzene. Il livello di benzene è misurato in μg/m³. Il benzene è un irritante per gli occhi e la pelle, lunghe esposizioni possono causare diversi tipi di cancro, leucemia e anemie. Il benzene è considerato un cancerogeno per l'uomo di gruppo 1 dalla IARC.</td>
</tr>
<tr>
<td><b>EBE:</b></td>
<td>
questo campo contiene il rilevamento dell’etilbenzene. Il livello di etilbenzene è misurato in μg/m³. L'esposizione a lungo termine può causare problemi all'udito o ai reni e l'IARC ha concluso che l'esposizione a lungo termine può produrre il cancro.</td>
</tr>
<tr>
<td><b>CO:</b></td>
<td>
questo campo contiene il rilevamento del monossido di carbonio. Il livello di monossido di carbonio è misurato in mg/m³. L'avvelenamento da monossido di carbonio comporta mal di testa, vertigini e confusione in brevi esposizioni e può provocare perdita di coscienza, aritmie, convulsioni o persino la morte a lungo termine.</td>
</tr>
<tr>
<td><b>NMHC:</b></td>
<td>
questo campo contiene il rilevamento di idrocarburi non metanici (composti organici volatili). Il livello di idrocarburi non metanici è misurato in mg/m³. L'esposizione prolungata ad alcune di queste sostanze può causare danni al fegato, ai reni e al sistema nervoso centrale. Si sospetta che alcuni di loro causino il cancro negli esseri umani.</td>
</tr>
<tr>
<td><b>NO:</b></td>
<td>
questo campo contiene il rilevamento dell’ossido nitrico. Il livello di ossido nitrico è misurato in μg/m³. Questo è un gas altamente corrosivo generato, tra l'altro, dai veicoli a motore e dai processi di combustione del carburante.</td>
</tr>
<tr>
<td><b>NO_2:</b></td>
<td>
questo campo contiene il rilevamento del biossido di azoto. Il livello di biossido di azoto è misurato in μg/m³. L'esposizione a lungo termine è causa di malattie polmonari croniche e sono dannose per la vegetazione.</td>
</tr>
<tr>
<td><b>O_3:</b></td>
<td>
questo campo contiene il rilevamento dell’ozono. Il livello di ozono è misurato in μg/m³. Livelli elevati possono produrre asma, bronchite o altre malattie polmonari croniche in gruppi sensibili o lavoratori all'aperto.</td>
</tr>
<tr>
<td><b>PM10:</b></td>
<td>
questo campo contiene il rilevamento del materiale particolato aerodisperso con particelle inferiori a 10 μm. Il livello di materiale particolato aerodisperso è misurato in μg/m³. Anche se non possono penetrare nell'alveolo, possono comunque penetrare attraverso i polmoni e colpire altri organi. L'esposizione a lungo termine può causare cancro ai polmoni e complicazioni cardiovascolari. </td>
</tr>
<tr>
<td><b>PM_25:</b></td>
<td>
questo campo contiene il rilevamento del materiale particolato aerodisperso, di diametro maggiore rispetto al precedente. Il livello di materiale particolato aerodisperso è misurato in μg/m³. Le dimensioni di queste particelle consentono loro di penetrare nelle regioni di scambio gassoso dei polmoni (alveoli) e persino di entrare nelle arterie. È stato dimostrato che l'esposizione a lungo termine è correlata al basso peso alla nascita e all'ipertensione nei neonati.
</td>
</tr>
<tr>
<td><b>SO_2:</b></td>
<td>
questo campo contiene il rilevamento dell’anidride solforosa. Il livello di anidride solforosa è misurato in μg/m³. Alti livelli di anidride solforosa possono produrre irritazione della pelle e delle membrane e peggiorare l'asma o le malattie cardiache nei gruppi sensibili.
</td>
</tr>
<tr>
<td><b>TCH:</b></td>
<td>
questo campo contiene il rilevamento del livello totale di idrocarburi. Questo livello totale di idrocarburi è misurato in mg/m³. Questo gruppo di sostanze può essere responsabile di diverse malattie del sangue, del sistema immunitario, del fegato, della milza, dei reni o dei polmoni.
</td> </tr>
<tr>
<td><b>TOL:</b></td>
<td>
questo campo contiene il rilevamento del toluene ( metilbenzene ). Il livello di toluene è misurato in μg/m³. L'esposizione a lungo termine a questa sostanza (presente anche nel fumo di tabacco) può causare complicazioni renali o danni permanenti al cervello.
</td> </tr>
<tr>
<td><b>Station:</b></td>
<td>	
questo campo contiene il codice identificativo della stazione che ha effettuato quel rilevamento. Nel dataset abbiamo una tabella `Station`, all’interno della quale sono contenuti i codici delle stazioni più altre informazioni molto importanti. Queste informazioni sono il nome della stazione, il nome del luogo dov’è situata e le indicazioni geografiche di questo luogo.
</td> </tr>
<tr>
<td><b>CH4:</b></td>
<td>
questo campo contiene il rilevamento del livello di metano. Il livello di metano è misurato in mg/m³. Questo gas è un asfissiante, che sostituisce l'ossigeno di cui gli animali hanno bisogno per respirare. Il metano può provocare vertigini, debolezza, nausea e perdita di coordinazione.
</td> </tr>
<tr>
<td><b>MXY:</b></td>
<td>
questo campo contiene il rilevamento del livello di m-xilene. Il livello di m-xilene è misurato in μg/m³. Gli xileni possono influenzare non solo l'aria, ma anche l'acqua e il suolo e una lunga esposizione a livelli elevati di xileni può provocare malattie che colpiscono il fegato, i reni e il sistema nervoso (in particolare la memoria e la reazione allo stimolo alterata).
</td> </tr>	
<tr>
<td><b>PXY:</b></td>
<td>
questo campo contiene il rilevamento del livello di p-xilene. Il livello di p-xilene è misurato in μg/m³. Vedere MXY per gli effetti dell'esposizione allo xilene sulla salute.
</td> </tr>
<tr>
<td><b>OXY:</b></td>
<td>
questo campo contiene il rilevamento del livello di o-xilene. Il livello di o-xilene è misurato in μg/m³. Vedere MXY per gli effetti dell'esposizione allo xilene sulla salute.
</td> </tr>
<tr>
<td><b>NOX:</b></td>
<td>
questo campo contiene il rilevamento del livello di ossidi di azoto. Il livello di ossidi di azoto è misurato in μg/m³. Colpiscono il sistema respiratorio umano peggiorando l'asma o altre malattie, e sono responsabili del colore bruno-giallastro dello smog fotochimico.

</table>

[Link](https://www.kaggle.com/datasets/decide-soluciones/air-quality-madrid) al dataset su kaggle

## Fase di ETL
Per poter proseguire con il nostro progetto abbiamo dovuto eseguire una fase di ETL (*Extraction, Transfor-mation, Load*).

Come prima cosa abbiamo analizzato i dati visivamente, per capire se tutti i file del nostro dataset erano conformi tra di loro e non presentavano anomalie, poi abbiamo effettuato la vera e propria "pulizia dei dati". 
![](https://github.com/Simone-Scalella/DataScience2Project/blob/main/img_doc/etl1.png)

Il dataset era composto da un file CSV per ogni anno, quindi, per una maggiore comodità abbiamo deciso di unificare tale csv in un unico dataframe.
![](https://github.com/Simone-Scalella/DataScience2Project/blob/main/img_doc/etl2.png)


## Tecnologie utilizzate
### Python

### Pandas

### Seaborn 

### Matplotlib

### Sklearn

###Statsmodel

