---
title: Accedere con Azure PowerShell
description: Come eseguire l'accesso con Azure PowerShell come utente, come entità servizio o con le identità gestite per le risorse di Azure.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 09/09/2018
ms.custom: devx-track-azurepowershell
ms.openlocfilehash: d6a825ef91dbbcb18cd8b05dc1e0113433372b8a
ms.sourcegitcommit: 8b3126b5c79f453464d90669f0046ba86b7a3424
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "89243430"
---
# <a name="sign-in-with-azure-powershell"></a>Accedere con Azure PowerShell

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

Azure PowerShell supporta diversi metodi di autenticazione. Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.

## <a name="sign-in-interactively"></a>Accedere in modo interattivo

Per accedere in modo interattivo, usare il cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell-interactive
Connect-AzureRmAccount
```

Durante l'esecuzione, questo cmdlet aprirà una finestra di dialogo che chiederà l'indirizzo e-mail e la password associati all'account Azure. Questa autenticazione dura per la sessione corrente di PowerShell.

> [!IMPORTANT]
> A partire dalla versione Azure PowerShell 6.3.0, le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi a Windows. Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Accedere con un'entità servizio

Le entità servizio sono account Azure non interattivi. Come per gli altri account utente, le relative autorizzazioni vengono gestite con Azure Active Directory. Concedendo a un'entità servizio solo le autorizzazioni necessarie, viene garantita la sicurezza degli script di automazione.

Per informazioni su come creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).

Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzureRmAccount`. Saranno necessari anche le credenziali di accesso dell'entità servizio e l'ID tenant associato all'entità servizio. Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Questo cmdlet visualizza una finestra di dialogo in cui inserire l'ID utente e la password dell'entità servizio.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-managed-service-identity"></a>Accedere con un'identità del servizio gestita di Azure

Le identità gestite per le risorse di Azure sono una funzionalità di Azure Active Directory. È possibile usare l'entità servizio di un'identità gestita per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse. Le identità gestite sono disponibili solo nelle macchine virtuali in esecuzione in un cloud di Azure.

Per informazioni sulle identità gestite per le risorse di Azure, vedere [Come usare le identità gestite per le risorse di Azure in una macchina virtuale di Azure per acquisire un token di accesso](/azure/active-directory/managed-identities-azure-resources/how-to-use-vm-token).

## <a name="sign-in-as-a-cloud-solution-provider-csp"></a>Effettuare l'accesso come Cloud Solution Provider (CSP)

L'accesso come [Cloud Solution Provider (CSP)](https://azure.microsoft.com/offers/ms-azr-0145p/) richiede l'uso di `-TenantId`. Questo parametro può essere generalmente specificato come ID tenant o nome dominio. Per l'accesso come CSP è tuttavia necessario specificare un **ID tenant**.

```azurepowershell-interactive
Connect-AzureRmAccount -TenantId 'xxxx-xxxx-xxxx-xxxx'
```

## <a name="sign-in-to-another-cloud"></a>Accedere a un altro cloud

I servizi cloud di Azure offrono ambienti conformi alle normative di gestione dei dati a livello di area.
Per gli account nel cloud di un'area, impostare l'ambiente al momento dell'accesso con l'argomento `-Environment`.
Ad esempio, se l'account si trova nel cloud della Cina:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Il comando seguente recupera un elenco degli ambienti disponibili:

```azurepowershell-interactive
Get-AzureRmEnvironment | Select-Object Name
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Altre informazioni sulla gestione degli accessi in base al ruolo in Azure

Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).

Cmdlet di Azure PowerShell per la gestione dei ruoli:

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Set-AzureRmRoleDefinition)
