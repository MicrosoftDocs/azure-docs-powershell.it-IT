---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadserviceprincipal
schema: 2.0.0
ms.openlocfilehash: 9d0fb4f188b3753e22258a27cf8632d85fe866dc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866829"
---
# <span data-ttu-id="5f131-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5f131-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="5f131-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f131-102">SYNOPSIS</span></span>
<span data-ttu-id="5f131-103">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5f131-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f131-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f131-104">SYNTAX</span></span>

### <span data-ttu-id="5f131-105">SimpleParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5f131-105">SimpleParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal [-ApplicationId <Guid>] [-DisplayName <String>] [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-Scope <String>] [-Role <String>] [-SkipAssignment]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-106">ApplicationWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-106">ApplicationWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-107">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-107">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-108">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-108">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-109">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-109">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-110">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-110">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-111">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-111">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-112">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-112">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-113">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-113">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredential <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-114">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-114">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-115">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-115">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-116">ApplicationObjectWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-116">ApplicationObjectWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-117">ApplicationObjectWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-117">ApplicationObjectWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f131-118">ApplicationObjectWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-118">ApplicationObjectWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication>
 -PasswordCredential <PSADPasswordCredential[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5f131-119">ApplicationObjectWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-119">ApplicationObjectWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f131-120">ApplicationObjectWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="5f131-120">ApplicationObjectWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationObject <PSADApplication> -KeyCredential <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f131-121">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f131-121">DESCRIPTION</span></span>
<span data-ttu-id="5f131-122">Crea una nuova entità servizio di Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5f131-122">Creates a new azure active directory service principal.</span></span> <span data-ttu-id="5f131-123">Il set di parametri predefinito usa i valori predefiniti per i parametri se l'utente non ne offre uno.</span><span class="sxs-lookup"><span data-stu-id="5f131-123">The default parameter set uses default values for parameters if the user does not provide one for them.</span></span> <span data-ttu-id="5f131-124">Per altre informazioni sui valori predefiniti usati, vedere la descrizione per i parametri specificati di seguito.</span><span class="sxs-lookup"><span data-stu-id="5f131-124">For more information on the default values used, please see the description for the given parameters below.</span></span>
<span data-ttu-id="5f131-125">Questo cmdlet offre la possibilità di assegnare un ruolo all'entità servizio con i `Role` parametri e, `Scope` se nessuno di questi parametri viene fornito, nessun ruolo verrà assegnato all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-125">This cmdlet has the ability to assign a role to the service principal with the `Role` and `Scope` parameters; if neither of these parameters are provided, no role will be assigned to the service principal.</span></span> <span data-ttu-id="5f131-126">I valori predefiniti per i `Role` `Scope` parametri e sono rispettivamente "collaboratore" e l'abbonamento corrente ( _Nota_ : le impostazioni predefinite vengono usate solo quando l'utente fornisce un valore per uno dei due parametri, ma non per l'altro).</span><span class="sxs-lookup"><span data-stu-id="5f131-126">The default values for the `Role` and `Scope` parameters are "Contributor" and the current subscription, respectively ( _note_ : the defaults are only used when the user provides a value for one of the two parameters, but not the other).</span></span>
<span data-ttu-id="5f131-127">Il cmdlet crea inoltre in modo implicito un'applicazione e ne imposta le proprietà (se ApplicationId non è disponibile).</span><span class="sxs-lookup"><span data-stu-id="5f131-127">The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span> <span data-ttu-id="5f131-128">Per aggiornare i parametri specifici dell'applicazione, usare Set-AzureRmADApplication cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f131-128">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="5f131-129">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f131-129">EXAMPLES</span></span>

### <span data-ttu-id="5f131-130">Esempio 1-creazione di un servizio di Active Directory semplice</span><span class="sxs-lookup"><span data-stu-id="5f131-130">Example 1 - Simple AD service principal creation</span></span>

```
PS C:\> New-AzureRmADServicePrincipal

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="5f131-131">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="5f131-131">The above command creates an AD service principal using default values for parameters not provided.</span></span> <span data-ttu-id="5f131-132">Dato che non è stato fornito un ID applicazione, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-132">Since an application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5f131-133">Dato che non sono stati forniti valori `Role` o `Scope` , l'entità servizio creata non ha le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="5f131-133">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="5f131-134">Esempio 2-Creazione di un servizio di Active Directory semplice con un ruolo specificato e un ambito predefinito</span><span class="sxs-lookup"><span data-stu-id="5f131-134">Example 2 - Simple AD service principal creation with a specified role and default scope</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz' to the new service principal.
```

<span data-ttu-id="5f131-135">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="5f131-135">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="5f131-136">Dato che l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-136">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5f131-137">L'entità servizio è stata creata con le autorizzazioni "Reader" per l'abbonamento corrente (dato che non è stato specificato alcun valore per il `Scope` parametro).</span><span class="sxs-lookup"><span data-stu-id="5f131-137">The service principal was created with "Reader" permissions over the current subscription (since no value was provided for the `Scope` parameter).</span></span>

### <span data-ttu-id="5f131-138">Esempio 3-creazione di un servizio di Active Directory semplice con un ambito specificato e un ruolo predefinito</span><span class="sxs-lookup"><span data-stu-id="5f131-138">Example 3 - Simple AD service principal creation with a specified scope and default role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Contributor' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="5f131-139">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="5f131-139">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="5f131-140">Dato che l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-140">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5f131-141">L'entità servizio è stata creata con le autorizzazioni "collaboratore" (poiché non è stato specificato alcun valore per il `Role` parametro) nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f131-141">The service principal was created with "Contributor" permissions (since no value was provided for the `Role` parameter) over the provided resource group scope.</span></span>

### <span data-ttu-id="5f131-142">Esempio 4-creazione di un servizio di Active Directory semplice con un ambito e un ruolo specificati</span><span class="sxs-lookup"><span data-stu-id="5f131-142">Example 4 - Simple AD service principal creation with a specified scope and role</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -Role Reader -Scope /subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup

Secret                : System.Security.SecureString
ServicePrincipalNames : {xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx, http://azure-powershell-05-22-2018-18-23-43}
ApplicationId         : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
DisplayName           : azure-powershell-05-22-2018-18-23-43
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal

WARNING: Assigning role 'Reader' over scope '/subscriptions/zzzzzzzz-zzzz-zzzz-zzzz-zzzzzzzzzzzz/resourceGroups/myResourceGroup' to the new service principal.
```

<span data-ttu-id="5f131-143">Il comando precedente crea un'entità del servizio Active Directory usando i valori predefiniti per i parametri non forniti.</span><span class="sxs-lookup"><span data-stu-id="5f131-143">The above command creates an AD service principal using the default values for parameters not provided.</span></span> <span data-ttu-id="5f131-144">Dato che l'ID applicazione non è stato fornito, è stata creata un'applicazione per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-144">Since the application id was not provided, an application was created for the service principal.</span></span> <span data-ttu-id="5f131-145">L'entità servizio è stata creata con le autorizzazioni "Reader" nell'ambito del gruppo di risorse specificato.</span><span class="sxs-lookup"><span data-stu-id="5f131-145">The service principal was created with "Reader" permissions over the provided resource group scope.</span></span>

### <span data-ttu-id="5f131-146">Esempio 5-creare una nuova entità servizio annunci usando l'ID applicazione con assegnazione ruolo</span><span class="sxs-lookup"><span data-stu-id="5f131-146">Example 5 - Create a new AD service principal using application id with role assignment</span></span>

```
PS C:\> New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e

ServicePrincipalNames : {34a28ad2-dec4-4a41-bc3b-d22ddf90000e, http://my-temp-app}
ApplicationId         : 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
DisplayName           : my-temp-app
Id                    : yyyyyyyy-yyyy-yyyy-yyyy-yyyyyyyyyyyy
Type                  : ServicePrincipal
```

<span data-ttu-id="5f131-147">Crea una nuova entità servizio annunci per l'applicazione con l'ID applicazione "34a28ad2-DEC4-4A41-bc3b-d22ddf90000e".</span><span class="sxs-lookup"><span data-stu-id="5f131-147">Creates a new AD service principal for the application with application id '34a28ad2-dec4-4a41-bc3b-d22ddf90000e'.</span></span> <span data-ttu-id="5f131-148">Dato che non sono stati forniti valori `Role` o `Scope` , l'entità servizio creata non ha le autorizzazioni necessarie.</span><span class="sxs-lookup"><span data-stu-id="5f131-148">Since no values were provided for `Role` or `Scope`, the created service principal does not have any permissions.</span></span>

### <span data-ttu-id="5f131-149">Esempio 6-creare una nuova entità del servizio PUBBLICITARIo usando piping</span><span class="sxs-lookup"><span data-stu-id="5f131-149">Example 6 - Create a new AD service principal using piping</span></span>

```
PS C:\> Get-AzureRmADApplication -ObjectId 3ede3c26-b443-4e0b-9efc-b05e68338dc3 | New-AzureRmADServicePrincipal
```

<span data-ttu-id="5f131-150">Ottiene l'applicazione con l'ID oggetto "3ede3c26-B443-4e0b-9efc-b05e68338dc3" e le pipe al cmdlet New-AzureRmADServicePrincipal per creare una nuova entità del servizio Active Directory per tale applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f131-150">Gets the application with object id '3ede3c26-b443-4e0b-9efc-b05e68338dc3' and pipes that to the New-AzureRmADServicePrincipal cmdlet to create a new AD service principal for that application.</span></span>

## <span data-ttu-id="5f131-151">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f131-151">PARAMETERS</span></span>

### <span data-ttu-id="5f131-152">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="5f131-152">-ApplicationId</span></span>
<span data-ttu-id="5f131-153">ID applicazione univoco per un'entità di servizio in un tenant.</span><span class="sxs-lookup"><span data-stu-id="5f131-153">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="5f131-154">Una volta creata questa proprietà non può essere modificata.</span><span class="sxs-lookup"><span data-stu-id="5f131-154">Once created this property cannot be changed.</span></span>
<span data-ttu-id="5f131-155">Se non viene specificato un ID applicazione, verrà generato uno.</span><span class="sxs-lookup"><span data-stu-id="5f131-155">If an application id is not specified, one will be generated.</span></span>

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

### <span data-ttu-id="5f131-156">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="5f131-156">-ApplicationObject</span></span>
<span data-ttu-id="5f131-157">Oggetto che rappresenta l'applicazione per cui viene creata l'entità di servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-157">The object representing the application for which the service principal is created.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithoutCredentialParameterSet, ApplicationObjectWithPasswordPlainParameterSet, ApplicationObjectWithPasswordCredentialParameterSet, ApplicationObjectWithKeyPlainParameterSet, ApplicationObjectWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-158">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5f131-158">-CertValue</span></span>
<span data-ttu-id="5f131-159">Il valore del tipo di credenziale "asimmetrico".</span><span class="sxs-lookup"><span data-stu-id="5f131-159">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5f131-160">Rappresenta il certificato codificato 64 di base.</span><span class="sxs-lookup"><span data-stu-id="5f131-160">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="5f131-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f131-161">-DefaultProfile</span></span>
<span data-ttu-id="5f131-162">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="5f131-162">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-163">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5f131-163">-DisplayName</span></span>
<span data-ttu-id="5f131-164">Nome descrittivo dell'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-164">The friendly name of the service principal.</span></span> <span data-ttu-id="5f131-165">Se non viene specificato un nome visualizzato, il valore predefinito sarà "Azure-PowerShell-MM-DD-AAAA-HH-mm-SS", in cui il suffisso è il momento della creazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f131-165">If a display name is not provided, this value will default to 'azure-powershell-MM-dd-yyyy-HH-mm-ss', where the suffix is the time of application creation.</span></span>

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

### <span data-ttu-id="5f131-166">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5f131-166">-EndDate</span></span>
<span data-ttu-id="5f131-167">Data di fine effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="5f131-167">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5f131-168">Il valore di data di fine predefinito è di un anno da oggi.</span><span class="sxs-lookup"><span data-stu-id="5f131-168">The default end date value is one year from today.</span></span> <span data-ttu-id="5f131-169">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o prima della data in cui il certificato X509 è valido.</span><span class="sxs-lookup"><span data-stu-id="5f131-169">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5f131-170">-Credenziale</span><span class="sxs-lookup"><span data-stu-id="5f131-170">-KeyCredential</span></span>
<span data-ttu-id="5f131-171">Raccolta di credenziali chiave associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f131-171">The collection of key credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationObjectWithKeyCredentialParameterSet
Aliases: KeyCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-172">-Password</span><span class="sxs-lookup"><span data-stu-id="5f131-172">-Password</span></span>
<span data-ttu-id="5f131-173">La password da associare all'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-173">The password to be associated with the service principal.</span></span> <span data-ttu-id="5f131-174">Se non viene specificata una password, verrà generato e usato un GUID casuale come password.</span><span class="sxs-lookup"><span data-stu-id="5f131-174">If a password is not provided, a random GUID will be generated and used as the password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SimpleParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-175">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="5f131-175">-PasswordCredential</span></span>
<span data-ttu-id="5f131-176">Raccolta di credenziali password associata all'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5f131-176">The collection of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationObjectWithPasswordCredentialParameterSet
Aliases: PasswordCredentials

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f131-177">-Ruolo</span><span class="sxs-lookup"><span data-stu-id="5f131-177">-Role</span></span>
<span data-ttu-id="5f131-178">Il ruolo che l'entità servizio ha sull'ambito.</span><span class="sxs-lookup"><span data-stu-id="5f131-178">The role that the service principal has over the scope.</span></span> <span data-ttu-id="5f131-179">Se viene specificato un valore per, `Scope` ma non viene specificato alcun valore `Role` , `Role` il ruolo "collaboratore" verrà impostato come predefinito.</span><span class="sxs-lookup"><span data-stu-id="5f131-179">If a value for `Scope` is provided, but no value is provided for `Role`, then `Role` will default to the 'Contributor' role.</span></span>

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

### <span data-ttu-id="5f131-180">-Ambito</span><span class="sxs-lookup"><span data-stu-id="5f131-180">-Scope</span></span>
<span data-ttu-id="5f131-181">Ambito per cui l'entità del servizio dispone delle autorizzazioni.</span><span class="sxs-lookup"><span data-stu-id="5f131-181">The scope that the service principal has permissions on.</span></span> <span data-ttu-id="5f131-182">Se viene specificato un valore per, `Role` ma non viene specificato alcun valore `Scope` , `Scope` verrà impostato come predefinito per l'abbonamento corrente.</span><span class="sxs-lookup"><span data-stu-id="5f131-182">If a value for `Role` is provided, but no value is provided for `Scope`, then `Scope` will default to the current subscription.</span></span>

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

### <span data-ttu-id="5f131-183">-SkipAssignment</span><span class="sxs-lookup"><span data-stu-id="5f131-183">-SkipAssignment</span></span>
<span data-ttu-id="5f131-184">Se impostato, salterà la creazione dell'assegnazione di ruolo predefinita per l'entità servizio.</span><span class="sxs-lookup"><span data-stu-id="5f131-184">If set, will skip creating the default role assignment for the service principal.</span></span>

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

### <span data-ttu-id="5f131-185">-StartDate</span><span class="sxs-lookup"><span data-stu-id="5f131-185">-StartDate</span></span>
<span data-ttu-id="5f131-186">Data di inizio effettiva dell'utilizzo delle credenziali.</span><span class="sxs-lookup"><span data-stu-id="5f131-186">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5f131-187">Il valore predefinito della data di inizio è oggi.</span><span class="sxs-lookup"><span data-stu-id="5f131-187">The default start date value is today.</span></span> <span data-ttu-id="5f131-188">Per le credenziali di tipo "asimmetrico", deve essere impostato su attivato o successivo alla data di validità del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="5f131-188">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5f131-189">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5f131-189">-Confirm</span></span>
<span data-ttu-id="5f131-190">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f131-190">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f131-191">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f131-191">-WhatIf</span></span>
<span data-ttu-id="5f131-192">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f131-192">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f131-193">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5f131-193">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f131-194">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f131-194">CommonParameters</span></span>
<span data-ttu-id="5f131-195">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f131-195">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f131-196">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f131-196">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f131-197">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f131-197">INPUTS</span></span>

### <span data-ttu-id="5f131-198">System. Guid</span><span class="sxs-lookup"><span data-stu-id="5f131-198">System.Guid</span></span>

### <span data-ttu-id="5f131-199">System. String</span><span class="sxs-lookup"><span data-stu-id="5f131-199">System.String</span></span>

### <span data-ttu-id="5f131-200">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="5f131-200">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="5f131-201">Parametri: ApplicationObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="5f131-201">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="5f131-202">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="5f131-202">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="5f131-203">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="5f131-203">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="5f131-204">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="5f131-204">System.Security.SecureString</span></span>

### <span data-ttu-id="5f131-205">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="5f131-205">System.DateTime</span></span>

## <span data-ttu-id="5f131-206">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f131-206">OUTPUTS</span></span>

### <span data-ttu-id="5f131-207">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5f131-207">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="5f131-208">Microsoft. Azure. Commands. resources. Models. Authorization. PSADServicePrincipalWrapper</span><span class="sxs-lookup"><span data-stu-id="5f131-208">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADServicePrincipalWrapper</span></span>

## <span data-ttu-id="5f131-209">Note</span><span class="sxs-lookup"><span data-stu-id="5f131-209">NOTES</span></span>
<span data-ttu-id="5f131-210">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Resource, Group, template, Deployment</span><span class="sxs-lookup"><span data-stu-id="5f131-210">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="5f131-211">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f131-211">RELATED LINKS</span></span>

[<span data-ttu-id="5f131-212">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5f131-212">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5f131-213">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5f131-213">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="5f131-214">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5f131-214">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="5f131-215">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="5f131-215">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="5f131-216">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5f131-216">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="5f131-217">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5f131-217">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="5f131-218">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5f131-218">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

