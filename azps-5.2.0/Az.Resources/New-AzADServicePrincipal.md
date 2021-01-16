---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADServicePrincipal.md
ms.openlocfilehash: 6d268c2378c93bcfb98e64c654880e8055bcede8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358060"
---
# <span data-ttu-id="0e363-101">New-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0e363-101">New-AzADServicePrincipal</span></span>

## <span data-ttu-id="0e363-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0e363-102">SYNOPSIS</span></span>
<span data-ttu-id="0e363-103">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0e363-103">Creates a new Azure active directory service principal.</span></span>

## <span data-ttu-id="0e363-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0e363-104">SYNTAX</span></span>

### <span data-ttu-id="0e363-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0e363-105">SimpleParameterSet (Default)</span></span>

```
New-AzADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-106">ApplicationWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e363-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-107">ApplicationWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-108">ApplicationWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-109">ApplicationWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-110">ApplicationWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-111">DisplayNameWithoutCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0e363-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-112">DisplayNameWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-113">DisplayNameWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-114">DisplayNameWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-115">DisplayNameWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-116">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-116">ApplicationObjectWithPasswordPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-117">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-117">ApplicationObjectWithPasswordCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-118">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-118">ApplicationObjectWithKeyPlainParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e363-119">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="0e363-119">ApplicationObjectWithKeyCredentialParameterSet</span></span>

```
New-AzADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e363-120">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0e363-120">DESCRIPTION</span></span>

<span data-ttu-id="0e363-121">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="0e363-121">Creates a new Azure active directory service principal.</span></span> <span data-ttu-id="0e363-122">Il set di parametri predefinito usa i valori predefiniti per i parametri se non sono forniti.</span><span class="sxs-lookup"><span data-stu-id="0e363-122">The default parameter set uses default values for parameters if they are not provided.</span></span> <span data-ttu-id="0e363-123">Per altre informazioni sui valori predefiniti, vedere la descrizione di ogni parametro.</span><span class="sxs-lookup"><span data-stu-id="0e363-123">For more information on default values, see the description for each parameter.</span></span> <span data-ttu-id="0e363-124">Questo cmdlet offre la possibilità di assegnare un ruolo all'entità servizio con i parametri **Role** e **scope** .</span><span class="sxs-lookup"><span data-stu-id="0e363-124">This cmdlet has the ability to assign a role to the service principal with the **Role** and **Scope** parameters.</span></span> <span data-ttu-id="0e363-125">Se entrambi vengono omessi, il ruolo di collaboratore viene assegnato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-125">If both are omitted, the contributor role is assigned to the service principal.</span></span> <span data-ttu-id="0e363-126">I valori predefiniti per i parametri **Role** e **scope** sono **collaboratori** per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="0e363-126">The default values for the **Role** and **Scope** parameters are **Contributor** for the current subscription.</span></span> <span data-ttu-id="0e363-127">Il cmdlet crea un'applicazione e ne imposta le proprietà se non è disponibile un ApplicationId.</span><span class="sxs-lookup"><span data-stu-id="0e363-127">The cmdlet creates an application and sets its properties if an ApplicationId is not provided.</span></span> <span data-ttu-id="0e363-128">Per aggiornare i parametri specifici dell'applicazione, usare il cmdlet [Update-AzADApplication](./update-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="0e363-128">To update the application-specific parameters, use the [Update-AzADApplication](./update-azadapplication.md) cmdlet.</span></span>

