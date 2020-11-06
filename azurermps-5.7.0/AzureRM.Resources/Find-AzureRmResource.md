---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BB90E6BB-7F53-4441-A7B2-EDA940621D49
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/find-azurermresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Find-AzureRmResource.md
ms.openlocfilehash: 67389829eb5edc5ea7ac21fcc891cc85787b5e9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518027"
---
# <span data-ttu-id="22834-101">Find-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="22834-101">Find-AzureRmResource</span></span>

## <span data-ttu-id="22834-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="22834-102">SYNOPSIS</span></span>
<span data-ttu-id="22834-103">Cerca risorse in base a parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="22834-103">Searches for resources based on specified parameters.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22834-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="22834-104">SYNTAX</span></span>

### <span data-ttu-id="22834-105">GetBySpecifiedScope (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="22834-105">GetBySpecifiedScope (Default)</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] [-ResourceType <String>]
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22834-106">GetBySpecifiedScopeAtTenantLevel</span><span class="sxs-lookup"><span data-stu-id="22834-106">GetBySpecifiedScopeAtTenantLevel</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ExpandProperties] [-TenantLevel]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22834-107">GetByMultiSubscriptionQuery</span><span class="sxs-lookup"><span data-stu-id="22834-107">GetByMultiSubscriptionQuery</span></span>
```
Find-AzureRmResource [-ResourceNameContains <String>] [-ResourceNameEquals <String>] -ResourceType <String>
 [-ExtensionResourceType <String>] [-Top <Int32>] [-ODataQuery <String>] [-ResourceGroupNameContains <String>]
 [-ResourceGroupNameEquals <String>] [-ExpandProperties] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22834-108">GetByTagObject</span><span class="sxs-lookup"><span data-stu-id="22834-108">GetByTagObject</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-Tag <Hashtable>] [-ExpandProperties]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="22834-109">GetByTagNameValue</span><span class="sxs-lookup"><span data-stu-id="22834-109">GetByTagNameValue</span></span>
```
Find-AzureRmResource [-Top <Int32>] [-ODataQuery <String>] [-TagName <String>] [-TagValue <String>]
 [-ExpandProperties] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="22834-110">Descrizione</span><span class="sxs-lookup"><span data-stu-id="22834-110">DESCRIPTION</span></span>
<span data-ttu-id="22834-111">Il cmdlet **Find-AzureRmResource** Cerca le risorse in base a parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="22834-111">The **Find-AzureRmResource** cmdlet searches for resources based on specified parameters.</span></span>

## <span data-ttu-id="22834-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="22834-112">EXAMPLES</span></span>

