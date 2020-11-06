---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: e626a57088a9c726bfe9040f76157f0b011a6405
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513015"
---
# <span data-ttu-id="70355-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="70355-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="70355-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="70355-102">SYNOPSIS</span></span>
<span data-ttu-id="70355-103">Cerca risorse in base a parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="70355-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="70355-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="70355-104">SYNTAX</span></span>

### <span data-ttu-id="70355-105">Elenca le risorse in base all'ambito specificato.</span><span class="sxs-lookup"><span data-stu-id="70355-105">Lists the resources based on the specified scope.</span></span> <span data-ttu-id="70355-106">Predefinita</span><span class="sxs-lookup"><span data-stu-id="70355-106">(Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="70355-107">Elenca le risorse in base all'ambito specificato a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="70355-107">Lists the resources based on the specified scope at the tenant level.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="70355-108">Ottenere risorse tramite una query con più abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="70355-108">Get a resources using a multi-subscription query.</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="70355-109">Elenca le risorse in base a un oggetto tag specificato come HashSet.</span><span class="sxs-lookup"><span data-stu-id="70355-109">Lists resources by a tag object specified as a hashset.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="70355-110">Elenca le risorse in base a un tag specificato come singoli parametri nome e valore.</span><span class="sxs-lookup"><span data-stu-id="70355-110">Lists resources by a tag specified as a individual name and value parameters.</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="70355-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="70355-111">DESCRIPTION</span></span>
<span data-ttu-id="70355-112">Il cmdlet **Find-AzureRmResource** Cerca le risorse in base a parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="70355-112">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="70355-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="70355-113">EXAMPLES</span></span>

### <span data-ttu-id="70355-114">Esempio 1: ricerca di risorse per tipo e nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="70355-114">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="70355-115">Questo comando consente di cercare le risorse del tipo Microsoft. Web/sites in gruppi di risorse che hanno nomi corrispondenti alla stringa ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="70355-115">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="70355-116">Esempio 2: cercare risorse per tipo e nome risorsa</span><span class="sxs-lookup"><span data-stu-id="70355-116">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="70355-117">Questo comando Cerca le risorse del tipo Microsoft. Web/Sites che hanno un nome di risorsa che corrisponde al test della stringa.</span><span class="sxs-lookup"><span data-stu-id="70355-117">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="70355-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="70355-118">PARAMETERS</span></span>

