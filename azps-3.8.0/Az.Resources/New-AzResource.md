---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzResource.md
ms.openlocfilehash: 37561ecc57f5b729a33b2011c26a297bcb2bf52b
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/08/2020
ms.locfileid: "94030881"
---
# <span data-ttu-id="e4cc9-101">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="e4cc9-101">New-AzResource</span></span>

## <span data-ttu-id="e4cc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e4cc9-102">SYNOPSIS</span></span>
<span data-ttu-id="e4cc9-103">Crea una risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-103">Creates a resource.</span></span>

## <span data-ttu-id="e4cc9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e4cc9-104">SYNTAX</span></span>

### <span data-ttu-id="e4cc9-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e4cc9-105">ByResourceId (Default)</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4cc9-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="e4cc9-106">BySubscriptionLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4cc9-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="e4cc9-107">ByTenantLevel</span></span>
```
New-AzResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4cc9-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e4cc9-108">DESCRIPTION</span></span>
<span data-ttu-id="e4cc9-109">Il cmdlet **New-AzResource** crea una risorsa Azure, ad esempio un sito Web, un server di database SQL di Azure o un database SQL di Azure, in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-109">The **New-AzResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="e4cc9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e4cc9-110">EXAMPLES</span></span>

### <span data-ttu-id="e4cc9-111">Esempio 1: creare una risorsa</span><span class="sxs-lookup"><span data-stu-id="e4cc9-111">Example 1: Create a resource</span></span>
```
PS> New-AzResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="e4cc9-112">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="e4cc9-113">Esempio 2: creare una risorsa con splatting</span><span class="sxs-lookup"><span data-stu-id="e4cc9-113">Example 2: Create a resource using splatting</span></span>
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

<span data-ttu-id="e4cc9-114">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="e4cc9-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e4cc9-115">PARAMETERS</span></span>

### <span data-ttu-id="e4cc9-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e4cc9-116">-ApiVersion</span></span>
<span data-ttu-id="e4cc9-117">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="e4cc9-118">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e4cc9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4cc9-119">-AsJob</span></span>
<span data-ttu-id="e4cc9-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="e4cc9-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="e4cc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4cc9-121">-DefaultProfile</span></span>
<span data-ttu-id="e4cc9-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e4cc9-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4cc9-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="e4cc9-123">-ExtensionResourceName</span></span>
<span data-ttu-id="e4cc9-124">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="e4cc9-125">Ad esempio, per specificare un database, usare il formato seguente: nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="e4cc9-125">For instance, to specify a database, use the following format: server name`/`database name</span></span>

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

### <span data-ttu-id="e4cc9-126">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="e4cc9-126">-ExtensionResourceType</span></span>
<span data-ttu-id="e4cc9-127">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-127">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="e4cc9-128">Ad esempio, se la risorsa di estensione è un database, specifica il tipo seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e4cc9-128">For instance, if the extension resource is a database, specify the following type: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e4cc9-129">-Force</span><span class="sxs-lookup"><span data-stu-id="e4cc9-129">-Force</span></span>
<span data-ttu-id="e4cc9-130">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-130">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="e4cc9-131">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="e4cc9-131">-IsFullObject</span></span>
<span data-ttu-id="e4cc9-132">Indica che l'oggetto specificato dal parametro *Properties* è l'oggetto completo.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-132">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="e4cc9-133">-Tipo</span><span class="sxs-lookup"><span data-stu-id="e4cc9-133">-Kind</span></span>
<span data-ttu-id="e4cc9-134">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-134">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="e4cc9-135">-Posizione</span><span class="sxs-lookup"><span data-stu-id="e4cc9-135">-Location</span></span>
<span data-ttu-id="e4cc9-136">Specifica la posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-136">Specifies the location of the resource.</span></span>
<span data-ttu-id="e4cc9-137">Specificare la posizione del centro dati, ad esempio Stati Uniti centrali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-137">Specify data center location, such as Central US or Southeast Asia.</span></span>
<span data-ttu-id="e4cc9-138">Puoi inserire una risorsa in qualsiasi posizione che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-138">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="e4cc9-139">I gruppi di risorse possono contenere risorse da posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-139">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="e4cc9-140">Per determinare quali posizioni supportano ogni tipo di risorsa, usare il cmdlet Get-AzLocation.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-140">To determine which locations support each resource type, use the Get-AzLocation cmdlet.</span></span>

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

