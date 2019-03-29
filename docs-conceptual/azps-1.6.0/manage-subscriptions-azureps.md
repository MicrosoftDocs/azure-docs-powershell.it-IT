---
title: Gestire le sottoscrizioni di Azure con Azure PowerShell
description: Gestire le sottoscrizioni di Azure con Azure PowerShell
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 02/04/2019
ms.openlocfilehash: 29d7c84d0ca9ae8d3e4e22f407b007d2d582f8bc
ms.sourcegitcommit: 8f59e11e5c991543964154d63648aa1e6ae22512
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 03/26/2019
ms.locfileid: "58475419"
---
# <a name="use-multiple-azure-subscriptions"></a>Usare più sottoscrizioni di Azure

La maggior parte degli utenti di Azure non avrà mai più di una sottoscrizione. Si possono tuttavia avere più sottoscrizioni in Azure se si fa parte di più organizzazioni o se l'organizzazione ha suddiviso l'accesso a determinate risorse tra vari gruppi. L'interfaccia della riga di comando supporta la selezione di una sottoscrizione sia a livello globale che per ogni comando.

## <a name="tenants-users-and-subscriptions"></a>Tenant, utenti e sottoscrizioni

La differenza tra tenant, utenti e sottoscrizioni in Azure potrebbe non essere del tutto chiara. Un _tenant_ è l'entità di Azure Active Directory che include un'intera organizzazione. Il tenant ha almeno una _sottoscrizione_ e un _utente_. Un utente è una persona ed è associato a un solo tenant, corrispondente all'organizzazione a cui appartiene. Gli utenti sono gli account che accedono ad Azure per creare, gestire e usare le risorse.
Un utente può avere accesso a più _sottoscrizioni_, che sono contratti con Microsoft per l'uso dei servizi cloud, incluso Azure. Ogni risorsa è associata a una sottoscrizione.

Per altre informazioni sulle differenze tra tenant, utenti e sottoscrizioni, vedere il [dizionario della terminologia cloud di Azure](/azure/azure-glossary-cloud-terminology).  Per informazioni su come aggiungere una sottoscrizione al tenant di Azure Active Directory, vedere [Come aggiungere una sottoscrizione di Azure ad Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).
Per informazioni su come eseguire l'accesso a un tenant specifico, vedere [Accedere con Azure PowerShell](/powershell/azure/authenticate-azureps).

## <a name="change-the-active-subscription"></a>Cambiare la sottoscrizione attiva

In Azure PowerShell l'accesso alle risorse per una sottoscrizione richiede la modifica della sottoscrizione associata alla sessione corrente di Azure.
Questa operazione viene eseguita modificando il contesto della sessione attiva, cioè le informazioni su tenant, sottoscrizione e cmdlet dell'utente in cui deve essere eseguita.
Per modificare le sottoscrizioni, è prima necessario recuperare un oggetto di contesto di Azure PowerShell con [Get-AzSubscription](/powershell/module/az.accounts/get-azsubscription) e quindi di modificare il contesto corrente con [Set-AzContext](/powershell/module/az.accounts/set-azcontext).

L'esempio seguente mostra come ottenere una sottoscrizione nel tenant attualmente attivo e impostarla come sessione attiva:

```powershell-interactive
$context = Get-AzSubscription -SubscriptionId ...
Set-AzContext $context
```

Per altre informazioni sui contesti di Azure PowerShell, tra cui come salvarli e passare rapidamente dall'uno all'altro per lavorare facilmente con più sottoscrizioni, vedere [Conservare le credenziali con i contesti di Azure PowerShell](context-persistence.md).