### <span data-ttu-id="22834-113">Esempio 1: ricerca di risorse per tipo e nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="22834-113">Example 1: Search for resources by type and resource group name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceGroupNameContains "ResourceGroup"
```

<span data-ttu-id="22834-114">Questo comando consente di cercare le risorse del tipo Microsoft. Web/sites in gruppi di risorse che hanno nomi corrispondenti alla stringa ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="22834-114">This command searches for resources of the type microsoft.web/sites under resource groups that have names that match the string ResourceGroup.</span></span>

### <span data-ttu-id="22834-115">Esempio 2: cercare risorse per tipo e nome risorsa</span><span class="sxs-lookup"><span data-stu-id="22834-115">Example 2: Search for resources by type and resource name</span></span>
```
PS C:\>Find-AzureRmResource -ResourceType "microsoft.web/sites" -ResourceNameContains "test"
```

<span data-ttu-id="22834-116">Questo comando Cerca le risorse del tipo Microsoft. Web/Sites che hanno un nome di risorsa che corrisponde al test della stringa.</span><span class="sxs-lookup"><span data-stu-id="22834-116">This command searches for resources of the type microsoft.web/sites that have a resource name that matches the string test.</span></span>

## <span data-ttu-id="22834-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="22834-117">PARAMETERS</span></span>

### <span data-ttu-id="22834-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="22834-118">-ApiVersion</span></span>
<span data-ttu-id="22834-119">Specifica la versione dell'API del provider di risorse da usare.</span><span class="sxs-lookup"><span data-stu-id="22834-119">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="22834-120">Se non specifichi una versione, questo cmdlet usa la versione più recente disponibile.</span><span class="sxs-lookup"><span data-stu-id="22834-120">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="22834-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22834-121">-DefaultProfile</span></span>
<span data-ttu-id="22834-122">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="22834-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="22834-123">-ExpandProperties</span><span class="sxs-lookup"><span data-stu-id="22834-123">-ExpandProperties</span></span>
<span data-ttu-id="22834-124">Indica che questo cmdlet espande le proprietà della risorsa.</span><span class="sxs-lookup"><span data-stu-id="22834-124">Indicates that this cmdlet expands the properties of the resource.</span></span>

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

### <span data-ttu-id="22834-125">-ExtensionResourceType</span><span class="sxs-lookup"><span data-stu-id="22834-125">-ExtensionResourceType</span></span>
<span data-ttu-id="22834-126">Specifica il tipo di risorsa di estensione per le risorse per cui questo cmdlet esegue la ricerca.</span><span class="sxs-lookup"><span data-stu-id="22834-126">Specifies the extension resource type for the resources for which this cmdlet searches.</span></span>
<span data-ttu-id="22834-127">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="22834-127">For instance:</span></span>

`Microsoft.Sql/Servers/Databases`

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-128">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="22834-128">-InformationAction</span></span>
<span data-ttu-id="22834-129">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="22834-129">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="22834-130">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="22834-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="22834-131">Continuare</span><span class="sxs-lookup"><span data-stu-id="22834-131">Continue</span></span>
- <span data-ttu-id="22834-132">Ignora</span><span class="sxs-lookup"><span data-stu-id="22834-132">Ignore</span></span>
- <span data-ttu-id="22834-133">Informarsi</span><span class="sxs-lookup"><span data-stu-id="22834-133">Inquire</span></span>
- <span data-ttu-id="22834-134">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="22834-134">SilentlyContinue</span></span>
- <span data-ttu-id="22834-135">Stop</span><span class="sxs-lookup"><span data-stu-id="22834-135">Stop</span></span>
- <span data-ttu-id="22834-136">Sospensione</span><span class="sxs-lookup"><span data-stu-id="22834-136">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22834-137">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="22834-137">-InformationVariable</span></span>
<span data-ttu-id="22834-138">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="22834-138">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22834-139">-ODataQuery</span><span class="sxs-lookup"><span data-stu-id="22834-139">-ODataQuery</span></span>
<span data-ttu-id="22834-140">Specifica un filtro di stile OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="22834-140">Specifies an Open Data Protocol (OData) style filter.</span></span>
<span data-ttu-id="22834-141">Questo cmdlet aggiunge questo valore alla richiesta oltre ad altri filtri.</span><span class="sxs-lookup"><span data-stu-id="22834-141">This cmdlet appends this value to the request in addition to any other filters.</span></span>

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

### <span data-ttu-id="22834-142">-Pre</span><span class="sxs-lookup"><span data-stu-id="22834-142">-Pre</span></span>
<span data-ttu-id="22834-143">Indica che questo cmdlet considera le versioni dell'API di pre-rilascio quando determina automaticamente la versione da usare.</span><span class="sxs-lookup"><span data-stu-id="22834-143">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="22834-144">-ResourceGroupNameContains</span><span class="sxs-lookup"><span data-stu-id="22834-144">-ResourceGroupNameContains</span></span>
<span data-ttu-id="22834-145">Specifica un nome parziale di un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="22834-145">Specifies a partial name of a resource group.</span></span>
<span data-ttu-id="22834-146">Questo cmdlet corrisponde a gruppi di risorse di cui questo valore è una sottostringa.</span><span class="sxs-lookup"><span data-stu-id="22834-146">This cmdlet matches resource groups of which this value is a substring.</span></span>
<span data-ttu-id="22834-147">Il cmdlet cerca le risorse in tali gruppi di risorse.</span><span class="sxs-lookup"><span data-stu-id="22834-147">The cmdlet searches for resources in those resource groups.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases: ResourceGroupName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-148">-ResourceGroupNameEquals</span><span class="sxs-lookup"><span data-stu-id="22834-148">-ResourceGroupNameEquals</span></span>
<span data-ttu-id="22834-149">Nome del gruppo di risorse per una corrispondenza completa.</span><span class="sxs-lookup"><span data-stu-id="22834-149">The resource group name for a full match.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-150">-ResourceNameContains</span><span class="sxs-lookup"><span data-stu-id="22834-150">-ResourceNameContains</span></span>
<span data-ttu-id="22834-151">Specifica un nome parziale di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="22834-151">Specifies a partial name of a resource.</span></span>
<span data-ttu-id="22834-152">Il cmdlet cerca le risorse che contengono questo valore come sottostringa.</span><span class="sxs-lookup"><span data-stu-id="22834-152">The cmdlet searches for resources which contain this value as a substring.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases: Name

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-153">-ResourceNameEquals</span><span class="sxs-lookup"><span data-stu-id="22834-153">-ResourceNameEquals</span></span>
<span data-ttu-id="22834-154">Il nome della risorsa per una corrispondenza completa.</span><span class="sxs-lookup"><span data-stu-id="22834-154">The resource name for a full match.</span></span> <span data-ttu-id="22834-155">ad esempio, se il nome della risorsa è testResource, è possibile specificare testResource.</span><span class="sxs-lookup"><span data-stu-id="22834-155">e.g. if your resource name is testResource, you can specify testResource.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope, GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-156">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="22834-156">-ResourceType</span></span>
<span data-ttu-id="22834-157">Specifica il tipo di una risorsa.</span><span class="sxs-lookup"><span data-stu-id="22834-157">Specifies the type of a resource.</span></span>
<span data-ttu-id="22834-158">Per un database, ad esempio, il tipo di risorsa è il seguente:</span><span class="sxs-lookup"><span data-stu-id="22834-158">For instance, for a database, the resource type is as follows:</span></span>

`Microsoft.Sql/Servers/Databases`

<span data-ttu-id="22834-159">Questo cmdlet cerca le risorse del tipo specificato.</span><span class="sxs-lookup"><span data-stu-id="22834-159">This cmdlet searches for resources of the specified type.</span></span>

```yaml
Type: String
Parameter Sets: GetBySpecifiedScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetBySpecifiedScopeAtTenantLevel, GetByMultiSubscriptionQuery
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-160">-Tag</span><span class="sxs-lookup"><span data-stu-id="22834-160">-Tag</span></span>
<span data-ttu-id="22834-161">Filtro tag per la query OData.</span><span class="sxs-lookup"><span data-stu-id="22834-161">The tag filter for the OData query.</span></span> <span data-ttu-id="22834-162">Il formato previsto è @ {tagName = $null} oppure @ {tagName =' tagValue '}.</span><span class="sxs-lookup"><span data-stu-id="22834-162">The expected format is @{tagName=$null} or @{tagName = 'tagValue'}.</span></span>

