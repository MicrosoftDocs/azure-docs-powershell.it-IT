---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzResource.md
ms.openlocfilehash: bf01232939881feb5a60420cde76e0e809cbcb3d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98382563"
---
# <span data-ttu-id="22ece-101">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="22ece-101">Set-AzResource</span></span>

## <span data-ttu-id="22ece-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22ece-102">SYNOPSIS</span></span>
<span data-ttu-id="22ece-103">Modifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-103">Modifies a resource.</span></span>

## <span data-ttu-id="22ece-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22ece-104">SYNTAX</span></span>

### <span data-ttu-id="22ece-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22ece-105">ByResourceId (Default)</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ece-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="22ece-106">ByInputObject</span></span>
```
Set-AzResource -InputObject <PSResource> [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="22ece-107">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="22ece-107">BySubscriptionLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22ece-108">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="22ece-108">ByTenantLevel</span></span>
```
Set-AzResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="22ece-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22ece-109">DESCRIPTION</span></span>
<span data-ttu-id="22ece-110">Il cmdlet **set-AzResource** modifica una risorsa Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="22ece-110">The **Set-AzResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="22ece-111">Specificare una risorsa da modificare per nome e tipo oppure per ID.</span><span class="sxs-lookup"><span data-stu-id="22ece-111">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="22ece-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22ece-112">EXAMPLES</span></span>

### <span data-ttu-id="22ece-113">Esempio 1: modificare una risorsa</span><span class="sxs-lookup"><span data-stu-id="22ece-113">Example 1: Modify a resource</span></span>
```
PS C:\> $Resource = Get-AzResource -ResourceType Microsoft.Web/sites -ResourceGroupName ResourceGroup11 -ResourceName ContosoSite
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzResource -Force
```

<span data-ttu-id="22ece-114">Il primo comando ottiene la risorsa denominata ContosoSite usando il cmdlet Get-AzResource e lo archivia nella variabile $Resource.</span><span class="sxs-lookup"><span data-stu-id="22ece-114">The first command gets the resource named ContosoSite by using the Get-AzResource cmdlet, and then stores it in the $Resource variable.</span></span>
<span data-ttu-id="22ece-115">Il secondo comando modifica una proprietà di $Resource.</span><span class="sxs-lookup"><span data-stu-id="22ece-115">The second command modifies a property of $Resource.</span></span>
<span data-ttu-id="22ece-116">Il comando finale aggiorna la risorsa in base alla $Resource.</span><span class="sxs-lookup"><span data-stu-id="22ece-116">The final command updates the resource to match $Resource.</span></span>

### <span data-ttu-id="22ece-117">Esempio 2: modificare tutte le risorse di un gruppo di risorse specifico</span><span class="sxs-lookup"><span data-stu-id="22ece-117">Example 2: Modify all resources in a given resource group</span></span>
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

<span data-ttu-id="22ece-118">Il primo comando recupera le risorse nel gruppo di risorse testrg e le archivia nella variabile $Resource.</span><span class="sxs-lookup"><span data-stu-id="22ece-118">The first command gets the resources in the testrg resource group, and then stores them in the $Resource variable.</span></span>

<span data-ttu-id="22ece-119">Il secondo comando scorre tutte le risorse del gruppo di risorse e aggiunge un nuovo tag.</span><span class="sxs-lookup"><span data-stu-id="22ece-119">The second command iterates over each of these resources in the resource group and adds a new tag to them.</span></span>

<span data-ttu-id="22ece-120">Il comando finale Aggiorna ognuna di queste risorse.</span><span class="sxs-lookup"><span data-stu-id="22ece-120">The final command updates each of these resources.</span></span>

## <span data-ttu-id="22ece-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22ece-121">PARAMETERS</span></span>

### <span data-ttu-id="22ece-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22ece-122">-ApiVersion</span></span>
<span data-ttu-id="22ece-123">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="22ece-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="22ece-124">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="22ece-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="22ece-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="22ece-125">-AsJob</span></span>
<span data-ttu-id="22ece-126">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="22ece-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="22ece-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22ece-127">-DefaultProfile</span></span>
<span data-ttu-id="22ece-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="22ece-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22ece-129">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="22ece-129">-ExtensionResourceName</span></span>
<span data-ttu-id="22ece-130">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-130">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="22ece-131">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="22ece-131">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="22ece-132">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="22ece-132">-ExtensionResourceType</span></span>
<span data-ttu-id="22ece-133">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="22ece-133">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="22ece-134">Ad esempio, se la risorsa di estensione è un database, specificare quanto segue: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="22ece-134">For instance, if the extension resource is a database specify the following: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="22ece-135">-Force</span><span class="sxs-lookup"><span data-stu-id="22ece-135">-Force</span></span>
<span data-ttu-id="22ece-136">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="22ece-136">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="22ece-137">-InputObject</span><span class="sxs-lookup"><span data-stu-id="22ece-137">-InputObject</span></span>
<span data-ttu-id="22ece-138">Rappresentazione dell'oggetto della risorsa da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="22ece-138">The object representation of the resource to update.</span></span>

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

