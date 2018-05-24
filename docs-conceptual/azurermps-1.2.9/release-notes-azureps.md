---
title: Log delle modifiche di Azure PowerShell | Microsoft Docs
description: Questa è una cronologia delle modifiche apportate ad Azure PowerShell nella versione più recente.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.service: azure-powershell
ms.product: azure
ms.devlang: powershell
ms.topic: conceptual
ms.workload: ''
ms.date: 05/18/2017
ms.openlocfilehash: b42ad6f22f47e10c9190cf5a919f781375ff26f2
ms.sourcegitcommit: 5971c92cb023bdd1d71fa2ad0a3b378abfbd092a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/23/2018
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