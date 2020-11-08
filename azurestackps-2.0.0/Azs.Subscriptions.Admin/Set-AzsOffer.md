---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/set-azsoffer
schema: 2.0.0
ms.openlocfilehash: 82be26ae402278d8cdc24195fd62ed09b67bdc14
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023066"
---
# <span data-ttu-id="a1f55-101">Set-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="a1f55-101">Set-AzsOffer</span></span>

## <span data-ttu-id="a1f55-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1f55-102">SYNOPSIS</span></span>
<span data-ttu-id="a1f55-103">Creare o aggiornare l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-103">Create or update the offer.</span></span>

## <span data-ttu-id="a1f55-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1f55-104">SYNTAX</span></span>

### <span data-ttu-id="a1f55-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a1f55-105">UpdateExpanded (Default)</span></span>
```
Set-AzsOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-AddonPlanDefinition <IAddonPlanDefinition[]>] [-BasePlanIds <String[]>] [-Description <String>]
 [-DisplayName <String>] [-ExternalReferenceId <String>] [-Location <String>]
 [-MaxSubscriptionsPerAccount <Int32>] [-PropertiesName <String>] [-State <AccessibilityState>]
 [-SubscriptionCount <Int32>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a1f55-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="a1f55-106">Update</span></span>
```
Set-AzsOffer -OfferDefinition <IOffer> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a1f55-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1f55-107">DESCRIPTION</span></span>
<span data-ttu-id="a1f55-108">Creare o aggiornare l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-108">Create or update the offer.</span></span>

## <span data-ttu-id="a1f55-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1f55-109">EXAMPLES</span></span>

