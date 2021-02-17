---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192735"
---
# <span data-ttu-id="0f9ef-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="0f9ef-101">New-AzResource</span></span>

## <span data-ttu-id="0f9ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f9ef-102">SYNOPSIS</span></span>
<span data-ttu-id="0f9ef-103">Crea una risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-103">Creates a resource.</span></span>

## <span data-ttu-id="0f9ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f9ef-104">SYNTAX</span></span>

### <span data-ttu-id="0f9ef-105">ByResourceId (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f9ef-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f9ef-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="0f9ef-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f9ef-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="0f9ef-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0f9ef-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f9ef-108">DESCRIPTION</span></span>
<span data-ttu-id="0f9ef-109">Il cmdlet **New-AzResource** crea una risorsa di Azure, ad esempio un sito Web, un server di database di Azure SQL o un database SQL di Azure, in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="0f9ef-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f9ef-110">EXAMPLES</span></span>

### <span data-ttu-id="0f9ef-111">Esempio 1: Creare una risorsa</span><span class="sxs-lookup"><span data-stu-id="0f9ef-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="0f9ef-112">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="0f9ef-113">Esempio 2: Creare una risorsa usando la creazione di una risorsa</span><span class="sxs-lookup"><span data-stu-id="0f9ef-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US"
    Properties        = @{test = "test"}
    ResourceName      = "TestSite06"
    ResourceType      = "microsoft.web/sites"
    ResourceGroupName = "ResourceGroup11"
    Force             = $true
}

PS> New-AzResource @prop
```

<span data-ttu-id="0f9ef-114">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="0f9ef-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f9ef-115">PARAMETERS</span></span>

### <span data-ttu-id="0f9ef-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0f9ef-116">-ApiVersion</span></span>
<span data-ttu-id="0f9ef-117">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="0f9ef-118">Se non si specifica una versione, questo cmdlet usa l'ultima versione disponibile.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0f9ef-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0f9ef-119">-AsJob</span></span>
<span data-ttu-id="0f9ef-120">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="0f9ef-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0f9ef-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f9ef-121">-DefaultProfile</span></span>
<span data-ttu-id="0f9ef-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="0f9ef-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f9ef-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="0f9ef-123">-ExtensionResourceName</span></span>
<span data-ttu-id="0f9ef-124">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="0f9ef-125">Ad esempio, per specificare un database, usare il formato seguente: nome database nome `/` server</span><span class="sxs-lookup"><span data-stu-id="0f9ef-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="0f9ef-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="0f9ef-126">-ExtensionResourceType</span></span>
<span data-ttu-id="0f9ef-127">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="0f9ef-128">Ad esempio, se la risorsa dell'estensione è un database, specificare il tipo seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0f9ef-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0f9ef-129">-Force</span><span class="sxs-lookup"><span data-stu-id="0f9ef-129">-Force</span></span>
<span data-ttu-id="0f9ef-130">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0f9ef-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="0f9ef-131">-IsFullObject</span></span>
<span data-ttu-id="0f9ef-132">Indica che l'oggetto specificato *dal parametro Properties* è l'oggetto completo.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="0f9ef-133">-Kind</span><span class="sxs-lookup"><span data-stu-id="0f9ef-133">-Kind</span></span>
<span data-ttu-id="0f9ef-134">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="0f9ef-135">-Location</span><span class="sxs-lookup"><span data-stu-id="0f9ef-135">-Location</span></span>
<span data-ttu-id="0f9ef-136">Specifica la posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="0f9ef-137">Specificare la posizione del data center, ad esempio Stati Uniti centrali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="0f9ef-138">È possibile inserire una risorsa in qualsiasi posizione che supporti risorse di quel tipo.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="0f9ef-139">I gruppi di risorse possono contenere risorse da posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="0f9ef-140">Per determinare le posizioni che supportano ogni tipo di risorsa, usare Get-AzLocation cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="0f9ef-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="0f9ef-141">-ODataQuery</span></span>
<span data-ttu-id="0f9ef-142">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="0f9ef-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="0f9ef-143">Questo cmdlet aggiunge questo valore alla richiesta in aggiunta ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="0f9ef-144">-Plan</span><span class="sxs-lookup"><span data-stu-id="0f9ef-144">-Plan</span></span>
<span data-ttu-id="0f9ef-145">Tabella hash che rappresenta le proprietà del piano delle risorse.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-145">A hash table that represents resource plan properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9ef-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="0f9ef-146">-Pre</span></span>
<span data-ttu-id="0f9ef-147">Indica che questo cmdlet considera le versioni delle API non ancora rilasciate quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0f9ef-148">-Properties</span><span class="sxs-lookup"><span data-stu-id="0f9ef-148">-Properties</span></span>
<span data-ttu-id="0f9ef-149">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="0f9ef-150">Usare questo parametro per specificare i valori delle proprietà specifiche per un tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9ef-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f9ef-151">-ResourceGroupName</span></span>
<span data-ttu-id="0f9ef-152">Specifica il nome del gruppo di risorse in cui questo cmdlet crea la risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="0f9ef-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f9ef-153">-ResourceId</span></span>
<span data-ttu-id="0f9ef-154">Specifica l'ID risorsa completo, inclusa la sottoscrizione, come nell'esempio seguente: `/subscriptions/` ID sottoscrizione`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0f9ef-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0f9ef-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="0f9ef-155">-ResourceName</span></span>
<span data-ttu-id="0f9ef-156">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-156">Specifies the name of the resource.</span></span> <span data-ttu-id="0f9ef-157">Ad esempio, per specificare un database, usare il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="0f9ef-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="0f9ef-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="0f9ef-158">-ResourceType</span></span>
<span data-ttu-id="0f9ef-159">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="0f9ef-160">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="0f9ef-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="0f9ef-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="0f9ef-161">-Sku</span></span>
<span data-ttu-id="0f9ef-162">Tabella hash che rappresenta le proprietà delle SKU.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="0f9ef-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="0f9ef-163">-Tag</span></span>
<span data-ttu-id="0f9ef-164">Coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0f9ef-165">Ad esempio: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="0f9ef-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f9ef-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="0f9ef-166">-TenantLevel</span></span>
<span data-ttu-id="0f9ef-167">Indica che questo cmdlet opera a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="0f9ef-168">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f9ef-168">-Confirm</span></span>
<span data-ttu-id="0f9ef-169">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f9ef-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f9ef-170">-WhatIf</span></span>
<span data-ttu-id="0f9ef-171">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f9ef-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f9ef-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f9ef-173">CommonParameters</span></span>
<span data-ttu-id="0f9ef-174">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f9ef-175">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f9ef-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f9ef-176">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f9ef-176">INPUTS</span></span>

### <span data-ttu-id="0f9ef-177">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="0f9ef-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="0f9ef-178">System.String</span><span class="sxs-lookup"><span data-stu-id="0f9ef-178">System.String</span></span>

## <span data-ttu-id="0f9ef-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f9ef-179">OUTPUTS</span></span>

### <span data-ttu-id="0f9ef-180">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0f9ef-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0f9ef-181">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f9ef-181">NOTES</span></span>

## <span data-ttu-id="0f9ef-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f9ef-182">RELATED LINKS</span></span>

[<span data-ttu-id="0f9ef-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="0f9ef-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="0f9ef-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="0f9ef-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="0f9ef-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="0f9ef-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="0f9ef-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="0f9ef-186">Set-AzResource</span></span>](./Set-AzResource.md)
