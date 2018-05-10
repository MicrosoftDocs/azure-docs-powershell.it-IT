---
title: Accedere ad Azure PowerShell
description: Accedere ad Azure PowerShell
services: azure
author: sdwheeler
ms.author: sewhee
manager: carmonm
ms.product: azure
ms.service: azure-powershell
ms.devlang: powershell
ms.topic: conceptual
ms.date: 05/15/2017
ms.openlocfilehash: 1af5aeffb8e87e916df3e2440a84805935136c0f
ms.sourcegitcommit: 37bfbf11fd0967a8e7977c692ab829d286baf88a
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 05/08/2018
---
# <a name="log-in-with-azure-powershell"></a>Accedere ad Azure PowerShell

Azure PowerShell supporta più metodi di accesso. Il modo più semplice per iniziare consiste nell'accedere in modo interattivo dalla riga di comando.

## <a name="interactive-log-in"></a>Accesso interattivo

1. Digitare `Login-AzureRmAccount`. Apparirà una finestra di dialogo che richiede le credenziali di Azure.

2. Digitare l'indirizzo di posta elettronica e la password associati all'account. Le informazioni delle credenziali vengono autenticate e salvate in Azure, quindi la finestra viene chiusa.

## <a name="log-in-with-a-service-principal"></a>Accesso con un'entità servizio

Le entità servizio consentono di creare account non interattivi da usare per la modifica delle risorse. Le entità servizio sono analoghe agli account utente a cui è possibile applicare delle regole mediante Azure Active Directory. Concedendo le autorizzazioni minime necessarie a un'entità servizio, è possibile garantire una sicurezza ancora maggiore agli script di automazione.

1. Se non si dispone già di un'entità servizio, [crearne una](create-azure-service-principal-azureps.md).

2. Accedere con l'entità servizio.

    ```powershell
    Login-AzureRmAccount -ServicePrincipal -ApplicationId  "http://my-app" -Credential $pscredential -TenantId $tenantid
    ```

    Per ottenere il TenantId, accedere in modo interattivo e quindi recuperare il TenantId dalla sottoscrizione.

    ```powershell
    Get-AzureRmSubscription
    ```

    ```
    Environment           : AzureCloud
    Account               : username@contoso.com
    TenantId              : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionId        : XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
    SubscriptionName      : My Production Subscription
    CurrentStorageAccount :
    ```

### <a name="log-in-using-an-azure-vm-managed-service-identity"></a>Accedere tramite un'Identità del servizio gestito della macchina virtuale di Azure

Identità del servizio gestito è una funzionalità in anteprima di Azure Active Directory. È possibile usare un'entità servizio di Identità del servizio gestito per eseguire l'accesso e acquisire un token di accesso solo app per accedere ad altre risorse.

Per altre informazioni su Identità del servizio gestito, vedere [How to use an Azure VM Managed Service Identity (MSI) for sign-in and token acquisition](/azure/active-directory/msi-how-to-get-access-token-using-msi) (Come usare un'Identità del servizio gestito della macchina virtuale di Azure per l'accesso e l'acquisizione di token).

## <a name="log-in-to-another-cloud"></a>Accedere a un altro cloud

I servizi cloud di Azure offrono più ambienti conformi alle norme in materia di gestione dei dati vigenti in diversi paesi. Se l'account di Azure si trova in un cloud governativo è necessario specificare l'ambiente quando si accede. Ad esempio, se l'account si trova nel cloud della Cina, accedere usando il comando seguente:

```powershell
Login-AzureRmAccount -EnvironmentName AzureChinaCloud
```

Usare il comando seguente per visualizzare un elenco degli ambienti disponibili:

```powershell
Get-AzureRmEnvironment | Select-Object Name
```

```
Name
----
AzureCloud
AzureChinaCloud
AzureUSGovernment
AzureGermanCloud
```

## <a name="learn-more-about-managing-azure-role-based-access"></a>Altre informazioni sulla gestione degli accessi in base al ruolo in Azure

Per altre informazioni su autenticazione e gestione delle sottoscrizioni in Azure, vedere [Gestire account, sottoscrizioni e ruoli amministrativi](/azure/active-directory/role-based-access-control-configure).

Cmdlet di Azure PowerShell per la gestione dei ruoli

* [Get-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Get-AzureRmRoleAssignment)
* [Get-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Get-AzureRmRoleDefinition)
* [New-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/New-AzureRmRoleAssignment)
* [New-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/New-AzureRmRoleDefinition)
* [Remove-AzureRmRoleAssignment](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleAssignment)
* [Remove-AzureRmRoleDefinition](/powershell/module/AzureRM.Resources/Remove-AzureRmRoleDefinition)
* [Set-AzureRmRoleDefinition](/powershell/moduel/AzureRM.Resources/Set-AzureRmRoleDefinition)
