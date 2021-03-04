---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: f826ecbde81bc301cc51e031b2047bc7a9f284e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988929"
---
# <span data-ttu-id="c407d-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c407d-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="c407d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c407d-102">SYNOPSIS</span></span>
<span data-ttu-id="c407d-103">Crea una nuova entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c407d-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="c407d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c407d-104">SYNTAX</span></span>

### <span data-ttu-id="c407d-105">SimpleParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="c407d-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c407d-107">ApplicationWithPasswordPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-109">ApplicationWithKeyPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c407d-112">DisplayNameWithPasswordPparameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-114">DisplayNameWithKeyPparameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-116">ApplicationObjectWithPasswordPparameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-118">ApplicationObjectWithKeyPparamParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c407d-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="c407d-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c407d-120">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c407d-120">DESCRIPTION</span></span>

<span data-ttu-id="c407d-121">Crea una nuova entità servizio Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="c407d-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="c407d-122">Se non vengono forniti, il set di parametri predefinito usa i valori predefiniti per i parametri.</span><span class="sxs-lookup"><span data-stu-id="c407d-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="c407d-123">Per altre informazioni sui valori predefiniti, vedere la descrizione di ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="c407d-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="c407d-124">Questo cmdlet consente di assegnare un ruolo all'entità servizio con i **parametri Role** **e Scope.**</span><span class="sxs-lookup"><span data-stu-id="c407d-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="c407d-125">Se entrambi vengono omessi, il ruolo di collaboratore viene assegnato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="c407d-126">I valori predefiniti per i **parametri Ruolo** **e** Ambito **sono Collaboratore** per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c407d-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="c407d-127">Il cmdlet crea un'applicazione e imposta le relative proprietà se non viene fornito un valore ApplicationId.</span><span class="sxs-lookup"><span data-stu-id="c407d-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="c407d-128">Per aggiornare i parametri specifici dell'applicazione, usare il cmdlet [Update-AzADApplication.](./update-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="c407d-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="c407d-129">Quando si crea un'entità servizio con il comando **New-AzADServicePrincipal,** l'output include le credenziali che è necessario proteggere.</span><span class="sxs-lookup"><span data-stu-id="c407d-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="c407d-130">In alternativa, è consigliabile usare le identità [gestite](/azure/active-directory/managed-identities-azure-resources/overview) per evitare l'uso delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c407d-130">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="c407d-131">Per impostazione predefinita, **New-AzADServicePrincipal** assegna il ruolo [Collaboratore](/azure/role-based-access-control/built-in-roles#contributor) all'entità servizio nell'ambito della sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c407d-131">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="c407d-132">Per ridurre il rischio di un'entità servizio compromessa, assegnare un ruolo più specifico e restringere l'ambito a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c407d-132">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="c407d-133">Per [altre informazioni, vedere La procedura per aggiungere un'assegnazione](/azure/role-based-access-control/role-assignments-steps) di ruolo.</span><span class="sxs-lookup"><span data-stu-id="c407d-133">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="c407d-134">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c407d-134">EXAMPLES</span></span>

