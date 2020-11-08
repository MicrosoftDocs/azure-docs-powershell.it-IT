---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/new-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 6ccc47c6b6254e23050cf4341cae355bda78d8df
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030543"
---
# <span data-ttu-id="4ba6b-101">New-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="4ba6b-101">New-AzsUserSubscription</span></span>

## <span data-ttu-id="4ba6b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ba6b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ba6b-103">Crea o aggiorna l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-103">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="4ba6b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ba6b-104">SYNTAX</span></span>

### <span data-ttu-id="4ba6b-105">CreateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ba6b-105">CreateExpanded (Default)</span></span>
```
New-AzsUserSubscription -OfferId <String> -Owner <String> [-TargetSubscriptionId <String>]
 [-DelegatedProviderSubscriptionId <String>] [-DisplayName <String>] [-ExternalReferenceId <String>]
 [-Id <String>] [-RoutingResourceManagerType <ResourceManagerType>] [-State <SubscriptionState>]
 [-TenantId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ba6b-106">Creare</span><span class="sxs-lookup"><span data-stu-id="4ba6b-106">Create</span></span>
```
New-AzsUserSubscription -SubscriptionDefinition <ISubscriptionDefinition> [-TargetSubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ba6b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ba6b-107">DESCRIPTION</span></span>
<span data-ttu-id="4ba6b-108">Crea o aggiorna l'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-108">Creates or updates the specified subscription.</span></span>

## <span data-ttu-id="4ba6b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ba6b-109">EXAMPLES</span></span>

### <span data-ttu-id="4ba6b-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ba6b-110">Example 1</span></span>
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

<span data-ttu-id="4ba6b-111">Crea un nuovo abbonamento utente</span><span class="sxs-lookup"><span data-stu-id="4ba6b-111">Creates a new user subscription</span></span>

## <span data-ttu-id="4ba6b-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ba6b-112">PARAMETERS</span></span>

### <span data-ttu-id="4ba6b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ba6b-113">-DefaultProfile</span></span>
<span data-ttu-id="4ba6b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ba6b-115">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ba6b-115">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="4ba6b-116">Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-116">Parent DelegatedProvider subscription identifier.</span></span>

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

### <span data-ttu-id="4ba6b-117">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4ba6b-117">-DisplayName</span></span>
<span data-ttu-id="4ba6b-118">Nome dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-118">Subscription name.</span></span>

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

### <span data-ttu-id="4ba6b-119">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="4ba6b-119">-ExternalReferenceId</span></span>
<span data-ttu-id="4ba6b-120">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-120">External reference identifier.</span></span>

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

### <span data-ttu-id="4ba6b-121">-ID</span><span class="sxs-lookup"><span data-stu-id="4ba6b-121">-Id</span></span>
<span data-ttu-id="4ba6b-122">Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-122">Fully qualified identifier.</span></span>

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

### <span data-ttu-id="4ba6b-123">-Idofferta</span><span class="sxs-lookup"><span data-stu-id="4ba6b-123">-OfferId</span></span>
<span data-ttu-id="4ba6b-124">Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-124">Identifier of the offer under the scope of a delegated provider.</span></span>

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

### <span data-ttu-id="4ba6b-125">-Proprietario</span><span class="sxs-lookup"><span data-stu-id="4ba6b-125">-Owner</span></span>
<span data-ttu-id="4ba6b-126">Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-126">Subscription owner.</span></span>

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

### <span data-ttu-id="4ba6b-127">-RoutingResourceManagerType</span><span class="sxs-lookup"><span data-stu-id="4ba6b-127">-RoutingResourceManagerType</span></span>
<span data-ttu-id="4ba6b-128">Tipo di gestione risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-128">Routing resource manager type.</span></span>

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

### <span data-ttu-id="4ba6b-129">-Stato</span><span class="sxs-lookup"><span data-stu-id="4ba6b-129">-State</span></span>
<span data-ttu-id="4ba6b-130">Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-130">Subscription state.</span></span>

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

### <span data-ttu-id="4ba6b-131">-SubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="4ba6b-131">-SubscriptionDefinition</span></span>
<span data-ttu-id="4ba6b-132">Proprietà dell'oggetto Subscription.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-132">Subscription object properties.</span></span>
<span data-ttu-id="4ba6b-133">Per costruire, vedere la sezione Note per le proprietà di SUBSCRIPTIONDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-133">To construct, see NOTES section for SUBSCRIPTIONDEFINITION properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ba6b-134">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4ba6b-134">-TargetSubscriptionId</span></span>
<span data-ttu-id="4ba6b-135">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-135">The target subscription ID.</span></span>

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

### <span data-ttu-id="4ba6b-136">-ID tenant</span><span class="sxs-lookup"><span data-stu-id="4ba6b-136">-TenantId</span></span>
<span data-ttu-id="4ba6b-137">Identificatore del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-137">Directory tenant identifier.</span></span>

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

### <span data-ttu-id="4ba6b-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ba6b-138">-Confirm</span></span>
<span data-ttu-id="4ba6b-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ba6b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ba6b-140">-WhatIf</span></span>
<span data-ttu-id="4ba6b-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ba6b-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ba6b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ba6b-143">CommonParameters</span></span>
<span data-ttu-id="4ba6b-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ba6b-145">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ba6b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ba6b-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ba6b-146">INPUTS</span></span>

### <span data-ttu-id="4ba6b-147">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="4ba6b-147">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

## <span data-ttu-id="4ba6b-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ba6b-148">OUTPUTS</span></span>

### <span data-ttu-id="4ba6b-149">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="4ba6b-149">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="4ba6b-150">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4ba6b-150">ALIASES</span></span>

## <span data-ttu-id="4ba6b-151">Note</span><span class="sxs-lookup"><span data-stu-id="4ba6b-151">NOTES</span></span>

<span data-ttu-id="4ba6b-152">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-152">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ba6b-153">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-153">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4ba6b-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition> : proprietà dell'oggetto Subscription.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-154">SUBSCRIPTIONDEFINITION <ISubscriptionDefinition>: Subscription object properties.</span></span>
  - <span data-ttu-id="4ba6b-155">`[DelegatedProviderSubscriptionId <String>]`: Identificatore dell'abbonamento a DelegatedProvider padre.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-155">`[DelegatedProviderSubscriptionId <String>]`: Parent DelegatedProvider subscription identifier.</span></span>
  - <span data-ttu-id="4ba6b-156">`[DisplayName <String>]`: Nome sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-156">`[DisplayName <String>]`: Subscription name.</span></span>
  - <span data-ttu-id="4ba6b-157">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-157">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="4ba6b-158">`[Id <String>]`: Identificatore completo.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-158">`[Id <String>]`: Fully qualified identifier.</span></span>
  - <span data-ttu-id="4ba6b-159">`[OfferId <String>]`: Identificatore dell'offerta sotto l'ambito di un provider delegato.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-159">`[OfferId <String>]`: Identifier of the offer under the scope of a delegated provider.</span></span>
  - <span data-ttu-id="4ba6b-160">`[Owner <String>]`: Proprietario dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-160">`[Owner <String>]`: Subscription owner.</span></span>
  - <span data-ttu-id="4ba6b-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Tipo di gestore delle risorse di routing.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-161">`[RoutingResourceManagerType <ResourceManagerType?>]`: Routing resource manager type.</span></span>
  - <span data-ttu-id="4ba6b-162">`[State <SubscriptionState?>]`: Stato sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-162">`[State <SubscriptionState?>]`: Subscription state.</span></span>
  - <span data-ttu-id="4ba6b-163">`[SubscriptionId <String>]`: Identificatore dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-163">`[SubscriptionId <String>]`: Subscription identifier.</span></span>
  - <span data-ttu-id="4ba6b-164">`[TenantId <String>]`: Identificatore tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="4ba6b-164">`[TenantId <String>]`: Directory tenant identifier.</span></span>

## <span data-ttu-id="4ba6b-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ba6b-165">RELATED LINKS</span></span>

