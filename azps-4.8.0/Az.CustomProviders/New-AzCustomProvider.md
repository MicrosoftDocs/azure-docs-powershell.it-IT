---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/en-us/powershell/module/az.customproviders/new-azcustomprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProvider.md
ms.openlocfilehash: 7f91fee2e8cc772be291662af325fd87edebdfd9
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192558"
---
# <span data-ttu-id="ee0f1-101">New-AzCustomProvider</span><span class="sxs-lookup"><span data-stu-id="ee0f1-101">New-AzCustomProvider</span></span>

## <span data-ttu-id="ee0f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ee0f1-102">SYNOPSIS</span></span>
<span data-ttu-id="ee0f1-103">Crea o aggiorna il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-103">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="ee0f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee0f1-104">SYNTAX</span></span>

```
New-AzCustomProvider -Name <String> -ResourceGroupName <String> -Location <String> [-SubscriptionId <String>]
 [-Action <ICustomRpActionRouteDefinition[]>] [-ResourceType <ICustomRpResourceTypeRouteDefinition[]>]
 [-Tag <Hashtable>] [-Validation <ICustomRpValidations[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ee0f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ee0f1-105">DESCRIPTION</span></span>
<span data-ttu-id="ee0f1-106">Crea o aggiorna il provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-106">Creates or updates the custom resource provider.</span></span>

## <span data-ttu-id="ee0f1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee0f1-107">EXAMPLES</span></span>

### <span data-ttu-id="ee0f1-108">Esempio 1: creare un provider personalizzato</span><span class="sxs-lookup"><span data-stu-id="ee0f1-108">Example 1: Create a custom provider</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}


Location  Name             Type
--------  ----             ----
West US 2 Namespace.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="ee0f1-109">Creare un provider di risorse personalizzato</span><span class="sxs-lookup"><span data-stu-id="ee0f1-109">Create a custom resource provider</span></span>

### <span data-ttu-id="ee0f1-110">Esempio 2: creare un provider personalizzato con le associazioni</span><span class="sxs-lookup"><span data-stu-id="ee0f1-110">Example 2: Create a custom provider with associations</span></span>
```powershell
PS C:\> New-AzCustomProvider -ResourceGroupName myRG -Name Namespace2.Type -Location "West US 2" -ResourceType @{Name="CustomRoute1"; Endpoint="https://www.contoso.com/"}, @{Name="Associations"; Endpoint="https://contoso.com/myService", RoutingType="Proxy,Cache,Extension"}