### <span data-ttu-id="c407d-135">Esempio 1: Creazione di entità servizio Active Directory semplice</span><span class="sxs-lookup"><span data-stu-id="c407d-135">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="c407d-136">L'esempio seguente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="c407d-136">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="c407d-137">Poiché non viene fornito un ID applicazione, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-137">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="c407d-138">Poiché non vengono forniti valori per **Ruolo** **o** Ambito, all'entità servizio creata viene assegnato il ruolo di **collaboratore** per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c407d-138">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="c407d-139">Esempio 2: Creazione di un'entità servizio Active Directory semplice con un ruolo specificato e un ambito predefinito</span><span class="sxs-lookup"><span data-stu-id="c407d-139">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="c407d-140">L'esempio seguente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="c407d-140">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="c407d-141">Poiché l'ID applicazione non viene fornito, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-141">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="c407d-142">L'entità servizio viene creata con **autorizzazioni di** lettura per la sottoscrizione corrente perché non viene fornito alcun valore per il **parametro Scope.**</span><span class="sxs-lookup"><span data-stu-id="c407d-142">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000' to the new service principal.
```

### <span data-ttu-id="c407d-143">Esempio 3: Creazione semplice di un'entità servizio Active Directory con un ambito e un ruolo predefiniti specificati</span><span class="sxs-lookup"><span data-stu-id="c407d-143">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="c407d-144">L'esempio seguente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="c407d-144">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="c407d-145">Poiché l'ID applicazione non viene fornito, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-145">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="c407d-146">L'entità servizio viene creata con **autorizzazioni di collaboratore** per l'ambito del gruppo di risorse fornito perché non viene fornito alcun valore per il **parametro** Role.</span><span class="sxs-lookup"><span data-stu-id="c407d-146">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

```powershell
New-AzADServicePrincipal -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="c407d-147">Esempio 4: Creazione semplice di un'entità servizio Active Directory con un ambito e un ruolo specificati</span><span class="sxs-lookup"><span data-stu-id="c407d-147">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="c407d-148">L'esempio seguente crea un'entità servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="c407d-148">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="c407d-149">Poiché l'ID applicazione non viene fornito, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-149">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="c407d-150">L'entità servizio viene creata con autorizzazioni **di lettura** per l'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="c407d-150">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

```powershell
New-AzADServicePrincipal -Role Reader -Scope /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup
```

```Output
Secret                : System.Security.SecureString
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup' to the new service principal.
```

### <span data-ttu-id="c407d-151">Esempio 5: Creare una nuova entità servizio Active Directory usando l'ID applicazione con l'assegnazione di ruoli</span><span class="sxs-lookup"><span data-stu-id="c407d-151">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="c407d-152">L'esempio seguente crea una nuova entità servizio Active Directory per l'applicazione con ID applicazione '00000000-0000-0000-0000000000000''.</span><span class="sxs-lookup"><span data-stu-id="c407d-152">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="c407d-153">Poiché non vengono forniti valori per **Ruolo** **o** Ambito, all'entità servizio creata viene assegnato il ruolo di **collaboratore** per la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c407d-153">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

```powershell
New-AzADServicePrincipal -ApplicationId 00000000-0000-0000-0000-000000000000
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://my-temp-app}
ApplicationId         : 00000000-0000-0000-0000-000000000000
DisplayName           : my-temp-app
Id                    : 00000000-0000-0000-0000-000000000000
Type                  : ServicePrincipal
```

### <span data-ttu-id="c407d-154">Esempio 6: Creare una nuova entità servizio Active Directory tramite piping</span><span class="sxs-lookup"><span data-stu-id="c407d-154">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="c407d-155">L'esempio seguente recupera l'applicazione con ID oggetto '3ede3c26-b443-4e0b-9efc-b05e68338dc3' usando il cmdlet [Get-AzADApplication.](./get-azadapplication.md)</span><span class="sxs-lookup"><span data-stu-id="c407d-155">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="c407d-156">I risultati vengono reindirizzati al cmdlet per creare una nuova entità `New-AzADServicePrincipal` servizio Active Directory per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c407d-156">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="c407d-157">Esempio 7: Creare una nuova entità servizio Active Directory usando DisplayName e le credenziali della password</span><span class="sxs-lookup"><span data-stu-id="c407d-157">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="c407d-158">L'esempio seguente crea una nuova applicazione con il nome **ServicePrincipalName** e la password **StrongPassworld!23.**</span><span class="sxs-lookup"><span data-stu-id="c407d-158">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="c407d-159">Crea l'entità servizio in base all'applicazione creata.</span><span class="sxs-lookup"><span data-stu-id="c407d-159">It creates the service principal based on the created application.</span></span> <span data-ttu-id="c407d-160">La data di inizio e la data di fine vengono aggiunte alle credenziali della password.</span><span class="sxs-lookup"><span data-stu-id="c407d-160">The start date and end date are added to the password credential.</span></span>