> [!WARNING]
> <span data-ttu-id="0e363-129">Quando si crea un'entità di servizio usando il comando **New-AzADServicePrincipal** , l'output include le credenziali che è necessario proteggere.</span><span class="sxs-lookup"><span data-stu-id="0e363-129">When you create a service principal using the **New-AzADServicePrincipal** command, the output includes credentials that you must protect.</span></span> <span data-ttu-id="0e363-130">Assicurati di non includere queste credenziali nel codice o di controllare le credenziali nel controllo di origine.</span><span class="sxs-lookup"><span data-stu-id="0e363-130">Be sure that you do not include these credentials in your code or check the credentials into your source control.</span></span> <span data-ttu-id="0e363-131">In alternativa, è consigliabile usare le [identità gestite](/azure/active-directory/managed-identities-azure-resources/overview) per evitare la necessità di usare le credenziali.</span><span class="sxs-lookup"><span data-stu-id="0e363-131">As an alternative, consider using [managed identities](/azure/active-directory/managed-identities-azure-resources/overview) to avoid the need to use credentials.</span></span>
>
> <span data-ttu-id="0e363-132">Per impostazione predefinita, **New-AzADServicePrincipal** assegna il ruolo di [collaboratore](/azure/role-based-access-control/built-in-roles#contributor) all'entità del servizio nell'ambito dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0e363-132">By default, **New-AzADServicePrincipal** assigns the [Contributor](/azure/role-based-access-control/built-in-roles#contributor) role to the service principal at the subscription scope.</span></span> <span data-ttu-id="0e363-133">Per ridurre il rischio di un'entità di servizio compromessa, assegnare un ruolo più specifico e limitare l'ambito a una risorsa o a un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0e363-133">To reduce your risk of a compromised service principal, assign a more specific role and narrow the scope to a resource or resource group.</span></span> <span data-ttu-id="0e363-134">Per altre informazioni, vedere [procedura per aggiungere un'assegnazione di ruolo](/azure/role-based-access-control/role-assignments-steps) .</span><span class="sxs-lookup"><span data-stu-id="0e363-134">See [Steps to add a role assignment](/azure/role-based-access-control/role-assignments-steps) for more information.</span></span>

## <span data-ttu-id="0e363-135">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0e363-135">EXAMPLES</span></span>

### <span data-ttu-id="0e363-136">Esempio 1: creazione dell'entità servizio di annunci semplici</span><span class="sxs-lookup"><span data-stu-id="0e363-136">Example 1: Simple AD service principal creation</span></span>

<span data-ttu-id="0e363-137">L'esempio seguente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="0e363-137">The following example creates an AD service principal using default values for parameters not specified.</span></span> <span data-ttu-id="0e363-138">Dato che non è disponibile un ID applicazione, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-138">Since an application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="0e363-139">Poiché nessun valore viene fornito per **ruolo** o **ambito**, all'entità servizio creato viene assegnato il ruolo di **collaboratore** per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="0e363-139">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="0e363-140">Esempio 2: creazione dell'entità del servizio Active Directory con un ruolo specificato e un ambito predefinito</span><span class="sxs-lookup"><span data-stu-id="0e363-140">Example 2: Simple AD service principal creation with a specified role and default scope</span></span>

<span data-ttu-id="0e363-141">L'esempio seguente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="0e363-141">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="0e363-142">Dato che l'ID applicazione non è disponibile, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-142">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="0e363-143">L'entità servizio viene creata con le autorizzazioni di **lettura** per l'abbonamento corrente perché non viene specificato alcun valore per il parametro **scope** .</span><span class="sxs-lookup"><span data-stu-id="0e363-143">The service principal is created with **Reader** permissions for the current subscription since no value is provided for the **Scope** parameter.</span></span>

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

### <span data-ttu-id="0e363-144">Esempio 3: creazione semplificata dell'entità servizio Active Directory con un ambito specificato e un ruolo predefinito</span><span class="sxs-lookup"><span data-stu-id="0e363-144">Example 3: Simple AD service principal creation with a specified scope and default role</span></span>

<span data-ttu-id="0e363-145">L'esempio seguente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="0e363-145">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="0e363-146">Dato che l'ID applicazione non è disponibile, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-146">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="0e363-147">L'entità servizio viene creata con le autorizzazioni per il **collaboratore** per l'ambito del gruppo di risorse specificato, poiché non viene specificato alcun valore per il parametro **Role** .</span><span class="sxs-lookup"><span data-stu-id="0e363-147">The service principal is created with **Contributor** permissions for the provided resource group scope since no value is provided for the **Role** parameter.</span></span>

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

### <span data-ttu-id="0e363-148">Esempio 4: creazione dell'entità del servizio Active Directory con un ambito e un ruolo specificati</span><span class="sxs-lookup"><span data-stu-id="0e363-148">Example 4: Simple AD service principal creation with a specified scope and role</span></span>

<span data-ttu-id="0e363-149">L'esempio seguente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non specificati.</span><span class="sxs-lookup"><span data-stu-id="0e363-149">The following example creates an AD service principal using the default values for parameters not specified.</span></span> <span data-ttu-id="0e363-150">Dato che l'ID applicazione non è disponibile, viene creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-150">Since the application ID is not provided, an application is created for the service principal.</span></span> <span data-ttu-id="0e363-151">L'entità servizio viene creata con le autorizzazioni di **lettura** per l'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="0e363-151">The service principal is created with **Reader** permissions for the provided resource group scope.</span></span>

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

### <span data-ttu-id="0e363-152">Esempio 5: creare una nuova entità del servizio Active Directory usando l'ID applicazione con l'assegnazione di ruolo</span><span class="sxs-lookup"><span data-stu-id="0e363-152">Example 5: Create a new AD service principal using application ID with role assignment</span></span>

<span data-ttu-id="0e363-153">Nell'esempio seguente viene creata una nuova entità del servizio Active Directory per l'applicazione con l'ID applicazione "00000000-0000-0000-0000-000000000000".</span><span class="sxs-lookup"><span data-stu-id="0e363-153">The following example creates a new AD service principal for the application with application ID '00000000-0000-0000-0000-000000000000'.</span></span> <span data-ttu-id="0e363-154">Poiché nessun valore viene fornito per **ruolo** o **ambito**, all'entità servizio creato viene assegnato il ruolo di **collaboratore** per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="0e363-154">Since no values are provided for **Role** or **Scope**, the created service principal is assigned the **contributor** role for the current subscription.</span></span>

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

### <span data-ttu-id="0e363-155">Esempio 6: creare una nuova entità del servizio PUBBLICITARIo usando piping</span><span class="sxs-lookup"><span data-stu-id="0e363-155">Example 6: Create a new AD service principal using piping</span></span>

<span data-ttu-id="0e363-156">L'esempio seguente recupera l'applicazione con l'ID oggetto "3ede3c26-B443-4e0b-9efc-b05e68338dc3" usando il cmdlet [Get-AzADApplication](./get-azadapplication.md) .</span><span class="sxs-lookup"><span data-stu-id="0e363-156">The following example retrieves the application with object ID '3ede3c26-b443-4e0b-9efc-b05e68338dc3' using the [Get-AzADApplication](./get-azadapplication.md) cmdlet.</span></span> <span data-ttu-id="0e363-157">I risultati vengono inviati tramite pipe al `New-AzADServicePrincipal` cmdlet per creare una nuova entità del servizio Active Directory per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e363-157">The results are piped to the `New-AzADServicePrincipal` cmdlet to create a new AD service principal for that application.</span></span>

```powershell
Get-AzADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzADServicePrincipal
```

### <span data-ttu-id="0e363-158">Esempio 7: creare una nuova entità del servizio Active Directory usando le credenziali DisplayName e password</span><span class="sxs-lookup"><span data-stu-id="0e363-158">Example 7: Create a new AD service principal using DisplayName and password credential</span></span>

<span data-ttu-id="0e363-159">L'esempio seguente crea una nuova applicazione con il nome **servicePrincipalName** e una password di **StrongPassworld! 23**.</span><span class="sxs-lookup"><span data-stu-id="0e363-159">The following example creates a new application with the name **ServicePrincipalName** and a password of **StrongPassworld!23**.</span></span> <span data-ttu-id="0e363-160">Crea l'entità servizio in base all'applicazione creata.</span><span class="sxs-lookup"><span data-stu-id="0e363-160">It creates the service principal based on the created application.</span></span> <span data-ttu-id="0e363-161">La data di inizio e di fine viene aggiunta alla credenziale password.</span><span class="sxs-lookup"><span data-stu-id="0e363-161">The start date and end date are added to the password credential.</span></span>

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

### <span data-ttu-id="0e363-162">Esempio 8: creare una nuova entità del servizio Active Directory usando DisplayName e le credenziali con chiave normale</span><span class="sxs-lookup"><span data-stu-id="0e363-162">Example 8: Create a new AD service principal using DisplayName and plain key credential</span></span>

<span data-ttu-id="0e363-163">Nell'esempio seguente viene creata una nuova applicazione con il nome **servicePrincipalName** e un certificato **$CERT**. Crea l'entità servizio in base all'applicazione creata.</span><span class="sxs-lookup"><span data-stu-id="0e363-163">The following example creates a new application with the name **ServicePrincipalName** and a certificate **$cert**. It creates the service principal based on the application created.</span></span> <span data-ttu-id="0e363-164">La data di fine viene aggiunta alle credenziali chiave.</span><span class="sxs-lookup"><span data-stu-id="0e363-164">The end date is added to key credential.</span></span>

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

## <span data-ttu-id="0e363-165">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0e363-165">PARAMETERS</span></span>

### <span data-ttu-id="0e363-166">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="0e363-166">-ApplicationId</span></span>

<span data-ttu-id="0e363-167">ID applicazione univoco per un'entità di servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="0e363-167">The unique application ID for a service principal in a tenant.</span></span> <span data-ttu-id="0e363-168">Una volta creata questa proprietà non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="0e363-168">Once created this property cannot be changed.</span></span> <span data-ttu-id="0e363-169">Se non viene specificato un ID applicazione per un'applicazione esistente, viene creata un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e363-169">If an application ID for an existing application is not specified, an application is created.</span></span>

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

### <span data-ttu-id="0e363-170">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="0e363-170">-ApplicationObject</span></span>

<span data-ttu-id="0e363-171">Oggetto che rappresenta l'applicazione per cui viene creata l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-171">The object representing the application for which the service principal is created.</span></span>

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

### <span data-ttu-id="0e363-172">-CertValue</span><span class="sxs-lookup"><span data-stu-id="0e363-172">-CertValue</span></span>

<span data-ttu-id="0e363-173">Il valore del tipo di credenziale asimmetrica.</span><span class="sxs-lookup"><span data-stu-id="0e363-173">The value of the asymmetric credential type.</span></span> <span data-ttu-id="0e363-174">Rappresenta il certificato codificato Base64.</span><span class="sxs-lookup"><span data-stu-id="0e363-174">It represents the Base64 encoded certificate.</span></span>

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

### <span data-ttu-id="0e363-175">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e363-175">-DefaultProfile</span></span>

<span data-ttu-id="0e363-176">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0e363-176">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0e363-177">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0e363-177">-DisplayName</span></span>

<span data-ttu-id="0e363-178">Nome descrittivo dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-178">The friendly name of the service principal.</span></span> <span data-ttu-id="0e363-179">Se non viene specificato un nome visualizzato, il valore predefinito sarà **Azure-PowerShell-mm-DD-aaaa-hh-mm-SS** , dove il suffisso è il momento della creazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e363-179">If a display name is not provided, this value will default to **azure-powershell-MM-dd-yyyy-HH-mm-ss** where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="0e363-180">-EndDate</span><span class="sxs-lookup"><span data-stu-id="0e363-180">-EndDate</span></span>

<span data-ttu-id="0e363-181">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="0e363-181">The effective end date of the credential usage.</span></span> <span data-ttu-id="0e363-182">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="0e363-182">The default end date value is one year from today.</span></span>
<span data-ttu-id="0e363-183">Per le credenziali di tipo asimmetrico, deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="0e363-183">For an asymmetric type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="0e363-184">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="0e363-184">-KeyCredential</span></span>

<span data-ttu-id="0e363-185">Raccolta di credenziali chiave associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e363-185">The collection of key credentials associated with the application.</span></span>

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

### <span data-ttu-id="0e363-186">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="0e363-186">-PasswordCredential</span></span>

<span data-ttu-id="0e363-187">Raccolta di credenziali password associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="0e363-187">The collection of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="0e363-188">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="0e363-188">-Role</span></span>

<span data-ttu-id="0e363-189">Il ruolo che l'entità servizio ha sull'ambito.</span><span class="sxs-lookup"><span data-stu-id="0e363-189">The role that the service principal has over the scope.</span></span> <span data-ttu-id="0e363-190">Se non viene specificato alcun valore **, il ruolo predefinito** per il ruolo **collaboratore** .</span><span class="sxs-lookup"><span data-stu-id="0e363-190">If no value is provided, **Role** defaults to the **Contributor** role.</span></span>

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

### <span data-ttu-id="0e363-191">-Ambito</span><span class="sxs-lookup"><span data-stu-id="0e363-191">-Scope</span></span>

<span data-ttu-id="0e363-192">Ambito per cui l'entità del servizio dispone delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="0e363-192">The scope that the service principal has permissions for.</span></span> <span data-ttu-id="0e363-193">Se non viene specificato alcun valore, l' **ambito** viene impostato su default per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="0e363-193">If no value is provided, **Scope** defaults to the current subscription.</span></span>

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

### <span data-ttu-id="0e363-194">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="0e363-194">-SkipAssignment</span></span>

<span data-ttu-id="0e363-195">Se impostato, ignorare la creazione dell'assegnazione di ruolo predefinita per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="0e363-195">If set, skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="0e363-196">-StartDate</span><span class="sxs-lookup"><span data-stu-id="0e363-196">-StartDate</span></span>

<span data-ttu-id="0e363-197">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="0e363-197">The effective start date of the credential usage.</span></span> <span data-ttu-id="0e363-198">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="0e363-198">The default start date value is today.</span></span> <span data-ttu-id="0e363-199">Per le credenziali di tipo asimmetrico, deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="0e363-199">For an asymmetric type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="0e363-200">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0e363-200">-Confirm</span></span>

<span data-ttu-id="0e363-201">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e363-201">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e363-202">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e363-202">-WhatIf</span></span>

<span data-ttu-id="0e363-203">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e363-203">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0e363-204">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0e363-204">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e363-205">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e363-205">CommonParameters</span></span>
<span data-ttu-id="0e363-206">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e363-206">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e363-207">Per altre informazioni, Vedi [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span><span class="sxs-lookup"><span data-stu-id="0e363-207">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>
## <span data-ttu-id="0e363-208">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0e363-208">INPUTS</span></span>

### <span data-ttu-id="0e363-209">System. Guid</span><span class="sxs-lookup"><span data-stu-id="0e363-209">System.Guid</span></span>

### <span data-ttu-id="0e363-210">System. String</span><span class="sxs-lookup"><span data-stu-id="0e363-210">System.String</span></span>

### <span data-ttu-id="0e363-211">Microsoft. Azure. Commands. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="0e363-211">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="0e363-212">Microsoft. Azure. Commands. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="0e363-212">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="0e363-213">Microsoft. Azure. Commands. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="0e363-213">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="0e363-214">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="0e363-214">System.DateTime</span></span>

## <span data-ttu-id="0e363-215">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0e363-215">OUTPUTS</span></span>

### <span data-ttu-id="0e363-216">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0e363-216">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="0e363-217">Microsoft. Azure. Commands. resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="0e363-217">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="0e363-218">Note</span><span class="sxs-lookup"><span data-stu-id="0e363-218">NOTES</span></span>

<span data-ttu-id="0e363-219">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="0e363-219">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="0e363-220">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0e363-220">RELATED LINKS</span></span>

[<span data-ttu-id="0e363-221">Remove-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0e363-221">Remove-AzADServicePrincipal</span></span>](./Remove-AzADServicePrincipal.md)

[<span data-ttu-id="0e363-222">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="0e363-222">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)

[<span data-ttu-id="0e363-223">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0e363-223">New-AzADApplication</span></span>](./New-AzADApplication.md)

[<span data-ttu-id="0e363-224">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="0e363-224">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="0e363-225">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0e363-225">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="0e363-226">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0e363-226">New-AzADSpCredential</span></span>](./New-AzADSpCredential.md)

[<span data-ttu-id="0e363-227">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="0e363-227">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)