Location  Name             Type
--------  ----             ----
West US 2 Namespace2.Type   Microsoft.CustomProviders/resourceproviders
```

<span data-ttu-id="ee0f1-111">Creare un provider personalizzato con una route per le associazioni di provider personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-111">Create a custom provider, with a route for Custom provider associations.</span></span>

## <span data-ttu-id="ee0f1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee0f1-112">PARAMETERS</span></span>

### <span data-ttu-id="ee0f1-113">-Azione</span><span class="sxs-lookup"><span data-stu-id="ee0f1-113">-Action</span></span>
<span data-ttu-id="ee0f1-114">Elenco di azioni implementate dal provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-114">A list of actions that the custom resource provider implements.</span></span>
<span data-ttu-id="ee0f1-115">Per costruire, vedere la sezione Note per le proprietà delle azioni e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-115">To construct, see NOTES section for ACTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee0f1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee0f1-116">-AsJob</span></span>
<span data-ttu-id="ee0f1-117">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ee0f1-117">Run the command as a job</span></span>

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

### <span data-ttu-id="ee0f1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee0f1-118">-DefaultProfile</span></span>
<span data-ttu-id="ee0f1-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee0f1-120">-Posizione</span><span class="sxs-lookup"><span data-stu-id="ee0f1-120">-Location</span></span>
<span data-ttu-id="ee0f1-121">Posizione delle risorse</span><span class="sxs-lookup"><span data-stu-id="ee0f1-121">Resource location</span></span>

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

### <span data-ttu-id="ee0f1-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ee0f1-122">-Name</span></span>
<span data-ttu-id="ee0f1-123">Nome del provider di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-123">The name of the resource provider.</span></span>

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

### <span data-ttu-id="ee0f1-124">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="ee0f1-124">-NoWait</span></span>
<span data-ttu-id="ee0f1-125">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ee0f1-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ee0f1-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee0f1-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee0f1-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-127">The name of the resource group.</span></span>

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

### <span data-ttu-id="ee0f1-128">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="ee0f1-128">-ResourceType</span></span>
<span data-ttu-id="ee0f1-129">Elenco dei tipi di risorsa implementati dal provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-129">A list of resource types that the custom resource provider implements.</span></span>
<span data-ttu-id="ee0f1-130">Per costruire, vedere la sezione Note per le proprietà RESOURCETYPE e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-130">To construct, see NOTES section for RESOURCETYPE properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee0f1-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ee0f1-131">-SubscriptionId</span></span>
<span data-ttu-id="ee0f1-132">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-132">The Azure subscription ID.</span></span>
<span data-ttu-id="ee0f1-133">Si tratta di una stringa formattata con GUID (ad esempio 00000000-0000-0000-0000-000000000000)</span><span class="sxs-lookup"><span data-stu-id="ee0f1-133">This is a GUID-formatted string (e.g. 00000000-0000-0000-0000-000000000000)</span></span>

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

### <span data-ttu-id="ee0f1-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="ee0f1-134">-Tag</span></span>
<span data-ttu-id="ee0f1-135">Tag delle risorse</span><span class="sxs-lookup"><span data-stu-id="ee0f1-135">Resource tags</span></span>

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

### <span data-ttu-id="ee0f1-136">-Convalida</span><span class="sxs-lookup"><span data-stu-id="ee0f1-136">-Validation</span></span>
<span data-ttu-id="ee0f1-137">Elenco delle convalide da eseguire nelle richieste del provider di risorse personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-137">A list of validations to run on the custom resource provider's requests.</span></span>
<span data-ttu-id="ee0f1-138">Per costruire, vedere la sezione Note per le proprietà di convalida e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-138">To construct, see NOTES section for VALIDATION properties and create a hash table.</span></span>

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

### <span data-ttu-id="ee0f1-139">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ee0f1-139">-Confirm</span></span>
<span data-ttu-id="ee0f1-140">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee0f1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee0f1-141">-WhatIf</span></span>
<span data-ttu-id="ee0f1-142">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee0f1-143">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee0f1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee0f1-144">CommonParameters</span></span>
<span data-ttu-id="ee0f1-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee0f1-146">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee0f1-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee0f1-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ee0f1-147">INPUTS</span></span>

## <span data-ttu-id="ee0f1-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee0f1-148">OUTPUTS</span></span>

### <span data-ttu-id="ee0f1-149">Microsoft. Azure. PowerShell. Cmdlets. CustomProviders. Models. Api20180901Preview. ICustomRpManifest</span><span class="sxs-lookup"><span data-stu-id="ee0f1-149">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.ICustomRpManifest</span></span>

## <span data-ttu-id="ee0f1-150">Note</span><span class="sxs-lookup"><span data-stu-id="ee0f1-150">NOTES</span></span>

<span data-ttu-id="ee0f1-151">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ee0f1-151">ALIASES</span></span>

<span data-ttu-id="ee0f1-152">PROPRIETÀ COMPLESSE DI PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ee0f1-152">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="ee0f1-153">Per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-153">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="ee0f1-154">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-154">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="ee0f1-155">ACTION <ICustomRpActionRouteDefinition [] >: elenco delle azioni implementate dal provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-155">ACTION <ICustomRpActionRouteDefinition[]>: A list of actions that the custom resource provider implements.</span></span>
  - <span data-ttu-id="ee0f1-156">`Endpoint <String>`: L'URI dell'endpoint della definizione della route a cui il provider di risorse personalizzato invierà richieste proxy.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-156">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="ee0f1-157">Può essere nella forma di un URI Flat (ad esempio,' https://testendpoint/ ') o può specificare di instradare tramite un percorso (ad esempio ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="ee0f1-157">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="ee0f1-158">`Name <String>`: Nome della definizione della route.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-158">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="ee0f1-159">Questo diventa il nome dell'estensione ARM (ad esempio, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="ee0f1-159">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="ee0f1-160">`[RoutingType <ActionRouting?>]`: I tipi di routing supportati per le richieste di azione.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-160">`[RoutingType <ActionRouting?>]`: The routing types that are supported for action requests.</span></span>

<span data-ttu-id="ee0f1-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition [] >: elenco dei tipi di risorsa implementati dal provider di risorse personalizzato.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-161">RESOURCETYPE <ICustomRpResourceTypeRouteDefinition[]>: A list of resource types that the custom resource provider implements.</span></span>
  - <span data-ttu-id="ee0f1-162">`Endpoint <String>`: L'URI dell'endpoint della definizione della route a cui il provider di risorse personalizzato invierà richieste proxy.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-162">`Endpoint <String>`: The route definition endpoint URI that the custom resource provider will proxy requests to.</span></span> <span data-ttu-id="ee0f1-163">Può essere nella forma di un URI Flat (ad esempio,' https://testendpoint/ ') o può specificare di instradare tramite un percorso (ad esempio ' https://testendpoint/{requestPath} ')</span><span class="sxs-lookup"><span data-stu-id="ee0f1-163">This can be in the form of a flat URI (e.g. 'https://testendpoint/') or can specify to route via a path (e.g. 'https://testendpoint/{requestPath}')</span></span>
  - <span data-ttu-id="ee0f1-164">`Name <String>`: Nome della definizione della route.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-164">`Name <String>`: The name of the route definition.</span></span> <span data-ttu-id="ee0f1-165">Questo diventa il nome dell'estensione ARM (ad esempio, "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}")</span><span class="sxs-lookup"><span data-stu-id="ee0f1-165">This becomes the name for the ARM extension (e.g. '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.CustomProviders/resourceProviders/{resourceProviderName}/{name}')</span></span>
  - <span data-ttu-id="ee0f1-166">`[RoutingType <ResourceTypeRouting?>]`: I tipi di routing supportati per le richieste di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-166">`[RoutingType <ResourceTypeRouting?>]`: The routing types that are supported for resource requests.</span></span>

<span data-ttu-id="ee0f1-167">VALIDATION <ICustomRpValidations [] >: elenco delle convalide da eseguire nelle richieste del provider di risorse personalizzate.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-167">VALIDATION <ICustomRpValidations[]>: A list of validations to run on the custom resource provider's requests.</span></span>
  - <span data-ttu-id="ee0f1-168">`Specification <String>`: Collegamento alla specifica di convalida.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-168">`Specification <String>`: A link to the validation specification.</span></span> <span data-ttu-id="ee0f1-169">La specifica deve essere ospitata in raw.githubusercontent.com.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-169">The specification must be hosted on raw.githubusercontent.com.</span></span>
  - <span data-ttu-id="ee0f1-170">`[ValidationType <ValidationType?>]`: Il tipo di convalida da eseguire in corrispondenza di una richiesta corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ee0f1-170">`[ValidationType <ValidationType?>]`: The type of validation to run against a matching request.</span></span>

## <span data-ttu-id="ee0f1-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee0f1-171">RELATED LINKS</span></span>

