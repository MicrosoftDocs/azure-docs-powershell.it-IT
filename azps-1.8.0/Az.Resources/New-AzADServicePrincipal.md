---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: aa46a09eec134797f1dcacfeb0541769c4569e9e
ms.sourcegitcommit: e680033f216d86cd91a1dfdb8328d32f4c99d21a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "99251742"
---
# <span data-ttu-id="9790d-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9790d-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="9790d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9790d-102">SYNOPSIS</span></span>
<span data-ttu-id="9790d-103">Crea una nuova entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9790d-103">Creates a new azure active directory service principal.</span></span>

## <span data-ttu-id="9790d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9790d-104">SYNTAX</span></span>

### <span data-ttu-id="9790d-105">SimpleParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9790d-105">SimpleParameterSet (Default)</span></span>
```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9790d-107">ApplicationWithPasswordPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-109">ApplicationWithKeyPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9790d-112">DisplayNameWithPasswordPparamSet</span><span class="sxs-lookup"><span data-stu-id="9790d-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-114">DisplayNameWithKeyPparameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-117">ApplicationObjectWithPasswordPparameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-119">ApplicationObjectWithKeyPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9790d-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="9790d-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9790d-121">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9790d-121">DESCRIPTION</span></span>
<span data-ttu-id="9790d-122">Crea una nuova entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="9790d-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="9790d-123">Se l'utente non ne fornisce uno, il set di parametri predefinito usa i valori predefiniti per i parametri.</span><span class="sxs-lookup"><span data-stu-id="9790d-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="9790d-124">Per altre informazioni sui valori predefiniti usati, vedere la descrizione dei parametri specificati di seguito.</span><span class="sxs-lookup"><span data-stu-id="9790d-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="9790d-125">Questo cmdlet ha la possibilità di assegnare un ruolo all'entità servizio con i parametri e. Se nessuno di questi parametri viene fornito, non verrà assegnato alcun ruolo `Role` `Scope` all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="9790d-126">I valori predefiniti per i parametri e sono rispettivamente "Collaboratore" e la sottoscrizione corrente (nota: i valori predefiniti vengono utilizzati solo quando l'utente fornisce un valore per uno dei due parametri, ma non `Role` `Scope` l'altro).</span><span class="sxs-lookup"><span data-stu-id="9790d-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively (_note_: the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="9790d-127">Il cmdlet crea anche un'applicazione in modo implicito e ne imposta le proprietà, se non viene fornito il valore ApplicationId.</span><span class="sxs-lookup"><span data-stu-id="9790d-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="9790d-128">Per aggiornare i parametri specifici dell'applicazione, usare Set-AzADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9790d-128">In order to update the application specific parameters please use Set-AzADApplication cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="9790d-129">Quando si crea un'entità servizio con il comando **New-AzADServicePrincipal,** l'output include le credenziali che è necessario proteggere.</span><span class="sxs-lookup"><span data-stu-id="9790d-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="9790d-130">In alternativa, è consigliabile usare le identità [gestite](/azure/active-directory/managed-identities-azure-resources/overview) per evitare l'uso delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9790d-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="9790d-131">Per impostazione predefinita, **New-AzADServicePrincipal** assegna il ruolo [Collaboratore](/azure/role-based-access-control/built-in-roles#contributor) all'entità servizio nell'ambito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="9790d-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="9790d-132">Per ridurre il rischio di un'entità servizio compromessa, assegnare un ruolo più specifico e restringere l'ambito a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9790d-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="9790d-133">Per [altre informazioni, vedere La procedura per aggiungere un'assegnazione](/azure/role-based-access-control/role-assignments-steps) di ruolo.</span><span class="sxs-lookup"><span data-stu-id="9790d-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="9790d-134">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9790d-134">EXAMPLES</span></span>

### <span data-ttu-id="9790d-135">Esempio 1 - Creazione di entità servizio Active Directory semplice</span><span class="sxs-lookup"><span data-stu-id="9790d-135">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="9790d-136">Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="9790d-136">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="9790d-137">Poiché non è stato fornito un ID applicazione, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-137">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9790d-138">Poiché non sono stati forniti valori per `Role` o `Scope` , l'entità servizio creata non ha autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="9790d-138">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="9790d-139">Esempio 2 - Creazione semplice di un'entità servizio Active Directory con un ruolo specificato e un ambito predefinito</span><span class="sxs-lookup"><span data-stu-id="9790d-139">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

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

<span data-ttu-id="9790d-140">Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="9790d-140">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="9790d-141">Poiché l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-141">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9790d-142">L'entità servizio è stata creata con le autorizzazioni "Lettore" per la sottoscrizione corrente, poiché non è stato fornito alcun valore per il `Scope` parametro.</span><span class="sxs-lookup"><span data-stu-id="9790d-142">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="9790d-143">Esempio 3 - Creazione semplice di un'entità servizio Active Directory con un ambito e un ruolo predefiniti specificati</span><span class="sxs-lookup"><span data-stu-id="9790d-143">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

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

<span data-ttu-id="9790d-144">Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="9790d-144">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="9790d-145">Poiché l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-145">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9790d-146">L'entità servizio è stata creata con autorizzazioni "Collaboratore" (poiché per il parametro non è stato fornito alcun `Role` valore) sull'ambito del gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="9790d-146">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="9790d-147">Esempio 4 - Creazione semplice di un'entità servizio Active Directory con un ambito e un ruolo specificati</span><span class="sxs-lookup"><span data-stu-id="9790d-147">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

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

<span data-ttu-id="9790d-148">Il comando precedente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="9790d-148">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="9790d-149">Poiché l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-149">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="9790d-150">L'entità servizio è stata creata con autorizzazioni "Lettore" sull'ambito del gruppo di risorse fornito.</span><span class="sxs-lookup"><span data-stu-id="9790d-150">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="9790d-151">Esempio 5 - Creare una nuova entità servizio Active Directory usando l'ID applicazione con l'assegnazione di ruoli</span><span class="sxs-lookup"><span data-stu-id="9790d-151">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="9790d-152">Crea una nuova entità servizio Active Directory per l'applicazione con ID applicazione '34a28ad2-dec4-4a41-bc3b-d22ddf900000e'.</span><span class="sxs-lookup"><span data-stu-id="9790d-152">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="9790d-153">Poiché non sono stati forniti valori per `Role` o `Scope` , l'entità servizio creata non ha autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="9790d-153">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="9790d-154">Esempio 6 - Creare una nuova entità servizio Active Directory tramite piping</span><span class="sxs-lookup"><span data-stu-id="9790d-154">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

<span data-ttu-id="9790d-155">Ottiene l'applicazione con ID oggetto '3ede3c26-b443-4e0b-9efc-b05e68338dc3' e pipe al cmdlet di New-AzADServicePrincipal per creare una nuova entità servizio Active Directory per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9790d-155">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="9790d-156">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9790d-156">PARAMETERS</span></span>

### <span data-ttu-id="9790d-157">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9790d-157">-ApplicationId</span></span>
<span data-ttu-id="9790d-158">ID applicazione univoco per un'entità servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="9790d-158">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="9790d-159">Una volta creata, questa proprietà non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="9790d-159">Once created this property cannot be changed.</span></span>
<span data-ttu-id="9790d-160">Se non si specifica un ID applicazione, ne viene generato uno.</span><span class="sxs-lookup"><span data-stu-id="9790d-160">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="9790d-161">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="9790d-161">-ApplicationObject</span></span>
<span data-ttu-id="9790d-162">Oggetto che rappresenta l'applicazione per cui viene creata l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-162">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9790d-163">-CertValue</span><span class="sxs-lookup"><span data-stu-id="9790d-163">-CertValue</span></span>
<span data-ttu-id="9790d-164">Valore del tipo di credenziali "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="9790d-164">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="9790d-165">Rappresenta il certificato codificato base 64.</span><span class="sxs-lookup"><span data-stu-id="9790d-165">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="9790d-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9790d-166">-DefaultProfile</span></span>
<span data-ttu-id="9790d-167">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9790d-167">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9790d-168">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="9790d-168">-DisplayName</span></span>
<span data-ttu-id="9790d-169">Nome descrittivo dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-169">The friendly name of the service principal.</span></span> <span data-ttu-id="9790d-170">Se non viene fornito un nome visualizzato, questo valore predefinito sarà "azure-powershell-MM-dd-yyyy-HH-mm-ss", dove il suffisso è l'ora di creazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9790d-170">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="9790d-171">-EndDate</span><span class="sxs-lookup"><span data-stu-id="9790d-171">-EndDate</span></span>
<span data-ttu-id="9790d-172">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9790d-172">The effective end date of the credential usage.</span></span>
<span data-ttu-id="9790d-173">Il valore predefinito per la data di fine è a un anno dalla data odierna.</span><span class="sxs-lookup"><span data-stu-id="9790d-173">The default end date value is one year from today.</span></span> <span data-ttu-id="9790d-174">Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="9790d-174">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="9790d-175">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="9790d-175">-KeyCredential</span></span>
<span data-ttu-id="9790d-176">Raccolta delle credenziali chiave associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9790d-176">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="9790d-177">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="9790d-177">-PasswordCredential</span></span>
<span data-ttu-id="9790d-178">Raccolta delle credenziali password associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="9790d-178">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="9790d-179">-Role</span><span class="sxs-lookup"><span data-stu-id="9790d-179">-Role</span></span>
<span data-ttu-id="9790d-180">Ruolo dell'entità servizio nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="9790d-180">The role that the service principal has over the scope.</span></span> <span data-ttu-id="9790d-181">Se viene fornito un valore per, ma per questo non viene fornito alcun valore, per impostazione predefinita viene utilizzato il `Scope` `Role` ruolo `Role` "Collaboratore".</span><span class="sxs-lookup"><span data-stu-id="9790d-181">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="9790d-182">-Scope</span><span class="sxs-lookup"><span data-stu-id="9790d-182">-Scope</span></span>
<span data-ttu-id="9790d-183">Ambito per cui l'entità servizio ha le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="9790d-183">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="9790d-184">Se viene fornito un valore per, ma non per , verrà utilizzato per impostazione predefinita `Role` `Scope` la sottoscrizione `Scope` corrente.</span><span class="sxs-lookup"><span data-stu-id="9790d-184">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="9790d-185">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="9790d-185">-SkipAssignment</span></span>
<span data-ttu-id="9790d-186">Se è impostata, non verrà creata l'assegnazione di ruolo predefinita per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="9790d-186">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="9790d-187">-StartDate</span><span class="sxs-lookup"><span data-stu-id="9790d-187">-StartDate</span></span>
<span data-ttu-id="9790d-188">Data di inizio effettivo dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="9790d-188">The effective start date of the credential usage.</span></span>
<span data-ttu-id="9790d-189">Il valore predefinito per la data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="9790d-189">The default start date value is today.</span></span> <span data-ttu-id="9790d-190">Per le credenziali di tipo "asimmetrico", questa deve essere impostata su o dopo la data da cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="9790d-190">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="9790d-191">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9790d-191">-Confirm</span></span>
<span data-ttu-id="9790d-192">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9790d-192">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9790d-193">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9790d-193">-WhatIf</span></span>
<span data-ttu-id="9790d-194">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9790d-194">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9790d-195">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9790d-195">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9790d-196">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9790d-196">CommonParameters</span></span>
<span data-ttu-id="9790d-197">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9790d-197">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9790d-198">Per altre informazioni, vedere about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9790d-198">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9790d-199">INPUT</span><span class="sxs-lookup"><span data-stu-id="9790d-199">INPUTS</span></span>

### <span data-ttu-id="9790d-200">System.Guid</span><span class="sxs-lookup"><span data-stu-id="9790d-200">System.Guid</span></span>

### <span data-ttu-id="9790d-201">System.String</span><span class="sxs-lookup"><span data-stu-id="9790d-201">System.String</span></span>

### <span data-ttu-id="9790d-202">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="9790d-202">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="9790d-203">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="9790d-203">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="9790d-204">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="9790d-204">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="9790d-205">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="9790d-205">System.DateTime</span></span>

## <span data-ttu-id="9790d-206">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9790d-206">OUTPUTS</span></span>

### <span data-ttu-id="9790d-207">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9790d-207">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="9790d-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="9790d-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="9790d-209">NOTE</span><span class="sxs-lookup"><span data-stu-id="9790d-209">NOTES</span></span>
<span data-ttu-id="9790d-210">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="9790d-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="9790d-211">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9790d-211">RELATED LINKS</span></span>

[<span data-ttu-id="9790d-212">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9790d-212">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="9790d-213">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="9790d-213">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="9790d-214">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9790d-214">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="9790d-215">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="9790d-215">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="9790d-216">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9790d-216">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="9790d-217">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9790d-217">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="9790d-218">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="9790d-218">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

