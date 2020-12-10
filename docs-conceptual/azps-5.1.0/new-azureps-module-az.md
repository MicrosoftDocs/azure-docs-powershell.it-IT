---
title: Introduzione al modulo Azure Az di PowerShell
description: Introduzione al modulo Az di PowerShell, la scelta consigliata per interagire con Azure, che sostituisce il modulo AzureRM di PowerShell.
ms.date: 12/1/2020
ms.devlang: powershell
ms.topic: conceptual
ms.custom: devx-track-azurepowershell
ms.service: azure-powershell
ms.openlocfilehash: d922affd608ebfce41f9608ec82d565d6afe9f7f
ms.sourcegitcommit: 3ef9f7f6c20af98282a0499b1527c291ee54011b
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/05/2020
ms.locfileid: "96617720"
---
# <a name="introducing-the-azure-az-powershell-module"></a>Introduzione al modulo Azure Az di PowerShell

## <a name="overview"></a>Panoramica

Il modulo Az di Azure PowerShell è costituito da un set di cmdlet per la gestione delle risorse di Azure direttamente da PowerShell. PowerShell include potenti funzionalità per l'automazione che è possibile sfruttare per gestire le risorse di Azure, ad esempio nel contesto di una pipeline CI/CD.

Il modulo Az di PowerShell sostituisce il modulo AzureRM ed è la versione consigliata da usare per interagire con Azure.

È possibile usare il modulo Az di PowerShell con uno dei metodi seguenti:

* [Installare il modulo Az di PowerShell tramite PowerShellGet](install-az-ps.md) (opzione consigliata).
* [Installare il modulo Az di PowerShell con MSI](install-az-ps-msi.md).
* [Usare Azure Cloud Shell](/azure/cloud-shell/overview).
* [Usare il contenitore Docker di Az di PowerShell](azureps-in-docker.md).

## <a name="features"></a>Funzionalità

Il modulo Az di PowerShell offre i vantaggi seguenti:

* Sicurezza e stabilità
  * Crittografia della cache di token
  * Supporto per ADFS 2019
  * Meccanismo di sicurezza per prevenire attacchi di tipo man-in-the-middle
  * Supporto per funzionalità come la valutazione continua dell'accesso (disponibile nel 2021)
* Supporto per tutti i servizi di Azure
  * Disponibilità di un modulo per ogni servizio di Azure
  * Più correzioni di bug e aggiornamenti delle versioni delle API rispetto ad AzureRM
* Diverse nuove funzionalità aggiuntive
  * Supporto in Cloud Shell e multipiattaforma
  * Possibilità di ottenere e usare token per accedere alle risorse di Azure
  * Cmdlet Az generico per operazioni di emergenza

> [!NOTE]
> PowerShell 7 e versioni successive è la versione consigliata di PowerShell per l'uso con Az di PowerShell in tutte le piattaforme.

Il modulo Az di PowerShell è basato sulla libreria .NET Standard ed è compatibile con PowerShell 7 e versioni successive in tutte le piattaforme, tra cui Windows, macOS e Linux. È anche compatibile con Windows PowerShell 5.1.

Microsoft si impegna a includere il supporto di Azure in tutte le piattaforme, per cui tutti i moduli Az di PowerShell sono multipiattaforma.

## <a name="upgrade-your-environment-to-az"></a>Aggiornare l'ambiente a Az

Per restare al passo con le funzionalità più recenti di Azure in PowerShell, è consigliabile eseguire la migrazione al modulo Az. Se non si è pronti a installare il modulo Az in sostituzione di AzureRM, sono disponibili alcune opzioni per provare Az:

* Usare un ambiente `PowerShell` con [Azure Cloud Shell](/azure/cloud-shell/overview). Azure Cloud Shell è un ambiente di shell basato su browser che è disponibile quando si installa il modulo Az e si abilitano gli alias per la compatibilità con `Enable-AzureRM`.
* Mantenere installato il modulo AzureRM con Windows PowerShell 5.1 e installare il modulo Az in PowerShell 7 o versione successiva. Windows PowerShell 5.1 e PowerShell 7 e versioni successive usano raccolte di moduli separate. Seguire le istruzioni per installare l'[ultima versione di PowerShell](/powershell/scripting/install/installing-powershell) e quindi [installare il modulo Az](install-az-ps.md) da PowerShell 7 o versione successiva.

Per eseguire l'aggiornamento da un'installazione esistente di AzureRM:

1. [Disinstallare il modulo AzureRM di Azure PowerShell](/powershell/azure/uninstall-az-ps#uninstall-the-azurerm-module).
1. [Installare il modulo Az di Azure PowerShell](install-az-ps.md).
1. **FACOLTATIVO**: Mentre si acquisisce familiarità con il nuovo set di comandi, abilitare la modalità compatibilità per aggiungere gli alias per i cmdlet di AzureRM con [Enable-AzureRMAlias](/powershell/module/az.accounts/enable-azurermalias). Per altre informazioni, vedere la sezione successiva oppure [avviare la migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md).

## <a name="migrate-existing-scripts-from-azurerm-to-az"></a>Eseguire la migrazione degli script esistenti da AzureRM ad Az

Se gli script sono ancora basati sul modulo AzureRM, sono disponibili diverse risorse per supportare la migrazione:

* [Introduzione alla migrazione da AzureRM ad Az](migrate-from-azurerm-to-az.md)
* [Elenco completo delle modifiche di rilievo apportate durante la migrazione da AzureRM ad Az 1.0.0](migrate-az-1.0.0.md)
* Cmdlet [Enable-AzureRmAlias](/powershell/module/az.accounts/enable-azurermalias)

## <a name="supportability"></a>Facilità di supporto

Az è il modulo di PowerShell più recente per Azure. Problemi o richieste di funzionalità possono essere registrati direttamente nel [repository GitHub](https://github.com/Azure/azure-powershell) oppure tramite il supporto tecnico Microsoft, se è stato sottoscritto un contratto. Le funzionalità richieste verranno implementate nella versione più recente di Az. Le soluzioni dei problemi critici verranno implementate nelle ultime due versioni di Az.

AzureRM non riceverà più nuovi cmdlet o nuove funzionalità. Tuttavia, il modulo AzureRM è ancora ufficialmente supportato e riceverà correzioni di problemi critici fino a febbraio 2021.

## <a name="data-collection"></a>Raccolta dati

Azure PowerShell raccoglie dati di telemetria per impostazione predefinita. Microsoft aggrega i dati raccolti per identificare i modelli di utilizzo e i problemi comuni, oltre che per migliorare l'esperienza di Azure PowerShell.
Microsoft Azure PowerShell non raccoglie dati privati o personali. I dati di utilizzo consentono ad esempio di identificare problemi come i cmdlet di scarso successo e di stabilire le priorità del nostro lavoro.

Anche se apprezziamo le informazioni fornite da questi dati, sappiamo anche che non tutti sono disposti a inviare dati di utilizzo. È possibile disabilitare la raccolta dati con il cmdlet [`Disable-AzDataCollection`](/powershell/module/az.accounts/disable-azdatacollection). È anche possibile leggere l'[informativa sulla privacy](https://privacy.microsoft.com/privacystatement) per altre informazioni.
