---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: d3e7a1e947eb03c52c2cd8e032a359eb7765be03
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687696"
---
# <span data-ttu-id="be7cf-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="be7cf-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="be7cf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be7cf-102">SYNOPSIS</span></span>
<span data-ttu-id="be7cf-103">Modifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="be7cf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be7cf-104">SYNTAX</span></span>

### <span data-ttu-id="be7cf-105">ID risorsa (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be7cf-105">The resource Id. (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be7cf-106">Risorsa che risiede a livello di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="be7cf-106">Resource that resides at the subscription level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be7cf-107">Risorsa che risiede a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="be7cf-107">Resource that resides at the tenant level.</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be7cf-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be7cf-108">DESCRIPTION</span></span>
<span data-ttu-id="be7cf-109">Il cmdlet **set-AzureRmResource** modifica una risorsa Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="be7cf-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="be7cf-110">Specificare una risorsa da modificare per nome e tipo oppure per ID.</span><span class="sxs-lookup"><span data-stu-id="be7cf-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="be7cf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be7cf-111">EXAMPLES</span></span>

### <span data-ttu-id="be7cf-112">Esempio 1: modificare una risorsa</span><span class="sxs-lookup"><span data-stu-id="be7cf-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="be7cf-113">Il primo comando ottiene la risorsa denominata ContosoSite usando il cmdlet Get-AzureRmResource e lo archivia nella variabile $Resource.</span><span class="sxs-lookup"><span data-stu-id="be7cf-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="be7cf-114">Il secondo comando modifica una proprietà di $Resource.</span><span class="sxs-lookup"><span data-stu-id="be7cf-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="be7cf-115">Il comando finale aggiorna la risorsa in base alla $Resource.</span><span class="sxs-lookup"><span data-stu-id="be7cf-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="be7cf-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be7cf-116">PARAMETERS</span></span>

### <span data-ttu-id="be7cf-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="be7cf-117">-ApiVersion</span></span>
<span data-ttu-id="be7cf-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="be7cf-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="be7cf-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="be7cf-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="be7cf-120">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="be7cf-120">-ExtensionResourceName</span></span>
<span data-ttu-id="be7cf-121">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-121">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="be7cf-122">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="be7cf-122">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="be7cf-123">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="be7cf-123">server name`/`database name</span></span>

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

### <span data-ttu-id="be7cf-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="be7cf-124">-ExtensionResourceType</span></span>
<span data-ttu-id="be7cf-125">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="be7cf-125">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="be7cf-126">Ad esempio, se la risorsa di estensione è un database, specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="be7cf-126">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="be7cf-127">-Force</span><span class="sxs-lookup"><span data-stu-id="be7cf-127">-Force</span></span>
<span data-ttu-id="be7cf-128">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="be7cf-128">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="be7cf-129">-Tipo</span><span class="sxs-lookup"><span data-stu-id="be7cf-129">-Kind</span></span>
<span data-ttu-id="be7cf-130">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-130">Specifies the resource kind for the resource.</span></span>

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

### <span data-ttu-id="be7cf-131">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="be7cf-131">-ODataQuery</span></span>
<span data-ttu-id="be7cf-132">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="be7cf-132">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="be7cf-133">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="be7cf-133">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="be7cf-134">-Piano</span><span class="sxs-lookup"><span data-stu-id="be7cf-134">-Plan</span></span>
<span data-ttu-id="be7cf-135">Specifica le proprietà del piano di risorse, come tabella hash, per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-135">Specifies resource plan properties, as a hash table, for the resource.</span></span>

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

### <span data-ttu-id="be7cf-136">-Pre</span><span class="sxs-lookup"><span data-stu-id="be7cf-136">-Pre</span></span>
<span data-ttu-id="be7cf-137">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="be7cf-137">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="be7cf-138">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="be7cf-138">-Properties</span></span>
<span data-ttu-id="be7cf-139">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-139">Specifies resource properties for the resource.</span></span>

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

### <span data-ttu-id="be7cf-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be7cf-140">-ResourceGroupName</span></span>
<span data-ttu-id="be7cf-141">Specifica il nome del gruppo di risorse in cui questo cmdlet modifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-141">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="be7cf-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="be7cf-142">-ResourceId</span></span>
<span data-ttu-id="be7cf-143">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="be7cf-143">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="be7cf-144">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="be7cf-144">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="be7cf-145">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="be7cf-145">-ResourceName</span></span>
<span data-ttu-id="be7cf-146">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-146">Specifies the name of the resource.</span></span>
<span data-ttu-id="be7cf-147">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="be7cf-147">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="be7cf-148">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="be7cf-148">-ResourceType</span></span>
<span data-ttu-id="be7cf-149">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="be7cf-149">Specifies the type of the resource.</span></span>
<span data-ttu-id="be7cf-150">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="be7cf-150">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="be7cf-151">-SKU</span><span class="sxs-lookup"><span data-stu-id="be7cf-151">-Sku</span></span>
<span data-ttu-id="be7cf-152">Specifica l'oggetto SKU della risorsa come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="be7cf-152">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="be7cf-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="be7cf-153">-Tag</span></span>
<span data-ttu-id="be7cf-154">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="be7cf-154">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="be7cf-155">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="be7cf-155">For example:</span></span>

<span data-ttu-id="be7cf-156">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="be7cf-156">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="be7cf-157">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="be7cf-157">-TenantLevel</span></span>
<span data-ttu-id="be7cf-158">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="be7cf-158">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="be7cf-159">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="be7cf-159">-UsePatchSemantics</span></span>
<span data-ttu-id="be7cf-160">Indica che questo cmdlet usa una PATCH HTTP per aggiornare l'oggetto, invece di un post HTTP.</span><span class="sxs-lookup"><span data-stu-id="be7cf-160">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="be7cf-161">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be7cf-161">-Confirm</span></span>
<span data-ttu-id="be7cf-162">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be7cf-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be7cf-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be7cf-163">-WhatIf</span></span>
<span data-ttu-id="be7cf-164">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be7cf-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be7cf-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be7cf-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be7cf-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be7cf-166">-DefaultProfile</span></span>
<span data-ttu-id="be7cf-167">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be7cf-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be7cf-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be7cf-168">CommonParameters</span></span>
<span data-ttu-id="be7cf-169">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be7cf-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be7cf-170">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be7cf-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be7cf-171">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be7cf-171">INPUTS</span></span>

## <span data-ttu-id="be7cf-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be7cf-172">OUTPUTS</span></span>

### <span data-ttu-id="be7cf-173">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="be7cf-173">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="be7cf-174">Note</span><span class="sxs-lookup"><span data-stu-id="be7cf-174">NOTES</span></span>

## <span data-ttu-id="be7cf-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be7cf-175">RELATED LINKS</span></span>

[<span data-ttu-id="be7cf-176">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="be7cf-176">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="be7cf-177">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="be7cf-177">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="be7cf-178">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="be7cf-178">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="be7cf-179">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="be7cf-179">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="be7cf-180">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="be7cf-180">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
