---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181151"
---
# <span data-ttu-id="01cac-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="01cac-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="01cac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01cac-102">SYNOPSIS</span></span>
<span data-ttu-id="01cac-103">Crea o aggiorna il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="01cac-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="01cac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="01cac-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="01cac-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="01cac-105">DESCRIPTION</span></span>
<span data-ttu-id="01cac-106">Crea o aggiorna il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="01cac-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="01cac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="01cac-107">EXAMPLES</span></span>

### <span data-ttu-id="01cac-108">Esempio 1: Creare un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="01cac-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="01cac-109">Creare un provider di risorse personalizzato</span><span class="sxs-lookup"><span data-stu-id="01cac-109">Create a custom resource provider</span></span>

### <span data-ttu-id="01cac-110">Esempio 2: Creare un provider personalizzato con associazioni</span><span class="sxs-lookup"><span data-stu-id="01cac-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="01cac-111">Creare un provider personalizzato con un percorso per le associazioni dei provider personalizzati.</span><span class="sxs-lookup"><span data-stu-id="01cac-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="01cac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01cac-112">PARAMETERS</span></span>

### <span data-ttu-id="01cac-113">-Action</span><span class="sxs-lookup"><span data-stu-id="01cac-113">-Action</span></span>
<span data-ttu-id="01cac-114">Elenco di azioni implementate dal provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="01cac-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="01cac-115">Per creare, vedere la sezione NOTE per le proprietà ACTION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="01cac-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpActionRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01cac-116">-AsJob</span></span>
<span data-ttu-id="01cac-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="01cac-117">Run the command as a job</span></span>

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

### <span data-ttu-id="01cac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01cac-118">-DefaultProfile</span></span>
<span data-ttu-id="01cac-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="01cac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-120">-Location</span><span class="sxs-lookup"><span data-stu-id="01cac-120">-Location</span></span>
<span data-ttu-id="01cac-121">Luogo della risorsa</span><span class="sxs-lookup"><span data-stu-id="01cac-121">Resource location</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-122">-Name</span><span class="sxs-lookup"><span data-stu-id="01cac-122">-Name</span></span>
<span data-ttu-id="01cac-123">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="01cac-123">The name of the resource provider.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceProviderName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="01cac-124">-NoWait</span></span>
<span data-ttu-id="01cac-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="01cac-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01cac-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01cac-126">-ResourceGroupName</span></span>
<span data-ttu-id="01cac-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="01cac-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="01cac-128">-ResourceType</span></span>
<span data-ttu-id="01cac-129">Elenco di tipi di risorse implementati dal provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="01cac-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="01cac-130">Per creare, vedere la sezione NOTE per le proprietà RESOURCETYPE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="01cac-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpResourceTypeRouteDefinition[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01cac-131">-SubscriptionId</span></span>
<span data-ttu-id="01cac-132">ID sottoscrizione di Azure.</span><span class="sxs-lookup"><span data-stu-id="01cac-132">The Azure subscription ID.</span></span>
<span data-ttu-id="01cac-133">Stringa in formato GUID, ad esempio 00000000-0000-0000-0000-0000-00000000000000</span><span class="sxs-lookup"><span data-stu-id="01cac-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="01cac-134">-Tag</span></span>
<span data-ttu-id="01cac-135">Tag di risorse</span><span class="sxs-lookup"><span data-stu-id="01cac-135">Resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-136">-Convalida</span><span class="sxs-lookup"><span data-stu-id="01cac-136">-Validation</span></span>
<span data-ttu-id="01cac-137">Elenco di convalide da eseguire sulle richieste del provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="01cac-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="01cac-138">Per creare, vedere la sezione NOTE relativa alle proprietà CONVALIDA e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="01cac-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpValidations[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01cac-139">-Confirm</span></span>
<span data-ttu-id="01cac-140">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="01cac-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01cac-141">-WhatIf</span></span>
<span data-ttu-id="01cac-142">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01cac-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01cac-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="01cac-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="01cac-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01cac-144">CommonParameters</span></span>
<span data-ttu-id="01cac-145">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01cac-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01cac-146">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="01cac-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01cac-147">INPUT</span><span class="sxs-lookup"><span data-stu-id="01cac-147">INPUTS</span></span>

## <span data-ttu-id="01cac-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="01cac-148">OUTPUTS</span></span>

### <span data-ttu-id="01cac-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="01cac-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="01cac-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="01cac-150">NOTES</span></span>

<span data-ttu-id="01cac-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="01cac-151">ALIASES</span></span>

<span data-ttu-id="01cac-152">PROPRIETÀ DEI PARAMETRI COMPLESSE</span><span class="sxs-lookup"><span data-stu-id="01cac-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01cac-153">Per creare i parametri descritti di seguito, creare una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="01cac-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01cac-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="01cac-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01cac-155">ACTION <ICustomRpActionRouteDefinition[]>: elenco di azioni che il provider di risorse personalizzato implementa.</span><span class="sxs-lookup"><span data-stu-id="01cac-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="01cac-156">`Endpoint <String>`: URI endpoint della definizione della route a cui il provider di risorse personalizzato richiederà l'accesso proxy.</span><span class="sxs-lookup"><span data-stu-id="01cac-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="01cac-157">Può essere in forma di URI flat (ad esempio ' ') o può specificare di instradare tramite un percorso https://testendpoint/ (ad esempio ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="01cac-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="01cac-158">`Name <String>`: nome della definizione di route.</span><span class="sxs-lookup"><span data-stu-id="01cac-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="01cac-159">Diventa il nome dell'estensione del ARM (ad esempio '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="01cac-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="01cac-160">`[RoutingType <ActionRouting?>]`: tipi di routing supportati per le richieste di azione.</span><span class="sxs-lookup"><span data-stu-id="01cac-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="01cac-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: elenco di tipi di risorse che il provider di risorse personalizzato implementa.</span><span class="sxs-lookup"><span data-stu-id="01cac-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="01cac-162">`Endpoint <String>`: URI endpoint della definizione della route a cui il provider di risorse personalizzato richiederà l'accesso proxy.</span><span class="sxs-lookup"><span data-stu-id="01cac-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="01cac-163">Può essere in forma di URI flat (ad esempio ' ') o può specificare di instradare tramite un percorso https://testendpoint/ (ad esempio ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="01cac-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="01cac-164">`Name <String>`: nome della definizione di route.</span><span class="sxs-lookup"><span data-stu-id="01cac-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="01cac-165">Diventa il nome dell'estensione del ARM (ad esempio '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span><span class="sxs-lookup"><span data-stu-id="01cac-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="01cac-166">`[RoutingType <ResourceTypeRouting?>]`: tipi di routing supportati per le richieste di risorse.</span><span class="sxs-lookup"><span data-stu-id="01cac-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="01cac-167">VALIDATION <ICustomRpValids[]>: elenco di convalide da eseguire nelle richieste del provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="01cac-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="01cac-168">`Specification <String>`: collegamento alla specifica di convalida.</span><span class="sxs-lookup"><span data-stu-id="01cac-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="01cac-169">La specifica deve essere ospitata in raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="01cac-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="01cac-170">`[ValidationType <ValidationType?>]`: tipo di convalida da eseguire rispetto a una richiesta corrispondente.</span><span class="sxs-lookup"><span data-stu-id="01cac-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="01cac-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="01cac-171">RELATED LINKS</span></span>

