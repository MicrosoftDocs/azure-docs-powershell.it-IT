---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/add-azsplantooffer
schema: 2.0.0
ms.openlocfilehash: 65691116ea8e73e8f03e8cc7dc97f38c61ecebdb
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030152"
---
# <span data-ttu-id="9edd6-101">Add-AzsPlanToOffer</span><span class="sxs-lookup"><span data-stu-id="9edd6-101">Add-AzsPlanToOffer</span></span>

## <span data-ttu-id="9edd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9edd6-102">SYNOPSIS</span></span>
<span data-ttu-id="9edd6-103">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edd6-103">Links a plan to an offer.</span></span>

## <span data-ttu-id="9edd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9edd6-104">SYNTAX</span></span>

### <span data-ttu-id="9edd6-105">LinkExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9edd6-105">LinkExpanded (Default)</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9edd6-106">Collegamento</span><span class="sxs-lookup"><span data-stu-id="9edd6-106">Link</span></span>
```
Add-AzsPlanToOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9edd6-107">LinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9edd6-107">LinkViaIdentity</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9edd6-108">LinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="9edd6-108">LinkViaIdentityExpanded</span></span>
```
Add-AzsPlanToOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="9edd6-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9edd6-109">DESCRIPTION</span></span>
<span data-ttu-id="9edd6-110">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edd6-110">Links a plan to an offer.</span></span>

## <span data-ttu-id="9edd6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9edd6-111">EXAMPLES</span></span>

### <span data-ttu-id="9edd6-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9edd6-112">Example 1</span></span>
```powershell
PS C:\> Add-AzsPlanToOffer -PlanName "addonplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg" -MaxAcquisitionCount 18

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="9edd6-113">Collega un piano a un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edd6-113">Links a plan to an offer.</span></span>

## <span data-ttu-id="9edd6-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9edd6-114">PARAMETERS</span></span>

### <span data-ttu-id="9edd6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9edd6-115">-DefaultProfile</span></span>
<span data-ttu-id="9edd6-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9edd6-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9edd6-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9edd6-117">-InputObject</span></span>
<span data-ttu-id="9edd6-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9edd6-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: LinkViaIdentity, LinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="9edd6-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="9edd6-120">Numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="9edd6-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-121">-Offername</span><span class="sxs-lookup"><span data-stu-id="9edd6-121">-OfferName</span></span>
<span data-ttu-id="9edd6-122">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edd6-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="9edd6-123">-PlanLink</span></span>
<span data-ttu-id="9edd6-124">Definizione per collegare e scollegare i piani per le offerte.</span><span class="sxs-lookup"><span data-stu-id="9edd6-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="9edd6-125">Per costruire, vedere la sezione Note per le proprietà di PLANLINK e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9edd6-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Link, LinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="9edd6-126">-PlanLinkType</span></span>
<span data-ttu-id="9edd6-127">Tipo di collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="9edd6-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="9edd6-128">-PlanName</span></span>
<span data-ttu-id="9edd6-129">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="9edd6-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: LinkExpanded, LinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9edd6-130">-ResourceGroupName</span></span>
<span data-ttu-id="9edd6-131">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9edd6-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9edd6-132">-SubscriptionId</span></span>
<span data-ttu-id="9edd6-133">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9edd6-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Link, LinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edd6-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9edd6-134">-Confirm</span></span>
<span data-ttu-id="9edd6-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9edd6-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9edd6-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9edd6-136">-WhatIf</span></span>
<span data-ttu-id="9edd6-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9edd6-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9edd6-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9edd6-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9edd6-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9edd6-139">CommonParameters</span></span>
<span data-ttu-id="9edd6-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9edd6-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9edd6-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9edd6-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9edd6-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9edd6-142">INPUTS</span></span>

### <span data-ttu-id="9edd6-143">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="9edd6-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="9edd6-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9edd6-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9edd6-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9edd6-145">OUTPUTS</span></span>

### <span data-ttu-id="9edd6-146">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="9edd6-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="9edd6-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9edd6-147">ALIASES</span></span>

## <span data-ttu-id="9edd6-148">Note</span><span class="sxs-lookup"><span data-stu-id="9edd6-148">NOTES</span></span>

<span data-ttu-id="9edd6-149">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9edd6-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9edd6-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9edd6-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9edd6-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="9edd6-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9edd6-152">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="9edd6-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9edd6-153">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="9edd6-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9edd6-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="9edd6-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9edd6-155">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="9edd6-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9edd6-156">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="9edd6-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9edd6-157">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edd6-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9edd6-158">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edd6-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9edd6-159">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="9edd6-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9edd6-160">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="9edd6-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9edd6-161">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="9edd6-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9edd6-162">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="9edd6-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9edd6-163">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9edd6-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9edd6-164">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9edd6-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9edd6-165">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9edd6-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9edd6-166">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="9edd6-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="9edd6-167">PLANLINK <IPlanLinkDefinition> : definizione per il collegamento e la disconnessione di piani alle offerte.</span><span class="sxs-lookup"><span data-stu-id="9edd6-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="9edd6-168">`[MaxAcquisitionCount <Int32?>]`: Il numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="9edd6-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="9edd6-169">`[PlanLinkType <PlanLinkType?>]`: Tipo del collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="9edd6-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="9edd6-170">`[PlanName <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="9edd6-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="9edd6-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9edd6-171">RELATED LINKS</span></span>

