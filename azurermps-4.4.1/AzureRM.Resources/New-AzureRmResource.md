---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D6FF6BDD-4515-438D-B39D-C0BFC3342F4E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmResource.md
ms.openlocfilehash: eb75c1afc0b0fa82c0fee6b734ded951fdfa519f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519981"
---
# <span data-ttu-id="6b0b3-101">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6b0b3-101">New-AzureRmResource</span></span>

## <span data-ttu-id="6b0b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b0b3-102">SYNOPSIS</span></span>
<span data-ttu-id="6b0b3-103">Crea una risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-103">Creates a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6b0b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b0b3-104">SYNTAX</span></span>

### <span data-ttu-id="6b0b3-105">ID risorsa (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6b0b3-105">The resource Id. (Default)</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6b0b3-106">Risorsa che risiede a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-106">Resource that resides at the subscription level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6b0b3-107">Risorsa che risiede a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-107">Resource that resides at the tenant level.</span></span>
```
New-AzureRmResource [-Location <String>] [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>]
 [-Sku <Hashtable>] [-Tag <Hashtable>] [-IsFullObject] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6b0b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b0b3-108">DESCRIPTION</span></span>
<span data-ttu-id="6b0b3-109">Il cmdlet **New-AzureRmResource** crea una risorsa Azure, ad esempio un sito Web, un server di database SQL di Azure o un database SQL di Azure, in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-109">The **New-AzureRmResource** cmdlet creates an Azure resource, such as a website, Azure SQL Database server, or Azure SQL Database, in a resource group.</span></span>

## <span data-ttu-id="6b0b3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b0b3-110">EXAMPLES</span></span>

### <span data-ttu-id="6b0b3-111">Esempio 1: creare una risorsa</span><span class="sxs-lookup"><span data-stu-id="6b0b3-111">Example 1: Create a resource</span></span>
```
PS C:\>New-AzureRmResource -Location "West US" -Properties @{"test"="test"} -ResourceName "TestSite06" -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -Force
```

<span data-ttu-id="6b0b3-112">Questo comando crea una risorsa che è un sito Web in ResourceGroup11.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-112">This command creates a resource that is a website in ResourceGroup11.</span></span>

## <span data-ttu-id="6b0b3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b0b3-113">PARAMETERS</span></span>

### <span data-ttu-id="6b0b3-114">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6b0b3-114">-ApiVersion</span></span>
<span data-ttu-id="6b0b3-115">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-115">Specifies the version of the resource provider API to use.</span></span> <span data-ttu-id="6b0b3-116">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-116">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6b0b3-117">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="6b0b3-117">-ExtensionResourceName</span></span>
<span data-ttu-id="6b0b3-118">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-118">Specifies the name of an extension resource for the resource.</span></span> <span data-ttu-id="6b0b3-119">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="6b0b3-119">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="6b0b3-120">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="6b0b3-120">server name`/`database name</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-121">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="6b0b3-121">-ExtensionResourceType</span></span>
<span data-ttu-id="6b0b3-122">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-122">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="6b0b3-123">Ad esempio, se la risorsa di estensione è un database, specifica il tipo seguente:</span><span class="sxs-lookup"><span data-stu-id="6b0b3-123">For instance, if the extension resource is a database, specify the following type:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-124">-Force</span><span class="sxs-lookup"><span data-stu-id="6b0b3-124">-Force</span></span>
<span data-ttu-id="6b0b3-125">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-125">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6b0b3-126">-IsFullObject</span><span class="sxs-lookup"><span data-stu-id="6b0b3-126">-IsFullObject</span></span>
<span data-ttu-id="6b0b3-127">Indica che l'oggetto specificato dal parametro *Properties* è l'oggetto completo.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-127">Indicates that the object that the *Properties* parameter specifies is the full object.</span></span>

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

### <span data-ttu-id="6b0b3-128">-Tipo</span><span class="sxs-lookup"><span data-stu-id="6b0b3-128">-Kind</span></span>
<span data-ttu-id="6b0b3-129">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-129">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="6b0b3-130">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6b0b3-130">-Location</span></span>
<span data-ttu-id="6b0b3-131">Specifica la posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-131">Specifies the location of the resource.</span></span>
<span data-ttu-id="6b0b3-132">Specificare la posizione del centro dati, ad esempio Stati Uniti centrali o Asia sud-orientale.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-132">Specify data center location, such as Central US or Southeast Asia.</span></span>

<span data-ttu-id="6b0b3-133">Puoi inserire una risorsa in qualsiasi posizione che supporti le risorse del tipo.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-133">You can place a resource in any location that supports resources of that type.</span></span> <span data-ttu-id="6b0b3-134">I gruppi di risorse possono contenere risorse da posizioni diverse.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-134">Resource groups can contain resources from different locations.</span></span> <span data-ttu-id="6b0b3-135">Per determinare quali posizioni supportano ogni tipo di risorsa, usare il cmdlet Get-AzureLocation.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-135">To determine which locations support each resource type, use the Get-AzureLocation cmdlet.</span></span>

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

### <span data-ttu-id="6b0b3-136">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="6b0b3-136">-ODataQuery</span></span>
<span data-ttu-id="6b0b3-137">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="6b0b3-137">Specifies an Open Data Protocol (OData) style filter.</span></span> <span data-ttu-id="6b0b3-138">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-138">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="6b0b3-139">-Piano</span><span class="sxs-lookup"><span data-stu-id="6b0b3-139">-Plan</span></span>
<span data-ttu-id="6b0b3-140">Tabella hash che rappresenta le proprietà del piano risorse.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-140">A hash table that represents resource plan properties.</span></span>

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

### <span data-ttu-id="6b0b3-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="6b0b3-141">-Pre</span></span>
<span data-ttu-id="6b0b3-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6b0b3-143">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="6b0b3-143">-Properties</span></span>
<span data-ttu-id="6b0b3-144">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-144">Specifies resource properties for the resource.</span></span> <span data-ttu-id="6b0b3-145">Usa questo parametro per specificare i valori delle proprietà specifiche di un tipo di risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-145">Use this parameter to specify the values of properties that are specific to a resource type.</span></span>

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

### <span data-ttu-id="6b0b3-146">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b0b3-146">-ResourceGroupName</span></span>
<span data-ttu-id="6b0b3-147">Specifica il nome del gruppo di risorse in cui questo cmdlet crea la risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-147">Specifies the name of the resource group where this cmdlet creates the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-148">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6b0b3-148">-ResourceId</span></span>
<span data-ttu-id="6b0b3-149">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="6b0b3-149">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="6b0b3-150">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="6b0b3-150">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

```yaml
Type: System.String
Parameter Sets: The resource Id.
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-151">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="6b0b3-151">-ResourceName</span></span>
<span data-ttu-id="6b0b3-152">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-152">Specifies the name of the resource.</span></span> <span data-ttu-id="6b0b3-153">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="6b0b3-153">For instance, to specify a database, use the following format:</span></span>

