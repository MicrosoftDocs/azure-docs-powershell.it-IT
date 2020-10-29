---
title: Domande frequenti
description: Domande frequenti su Azure PowerShell.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 08/17/2020
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: b436f00ccef779464a555cd787a9ab0adcc970ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "92753756"
---
# <a name="frequently-asked-questions-about-azure-powershell"></a>Domande frequenti su Azure PowerShell

## <a name="what-is-azure-powershell"></a>Che cos'è Azure PowerShell?

Azure PowerShell è un set di cmdlet che consente di gestire le risorse di Azure direttamente con PowerShell. Nel dicembre 2018 il modulo Az PowerShell è diventato disponibile a livello generale. Ora è il modulo PowerShell consigliato per l'interazione con Azure. Per altre informazioni sul modulo Az PowerShell, vedere [Introduzione del nuovo modulo Az di Azure PowerShell](/powershell/azure/new-azureps-module-az).

## <a name="how-do-i-disable-breaking-change-warning-messages-in-azure-powershell"></a>Come si disabilitano i messaggi di avviso relativi a modifiche che causano interruzioni in Azure PowerShell?

Per non visualizzare i messaggi di avviso relativi a modifiche che causano interruzioni in Azure PowerShell, è necessario impostare la variabile di ambiente `SuppressAzurePowerShellBreakingChangeWarnings` su `true`.

```azurepowershell
Set-Item -Path Env:\SuppressAzurePowerShellBreakingChangeWarnings -Value $true
```