### <span data-ttu-id="a1f55-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a1f55-110">Example 1</span></span>
```powershell
PS C:\> $Offer = Get-AzsAdminManagedOffer | Select-Object -First 1
$Offer.MaxSubscriptionsPerAccount = 18
$Offer | Set-AzsOffer

AddonPlans                 : {}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/plans/DRPTestPlan5056}
Description                : 
DisplayName                : DRPTestOffer5056
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Location                   : redmond
MaxSubscriptionsPerAccount : 18
Name                       : DRPTestOffer5056
PropertiesName             : DRPTestOffer5056
State                      : Private
SubscriptionCount          : 5
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="a1f55-111">Aggiornare un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-111">Update an offer.</span></span>

## <span data-ttu-id="a1f55-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1f55-112">PARAMETERS</span></span>

### <span data-ttu-id="a1f55-113">-AddonPlanDefinition</span><span class="sxs-lookup"><span data-stu-id="a1f55-113">-AddonPlanDefinition</span></span>
<span data-ttu-id="a1f55-114">Riferimenti a piani per i componenti aggiuntivi che un tenant può acquistare facoltativamente come parte dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-114">References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
<span data-ttu-id="a1f55-115">Per costruire, vedere la sezione Note per le proprietà di ADDONPLANDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a1f55-115">To construct, see NOTES section for ADDONPLANDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IAddonPlanDefinition[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-116">-BasePlanIds</span><span class="sxs-lookup"><span data-stu-id="a1f55-116">-BasePlanIds</span></span>
<span data-ttu-id="a1f55-117">Identificatori dei piani di base che diventano disponibili per il tenant immediatamente quando un tenant sottoscrive l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-117">Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1f55-118">-DefaultProfile</span></span>
<span data-ttu-id="a1f55-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1f55-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1f55-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1f55-120">-Description</span></span>
<span data-ttu-id="a1f55-121">Descrizione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-121">Description of offer.</span></span>

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

### <span data-ttu-id="a1f55-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a1f55-122">-DisplayName</span></span>
<span data-ttu-id="a1f55-123">Nome visualizzato dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-123">Display name of offer.</span></span>

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

### <span data-ttu-id="a1f55-124">-ExternalReferenceId</span><span class="sxs-lookup"><span data-stu-id="a1f55-124">-ExternalReferenceId</span></span>
<span data-ttu-id="a1f55-125">Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="a1f55-125">External reference identifier.</span></span>

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

### <span data-ttu-id="a1f55-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a1f55-126">-Location</span></span>
<span data-ttu-id="a1f55-127">Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="a1f55-127">Location of the resource</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-128">-MaxSubscriptionsPerAccount</span><span class="sxs-lookup"><span data-stu-id="a1f55-128">-MaxSubscriptionsPerAccount</span></span>
<span data-ttu-id="a1f55-129">Numero massimo di abbonamenti per account.</span><span class="sxs-lookup"><span data-stu-id="a1f55-129">Maximum subscriptions per account.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-130">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1f55-130">-Name</span></span>
<span data-ttu-id="a1f55-131">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-131">Name of an offer.</span></span>

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

### <span data-ttu-id="a1f55-132">-OfferDefinition</span><span class="sxs-lookup"><span data-stu-id="a1f55-132">-OfferDefinition</span></span>
<span data-ttu-id="a1f55-133">Rappresenta un'offerta di servizi per cui è possibile creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1f55-133">Represents an offering of services against which a subscription can be created.</span></span>
<span data-ttu-id="a1f55-134">Per costruire, vedere la sezione Note per le proprietà di OFFERDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a1f55-134">To construct, see NOTES section for OFFERDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-135">-Propertiesname</span><span class="sxs-lookup"><span data-stu-id="a1f55-135">-PropertiesName</span></span>
<span data-ttu-id="a1f55-136">Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-136">Name of the Offer.</span></span>

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

### <span data-ttu-id="a1f55-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1f55-137">-ResourceGroupName</span></span>
<span data-ttu-id="a1f55-138">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a1f55-138">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="a1f55-139">-Stato</span><span class="sxs-lookup"><span data-stu-id="a1f55-139">-State</span></span>
<span data-ttu-id="a1f55-140">Offrire lo stato di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="a1f55-140">Offer accessibility state.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.AccessibilityState
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-141">-SubscriptionCount</span><span class="sxs-lookup"><span data-stu-id="a1f55-141">-SubscriptionCount</span></span>
<span data-ttu-id="a1f55-142">Conteggio corrente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1f55-142">Current subscription count.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a1f55-143">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a1f55-143">-SubscriptionId</span></span>
<span data-ttu-id="a1f55-144">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a1f55-144">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a1f55-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a1f55-145">-Confirm</span></span>
<span data-ttu-id="a1f55-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1f55-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1f55-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1f55-147">-WhatIf</span></span>
<span data-ttu-id="a1f55-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1f55-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1f55-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a1f55-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1f55-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1f55-150">CommonParameters</span></span>
<span data-ttu-id="a1f55-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1f55-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1f55-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a1f55-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1f55-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1f55-153">INPUTS</span></span>

### <span data-ttu-id="a1f55-154">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="a1f55-154">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

## <span data-ttu-id="a1f55-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1f55-155">OUTPUTS</span></span>

### <span data-ttu-id="a1f55-156">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="a1f55-156">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="a1f55-157">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a1f55-157">ALIASES</span></span>

## <span data-ttu-id="a1f55-158">Note</span><span class="sxs-lookup"><span data-stu-id="a1f55-158">NOTES</span></span>

<span data-ttu-id="a1f55-159">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a1f55-159">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a1f55-160">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a1f55-160">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a1f55-161">ADDONPLANDEFINITION <IAddonPlanDefinition [] >: riferimenti ai piani per i componenti aggiuntivi che un tenant può acquistare facoltativamente come parte dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-161">ADDONPLANDEFINITION <IAddonPlanDefinition[]>: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
  - <span data-ttu-id="a1f55-162">`[MaxAcquisitionCount <Int32?>]`: Numero massimo di istanze che possono essere acquisite da un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1f55-162">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="a1f55-163">Se non specificato, il valore assunto è 1.</span><span class="sxs-lookup"><span data-stu-id="a1f55-163">If not specified, the assumed value is 1.</span></span>
  - <span data-ttu-id="a1f55-164">`[PlanId <String>]`: Identificatore piano.</span><span class="sxs-lookup"><span data-stu-id="a1f55-164">`[PlanId <String>]`: Plan identifier.</span></span>

<span data-ttu-id="a1f55-165">OFFERDEFINITION <IOffer> : rappresenta un'offerta di servizi per cui è possibile creare un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1f55-165">OFFERDEFINITION <IOffer>: Represents an offering of services against which a subscription can be created.</span></span>
  - <span data-ttu-id="a1f55-166">`[Location <String>]`: Posizione della risorsa</span><span class="sxs-lookup"><span data-stu-id="a1f55-166">`[Location <String>]`: Location of the resource</span></span>
  - <span data-ttu-id="a1f55-167">`[AddonPlans <IAddonPlanDefinition[]>]`: Riferimenti ai piani per i componenti aggiuntivi che un tenant può acquistare facoltativamente come parte dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-167">`[AddonPlans <IAddonPlanDefinition[]>]`: References to add-on plans that a tenant can optionally acquire as a part of the offer.</span></span>
    - <span data-ttu-id="a1f55-168">`[MaxAcquisitionCount <Int32?>]`: Numero massimo di istanze che possono essere acquisite da un singolo abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1f55-168">`[MaxAcquisitionCount <Int32?>]`: Maximum number of instances that can be acquired by a single subscription.</span></span> <span data-ttu-id="a1f55-169">Se non specificato, il valore assunto è 1.</span><span class="sxs-lookup"><span data-stu-id="a1f55-169">If not specified, the assumed value is 1.</span></span>
    - <span data-ttu-id="a1f55-170">`[PlanId <String>]`: Identificatore piano.</span><span class="sxs-lookup"><span data-stu-id="a1f55-170">`[PlanId <String>]`: Plan identifier.</span></span>
  - <span data-ttu-id="a1f55-171">`[BasePlanIds <String[]>]`: Identificatori dei piani di base che diventano disponibili per il tenant immediatamente quando un tenant sottoscrive l'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-171">`[BasePlanIds <String[]>]`: Identifiers of the base plans that become available to the tenant immediately when a tenant subscribes to the offer.</span></span>
  - <span data-ttu-id="a1f55-172">`[Description <String>]`: Descrizione dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-172">`[Description <String>]`: Description of offer.</span></span>
  - <span data-ttu-id="a1f55-173">`[DisplayName <String>]`: Nome visualizzato dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-173">`[DisplayName <String>]`: Display name of offer.</span></span>
  - <span data-ttu-id="a1f55-174">`[ExternalReferenceId <String>]`: Identificatore di riferimento esterno.</span><span class="sxs-lookup"><span data-stu-id="a1f55-174">`[ExternalReferenceId <String>]`: External reference identifier.</span></span>
  - <span data-ttu-id="a1f55-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Abbonamento massimo per account.</span><span class="sxs-lookup"><span data-stu-id="a1f55-175">`[MaxSubscriptionsPerAccount <Int32?>]`: Maximum subscriptions per account.</span></span>
  - <span data-ttu-id="a1f55-176">`[PropertiesName <String>]`: Nome dell'offerta.</span><span class="sxs-lookup"><span data-stu-id="a1f55-176">`[PropertiesName <String>]`: Name of the Offer.</span></span>
  - <span data-ttu-id="a1f55-177">`[State <AccessibilityState?>]`: Offrire lo stato di accessibilità.</span><span class="sxs-lookup"><span data-stu-id="a1f55-177">`[State <AccessibilityState?>]`: Offer accessibility state.</span></span>
  - <span data-ttu-id="a1f55-178">`[SubscriptionCount <Int32?>]`: Conteggio corrente dell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a1f55-178">`[SubscriptionCount <Int32?>]`: Current subscription count.</span></span>

## <span data-ttu-id="a1f55-179">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1f55-179">RELATED LINKS</span></span>

