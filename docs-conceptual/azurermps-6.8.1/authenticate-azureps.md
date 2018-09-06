---
title: Accedere con Azure PowerShell
description: Come effettuare l'accesso con Azure PowerShell come utente, entità servizio o con l'identità del servizio gestita.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 20194ac2282d602ba61bf130791edac9f4ffae6c
ms.sourcegitcommit: 971f19181b2cd68b7845bbebdb22858c06541c8c
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 09/06/2018
ms.locfileid: "43383975"
---
# <a name="sign-in-with-azure-powershell"></a>Accedere con Azure PowerShell

Azure PowerShell supporta più metodi di autenticazione. Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.

## <a name="sign-in-interactively"></a>Accedere in modo interattivo

Per accedere in modo interattivo, usare il cmdlet [Connect-AzureRmAccount](/powershell/module/azurerm.profile/connect-azurermaccount).

```azurepowershell
Connect-AzureRmAccount
```

Durante l'esecuzione, questo cmdlet aprirà una finestra di dialogo che chiederà l'indirizzo e-mail e la password associati all'account Azure. Quando si esegue l'autenticazione, queste informazioni vengono salvate per la sessione corrente di PowerShell, la finestra di dialogo viene chiusa e si ha accesso a tutti i cmdlet di Azure PowerShell.

> [!IMPORTANT]
> A partire dalla versione Azure PowerShell 6.3.0, le credenziali vengono condivise tra più sessioni di PowerShell, purché si rimanga connessi a Windows. Per altre informazioni, vedere l'articolo relativo alle [Credenziali persistenti](context-persistence.md).

## <a name="sign-in-with-a-service-principal"></a>Accedere con un'entità servizio

Le entità servizio consentono di creare account non interattivi da usare per la modifica delle risorse. Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory. Concedendo le autorizzazioni minime necessarie a un'entità servizio, è possibile garantire una sicurezza ancora maggiore agli script di automazione.

Se è necessario creare un'entità servizio da usare con Azure PowerShell, vedere [Creare un'entità servizio di Azure con Azure PowerShell](create-azure-service-principal-azureps.md).

Per accedere con un'entità servizio, usare l'argomento `-ServicePrincipal` con il cmdlet `Connect-AzureRmAccount`. Saranno anche necessari l'ID applicazione dell'entità servizio, le credenziali di accesso e l'ID tenant associati all'entità servizio. Per ottenere le credenziali dell'entità servizio come oggetto appropriato, usare il cmdlet [Get-Credential](/powershell/module/microsoft.powershell.security/get-credential). Questo cmdlet visualizza una finestra di dialogo in cui inserire l'ID utente e la password dell'entità servizio.

```azurepowershell-interactive
$pscredential = Get-Credential
Connect-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
```

## <a name="sign-in-using-an-azure-vm-managed-service-identity"></a>Accedere tramite un'identità del servizio gestita della macchina virtuale di Azure

Identità del servizio gestito è una funzionalità in anteprima di Azure Active Directory. È possibile usare un'entità servizio di Identità del servizio gestito per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse. L'identità del servizio gestita è disponibile solo in macchine virtuali in esecuzione in un cloud di Azure.

Per altre informazioni su Identità del servizio gestito, vedere [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi) (Come usare un'Identità del servizio gestito della macchina virtuale di Azure per l'accesso e l'acquisizione di token).

## <a name="sign-in-to-another-cloud"></a>Accedere a un altro cloud

I servizi cloud di Azure offrono più ambienti conformi alle norme in materia di gestione dei dati vigenti in diverse aree. Se l'account di Azure si trova in un cloud associato a una di queste aree, è necessario specificare l'ambiente al momento dell'accesso. Ad esempio, se l'account si trova nel cloud della Cina, accedere usando il comando seguente:

```azurepowershell-interactive
Connect-AzureRmAccount -Environment AzureChinaCloud
```

Usare il comando seguente per visualizzare un elenco degli ambienti disponibili:

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
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
