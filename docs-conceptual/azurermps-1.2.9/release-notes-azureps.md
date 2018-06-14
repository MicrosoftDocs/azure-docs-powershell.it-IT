---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: 91d97260568a36e1135196899503fb0c8e1c6731
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 06/08/2018
ms.locfileid: "34853016"
---
# <a name="release-notes"></a>Note sulla versione

Questo è un elenco delle modifiche apportate ad Azure PowerShell in questa versione.

## <a name="version-129"></a>Versione 1.2.9

Modifiche di questa versione

* Modulo AzureRm.AzureStackAdmin
    + Modifiche apportate al cmdlet Add-AzureRmResourceProviderRegistration per il supporto della divisione tra Azure Resource Manager per amministratori e Azure Resource Manager per tenant. Aggiunta del nuovo parametro -ResourceManagerType.
    + Rimozione dei parametri -AdminUri, -ApiVersion, -SubscriptionId e -Token da ogni cmdlet. Dopo aver emesso avvisi relativi al fatto che questi parametri sarebbero stati deprecati, i parametri sono ora stati rimossi.
* Modulo AzureStackStorage
    + Aggiunta di nuovi cmdlet per supportare scenari di migrazione dei contenitori.
    + Rimozione dei cmdlet correlati a componenti interni e funzionalità sottostanti.
* AzureRM.BootStrapper
    + Creazione del nuovo modulo per gestire le versioni dei cmdlet di Azure PowerShell tramite l'uso dei profili di versione