---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 10/29/2018
ms.openlocfilehash: 8b085720aeabe26c1293ece193e050b31f99a693
ms.sourcegitcommit: ae81b08a45d8729fc8d40156422e3eb2e94de8c7
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 12/27/2018
ms.locfileid: "53786680"
---
# <a name="sign-in-with-azure-powershell"></a>Accedere con Azure PowerShell

Azure PowerShell supporta diversi metodi di autenticazione. Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.

## <a name="sign-in-interactively"></a>Accedere in modo interattivo

Per accedere in modo interattivo, usare il cmdlet [Connect-AzAccount](/powershell/module/az.accounts/connect-azaccount).

```azurepowershell-interactive
Connect-AzAccount
```

Quando viene eseguito, questo cmdlet visualizzerà una stringa del token. Per accedere, copiare questa stringa e incollarla in https://microsoft.com/devicelogin in un browser. La sessione di PowerShell verrà quindi autenticata per connettersi ad Azure. Questa autenticazione dura per la sessione corrente di PowerShell.

> [!IMPORTANT]
>
> Le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi.
> Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Accedere con un'entità servizio

Le entità servizio sono account Azure non interattivi. Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory. Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.

Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).

Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzAccount`. Saranno necessari anche l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associato all'entità servizio. Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Questo cmdlet visualizzerà la richiesta di inserimento dell'ID utente e della password dell'entità servizio.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Accedere con un'identità del servizio gestita di Azure

Le identità gestite per le risorse di Azure sono una funzionalità di Azure Active Directory. È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse. Le identità gestite sono disponibili solo nelle macchine virtuali in esecuzione in un cloud di Azure.

Per informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Effettuare l'accesso come Cloud Solution Provider (CSP)

L'accesso come [Cloud Solution Provider (CSP)](https://azure.microsoft.com/en-us/offers/ms-azr-0145p/) richiede l'uso di `-TenantId`. Questo parametro può essere generalmente specificato come ID tenant o nome dominio. Per l'accesso come CSP è tuttavia necessario specificare un **ID tenant**.

```azurepowershell-interactive
Connect-AzAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Accedere a un altro cloud

I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.
Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.
Ad esempio, se l'account si trova nel cloud della Cina:

```azurepowershell-interactive
Connect-AzAccount -Environment AzureChinaCloud
```

Il comando seguente recupera un elenco degli ambienti disponibili:

```azurepowershell-interactive
Get-AzEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Altre informazioni sulla gestione degli accessi in base al ruolo in Azure

Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).

Cmdlet di Azure PowerShell per la gestione dei ruoli:

* [Get-AzRoleAssignment](/powershell/module/az.Resources/Get-azRoleAssignment)
* [Get-AzRoleDefinition](/powershell/module/az.Resources/Get-azRoleDefinition)
* [New-AzRoleAssignment](/powershell/module/az.Resources/New-azRoleAssignment)
* [New-AzRoleDefinition](/powershell/module/az.Resources/New-azRoleDefinition)
* [Remove-AzRoleAssignment](/powershell/module/az.Resources/Remove-azRoleAssignment)
* [Remove-AzRoleDefinition](/powershell/module/az.Resources/Remove-azRoleDefinition)
* [Set-AzRoleDefinition](/powershell/module/az.Resources/Set-azRoleDefinition)