### <span data-ttu-id="70355-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="70355-119">-ApiVersion</span></span>
<span data-ttu-id="70355-120">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="70355-120">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="70355-121">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="70355-121">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="70355-122">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="70355-122">-ExpandProperties</span></span>
<span data-ttu-id="70355-123">Indica che questo cmdlet espande le proprietà della risorsa.</span><span class="sxs-lookup"><span data-stu-id="70355-123">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="70355-124">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="70355-124">-ExtensionResourceType</span></span>
<span data-ttu-id="70355-125">Specifica il tipo di risorsa di estensione per le risorse per cui questo cmdlet esegue la ricerca.</span><span class="sxs-lookup"><span data-stu-id="70355-125">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="70355-126">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="70355-126">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="70355-127">-InformationAction</span></span>
<span data-ttu-id="70355-128">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="70355-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="70355-129">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="70355-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="70355-130">Continuare</span><span class="sxs-lookup"><span data-stu-id="70355-130">Continue</span></span>
- <span data-ttu-id="70355-131">Ignora</span><span class="sxs-lookup"><span data-stu-id="70355-131">Ignore</span></span>
- <span data-ttu-id="70355-132">Informarsi</span><span class="sxs-lookup"><span data-stu-id="70355-132">Inquire</span></span>
- <span data-ttu-id="70355-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="70355-133">SilentlyContinue</span></span>
- <span data-ttu-id="70355-134">Stop</span><span class="sxs-lookup"><span data-stu-id="70355-134">Stop</span></span>
- <span data-ttu-id="70355-135">Sospensione</span><span class="sxs-lookup"><span data-stu-id="70355-135">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70355-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="70355-136">-InformationVariable</span></span>
<span data-ttu-id="70355-137">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="70355-137">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70355-138">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="70355-138">-ODataQuery</span></span>
<span data-ttu-id="70355-139">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="70355-139">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="70355-140">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="70355-140">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="70355-141">-Pre</span><span class="sxs-lookup"><span data-stu-id="70355-141">-Pre</span></span>
<span data-ttu-id="70355-142">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="70355-142">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="70355-143">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="70355-143">-ResourceGroupNameContains</span></span>
<span data-ttu-id="70355-144">Specifica un nome parziale di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="70355-144">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="70355-145">Questo cmdlet corrisponde a gruppi di risorse di cui questo valore è una sottostringa.</span><span class="sxs-lookup"><span data-stu-id="70355-145">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="70355-146">Il cmdlet cerca le risorse in tali gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="70355-146">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-147">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="70355-147">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="70355-148">Nome del gruppo di risorse per una corrispondenza completa.</span><span class="sxs-lookup"><span data-stu-id="70355-148">The resource group name for a full match.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-149">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="70355-149">-ResourceNameContains</span></span>
<span data-ttu-id="70355-150">Specifica un nome parziale di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="70355-150">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="70355-151">Il cmdlet cerca le risorse che contengono questo valore come sottostringa.</span><span class="sxs-lookup"><span data-stu-id="70355-151">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-152">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="70355-152">-ResourceNameEquals</span></span>
<span data-ttu-id="70355-153">Il nome della risorsa per una corrispondenza completa.</span><span class="sxs-lookup"><span data-stu-id="70355-153">The resource name for a full match.</span></span> <span data-ttu-id="70355-154">ad esempio, se il nome della risorsa è testResource, è possibile specificare testResource.</span><span class="sxs-lookup"><span data-stu-id="70355-154">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope., Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-155">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="70355-155">-ResourceType</span></span>
<span data-ttu-id="70355-156">Specifica il tipo di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="70355-156">Specifies the type of a resource.</span></span>
<span data-ttu-id="70355-157">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="70355-157">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="70355-158">Questo cmdlet cerca le risorse del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="70355-158">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Lists the resources based on the specified scope at the tenant level., Get a resources using a multi-subscription query.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-159">-Tag</span><span class="sxs-lookup"><span data-stu-id="70355-159">-Tag</span></span>
<span data-ttu-id="70355-160">Filtro tag per la query OData.</span><span class="sxs-lookup"><span data-stu-id="70355-160">The tag filter for the OData query.</span></span> <span data-ttu-id="70355-161">Il formato previsto è @ {tagName = $null} oppure @ {tagName =' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="70355-161">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Lists resources by a tag object specified as a hashset.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="70355-162">-TagName</span><span class="sxs-lookup"><span data-stu-id="70355-162">-TagName</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70355-163">-TagValue</span><span class="sxs-lookup"><span data-stu-id="70355-163">-TagValue</span></span>
```yaml
Type: System.String
Parameter Sets: Lists resources by a tag specified as a individual name and value parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70355-164">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="70355-164">-TenantLevel</span></span>
<span data-ttu-id="70355-165">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="70355-165">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Lists the resources based on the specified scope at the tenant level.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70355-166">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="70355-166">-Top</span></span>
<span data-ttu-id="70355-167">Specifica il numero di risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="70355-167">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="70355-168">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="70355-168">-DefaultProfile</span></span>
<span data-ttu-id="70355-169">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="70355-169">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="70355-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="70355-170">CommonParameters</span></span>
<span data-ttu-id="70355-171">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="70355-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="70355-172">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="70355-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="70355-173">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="70355-173">INPUTS</span></span>

## <span data-ttu-id="70355-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="70355-174">OUTPUTS</span></span>

### <span data-ttu-id="70355-175">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="70355-175">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="70355-176">Note</span><span class="sxs-lookup"><span data-stu-id="70355-176">NOTES</span></span>

## <span data-ttu-id="70355-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="70355-177">RELATED LINKS</span></span>

[<span data-ttu-id="70355-178">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="70355-178">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="70355-179">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="70355-179">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="70355-180">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="70355-180">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="70355-181">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="70355-181">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="70355-182">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="70355-182">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
