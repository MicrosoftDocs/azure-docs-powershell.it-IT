---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f921cceb3692032f61f99db825efeea074773faa
ms.sourcegitcommit: 375232b84336ef5e13052504deaa43f5bd4b7f65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/05/2020
ms.locfileid: "94311718"
---
# <span data-ttu-id="d75d9-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d75d9-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="d75d9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d75d9-102">SYNOPSIS</span></span>
<span data-ttu-id="d75d9-103">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d75d9-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="d75d9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d75d9-104">SYNTAX</span></span>

### <span data-ttu-id="d75d9-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d75d9-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d75d9-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d75d9-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-118">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d75d9-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="d75d9-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d75d9-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d75d9-120">DESCRIPTION</span></span>
<span data-ttu-id="d75d9-121">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d75d9-121">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="d75d9-122">Il set di parametri predefinito usa i valori predefiniti per i parametri se l'utente non ne offre uno.</span><span class="sxs-lookup"><span data-stu-id="d75d9-122">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="d75d9-123">Per altre informazioni sui valori predefiniti usati, vedere la descrizione per i parametri specificati di seguito.</span><span class="sxs-lookup"><span data-stu-id="d75d9-123">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="d75d9-124">Questo cmdlet offre la possibilità di assegnare un ruolo all'entità servizio con i `Role` parametri e, `Scope` se nessuno di questi parametri viene fornito, nessun ruolo verrà assegnato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-124">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="d75d9-125">I valori predefiniti per i `Role` `Scope` parametri e sono rispettivamente "collaboratore" e l'abbonamento corrente ( _Nota_ : le impostazioni predefinite vengono usate solo quando l'utente fornisce un valore per uno dei due parametri, ma non per l'altro).</span><span class="sxs-lookup"><span data-stu-id="d75d9-125">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="d75d9-126">Il cmdlet crea inoltre in modo implicito un'applicazione e ne imposta le proprietà (se ApplicationId non è disponibile).</span><span class="sxs-lookup"><span data-stu-id="d75d9-126">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="d75d9-127">Per aggiornare i parametri specifici dell'applicazione, usare Set-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75d9-127">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="d75d9-128">Quando si crea un'entità di servizio usando il comando **New-AzADServicePrincipal** , l'output include le credenziali che è necessario proteggere.</span><span class="sxs-lookup"><span data-stu-id="d75d9-128">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="d75d9-129">Assicurati di non includere queste credenziali nel codice o di controllare le credenziali nel controllo di origine.</span><span class="sxs-lookup"><span data-stu-id="d75d9-129">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="d75d9-130">In alternativa, è consigliabile usare le [identità gestite](/azure/active-directory/managed-identities-azure-resources/overview) per evitare la necessità di usare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="d75d9-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="d75d9-131">Per impostazione predefinita, **New-AzADServicePrincipal** assegna il ruolo di [collaboratore](/azure/role-based-access-control/built-in-roles#contributor) all'entità del servizio nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d75d9-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="d75d9-132">Per ridurre il rischio di un'entità di servizio compromessa, assegnare un ruolo più specifico e limitare l'ambito a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d75d9-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="d75d9-133">Per altre informazioni, vedere [procedura per aggiungere un'assegnazione di ruolo](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="d75d9-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="d75d9-134">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d75d9-134">EXAMPLES</span></span>

### <span data-ttu-id="d75d9-135">Esempio 1-creazione di un servizio di Active Directory semplice</span><span class="sxs-lookup"><span data-stu-id="d75d9-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="d75d9-136">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="d75d9-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="d75d9-137">Dato che non è stato fornito un ID applicazione, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d75d9-138">Dato che non sono stati forniti valori `Role` o `Scope` , l'entità servizio creata non ha le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="d75d9-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="d75d9-139">Esempio 2-Creazione di un servizio di Active Directory semplice con un ruolo specificato e un ambito predefinito</span><span class="sxs-lookup"><span data-stu-id="d75d9-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="d75d9-140">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="d75d9-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d75d9-141">Dato che l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d75d9-142">L'entità servizio è stata creata con le autorizzazioni "Reader" per l'abbonamento corrente (dato che non è stato specificato alcun valore per il `Scope` parametro).</span><span class="sxs-lookup"><span data-stu-id="d75d9-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="d75d9-143">Esempio 3-creazione di un servizio di Active Directory semplice con un ambito specificato e un ruolo predefinito</span><span class="sxs-lookup"><span data-stu-id="d75d9-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="d75d9-144">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="d75d9-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d75d9-145">Dato che l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d75d9-146">L'entità servizio è stata creata con le autorizzazioni "collaboratore" (poiché non è stato specificato alcun valore per il `Role` parametro) nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d75d9-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="d75d9-147">Esempio 4-creazione di un servizio di Active Directory semplice con un ambito e un ruolo specificati</span><span class="sxs-lookup"><span data-stu-id="d75d9-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="d75d9-148">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="d75d9-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="d75d9-149">Dato che l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="d75d9-150">L'entità servizio è stata creata con le autorizzazioni "Reader" nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="d75d9-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="d75d9-151">Esempio 5-creare una nuova entità servizio annunci usando l'ID applicazione con assegnazione ruolo</span><span class="sxs-lookup"><span data-stu-id="d75d9-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="d75d9-152">Crea una nuova entità servizio annunci per l'applicazione con l'ID applicazione "34a28ad2-DEC4-4A41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="d75d9-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="d75d9-153">Dato che non sono stati forniti valori `Role` o `Scope` , l'entità servizio creata non ha le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="d75d9-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="d75d9-154">Esempio 6-creare una nuova entità del servizio PUBBLICITARIo usando piping</span><span class="sxs-lookup"><span data-stu-id="d75d9-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="d75d9-155">Ottiene l'applicazione con l'ID oggetto "3ede3c26-B443-4e0b-9efc-b05e68338dc3" e le pipe al cmdlet New-AzADServicePrincipal per creare una nuova entità del servizio Active Directory per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="d75d9-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

### <span data-ttu-id="d75d9-156">Esempio 7-creare una nuova entità servizio annunci usando le credenziali DisplayName e password</span><span class="sxs-lookup"><span data-stu-id="d75d9-156">Example 7 - Create a new AD service principal using DisplayName and password credential</span></span>

```
PS C:\> $credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{ StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password="StrongPassworld!23"}
PS C:\> $sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials

ServicePrincipalNames : {exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc, http://ServicePrincipalName}
ApplicationId         : exxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxcc
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 6xxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxb
Type                  :
```

<span data-ttu-id="d75d9-157">Crea una nuova applicazione con il nome "ServicePrincipalName" e la password "StrongPassworld! 23" e crea l'entità servizio in base all'applicazione appena creata.</span><span class="sxs-lookup"><span data-stu-id="d75d9-157">Creates a new application with name "ServicePrincipalName" and password "StrongPassworld!23" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="d75d9-158">La data di inizio e di fine vengono aggiunte alle credenziali delle password.</span><span class="sxs-lookup"><span data-stu-id="d75d9-158">The start date and end date are added to password credential.</span></span>

### <span data-ttu-id="d75d9-159">Esempio 8: creare una nuova entità del servizio Active Directory usando DisplayName e le credenziali con chiave normale</span><span class="sxs-lookup"><span data-stu-id="d75d9-159">Example 8 - Create a new AD service principal using DisplayName and plain key credential</span></span>

```
PS C:\> $cert = <public certificate as base64-encoded string>
PS C:\> $sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate "2021-01-01"

ServicePrincipalNames : {cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6, http://ServicePrincipalName}
ApplicationId         : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxx6
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : cxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxc
Type                  :
```

<span data-ttu-id="d75d9-160">Crea una nuova applicazione con il nome "ServicePrincipalName" e certificato "$cert" e crea l'entità servizio in base all'applicazione appena creata.</span><span class="sxs-lookup"><span data-stu-id="d75d9-160">Creates a new application with name "ServicePrincipalName" and certifcate "$cert" and creates the service principal based on the application just created.</span></span> <span data-ttu-id="d75d9-161">La data di fine viene aggiunta alle credenziali chiave.</span><span class="sxs-lookup"><span data-stu-id="d75d9-161">The end date is added to key credential.</span></span>

## <span data-ttu-id="d75d9-162">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d75d9-162">PARAMETERS</span></span>

### <span data-ttu-id="d75d9-163">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d75d9-163">-ApplicationId</span></span>
<span data-ttu-id="d75d9-164">ID applicazione univoco per un'entità di servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="d75d9-164">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="d75d9-165">Una volta creata questa proprietà non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="d75d9-165">Once created this property cannot be changed.</span></span>
<span data-ttu-id="d75d9-166">Se non viene specificato un ID applicazione, verrà generato uno.</span><span class="sxs-lookup"><span data-stu-id="d75d9-166">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-167">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="d75d9-167">-ApplicationObject</span></span>
<span data-ttu-id="d75d9-168">Oggetto che rappresenta l'applicazione per cui viene creata l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-168">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-169">-CertValue</span><span class="sxs-lookup"><span data-stu-id="d75d9-169">-CertValue</span></span>
<span data-ttu-id="d75d9-170">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="d75d9-170">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="d75d9-171">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="d75d9-171">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-172">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d75d9-172">-DefaultProfile</span></span>
<span data-ttu-id="d75d9-173">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d75d9-173">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-174">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d75d9-174">-DisplayName</span></span>
<span data-ttu-id="d75d9-175">Nome descrittivo dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-175">The friendly name of the service principal.</span></span> <span data-ttu-id="d75d9-176">Se non viene specificato un nome visualizzato, il valore predefinito sarà "Azure-PowerShell-MM-DD-AAAA-HH-mm-SS", in cui il suffisso è il momento della creazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d75d9-176">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-177">-EndDate</span><span class="sxs-lookup"><span data-stu-id="d75d9-177">-EndDate</span></span>
<span data-ttu-id="d75d9-178">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="d75d9-178">The effective end date of the credential usage.</span></span>
<span data-ttu-id="d75d9-179">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="d75d9-179">The default end date value is one year from today.</span></span> <span data-ttu-id="d75d9-180">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="d75d9-180">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-181">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="d75d9-181">-KeyCredential</span></span>
<span data-ttu-id="d75d9-182">Raccolta di credenziali chiave associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d75d9-182">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-183">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="d75d9-183">-PasswordCredential</span></span>
<span data-ttu-id="d75d9-184">Raccolta di credenziali password associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="d75d9-184">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-185">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="d75d9-185">-Role</span></span>
<span data-ttu-id="d75d9-186">Il ruolo che l'entità servizio ha sull'ambito.</span><span class="sxs-lookup"><span data-stu-id="d75d9-186">The role that the service principal has over the scope.</span></span> <span data-ttu-id="d75d9-187">Se viene specificato un valore per, `Scope` ma non viene specificato alcun valore `Role` , `Role` il ruolo "collaboratore" verrà impostato come predefinito.</span><span class="sxs-lookup"><span data-stu-id="d75d9-187">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-188">-Ambito</span><span class="sxs-lookup"><span data-stu-id="d75d9-188">-Scope</span></span>
<span data-ttu-id="d75d9-189">Ambito per cui l'entità del servizio dispone delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="d75d9-189">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="d75d9-190">Se viene specificato un valore per, `Role` ma non viene specificato alcun valore `Scope` , `Scope` verrà impostato come predefinito per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="d75d9-190">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-191">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="d75d9-191">-SkipAssignment</span></span>
<span data-ttu-id="d75d9-192">Se impostato, salterà la creazione dell'assegnazione di ruolo predefinita per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="d75d9-192">If set, will skip creating the default role assignment for the service principal.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-193">-StartDate</span><span class="sxs-lookup"><span data-stu-id="d75d9-193">-StartDate</span></span>
<span data-ttu-id="d75d9-194">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="d75d9-194">The effective start date of the credential usage.</span></span>
<span data-ttu-id="d75d9-195">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="d75d9-195">The default start date value is today.</span></span> <span data-ttu-id="d75d9-196">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="d75d9-196">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: SimpleParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-197">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d75d9-197">-Confirm</span></span>
<span data-ttu-id="d75d9-198">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d75d9-198">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-199">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d75d9-199">-WhatIf</span></span>
<span data-ttu-id="d75d9-200">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d75d9-200">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d75d9-201">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d75d9-201">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d75d9-202">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d75d9-202">CommonParameters</span></span>
<span data-ttu-id="d75d9-203">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d75d9-203">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d75d9-204">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d75d9-204">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d75d9-205">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d75d9-205">INPUTS</span></span>

### <span data-ttu-id="d75d9-206">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d75d9-206">System.Guid</span></span>

### <span data-ttu-id="d75d9-207">System. String</span><span class="sxs-lookup"><span data-stu-id="d75d9-207">System.String</span></span>

### <span data-ttu-id="d75d9-208">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="d75d9-208">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="d75d9-209">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="d75d9-209">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="d75d9-210">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="d75d9-210">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="d75d9-211">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="d75d9-211">System.DateTime</span></span>

## <span data-ttu-id="d75d9-212">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d75d9-212">OUTPUTS</span></span>

### <span data-ttu-id="d75d9-213">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d75d9-213">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="d75d9-214">Microsoft. Azure. Commands. resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="d75d9-214">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="d75d9-215">Note</span><span class="sxs-lookup"><span data-stu-id="d75d9-215">NOTES</span></span>
<span data-ttu-id="d75d9-216">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="d75d9-216">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="d75d9-217">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d75d9-217">RELATED LINKS</span></span>

[<span data-ttu-id="d75d9-218">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d75d9-218">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="d75d9-219">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d75d9-219">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="d75d9-220">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d75d9-220">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="d75d9-221">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="d75d9-221">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="d75d9-222">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d75d9-222">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="d75d9-223">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d75d9-223">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="d75d9-224">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="d75d9-224">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

