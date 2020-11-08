---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: fcf6254cfbb29add4990197dddf3fb188e665937
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030619"
---
# <span data-ttu-id="47ef6-101">Set-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="47ef6-101">Set-AzsUserSubscription</span></span>

## <span data-ttu-id="47ef6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="47ef6-102">SYNOPSIS</span></span>
<span data-ttu-id="47ef6-103">Crea o aggiorna l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="47ef6-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="47ef6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47ef6-104">SYNTAX</span></span>

### <span data-ttu-id="47ef6-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47ef6-105">UpdateExpanded (Default)</span></span>
```
Set-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-OfferId <String>] [-Owner <String>] [-RoutingResourceManagerType <ResourceManagerType>]
 [-State <SubscriptionState>] [-SubscriptionId1 <String>] [-TenantId <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="47ef6-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="47ef6-106">Update</span></span>
```
Set-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="47ef6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="47ef6-107">DESCRIPTION</span></span>
<span data-ttu-id="47ef6-108">Crea o aggiorna l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="47ef6-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="47ef6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47ef6-109">EXAMPLES</span></span>

### <span data-ttu-id="47ef6-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47ef6-110">Example 1</span></span>
```powershell
PS C:\> $Subscription = Get-AzsUserSubscription | Select-Object -First 1
$Subscription.DisplayName = 'Update User Subscription'
$Subscription | Set-AzsUserSubscription | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : Update User Subscription
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="47ef6-111">Aggiorna un abbonamento</span><span class="sxs-lookup"><span data-stu-id="47ef6-111">Updates a subscription</span></span>

## <span data-ttu-id="47ef6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="47ef6-112">PARAMETERS</span></span>

### <span data-ttu-id="47ef6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47ef6-113">-DefaultProfile</span></span>
<span data-ttu-id="47ef6-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47ef6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47ef6-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ef6-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="47ef6-116">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="47ef6-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="47ef6-117">-DisplayName</span></span>
<span data-ttu-id="47ef6-118">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47ef6-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="47ef6-119">-ExternalReferenceId</span></span>
<span data-ttu-id="47ef6-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="47ef6-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-121">-ID</span><span class="sxs-lookup"><span data-stu-id="47ef6-121">-Id</span></span>
<span data-ttu-id="47ef6-122">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="47ef6-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-123">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="47ef6-123">-OfferId</span></span>
<span data-ttu-id="47ef6-124">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="47ef6-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-125">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="47ef6-125">-Owner</span></span>
<span data-ttu-id="47ef6-126">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47ef6-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="47ef6-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="47ef6-128">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="47ef6-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="47ef6-129">-State</span></span>
<span data-ttu-id="47ef6-130">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="47ef6-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="47ef6-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="47ef6-132">Proprietà dell'oggetto Subscription.</span><span class="sxs-lookup"><span data-stu-id="47ef6-132">Subscription object properties.</span></span>
<span data-ttu-id="47ef6-133">Per costruire, vedere la sezione Note per le proprietà di SUBSCRIPTIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="47ef6-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-134">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ef6-134">-SubscriptionId</span></span>
<span data-ttu-id="47ef6-135">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="47ef6-135">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="47ef6-136">-SubscriptionId1</span><span class="sxs-lookup"><span data-stu-id="47ef6-136">-SubscriptionId1</span></span>
<span data-ttu-id="47ef6-137">Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47ef6-137">Subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-138">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="47ef6-138">-TargetSubscriptionId</span></span>
<span data-ttu-id="47ef6-139">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="47ef6-139">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-140">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="47ef6-140">-TenantId</span></span>
<span data-ttu-id="47ef6-141">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="47ef6-141">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="47ef6-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="47ef6-142">-Confirm</span></span>
<span data-ttu-id="47ef6-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47ef6-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47ef6-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47ef6-144">-WhatIf</span></span>
<span data-ttu-id="47ef6-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47ef6-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47ef6-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47ef6-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47ef6-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47ef6-147">CommonParameters</span></span>
<span data-ttu-id="47ef6-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47ef6-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47ef6-149">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47ef6-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47ef6-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="47ef6-150">INPUTS</span></span>

### <span data-ttu-id="47ef6-151">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="47ef6-151">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="47ef6-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47ef6-152">OUTPUTS</span></span>

### <span data-ttu-id="47ef6-153">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="47ef6-153">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="47ef6-154">ALIAS</span><span class="sxs-lookup"><span data-stu-id="47ef6-154">ALIASES</span></span>

## <span data-ttu-id="47ef6-155">Note</span><span class="sxs-lookup"><span data-stu-id="47ef6-155">NOTES</span></span>

<span data-ttu-id="47ef6-156">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="47ef6-156">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="47ef6-157">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="47ef6-157">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="47ef6-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : proprietà dell'oggetto Subscription.</span><span class="sxs-lookup"><span data-stu-id="47ef6-158">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="47ef6-159">`[DelegatedProviderSubscriptionId <String>]`: Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="47ef6-159">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="47ef6-160">`[DisplayName <String>]`: Nome sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="47ef6-160">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="47ef6-161">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="47ef6-161">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="47ef6-162">`[Id <String>]`: Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="47ef6-162">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="47ef6-163">`[OfferId <String>]`: Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="47ef6-163">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="47ef6-164">`[Owner <String>]`: Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47ef6-164">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="47ef6-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Tipo di gestore delle risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="47ef6-165">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="47ef6-166">`[State <SubscriptionState?>]`: Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="47ef6-166">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="47ef6-167">`[SubscriptionId <String>]`: Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="47ef6-167">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="47ef6-168">`[TenantId <String>]`: Identificatore tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="47ef6-168">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="47ef6-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47ef6-169">RELATED LINKS</span></span>

