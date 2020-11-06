---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: c7a98f6fba2c690fb296c42f4f6eca902d7678bb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512348"
---
# <span data-ttu-id="d497d-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d497d-101">New-AzureRmResource</span></span>

## <span data-ttu-id="d497d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d497d-102">SYNOPSIS</span></span>
<span data-ttu-id="d497d-103">Crea una risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d497d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d497d-104">SYNTAX</span></span>

### <span data-ttu-id="d497d-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d497d-105">ByResourceId (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceId <String> [-ODataQuery <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d497d-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="d497d-106">BySubscriptionLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d497d-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="d497d-107">ByTenantLevel</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d497d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d497d-108">DESCRIPTION</span></span>
<span data-ttu-id="d497d-109">Il cmdlet **New-AzureRmResource** crea una risorsa Azure, ad esempio un sito Web, un server di database SQL di Azure o un database SQL di Azure, in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d497d-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="d497d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d497d-110">EXAMPLES</span></span>

### <span data-ttu-id="d497d-111">Esempio 1: creare una risorsa</span><span class="sxs-lookup"><span data-stu-id="d497d-111">Example 1: Create a resource</span></span>
```
PS> New-AzureRmResource -Location "West US" -Properties @{test="test"} -ResourceName TestSite06 -ResourceType microsoft.web/sites -ResourceGroupName ResourceGroup11 -Force
```

<span data-ttu-id="d497d-112">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d497d-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

### <span data-ttu-id="d497d-113">Esempio 2: creare una risorsa con splatting</span><span class="sxs-lookup"><span data-stu-id="d497d-113">Example 2: Create a resource using splatting</span></span>
```
PS> $prop = @{
    Location          = "West US" 
    Properties        = @{test = "test"} 
    ResourceName      = "TestSite06" 
    ResourceType      = "microsoft.web/sites" 
    ResourceGroupName = "ResourceGroup11" 
    Force             = $true
}

PS> New-AzureRmResource @prop
```

<span data-ttu-id="d497d-114">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="d497d-114">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="d497d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d497d-115">PARAMETERS</span></span>

### <span data-ttu-id="d497d-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d497d-116">-ApiVersion</span></span>
<span data-ttu-id="d497d-117">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="d497d-117">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="d497d-118">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="d497d-118">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d497d-119">-AsJob</span></span>
<span data-ttu-id="d497d-120">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d497d-120">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d497d-121">-DefaultProfile</span></span>
<span data-ttu-id="d497d-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d497d-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-123">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="d497d-123">-ExtensionResourceName</span></span>
<span data-ttu-id="d497d-124">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-124">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="d497d-125">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="d497d-125">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="d497d-126">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="d497d-126">server name`/`database name</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-127">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="d497d-127">-ExtensionResourceType</span></span>
<span data-ttu-id="d497d-128">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="d497d-128">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="d497d-129">Ad esempio, se la risorsa di estensione è un database, specifica il tipo seguente:</span><span class="sxs-lookup"><span data-stu-id="d497d-129">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-130">-Force</span><span class="sxs-lookup"><span data-stu-id="d497d-130">-Force</span></span>
<span data-ttu-id="d497d-131">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="d497d-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-132">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="d497d-132">-IsFullObject</span></span>
<span data-ttu-id="d497d-133">Indica che l'oggetto specificato dal parametro *Properties* è l'oggetto completo.</span><span class="sxs-lookup"><span data-stu-id="d497d-133">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-134">-Tipo</span><span class="sxs-lookup"><span data-stu-id="d497d-134">-Kind</span></span>
<span data-ttu-id="d497d-135">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-135">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-136">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d497d-136">-Location</span></span>
<span data-ttu-id="d497d-137">Specifica la posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-137">Specifies the location of the resource.</span></span>
<span data-ttu-id="d497d-138">Specificare la posizione del centro dati, ad esempio Stati Uniti centrali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="d497d-138">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="d497d-139">Puoi inserire una risorsa in qualsiasi posizione che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="d497d-139">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="d497d-140">I gruppi di risorse possono contenere risorse da posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="d497d-140">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="d497d-141">Per determinare quali posizioni supportano ogni tipo di risorsa, usare il cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="d497d-141">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-142">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="d497d-142">-ODataQuery</span></span>
<span data-ttu-id="d497d-143">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="d497d-143">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="d497d-144">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="d497d-144">This cmdlet appends this value to the request in addition to any other filters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-145">-Piano</span><span class="sxs-lookup"><span data-stu-id="d497d-145">-Plan</span></span>
<span data-ttu-id="d497d-146">Tabella hash che rappresenta le proprietà del piano risorse.</span><span class="sxs-lookup"><span data-stu-id="d497d-146">A hash table that represents resource plan properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-147">-Pre</span><span class="sxs-lookup"><span data-stu-id="d497d-147">-Pre</span></span>
<span data-ttu-id="d497d-148">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="d497d-148">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-149">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="d497d-149">-Properties</span></span>
<span data-ttu-id="d497d-150">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-150">Specifies resource properties for the resource.</span></span> <span data-ttu-id="d497d-151">Usa questo parametro per specificare i valori delle proprietà specifiche di un tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-151">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d497d-152">-ResourceGroupName</span></span>
<span data-ttu-id="d497d-153">Specifica il nome del gruppo di risorse in cui questo cmdlet crea la risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-153">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: String
Parameter Sets: BySubscriptionLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d497d-154">-ResourceId</span></span>
<span data-ttu-id="d497d-155">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="d497d-155">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="d497d-156">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="d497d-156">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-157">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d497d-157">-ResourceName</span></span>
<span data-ttu-id="d497d-158">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-158">Specifies the name of the resource.</span></span> <span data-ttu-id="d497d-159">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="d497d-159">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-160">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d497d-160">-ResourceType</span></span>
<span data-ttu-id="d497d-161">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d497d-161">Specifies the type of the resource.</span></span>
<span data-ttu-id="d497d-162">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="d497d-162">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: BySubscriptionLevel, ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-163">-SKU</span><span class="sxs-lookup"><span data-stu-id="d497d-163">-Sku</span></span>
<span data-ttu-id="d497d-164">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="d497d-164">A hash table that represents sku properties.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="d497d-165">-Tag</span></span>
<span data-ttu-id="d497d-166">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="d497d-166">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d497d-167">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="d497d-167">For example:</span></span>

<span data-ttu-id="d497d-168">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d497d-168">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-169">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="d497d-169">-TenantLevel</span></span>
<span data-ttu-id="d497d-170">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="d497d-170">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d497d-171">-Confirm</span></span>
<span data-ttu-id="d497d-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d497d-172">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d497d-173">-WhatIf</span></span>
<span data-ttu-id="d497d-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d497d-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d497d-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d497d-175">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d497d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d497d-176">CommonParameters</span></span>
<span data-ttu-id="d497d-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d497d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d497d-178">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d497d-178">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d497d-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d497d-179">INPUTS</span></span>

### <span data-ttu-id="d497d-180">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d497d-180">None</span></span>
<span data-ttu-id="d497d-181">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="d497d-181">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d497d-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d497d-182">OUTPUTS</span></span>

### <span data-ttu-id="d497d-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d497d-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d497d-184">Note</span><span class="sxs-lookup"><span data-stu-id="d497d-184">NOTES</span></span>

## <span data-ttu-id="d497d-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d497d-185">RELATED LINKS</span></span>

[<span data-ttu-id="d497d-186">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d497d-186">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="d497d-187">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d497d-187">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="d497d-188">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d497d-188">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="d497d-189">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d497d-189">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="d497d-190">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="d497d-190">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
