---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023074"
---
# <span data-ttu-id="cd2c2-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="cd2c2-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="cd2c2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd2c2-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2c2-103">Crea o aggiorna l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="cd2c2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd2c2-104">SYNTAX</span></span>

### <span data-ttu-id="cd2c2-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd2c2-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="cd2c2-106">Creare</span><span class="sxs-lookup"><span data-stu-id="cd2c2-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="cd2c2-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd2c2-107">DESCRIPTION</span></span>
<span data-ttu-id="cd2c2-108">Crea o aggiorna l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="cd2c2-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd2c2-109">EXAMPLES</span></span>

### <span data-ttu-id="cd2c2-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd2c2-110">Example 1</span></span>
```powershell
PS C:\> New-AzsUserSubscription -Owner "user@contoso.com" -OfferId "/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOffer" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : 
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/398466a8-7d43-455a-b842-772d356d119e
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/TenantResourceGroup/providers/Microsoft.Subscriptions.Admin/offers/TenantOff
                                  er
Owner                           : user@contoso.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : 398466a8-7d43-455a-b842-772d356d119e
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="cd2c2-111">Crea un nuovo abbonamento utente</span><span class="sxs-lookup"><span data-stu-id="cd2c2-111">Creates a new user subscription</span></span>

## <span data-ttu-id="cd2c2-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd2c2-112">PARAMETERS</span></span>

### <span data-ttu-id="cd2c2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2c2-113">-DefaultProfile</span></span>
<span data-ttu-id="cd2c2-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd2c2-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd2c2-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="cd2c2-116">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-116">Parent DelegatedProvider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd2c2-117">-DisplayName</span></span>
<span data-ttu-id="cd2c2-118">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-118">Subscription name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="cd2c2-119">-ExternalReferenceId</span></span>
<span data-ttu-id="cd2c2-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-120">External reference identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-121">-ID</span><span class="sxs-lookup"><span data-stu-id="cd2c2-121">-Id</span></span>
<span data-ttu-id="cd2c2-122">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-122">Fully qualified identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-123">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="cd2c2-123">-OfferId</span></span>
<span data-ttu-id="cd2c2-124">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-124">Identifier of the offer under the scope of a delegated provider.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-125">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="cd2c2-125">-Owner</span></span>
<span data-ttu-id="cd2c2-126">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-126">Subscription owner.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="cd2c2-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="cd2c2-128">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-128">Routing resource manager type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.ResourceManagerType
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Default"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="cd2c2-129">-State</span></span>
<span data-ttu-id="cd2c2-130">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-130">Subscription state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.SubscriptionState
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: Write-Output "Enabled"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="cd2c2-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="cd2c2-132">Proprietà dell'oggetto Subscription.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-132">Subscription object properties.</span></span>
<span data-ttu-id="cd2c2-133">Per costruire, vedere la sezione Note per le proprietà di SUBSCRIPTIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition
Parameter Sets: Create
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd2c2-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="cd2c2-135">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-135">The target subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: $([Guid]::NewGuid().ToString())
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-136">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="cd2c2-136">-TenantId</span></span>
<span data-ttu-id="cd2c2-137">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-137">Directory tenant identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd2c2-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cd2c2-138">-Confirm</span></span>
<span data-ttu-id="cd2c2-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd2c2-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd2c2-140">-WhatIf</span></span>
<span data-ttu-id="cd2c2-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd2c2-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd2c2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2c2-143">CommonParameters</span></span>
<span data-ttu-id="cd2c2-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2c2-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd2c2-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2c2-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd2c2-146">INPUTS</span></span>

### <span data-ttu-id="cd2c2-147">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="cd2c2-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="cd2c2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd2c2-148">OUTPUTS</span></span>

### <span data-ttu-id="cd2c2-149">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="cd2c2-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="cd2c2-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd2c2-150">ALIASES</span></span>

## <span data-ttu-id="cd2c2-151">Note</span><span class="sxs-lookup"><span data-stu-id="cd2c2-151">NOTES</span></span>

<span data-ttu-id="cd2c2-152">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd2c2-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cd2c2-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : proprietà dell'oggetto Subscription.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="cd2c2-155">`[DelegatedProviderSubscriptionId <String>]`: Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="cd2c2-156">`[DisplayName <String>]`: Nome sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="cd2c2-157">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="cd2c2-158">`[Id <String>]`: Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="cd2c2-159">`[OfferId <String>]`: Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="cd2c2-160">`[Owner <String>]`: Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="cd2c2-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Tipo di gestore delle risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="cd2c2-162">`[State <SubscriptionState?>]`: Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="cd2c2-163">`[SubscriptionId <String>]`: Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="cd2c2-164">`[TenantId <String>]`: Identificatore tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="cd2c2-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="cd2c2-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd2c2-165">RELATED LINKS</span></span>

