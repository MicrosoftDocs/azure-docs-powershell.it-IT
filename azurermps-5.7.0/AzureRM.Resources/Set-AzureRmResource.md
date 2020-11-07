---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: A00160B9-831F-4A20-8D9D-9E89BC4F5C91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmResource.md
ms.openlocfilehash: 9b1f12060ca7cc161f4f7fbe7c99948d9ddd10f8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687462"
---
# <span data-ttu-id="36eca-101">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="36eca-101">Set-AzureRmResource</span></span>

## <span data-ttu-id="36eca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36eca-102">SYNOPSIS</span></span>
<span data-ttu-id="36eca-103">Modifica una risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-103">Modifies a resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36eca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36eca-104">SYNTAX</span></span>

### <span data-ttu-id="36eca-105">ByResourceId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="36eca-105">ByResourceId (Default)</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceId <String> [-ODataQuery <String>] [-Force]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="36eca-106">BySubscriptionLevel</span><span class="sxs-lookup"><span data-stu-id="36eca-106">BySubscriptionLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>]
 [-ResourceGroupName <String>] [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36eca-107">ByTenantLevel</span><span class="sxs-lookup"><span data-stu-id="36eca-107">ByTenantLevel</span></span>
```
Set-AzureRmResource [-Kind <String>] [-Properties <PSObject>] [-Plan <Hashtable>] [-Sku <Hashtable>]
 [-Tag <Hashtable>] [-UsePatchSemantics] [-AsJob] -ResourceName <String> -ResourceType <String>
 [-ExtensionResourceName <String>] [-ExtensionResourceType <String>] [-ODataQuery <String>] [-TenantLevel]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="36eca-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36eca-108">DESCRIPTION</span></span>
<span data-ttu-id="36eca-109">Il cmdlet **set-AzureRmResource** modifica una risorsa Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="36eca-109">The **Set-AzureRmResource** cmdlet modifies an existing Azure resource.</span></span>
<span data-ttu-id="36eca-110">Specificare una risorsa da modificare per nome e tipo oppure per ID.</span><span class="sxs-lookup"><span data-stu-id="36eca-110">Specify a resource to modify by name and type or by ID.</span></span>

## <span data-ttu-id="36eca-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36eca-111">EXAMPLES</span></span>

### <span data-ttu-id="36eca-112">Esempio 1: modificare una risorsa</span><span class="sxs-lookup"><span data-stu-id="36eca-112">Example 1: Modify a resource</span></span>
```
PS C:\>$Resource = Get-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupName "ResourceGroup11" -ResourceName "ContosoSite"
PS C:\> $Resource.Properties.Enabled = "False"
PS C:\> $Resource | Set-AzureRmResource -Force
```

<span data-ttu-id="36eca-113">Il primo comando ottiene la risorsa denominata ContosoSite usando il cmdlet Get-AzureRmResource e lo archivia nella variabile $Resource.</span><span class="sxs-lookup"><span data-stu-id="36eca-113">The first command gets the resource named ContosoSite by using the Get-AzureRmResource cmdlet, and then stores it in the $Resource variable.</span></span>

<span data-ttu-id="36eca-114">Il secondo comando modifica una proprietà di $Resource.</span><span class="sxs-lookup"><span data-stu-id="36eca-114">The second command modifies a property of $Resource.</span></span>

<span data-ttu-id="36eca-115">Il comando finale aggiorna la risorsa in base alla $Resource.</span><span class="sxs-lookup"><span data-stu-id="36eca-115">The final command updates the resource to match $Resource.</span></span>

## <span data-ttu-id="36eca-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36eca-116">PARAMETERS</span></span>

### <span data-ttu-id="36eca-117">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="36eca-117">-ApiVersion</span></span>
<span data-ttu-id="36eca-118">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="36eca-118">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="36eca-119">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="36eca-119">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="36eca-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="36eca-120">-AsJob</span></span>
<span data-ttu-id="36eca-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="36eca-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="36eca-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36eca-122">-DefaultProfile</span></span>
<span data-ttu-id="36eca-123">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="36eca-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36eca-124">-ExtensionResourceName</span><span class="sxs-lookup"><span data-stu-id="36eca-124">-ExtensionResourceName</span></span>
<span data-ttu-id="36eca-125">Specifica il nome di una risorsa di estensione per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-125">Specifies the name of an extension resource for the resource.</span></span>
<span data-ttu-id="36eca-126">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="36eca-126">For instance, to specify a database, use the following format:</span></span>

<span data-ttu-id="36eca-127">nome del database del nome del server `/`</span><span class="sxs-lookup"><span data-stu-id="36eca-127">server name`/`database name</span></span>

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

### <span data-ttu-id="36eca-128">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="36eca-128">-ExtensionResourceType</span></span>
<span data-ttu-id="36eca-129">Specifica il tipo di risorsa per una risorsa di estensione.</span><span class="sxs-lookup"><span data-stu-id="36eca-129">Specifies the resource type for an extension resource.</span></span>
<span data-ttu-id="36eca-130">Ad esempio, se la risorsa di estensione è un database, specificare quanto segue:</span><span class="sxs-lookup"><span data-stu-id="36eca-130">For instance, if the extension resource is a database specify the following:</span></span>

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

### <span data-ttu-id="36eca-131">-Force</span><span class="sxs-lookup"><span data-stu-id="36eca-131">-Force</span></span>
<span data-ttu-id="36eca-132">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="36eca-132">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="36eca-133">-Tipo</span><span class="sxs-lookup"><span data-stu-id="36eca-133">-Kind</span></span>
<span data-ttu-id="36eca-134">Specifica il tipo di risorsa per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-134">Specifies the resource kind for the resource.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36eca-135">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="36eca-135">-ODataQuery</span></span>
<span data-ttu-id="36eca-136">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="36eca-136">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="36eca-137">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="36eca-137">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="36eca-138">-Piano</span><span class="sxs-lookup"><span data-stu-id="36eca-138">-Plan</span></span>
<span data-ttu-id="36eca-139">Specifica le proprietà del piano di risorse, come tabella hash, per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-139">Specifies resource plan properties, as a hash table, for the resource.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: PlanObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36eca-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="36eca-140">-Pre</span></span>
<span data-ttu-id="36eca-141">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="36eca-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="36eca-142">-Proprietà</span><span class="sxs-lookup"><span data-stu-id="36eca-142">-Properties</span></span>
<span data-ttu-id="36eca-143">Specifica le proprietà delle risorse per la risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-143">Specifies resource properties for the resource.</span></span>

```yaml
Type: PSObject
Parameter Sets: (All)
Aliases: PropertyObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36eca-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36eca-144">-ResourceGroupName</span></span>
<span data-ttu-id="36eca-145">Specifica il nome del gruppo di risorse in cui questo cmdlet modifica la risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-145">Specifies the name of the resource group where this cmdlet modifies the resource.</span></span>

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

### <span data-ttu-id="36eca-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="36eca-146">-ResourceId</span></span>
<span data-ttu-id="36eca-147">Specifica l'ID risorsa completo, incluso l'abbonamento, come nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="36eca-147">Specifies the fully qualified resource ID, including the subscription, as in the following example:</span></span>

<span data-ttu-id="36eca-148">`/subscriptions/`ID abbonamento`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span><span class="sxs-lookup"><span data-stu-id="36eca-148">`/subscriptions/`subscription ID`/providers/Microsoft.Sql/servers/ContosoServer/databases/ContosoDatabase`</span></span>

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

### <span data-ttu-id="36eca-149">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="36eca-149">-ResourceName</span></span>
<span data-ttu-id="36eca-150">Specifica il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-150">Specifies the name of the resource.</span></span>
<span data-ttu-id="36eca-151">Ad esempio, per specificare un database, usa il formato seguente:</span><span class="sxs-lookup"><span data-stu-id="36eca-151">For instance, to specify a database, use the following format:</span></span>

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

### <span data-ttu-id="36eca-152">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="36eca-152">-ResourceType</span></span>
<span data-ttu-id="36eca-153">Specifica il tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="36eca-153">Specifies the type of the resource.</span></span>
<span data-ttu-id="36eca-154">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="36eca-154">For instance, for a database, the resource type is as follows:</span></span>

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

### <span data-ttu-id="36eca-155">-SKU</span><span class="sxs-lookup"><span data-stu-id="36eca-155">-Sku</span></span>
<span data-ttu-id="36eca-156">Specifica l'oggetto SKU della risorsa come tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36eca-156">Specifies the SKU object of the resource as a hash table.</span></span>

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

### <span data-ttu-id="36eca-157">-Tag</span><span class="sxs-lookup"><span data-stu-id="36eca-157">-Tag</span></span>
<span data-ttu-id="36eca-158">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="36eca-158">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="36eca-159">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="36eca-159">For example:</span></span>

<span data-ttu-id="36eca-160">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="36eca-160">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36eca-161">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="36eca-161">-TenantLevel</span></span>
<span data-ttu-id="36eca-162">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="36eca-162">Indicates that this cmdlet operates at the tenant level.</span></span>

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

### <span data-ttu-id="36eca-163">-UsePatchSemantics</span><span class="sxs-lookup"><span data-stu-id="36eca-163">-UsePatchSemantics</span></span>
<span data-ttu-id="36eca-164">Indica che questo cmdlet usa una PATCH HTTP per aggiornare l'oggetto, invece di un post HTTP.</span><span class="sxs-lookup"><span data-stu-id="36eca-164">Indicates that this cmdlet uses an HTTP PATCH to update the object, instead of an HTTP PUT.</span></span>

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

### <span data-ttu-id="36eca-165">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36eca-165">-Confirm</span></span>
<span data-ttu-id="36eca-166">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36eca-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36eca-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36eca-167">-WhatIf</span></span>
<span data-ttu-id="36eca-168">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36eca-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36eca-169">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36eca-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36eca-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36eca-170">CommonParameters</span></span>
<span data-ttu-id="36eca-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36eca-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36eca-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36eca-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36eca-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36eca-173">INPUTS</span></span>

### <span data-ttu-id="36eca-174">Nessuno</span><span class="sxs-lookup"><span data-stu-id="36eca-174">None</span></span>
<span data-ttu-id="36eca-175">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="36eca-175">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="36eca-176">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36eca-176">OUTPUTS</span></span>

### <span data-ttu-id="36eca-177">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="36eca-177">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="36eca-178">Note</span><span class="sxs-lookup"><span data-stu-id="36eca-178">NOTES</span></span>

## <span data-ttu-id="36eca-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36eca-179">RELATED LINKS</span></span>

[<span data-ttu-id="36eca-180">Trova-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="36eca-180">Find-AzureRmResource</span></span>](./Find-AzureRmResource.md)

[<span data-ttu-id="36eca-181">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="36eca-181">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="36eca-182">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="36eca-182">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="36eca-183">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="36eca-183">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="36eca-184">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="36eca-184">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)
