---
title: Installare e configurare il modulo Gestione dei servizi di Azure PowerShell | Documenti di Microsoft
description: Come installare e configurare Azure PowerShell per il primo uso.
services: azure
author: sdwheeler
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/06/2017
ms.openlocfilehash: c51c727c1cb022eca59f819c7f24d8e058c677da
ms.sourcegitcommit: 226527be7cb647acfe2ea9ab151185053ab3c6db
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/29/2017
---
# <a name="installing-the-azure-powershell-service-management-module"></a>Installare il modulo Gestione dei servizi di Azure PowerShell

L'installazione di Azure PowerShell da [PowerShell Gallery](https://www.powershellgallery.com/) è il metodo preferito di installazione.

## <a name="step-1-install-powershellget"></a>Passaggio 1: installare PowerShellGet

L'installazione degli elementi da PowerShell Gallery richiede il modulo PowerShellGet. Assicurarsi di avere la versione appropriata di PowerShellGet e di soddisfare gli altri requisiti di sistema. Eseguire il comando seguente per determinare se PowerShellGet è installato nel sistema.

```powershell
Get-Module PowerShellGet -list | Select-Object Name,Version,Path
```

Verrà visualizzata una schermata simile all'output seguente:

```
Name          Version Path
----          ------- ----
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Se PowerShellGet non è installato, vedere la sezione [Come ottenere PowerShellGet](install-azurerm-ps.md#how-to-get-powershellget).

## <a name="step-2-install-azure-powershell"></a>Passaggio 2: Installare Azure PowerShell

Eseguire il comando seguente dalla console di Windows PowerShell come amministratore:

```powershell
Install-Module Azure
```

Il modulo Azure è un modulo di rollup per i cmdlet di Azure Resource Manager. Durante l'installazione del modulo AzureRM, qualsiasi modulo di Azure non installato precedentemente viene scaricato e installato da PowerShell Gallery.

Il modulo di Gestione dei servizi di Azure condivide le dipendenze con i moduli di Gestione risorse di Azure PowerShell. Se sono stati installati i moduli di Gestione risorse di Azure PowerShell, sarà necessario aggiungere il parametro `-AllowClobber` al comando di installazione. In questo modo le dipendenze condivise esistenti verranno aggiornate. Senza questo parametro, si verifica un errore di installazione del modulo.

```powershell
Install-Module Azure -AllowClobber
```

Dopo aver installato il modulo, è possibile importarlo eseguendo il comando seguente:

```powershell
Import-Module Azure
```

## <a name="to-use-the-cmdlets"></a>Usare i cmdlet

Per iniziare a lavorare con i cmdlet di Gestione dei servizi di Azure, accedere al proprio account Azure. Per accedere al proprio account, eseguire il comando seguente:

```powershell
Add-AzureAccount
```

Dopo l'accesso ad Azure, Azure PowerShell crea un contesto per la sessione specificata. Tale contesto contiene l'ambiente Azure PowerShell, l'account, il tenant e la sottoscrizione che verranno usati per tutti i cmdlet della sessione. È ora possibile usare i moduli seguenti.

## <a name="azure-service-management-cmdlets"></a>Cmdlet di Gestione dei servizi di Azure

I moduli di Azure PowerShell vengono aggiornati di frequente. Se si nota che la guida dei cmdlet online include cmdlet o parametri non presenti nel modulo, scaricare e installare la versione più recente del modulo. Per conoscere la versione del modulo, digitare: `(Get-Module Azure).Version`.

Per gli script di esempio che consentono di automatizzare alcune delle attività comuni in Azure, vedere lo [Script Center di Windows Azure](http://www.windowsazure.com/documentation/scripts/).

Per informazioni generali sull'installazione, la formazione, l'uso e la personalizzazione di Windows PowerShell, vedere [Scripting con Windows PowerShell](http://go.microsoft.com/fwlink/p/?linkid=320210).
