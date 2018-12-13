---
title: Uso dei moduli sperimentali di Azure PowerShell
description: Informazioni sulla filosofia e sull'utilizzo dei moduli sperimentali di Azure PowerShell.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/05/2017
ms.openlocfilehash: 30e57805dd59bd60d10c52422fcb68686563fadf
ms.sourcegitcommit: 087c588169786c005a3c177624fb3ac6c8870125
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/13/2018
ms.locfileid: "53217661"
---
# <a name="using-experimental-azure-powershell-modules"></a>Uso dei moduli sperimentali di Azure PowerShell

In considerazione della particolare importanza attribuita agli strumenti di sviluppo e soprattutto alle interfacce della riga di comando in Azure, il team di Azure PowerShell sta sperimentando molti miglioramenti nell'esperienza di Azure PowerShell.

## <a name="experimentation-methodology"></a>Metodologia di sperimentazione

Per facilitare la sperimentazione, vengono creati nuovi moduli di Azure PowerShell che implementano funzionalità esistenti di Azure SDK in nuovi modi più facili da usare. Nella maggior parte dei casi, i cmdlet rispecchiano esattamente cmdlet esistenti. I cmdlet sperimentali, tuttavia, offrono una notazione a sintassi abbreviata e valori predefiniti più intelligenti che semplificano la creazione e la gestione delle risorse di Azure.

Questi moduli possono essere installati side-by-side con i moduli di Azure PowerShell esistenti. I nomi dei cmdlet sono stati abbreviati per offrire nomi più corti ed evitare conflitti di nome con i cmdlet non sperimentali esistenti.

I moduli sperimentali adottano la convenzione di denominazione seguente: `AzureRM.*.Experiments`. Questa convenzione di denominazione è simile alla denominazione dei moduli in anteprima: `AzureRM.*.Preview`. I moduli in anteprima differiscono da quelli sperimentali perché implementano nuove funzionalità dei servizi di Azure che sono disponibili solo come anteprima. I moduli in anteprima sostituiscono moduli di Azure PowerShell esistenti e usano gli stessi nomi per cmdlet e parametri.

## <a name="how-to-install-an-experimental-module"></a>Come installare un modulo sperimentale

I moduli sperimentali vengono pubblicati in PowerShell Gallery così come i moduli di Azure PowerShell esistenti. Per visualizzare un elenco di moduli sperimentali, eseguire questo comando:

```powershell-interactive
Find-Module AzureRM.*.Experiments
```

```Output
Version Name                         Repository Description
------- ----                         ---------- -----------
1.0.25  AzureRM.Compute.Experiments  PSGallery  Azure Compute experiments for VM creation
1.0.0   AzureRM.Websites.Experiments PSGallery  Create and deploy web applications using Azure App Services.
```

Per installare il modulo sperimentale, usare i comandi seguenti in una sessione di PowerShell con privilegi elevati:

```powershell-interactive
Install-Module AzureRM.Compute.Experiments
Install-Module AzureRM.Websites.Experiments
```

### <a name="documentation-and-support"></a>Documentazione e supporto

La documentazione è inclusa nel pacchetto di installazione ed è accessibile con il cmdlet `Get-Help`. Per i moduli sperimentali non viene pubblicata documentazione ufficiale.

Gli utenti sono invitati a testare questi moduli e inviare commenti e suggerimenti, che consentiranno di migliorare l'usabilità e soddisfare le esigenze. Dato che sono sperimentali, tuttavia, il supporto per questi moduli è limitato. È possibile inviare domande o segnalare problemi creando un [problema](https://github.com/Azure/azure-powershell/issues) nel repository GitHub.

## <a name="experiments-and-areas-of-improvement"></a>Esperimenti e aree di miglioramento

Questi miglioramenti sono stati selezionati in base agli elementi di differenziazione chiave nei prodotti concorrenti. Uno degli obiettivi dell'interfaccia della riga di comando di Azure 2.0, ad esempio, è stato basare i comandi su _scenari_ anziché sulla _superficie di attacco dell'API_.
L'interfaccia della riga di comando di Azure 2.0 usa diverse impostazioni predefinite intelligenti che semplificano gli scenari "introduttivi" per gli utenti finali.

### <a name="core-improvements"></a>Miglioramenti di base

I miglioramenti di base sono considerati "buon senso" e non è necessaria molta sperimentazione per procedere all'implementazione di questi aggiornamenti.

- Cmdlet basati su scenari: i cmdlet <em>*All</em>- dovranno essere progettati sulla base di scenari, non del servizio REST di Azure.

- Nomi più brevi: include i nomi dei cmdlet (ad esempio, `New-AzureRmVM` => `New-AzVm`) e dei parametri (ad esempio, `-ResourceGroupName` => `-Rg`). Usare alias per la compatibilità con i cmdlet "meno recenti" e specificare set di parametri _compatibili con le versioni precedenti_.

- Impostazioni predefinite intelligenti: creare impostazioni predefinite intelligenti per immettere le informazioni "necessarie", Ad esempio: 
  - Gruppo di risorse
  - Località
  - Risorse dipendenti

### <a name="experimental-improvements"></a>Miglioramenti sperimentali

I miglioramenti sperimentali presentano un cambiamento significativo che il team vuole convalidare tramite la sperimentazione.

- Tipi semplici: per gli scenari di creazione non dovranno più essere usati tipi complessi e oggetti di configurazione. Semplificare la configurazione riducendola a uno o due parametri.

- "Creazione intelligente": tutti gli scenari di creazione che implementano la "creazione intelligente" _non_ avranno parametro obbligatori. Tutte le informazioni necessarie verranno scelte autonomamente da Azure PowerShell.

- Parametri "grigi": in molti casi, alcuni parametri potrebbero essere "grigi" o semifacoltativi. Se il parametro non viene specificato, all'utente viene richiesto se vuole che venga generato automaticamente. È anche opportuno che il valore per i parametri "grigi" venga dedotto in base al contesto con il consenso dell'utente,
  ad esempio suggerendo il valore usato di recente.

- Opzione `-Auto`: l'opzione `-Auto` offrirà agli utenti la possibilità di "acconsentire esplicitamente" all'_impostazione predefinita di tutti i valori_ mantenendo al tempo stesso l'integrità dei parametri obbligatori nel percorso principale.

### <a name="feature-specific-switches"></a>Opzioni specifiche delle funzionalità

Lo scenario di creazione di app Web, ad esempio, potrebbe avere un'opzione `-Git` o `-AddRemote` che aggiungerà automaticamente un'istanza remota di Azure a un repository Git esistente.

- Valori predefiniti impostabili: gli utenti dovranno avere la possibilità di impostare valori predefiniti per determinati parametri comuni come `-ResourceGroupName` e `-Location`.

- Impostazioni predefinite per le dimensioni: le "dimensioni" delle risorse possono confondere gli utenti perché molti provider di risorse usano nomi diversi, ad esempio "Standard\_DS1\_v2" o "S1". La maggior parte degli utenti, tuttavia presta molta attenzione al costo. È quindi opportuno definire dimensioni "universali" in base alla pianificazione prezzi. Gli utenti possono scegliere dimensioni specifiche o lasciare che Azure PowerShell scelga l'_opzione migliore_ in base alla risorsa e al budget.

- Formato di output: Azure PowerShell attualmente restituisce oggetti `PSObject` e l'output della console è ridotto. Potrebbe essere necessario visualizzare all'utente in Azure PowerShell alcune informazioni relative alle impostazioni predefinite intelligenti usate.