`ContosoServer/ContosoDatabase`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-154">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="6b0b3-154">-ResourceType</span></span>
<span data-ttu-id="6b0b3-155">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-155">Specifies the type of the resource.</span></span>
<span data-ttu-id="6b0b3-156">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="6b0b3-156">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Resource that resides at the subscription level., Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-157">-SKU</span><span class="sxs-lookup"><span data-stu-id="6b0b3-157">-Sku</span></span>
<span data-ttu-id="6b0b3-158">Tabella hash che rappresenta le proprietà SKU.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-158">A hash table that represents sku properties.</span></span>

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

### <span data-ttu-id="6b0b3-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="6b0b3-159">-Tag</span></span>
<span data-ttu-id="6b0b3-160">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-160">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6b0b3-161">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="6b0b3-161">For example:</span></span>

<span data-ttu-id="6b0b3-162">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="6b0b3-162">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="6b0b3-163">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="6b0b3-163">-TenantLevel</span></span>
<span data-ttu-id="6b0b3-164">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-164">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Resource that resides at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6b0b3-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b0b3-165">-Confirm</span></span>
<span data-ttu-id="6b0b3-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b0b3-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b0b3-167">-WhatIf</span></span>
<span data-ttu-id="6b0b3-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b0b3-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b0b3-170">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b0b3-170">-DefaultProfile</span></span>
<span data-ttu-id="6b0b3-171">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-171">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b0b3-172">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b0b3-172">CommonParameters</span></span>
<span data-ttu-id="6b0b3-173">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b0b3-173">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b0b3-174">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b0b3-174">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b0b3-175">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b0b3-175">INPUTS</span></span>

## <span data-ttu-id="6b0b3-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b0b3-176">OUTPUTS</span></span>

### <span data-ttu-id="6b0b3-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="6b0b3-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6b0b3-178">Note</span><span class="sxs-lookup"><span data-stu-id="6b0b3-178">NOTES</span></span>

## <span data-ttu-id="6b0b3-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b0b3-179">RELATED LINKS</span></span>

[<span data-ttu-id="6b0b3-180">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6b0b3-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="6b0b3-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6b0b3-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="6b0b3-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6b0b3-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="6b0b3-183">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6b0b3-183">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="6b0b3-184">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="6b0b3-184">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
