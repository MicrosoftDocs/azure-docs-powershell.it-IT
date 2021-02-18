---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: 82e06a4736a613111efac452eb1fced2713dc470
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415751"
---
# <span data-ttu-id="f551b-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="f551b-101">Set-AzResource</span></span>

## <span data-ttu-id="f551b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f551b-102">SYNOPSIS</span></span>
<span data-ttu-id="f551b-103">Modifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-103">Modifies a resource.</span></span>

## <span data-ttu-id="f551b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f551b-104">SYNTAX</span></span>

### <span data-ttu-id="f551b-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f551b-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f551b-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f551b-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f551b-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="f551b-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f551b-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="f551b-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f551b-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f551b-109">DESCRIPTION</span></span>
<span data-ttu-id="f551b-110">Il cmdlet **Set-AzResource** modifica una risorsa Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="f551b-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="f551b-111">Specificare una risorsa da modificare in base al nome e al tipo o in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="f551b-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="f551b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f551b-112">EXAMPLES</span></span>

### <span data-ttu-id="f551b-113">Esempio 1: Modificare una risorsa</span><span class="sxs-lookup"><span data-stu-id="f551b-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="f551b-114">Il primo comando recupera la risorsa denominata ContosoSite usando il cmdlet Get-AzResource, quindi la archivia nella $Resource variabile.</span><span class="sxs-lookup"><span data-stu-id="f551b-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="f551b-115">Il secondo comando modifica una proprietà di $Resource.</span><span class="sxs-lookup"><span data-stu-id="f551b-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="f551b-116">Il comando finale aggiorna la risorsa in modo che corrisponda $Resource.</span><span class="sxs-lookup"><span data-stu-id="f551b-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="f551b-117">Esempio 2: Modificare tutte le risorse in un determinato gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f551b-117">Example 2: Modify all resources in a given resource group</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceGroupName testrg
PS C:\> $Resource | ForEach-Object { $_.Tags.Add("testkey", "testval") }
PS C:\> $Resource | Set-AzResource -Force

Name              : kv-test
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Microsoft.KeyVault/vaults/kv-test
ResourceName      : kv-test
ResourceType      : Microsoft.KeyVault/vaults
ResourceGroupName : testrg
Location          : westus
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, key}
Properties        : @{}