```yaml
Type: Hashtable
Parameter Sets: GetByTagObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22834-163">-TagName</span><span class="sxs-lookup"><span data-stu-id="22834-163">-TagName</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22834-164">-TagValue</span><span class="sxs-lookup"><span data-stu-id="22834-164">-TagValue</span></span>
```yaml
Type: String
Parameter Sets: GetByTagNameValue
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22834-165">-TenantLevel</span><span class="sxs-lookup"><span data-stu-id="22834-165">-TenantLevel</span></span>
<span data-ttu-id="22834-166">Indica che il cmdlet funziona a livello di tenant.</span><span class="sxs-lookup"><span data-stu-id="22834-166">Indicates that this cmdlet operates at the tenant level.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: GetBySpecifiedScopeAtTenantLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22834-167">-Inizio pagina</span><span class="sxs-lookup"><span data-stu-id="22834-167">-Top</span></span>
<span data-ttu-id="22834-168">Specifica il numero di risorse da recuperare.</span><span class="sxs-lookup"><span data-stu-id="22834-168">Specifies the number of resources to retrieve.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22834-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22834-169">CommonParameters</span></span>
<span data-ttu-id="22834-170">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22834-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22834-171">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22834-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22834-172">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="22834-172">INPUTS</span></span>

### <span data-ttu-id="22834-173">Nessuno</span><span class="sxs-lookup"><span data-stu-id="22834-173">None</span></span>
<span data-ttu-id="22834-174">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="22834-174">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22834-175">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="22834-175">OUTPUTS</span></span>

### <span data-ttu-id="22834-176">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="22834-176">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="22834-177">Note</span><span class="sxs-lookup"><span data-stu-id="22834-177">NOTES</span></span>

## <span data-ttu-id="22834-178">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="22834-178">RELATED LINKS</span></span>

[<span data-ttu-id="22834-179">Get-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="22834-179">Get-AzureRmResource</span></span>](./Get-AzureRmResource.md)

[<span data-ttu-id="22834-180">Move-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="22834-180">Move-AzureRmResource</span></span>](./Move-AzureRmResource.md)

[<span data-ttu-id="22834-181">New-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="22834-181">New-AzureRmResource</span></span>](./New-AzureRmResource.md)

[<span data-ttu-id="22834-182">Remove-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="22834-182">Remove-AzureRmResource</span></span>](./Remove-AzureRmResource.md)

[<span data-ttu-id="22834-183">Set-AzureRmResource</span><span class="sxs-lookup"><span data-stu-id="22834-183">Set-AzureRmResource</span></span>](./Set-AzureRmResource.md)