### <span data-ttu-id="22ece-139">-Tipo</span><span class="sxs-lookup"><span data-stu-id="22ece-139">-Kind</span></span>
<span data-ttu-id="22ece-140">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-140">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="22ece-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="22ece-141">-ODataQuery</span></span>
<span data-ttu-id="22ece-142">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="22ece-142">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="22ece-143">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="22ece-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="22ece-144">-Piano</span><span class="sxs-lookup"><span data-stu-id="22ece-144">-Plan</span></span>
<span data-ttu-id="22ece-145">Specifica le proprietà del piano di risorse, come tabella hash, per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-145">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="22ece-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="22ece-146">-Pre</span></span>
<span data-ttu-id="22ece-147">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="22ece-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22ece-148">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="22ece-148">-Properties</span></span>
<span data-ttu-id="22ece-149">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-149">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="22ece-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22ece-150">-ResourceGroupName</span></span>
<span data-ttu-id="22ece-151">Specifica il nome del gruppo di risorse in cui questo cmdlet modifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-151">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="22ece-152">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22ece-152">-ResourceId</span></span>
<span data-ttu-id="22ece-153">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="22ece-153">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="22ece-154">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="22ece-154">-ResourceName</span></span>
<span data-ttu-id="22ece-155">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-155">Specifies the name of the resource.</span></span>
<span data-ttu-id="22ece-156">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="22ece-156">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="22ece-157">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="22ece-157">-ResourceType</span></span>
<span data-ttu-id="22ece-158">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="22ece-158">Specifies the type of the resource.</span></span>
<span data-ttu-id="22ece-159">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="22ece-159">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="22ece-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="22ece-160">-Sku</span></span>
<span data-ttu-id="22ece-161">Specifica l'oggetto SKU della risorsa come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="22ece-161">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="22ece-162">-Tag</span><span class="sxs-lookup"><span data-stu-id="22ece-162">-Tag</span></span>
<span data-ttu-id="22ece-163">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="22ece-163">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="22ece-164">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="22ece-164">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="22ece-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="22ece-165">-TenantLevel</span></span>
<span data-ttu-id="22ece-166">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="22ece-166">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="22ece-167">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="22ece-167">-UsePatchSemantics</span></span>
<span data-ttu-id="22ece-168">Indica che questo cmdlet usa una PATCH HTTP per aggiornare l'oggetto, invece di un post HTTP.</span><span class="sxs-lookup"><span data-stu-id="22ece-168">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="22ece-169">-Confermare</span><span class="sxs-lookup"><span data-stu-id="22ece-169">-Confirm</span></span>
<span data-ttu-id="22ece-170">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="22ece-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22ece-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22ece-171">-WhatIf</span></span>
<span data-ttu-id="22ece-172">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22ece-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22ece-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="22ece-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22ece-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22ece-174">CommonParameters</span></span>
<span data-ttu-id="22ece-175">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22ece-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22ece-176">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="22ece-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22ece-177">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22ece-177">INPUTS</span></span>

### <span data-ttu-id="22ece-178">Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSResource</span><span class="sxs-lookup"><span data-stu-id="22ece-178">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResource</span></span>

### <span data-ttu-id="22ece-179">System. String</span><span class="sxs-lookup"><span data-stu-id="22ece-179">System.String</span></span>

### <span data-ttu-id="22ece-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="22ece-180">System.Management.Automation.PSObject</span></span>

### <span data-ttu-id="22ece-181">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="22ece-181">System.Collections.Hashtable</span></span>

## <span data-ttu-id="22ece-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22ece-182">OUTPUTS</span></span>

### <span data-ttu-id="22ece-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="22ece-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="22ece-184">Note</span><span class="sxs-lookup"><span data-stu-id="22ece-184">NOTES</span></span>

## <span data-ttu-id="22ece-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22ece-185">RELATED LINKS</span></span>

[<span data-ttu-id="22ece-186">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="22ece-186">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="22ece-187">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="22ece-187">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="22ece-188">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="22ece-188">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="22ece-189">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="22ece-189">Remove-AzResource</span></span>](./Remove-AzResource.md)