Name              : testresource
ResourceId        : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testrg/providers/Providers.Test/statefulResources/testresource
ResourceName      : testresource
ResourceType      : Providers.Test/statefulResources
ResourceGroupName : testrg
Location          : West US 2
SubscriptionId    : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags              : {testrgkey, anothertesttag}
Properties        : @{key=value}
Sku               : @{name=A0}
```

<span data-ttu-id="f551b-118">Il primo comando recupera le risorse nel gruppo di risorse testrg e quindi le archivia nella $Resource variabile.</span><span class="sxs-lookup"><span data-stu-id="f551b-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="f551b-119">Il secondo comando iterazione su ognuna di queste risorse nel gruppo di risorse e aggiunge un nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="f551b-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="f551b-120">Il comando finale aggiorna ognuna di queste risorse.</span><span class="sxs-lookup"><span data-stu-id="f551b-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="f551b-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f551b-121">PARAMETERS</span></span>

### <span data-ttu-id="f551b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="f551b-122">-ApiVersion</span></span>
<span data-ttu-id="f551b-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="f551b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="f551b-124">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="f551b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f551b-125">-AsJob</span></span>
<span data-ttu-id="f551b-126">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f551b-126">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f551b-127">-DefaultProfile</span></span>
<span data-ttu-id="f551b-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f551b-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f551b-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="f551b-129">-ExtensionResourceName</span></span>
<span data-ttu-id="f551b-130">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="f551b-131">Ad esempio, per specificare un database, usare il formato seguente: nome database nome `/` server</span><span class="sxs-lookup"><span data-stu-id="f551b-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="f551b-132">-ExtensionResourceType</span></span>
<span data-ttu-id="f551b-133">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="f551b-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="f551b-134">Ad esempio, se la risorsa dell'estensione è un database, specificare quanto segue: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="f551b-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-135">-Force</span><span class="sxs-lookup"><span data-stu-id="f551b-135">-Force</span></span>
<span data-ttu-id="f551b-136">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="f551b-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f551b-137">-InputObject</span></span>
<span data-ttu-id="f551b-138">Rappresentazione dell'oggetto della risorsa da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="f551b-138">The object representation of the resource to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-139">-Kind</span><span class="sxs-lookup"><span data-stu-id="f551b-139">-Kind</span></span>
<span data-ttu-id="f551b-140">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-140">Specifies the resource kind for the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="f551b-141">-ODataQuery</span></span>
<span data-ttu-id="f551b-142">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="f551b-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="f551b-143">Questo cmdlet aggiunge questo valore alla richiesta in aggiunta ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="f551b-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="f551b-144">-Plan</span></span>
<span data-ttu-id="f551b-145">Specifica le proprietà del piano delle risorse, come tabella hash, per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="f551b-146">-Pre</span></span>
<span data-ttu-id="f551b-147">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="f551b-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="f551b-148">-Properties</span></span>
<span data-ttu-id="f551b-149">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-149">Specifies resource properties for the resource.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f551b-150">-ResourceGroupName</span></span>
<span data-ttu-id="f551b-151">Specifica il nome del gruppo di risorse in cui questo cmdlet modifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f551b-152">-ResourceId</span></span>
<span data-ttu-id="f551b-153">Specifica l'ID risorsa completo, inclusa la sottoscrizione, come nell'esempio seguente: `/subscriptions/` ID sottoscrizione`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f551b-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f551b-154">-ResourceName</span></span>
<span data-ttu-id="f551b-155">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="f551b-156">Ad esempio, per specificare un database, usare il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="f551b-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="f551b-157">-ResourceType</span></span>
<span data-ttu-id="f551b-158">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="f551b-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="f551b-159">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="f551b-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

```yaml
Type: System.String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="f551b-160">-Sku</span></span>
<span data-ttu-id="f551b-161">Specifica l'oggetto SKU della risorsa come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f551b-161">Specifies the SKU object of the resource as a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="f551b-162">-Tag</span></span>
<span data-ttu-id="f551b-163">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f551b-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f551b-164">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="f551b-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="f551b-165">-TenantLevel</span></span>
<span data-ttu-id="f551b-166">Indica che questo cmdlet opera a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="f551b-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="f551b-167">-UsePatchSemantics</span></span>
<span data-ttu-id="f551b-168">Indica che questo cmdlet usa una PATCH HTTP per aggiornare l'oggetto, invece di una HTTP PUT.</span><span class="sxs-lookup"><span data-stu-id="f551b-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f551b-169">-Confirm</span></span>
<span data-ttu-id="f551b-170">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f551b-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f551b-171">-WhatIf</span></span>
<span data-ttu-id="f551b-172">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f551b-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f551b-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f551b-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f551b-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f551b-174">CommonParameters</span></span>
<span data-ttu-id="f551b-175">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f551b-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f551b-176">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f551b-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f551b-177">INPUT</span><span class="sxs-lookup"><span data-stu-id="f551b-177">INPUTS</span></span>

### <span data-ttu-id="f551b-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span><span class="sxs-lookup"><span data-stu-id="f551b-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="f551b-179">System.String</span><span class="sxs-lookup"><span data-stu-id="f551b-179">System.String</span></span>

### <span data-ttu-id="f551b-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f551b-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="f551b-181">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f551b-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f551b-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f551b-182">OUTPUTS</span></span>

### <span data-ttu-id="f551b-183">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="f551b-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="f551b-184">NOTE</span><span class="sxs-lookup"><span data-stu-id="f551b-184">NOTES</span></span>

## <span data-ttu-id="f551b-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f551b-185">RELATED LINKS</span></span>


[<span data-ttu-id="f551b-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="f551b-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="f551b-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="f551b-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="f551b-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="f551b-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="f551b-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="f551b-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
