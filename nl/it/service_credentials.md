---

copyright:

  years: 2015, 2019
lastupdated: "2019-05-08"

keywords: service key, api key, bind, credential

subcollection: resources

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:note: .note}
{:tip: .tip}


# Aggiunta e visualizzazione delle credenziali
{: #service_credentials}

Puoi generare una nuova serie di credenziali per i casi in cui vuoi connettere manualmente un'applicazione o un consumatore esterno a un servizio {{site.data.keyword.Bluemix}}. Ad esempio, se stai tentando di associare un'applicazione AWS a un servizio Watson, devi generare una nuova credenziale che possa essere utilizzata per associarli. Dopo aver creato le tue credenziali, puoi [aggiungerle manualmente](/docs/apps/tutorials?topic=creating-apps-credentials_overview) alla tua applicazione {{site.data.keyword.Bluemix_notm}} o a un altro [consumatore esterno](/docs/resources?topic=resources-externalapp) per connettere il tuo servizio.

Per aggiungere manualmente le credenziali alle tue applicazioni, fai riferimento alla documentazione per il tipo di applicazione o opzione di calcolo che stai utilizzando.
{: tip}

## Aggiunta di una credenziale quando si associa un servizio abilitato a IAM
{: #IAM}

I servizi gestiti da {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) possono generare una chiave della risorsa, nota anche come credenziale. Le credenziali sono specifiche del servizio e variano in base a come ogni servizio definisce le credenziali che deve generare. Una credenziale può contenere un nome utente, una password, un nome host, una porta e un URL.

Tuttavia, mentre il contenuto di ogni credenziale è univoco per il servizio che la genera, tutti i servizi gestiti da IAM richiedono che le nuove credenziali includano un ruolo di accesso del servizio IAM. Alcuni servizi possono generare ulteriori dati che richiedono la trasmissione di parametri. Ad esempio, un servizio potrebbe richiederti di immettere un parametro lingua per impostare la lingua predefinita restituita nella chiave della risorsa generata.

Completa la seguente procedura per aggiungere una credenziale a un servizio gestito da IAM:

1. Dall'elenco risorse, seleziona il nome del servizio per aprire la relativa pagina dei dettagli. Quindi, seleziona la scheda Credenziali e fai clic su **Nuova credenziale + **.
2. Dalla finestra di dialogo dell'aggiunta della nuova credenziale, fornisci un **Nome**.
3. Specifica il ruolo. Questo valore imposta il ruolo di accesso del servizio IAM. Per ulteriori informazioni, vedi: [Accesso IAM](/docs/iam?topic=iam-userroles)
4. Facoltativamente, puoi fornire un ID servizio consentendo a IAM di generare per te un valore univoco o fornendo un ID di servizio esistente. Per ulteriori informazioni, vedi: [Creazione e gestione degli ID servizio](/docs/iam?topic=iam-serviceids)
5. Facoltativamente, puoi fornire ulteriori parametri come un oggetto JSON valido che contiene i parametri di configurazione specifici per il servizio, forniti sia incorporati che in un file.

  La maggior parte dei servizi non richiede ulteriori parametri, e per i servizi che li richiedono, ognuno di essi definisce il proprio elenco di parametri univoco. Per un elenco di parametri di configurazione supportati, consulta la documentazione per l'offerta del servizio in particolare.
  {: note}
6. Fai clic su **Aggiungi** per generare la nuova credenziale del servizio.

## Aggiunta di una credenziale quando si associa un servizio Cloud Foundry
{: #cf_credential}

I servizi Cloud Foundry possono generare una chiave del servizio, nota anche come credenziale. Le credenziali sono specifiche del servizio e variano in base a come ogni servizio definisce le credenziali che deve generare. Una credenziale del servizio può contenere un nome utente, una password, un nome host, una porta e un URL.

Tuttavia, il contenuto di ogni credenziale è univoco per il servizio che la genera. Alcuni servizi possono generare ulteriori dati che richiedono la trasmissione di parametri. Ad esempio, un servizio potrebbe richiederti di immettere un parametro lingua per impostare la lingua predefinita restituita nella chiave del servizio generata.

Completa la seguente procedura per aggiungere una credenziale Cloud Foundry:

1. Dalla pagina dei dettagli del servizio, seleziona la scheda Credenziali e fai clic su **Nuova credenziale + **.
2. Dalla finestra di dialogo dell'aggiunta della nuova credenziale, fornisci un **Nome**.
3. Facoltativamente, puoi fornire ulteriori parametri come un oggetto JSON valido che contiene i parametri di configurazione specifici per il servizio, forniti sia incorporati che in un file.

  La maggior parte dei servizi non richiede ulteriori parametri, e per i servizi che li richiedono, ognuno di essi definisce il proprio elenco di parametri univoco. Per un elenco di parametri di configurazione supportati, consulta la documentazione per l'offerta del servizio in particolare.
  {: note}
4. Fai clic su **Aggiungi** per generare la nuova credenziale del servizio.

## Visualizzazione di una credenziale
{: #viewing-credentials}

Dopo aver creato una credenziale per un servizio, può essere visualizzata in qualsiasi momento per gli utenti che hanno bisogno del valore chiave API. Tuttavia, tutti gli utenti devono disporre del corretto livello di accesso per vedere i dettagli di una credenziale, incluso il valore chiave API. L'accesso dell'utente deve essere pari o superiore a quello della credenziale del servizio. Ad esempio, se la credenziale ha il ruolo di servizio IAM `Scrittore`, l'utente che sta tentando di visualizzare la credenziale deve avere assegnato il ruolo del servizio IAM `Scrittore` o `Gestore` per tale particolare servizio. Quando un utente non dispone dell'accesso corretto, i dettagli come il valore chiave API vengono censurati.

Per visualizzare una credenziale esistente per un servizio, completa la seguente procedura:

1. Dall'elenco risorse, seleziona il nome del servizio per aprire la relativa pagina dei dettagli. 
2. Fai clic su **Credenziali del servizio**
3. Espandi **Visualizza credenziali** sulla riga di una credenziale esistente.


