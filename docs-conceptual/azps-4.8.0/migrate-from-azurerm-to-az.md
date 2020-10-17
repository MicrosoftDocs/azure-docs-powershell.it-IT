---
title: Eseguire la migrazione di script di Azure PowerShell da AzureRM ad Az
description: Informazioni sui passaggi e gli strumenti per eseguire la migrazione di script dal modulo AzureRM al nuovo modulo Az.
ms.devlang: powershell
ms.service: azure-powershell
ms.topic: conceptual
ms.date: 10/12/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: 2f3b6a55b3c674a6030a1d3568e57cdb15c43b02
ms.sourcegitcommit: d0045e283ef062c74a223258fd4d5d6432bac531
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/14/2020
ms.locfileid: "92021092"
---
# <a name="migrate-azure-powershell-from-azurerm-to-az"></a>Eseguire la migrazione di Azure PowerShell da AzureRM ad Az

Tutte le versioni del modulo AzureRM PowerShell non vengono più aggiornate, ma il supporto è ancora disponibile. Il [modulo Az PowerShell](install-az-ps.md) è ora il modulo di PowerShell consigliato per l'interazione con Azure.

Gli script scritti per i cmdlet di AzureRM non funzioneranno automaticamente con il nuovo modulo. Per semplificare la transizione, è stato sviluppato il [toolkit di migrazione da AzureRM ad Az](https://github.com/Azure/azure-powershell-migration). Per quanto nessuna migrazione a un nuovo set di comandi sia immediata, questo articolo consentirà di iniziare la transizione al modulo Az PowerShell. Per altre informazioni sui motivi per cui il modulo Az PowerShell è stato creato, vedere [Introduzione del nuovo modulo Az di Azure PowerShell](new-azureps-module-az.md).

Per visualizzare l'elenco completo delle modifiche di rilievo tra AzureRM e Az, vedere [Modifiche di rilievo della migrazione da AzureRM ad Az](migrate-az-1.0.0.md).

## <a name="ensure-existing-scripts-work-with-the-latest-azurerm-release"></a>Verificare il funzionamento degli script esistenti con l'ultima versione di AzureRM

Prima di eseguire i passaggi di migrazione, verificare quali versioni di AzureRM sono installate nel sistema.
In questo modo è possibile assicurarsi che gli script siano già in esecuzione nella versione più recente e sapere quali versioni di AzureRM devono essere disinstallate.

Per controllare quale versione di AzureRM è stata installata, eseguire questo esempio:

```azurepowershell
Get-Module -Name AzureRM -ListAvailable -All
```

La versione **più recente** disponibile di AzureRM è la **6.13.1**. Se questa versione non è installata, per poter usare gli script esistenti con il modulo Az, può essere necessario apportare altre modifiche oltre a quelle descritte in questo articolo e nell'[elenco di modifiche che causano un'interruzione](migrate-az-1.0.0.md).

Se gli script non funzionano con AzureRM 6.13.1, aggiornarli in base alle indicazioni della [guida alla migrazione di AzureRM dalla versione 5.x alla versione 6.x](/powershell/azure/azurerm/migration-guide.6.0.0). Se si usa una versione precedente del modulo AzureRM, sono disponibili guide alla migrazione per ogni versione principale.

## <a name="install-the-azurerm-to-az-migration-toolkit"></a>Installare il toolkit di migrazione da AzureRM ad Az

```azurepowershell
Install-Module -Name Az.Tools.Migration
```

## <a name="automatically-migrate-your-powershell-scripts"></a>Eseguire automaticamente la migrazione degli script di PowerShell

Grazie al toolkit di migrazione da AzureRM ad Az, è possibile generare un piano per determinare quali modifiche verranno eseguite sugli script prima di apportare modifiche agli script e prima di installare il modulo Az PowerShell.

L'avvio rapido [Eseguire automaticamente la migrazione degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell](quickstart-migrate-azurerm-to-az-automatically.md) illustra in modo dettagliato l'intero processo di aggiornamento automatico degli script di PowerShell dal modulo AzureRM al modulo Az PowerShell.

## <a name="next-steps"></a>Passaggi successivi

[Installare Azure PowerShell](install-az-ps.md)
[Disinstallare AzureRM](uninstall-az-ps.md#uninstall-the-azurerm-module)