### <span data-ttu-id="e4cc9-141">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="e4cc9-141">-ODataQuery</span></span>
<span data-ttu-id="e4cc9-142">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="e4cc9-142">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="e4cc9-143">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-143">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="e4cc9-144">-Piano</span><span class="sxs-lookup"><span data-stu-id="e4cc9-144">-Plan</span></span>
<span data-ttu-id="e4cc9-145">Tabella hash che rappresenta le proprietà del piano risorse.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-145">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="e4cc9-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="e4cc9-146">-Pre</span></span>
<span data-ttu-id="e4cc9-147">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e4cc9-148">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="e4cc9-148">-Properties</span></span>
<span data-ttu-id="e4cc9-149">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-149">Specifies resource properties for the resource.</span></span> <span data-ttu-id="e4cc9-150">Usa questo parametro per specificare i valori delle proprietà specifiche di un tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-150">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="e4cc9-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4cc9-151">-ResourceGroupName</span></span>
<span data-ttu-id="e4cc9-152">Specifica il nome del gruppo di risorse in cui questo cmdlet crea la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-152">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

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

### <span data-ttu-id="e4cc9-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4cc9-153">-ResourceId</span></span>
<span data-ttu-id="e4cc9-154">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente: `/subscriptions/` ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e4cc9-154">Specifies the fully qualified resource ID, including the subscription, as in the following example: `/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e4cc9-155">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e4cc9-155">-ResourceName</span></span>
<span data-ttu-id="e4cc9-156">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-156">Specifies the name of the resource.</span></span> <span data-ttu-id="e4cc9-157">Ad esempio, per specificare un database, usa il formato seguente: `ContosoServer/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="e4cc9-157">For instance, to specify a database, use the following format: `ContosoServer/ContosoDatabase`</span></span>

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

### <span data-ttu-id="e4cc9-158">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="e4cc9-158">-ResourceType</span></span>
<span data-ttu-id="e4cc9-159">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-159">Specifies the type of the resource.</span></span>
<span data-ttu-id="e4cc9-160">Per un database, ad esempio, il tipo di risorsa è il seguente: `Microsoft.Sql/Servers/Databases`</span><span class="sxs-lookup"><span data-stu-id="e4cc9-160">For instance, for a database, the resource type is as follows: `Microsoft.Sql/Servers/Databases`</span></span>

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

### <span data-ttu-id="e4cc9-161">-SKU</span><span class="sxs-lookup"><span data-stu-id="e4cc9-161">-Sku</span></span>
<span data-ttu-id="e4cc9-162">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-162">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="e4cc9-163">-Tag</span><span class="sxs-lookup"><span data-stu-id="e4cc9-163">-Tag</span></span>
<span data-ttu-id="e4cc9-164">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-164">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="e4cc9-165">Ad esempio: @ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="e4cc9-165">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="e4cc9-166">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="e4cc9-166">-TenantLevel</span></span>
<span data-ttu-id="e4cc9-167">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-167">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="e4cc9-168">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e4cc9-168">-Confirm</span></span>
<span data-ttu-id="e4cc9-169">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-169">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4cc9-170">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4cc9-170">-WhatIf</span></span>
<span data-ttu-id="e4cc9-171">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-171">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4cc9-172">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-172">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4cc9-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4cc9-173">CommonParameters</span></span>
<span data-ttu-id="e4cc9-174">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4cc9-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4cc9-175">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e4cc9-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4cc9-176">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e4cc9-176">INPUTS</span></span>

### <span data-ttu-id="e4cc9-177">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="e4cc9-177">System.Collections.Hashtable</span></span>

### <span data-ttu-id="e4cc9-178">System. String</span><span class="sxs-lookup"><span data-stu-id="e4cc9-178">System.String</span></span>

## <span data-ttu-id="e4cc9-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e4cc9-179">OUTPUTS</span></span>

### <span data-ttu-id="e4cc9-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e4cc9-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e4cc9-181">Note</span><span class="sxs-lookup"><span data-stu-id="e4cc9-181">NOTES</span></span>

## <span data-ttu-id="e4cc9-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e4cc9-182">RELATED LINKS</span></span>

[<span data-ttu-id="e4cc9-183">Get-AzResource</span><span class="sxs-lookup"><span data-stu-id="e4cc9-183">Get-AzResource</span></span>](./Get-AzResource.md)

[<span data-ttu-id="e4cc9-184">Move-AzResource</span><span class="sxs-lookup"><span data-stu-id="e4cc9-184">Move-AzResource</span></span>](./Move-AzResource.md)

[<span data-ttu-id="e4cc9-185">Remove-AzResource</span><span class="sxs-lookup"><span data-stu-id="e4cc9-185">Remove-AzResource</span></span>](./Remove-AzResource.md)

[<span data-ttu-id="e4cc9-186">Set-AzResource</span><span class="sxs-lookup"><span data-stu-id="e4cc9-186">Set-AzResource</span></span>](./Set-AzResource.md)