```powershell
$credentials = New-Object -TypeName Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential -Property @{
  StartDate=Get-Date; EndDate=Get-Date -Year 2024; Password='StrongPassworld!23'}
$sp = New-AzAdServicePrincipal -DisplayName ServicePrincipalName -PasswordCredential $credentials
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000c
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

### <span data-ttu-id="c407d-161">Esempio 8: Creare una nuova entità servizio Active Directory usando DisplayName e le credenziali della chiave normale</span><span class="sxs-lookup"><span data-stu-id="c407d-161">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="c407d-162">L'esempio seguente crea una nuova applicazione con il nome **ServicePrincipalName** e un certificato **$cert.** L'entità servizio viene creata in base all'applicazione creata.</span><span class="sxs-lookup"><span data-stu-id="c407d-162">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="c407d-163">La data di fine viene aggiunta alle credenziali della chiave.</span><span class="sxs-lookup"><span data-stu-id="c407d-163">The end date is added to key credential.</span></span>

```powershell
$cert = 'public certificate as Base64 encoded string'
$sp = New-AzADServicePrincipal -DisplayName ServicePrincipalName -CertValue $cert  -EndDate '2021-01-01'
```

```Output
ServicePrincipalNames : {00000000-0000-0000-0000-000000000000, http://ServicePrincipalName}
ApplicationId         : 00000000-0000-0000-0000-000000000000
ObjectType            : ServicePrincipal
DisplayName           : ServicePrincipalName
Id                    : 00000000-0000-0000-0000-000000000000
Type                  :
```

## <span data-ttu-id="c407d-164">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c407d-164">PARAMETERS</span></span>

### <span data-ttu-id="c407d-165">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c407d-165">-ApplicationId</span></span>

<span data-ttu-id="c407d-166">ID applicazione univoco per un'entità servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="c407d-166">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="c407d-167">Una volta creata, questa proprietà non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="c407d-167">Once created this property cannot be changed.</span></span> <span data-ttu-id="c407d-168">Se non si specifica un ID applicazione per un'applicazione esistente, viene creata un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c407d-168">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="c407d-169">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="c407d-169">-ApplicationObject</span></span>

<span data-ttu-id="c407d-170">Oggetto che rappresenta l'applicazione per cui viene creata l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-170">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="c407d-171">-CertValue</span><span class="sxs-lookup"><span data-stu-id="c407d-171">-CertValue</span></span>

<span data-ttu-id="c407d-172">Valore del tipo di credenziali asimmetriche.</span><span class="sxs-lookup"><span data-stu-id="c407d-172">The value of the asymmetric credential type.</span></span> <span data-ttu-id="c407d-173">Rappresenta il certificato codificato Base64.</span><span class="sxs-lookup"><span data-stu-id="c407d-173">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="c407d-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c407d-174">-DefaultProfile</span></span>

<span data-ttu-id="c407d-175">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c407d-175">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c407d-176">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c407d-176">-DisplayName</span></span>

<span data-ttu-id="c407d-177">Nome descrittivo dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-177">The friendly name of the service principal.</span></span> <span data-ttu-id="c407d-178">Se non viene fornito un nome visualizzato, questo valore predefinito sarà **azure-powershell-MM-gg-aaaa-HH-mm-ss,** dove il suffisso è l'ora di creazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c407d-178">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="c407d-179">-EndDate</span><span class="sxs-lookup"><span data-stu-id="c407d-179">-EndDate</span></span>

<span data-ttu-id="c407d-180">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c407d-180">The effective end date of the credential usage.</span></span> <span data-ttu-id="c407d-181">Il valore predefinito per la data di fine è a un anno dalla data odierna.</span><span class="sxs-lookup"><span data-stu-id="c407d-181">The default end date value is one year from today.</span></span>
<span data-ttu-id="c407d-182">Per le credenziali di un tipo asimmetrico, questa deve essere impostata su o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="c407d-182">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="c407d-183">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="c407d-183">-KeyCredential</span></span>

<span data-ttu-id="c407d-184">Raccolta delle credenziali chiave associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c407d-184">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="c407d-185">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="c407d-185">-PasswordCredential</span></span>

<span data-ttu-id="c407d-186">Raccolta delle credenziali password associate all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c407d-186">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="c407d-187">-Role</span><span class="sxs-lookup"><span data-stu-id="c407d-187">-Role</span></span>

<span data-ttu-id="c407d-188">Ruolo dell'entità servizio nell'ambito.</span><span class="sxs-lookup"><span data-stu-id="c407d-188">The role that the service principal has over the scope.</span></span> <span data-ttu-id="c407d-189">Se non viene fornito alcun valore, **per impostazione** predefinita viene utilizzato il **ruolo Collaboratore.**</span><span class="sxs-lookup"><span data-stu-id="c407d-189">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="c407d-190">-Scope</span><span class="sxs-lookup"><span data-stu-id="c407d-190">-Scope</span></span>

<span data-ttu-id="c407d-191">Ambito per cui l'entità servizio ha le autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="c407d-191">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="c407d-192">Se non viene fornito alcun valore, **per impostazione** predefinita l'ambito viene impostato sulla sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="c407d-192">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="c407d-193">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="c407d-193">-SkipAssignment</span></span>

<span data-ttu-id="c407d-194">Se impostato, ignorare la creazione dell'assegnazione di ruolo predefinita per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="c407d-194">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="c407d-195">-StartDate</span><span class="sxs-lookup"><span data-stu-id="c407d-195">-StartDate</span></span>

<span data-ttu-id="c407d-196">Data di inizio effettivo dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="c407d-196">The effective start date of the credential usage.</span></span> <span data-ttu-id="c407d-197">Il valore predefinito per la data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="c407d-197">The default start date value is today.</span></span> <span data-ttu-id="c407d-198">Per le credenziali di tipo asimmetrico, queste devono essere impostate su o dopo la data da cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="c407d-198">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="c407d-199">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c407d-199">-Confirm</span></span>

<span data-ttu-id="c407d-200">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c407d-200">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c407d-201">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c407d-201">-WhatIf</span></span>

<span data-ttu-id="c407d-202">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c407d-202">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c407d-203">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c407d-203">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c407d-204">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c407d-204">CommonParameters</span></span>
<span data-ttu-id="c407d-205">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c407d-205">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c407d-206">Per altre informazioni, [vedere](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c407d-206">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="c407d-207">INPUT</span><span class="sxs-lookup"><span data-stu-id="c407d-207">INPUTS</span></span>

### <span data-ttu-id="c407d-208">System.Guid</span><span class="sxs-lookup"><span data-stu-id="c407d-208">System.Guid</span></span>

### <span data-ttu-id="c407d-209">System.String</span><span class="sxs-lookup"><span data-stu-id="c407d-209">System.String</span></span>

### <span data-ttu-id="c407d-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="c407d-210">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="c407d-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="c407d-211">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="c407d-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="c407d-212">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="c407d-213">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="c407d-213">System.DateTime</span></span>

## <span data-ttu-id="c407d-214">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c407d-214">OUTPUTS</span></span>

### <span data-ttu-id="c407d-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c407d-215">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="c407d-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="c407d-216">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="c407d-217">NOTE</span><span class="sxs-lookup"><span data-stu-id="c407d-217">NOTES</span></span>

<span data-ttu-id="c407d-218">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, risorsa, gruppo, modello, distribuzione</span><span class="sxs-lookup"><span data-stu-id="c407d-218">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="c407d-219">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c407d-219">RELATED LINKS</span></span>

[<span data-ttu-id="c407d-220">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c407d-220">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="c407d-221">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="c407d-221">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="c407d-222">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c407d-222">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="c407d-223">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="c407d-223">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="c407d-224">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c407d-224">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="c407d-225">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c407d-225">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="c407d-226">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="c407d-226">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)