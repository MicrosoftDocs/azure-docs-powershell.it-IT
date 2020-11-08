---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplanfromoffer
schema: 2.0.0
ms.openlocfilehash: c3a68c028abc9033cef9d9fd7e8fbd39e4066d2d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030388"
---
# <span data-ttu-id="83455-101">Remove-AzsPlanFromOffer</span><span class="sxs-lookup"><span data-stu-id="83455-101">Remove-AzsPlanFromOffer</span></span>

## <span data-ttu-id="83455-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="83455-102">SYNOPSIS</span></span>
<span data-ttu-id="83455-103">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83455-103">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="83455-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="83455-104">SYNTAX</span></span>

### <span data-ttu-id="83455-105">UnlinkExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="83455-105">UnlinkExpanded (Default)</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-MaxAcquisitionCount <Int32>] [-PlanLinkType <PlanLinkType>] [-PlanName <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83455-106">Scollegare</span><span class="sxs-lookup"><span data-stu-id="83455-106">Unlink</span></span>
```
Remove-AzsPlanFromOffer -OfferName <String> -ResourceGroupName <String> -PlanLink <IPlanLinkDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83455-107">UnlinkViaIdentity</span><span class="sxs-lookup"><span data-stu-id="83455-107">UnlinkViaIdentity</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> -PlanLink <IPlanLinkDefinition>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83455-108">UnlinkViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83455-108">UnlinkViaIdentityExpanded</span></span>
```
Remove-AzsPlanFromOffer -InputObject <ISubscriptionsAdminIdentity> [-MaxAcquisitionCount <Int32>]
 [-PlanLinkType <PlanLinkType>] [-PlanName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="83455-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="83455-109">DESCRIPTION</span></span>
<span data-ttu-id="83455-110">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83455-110">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="83455-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="83455-111">EXAMPLES</span></span>

### <span data-ttu-id="83455-112">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="83455-112">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsPlanFromOffer -PlanName "testplan" -PlanLinkType Addon -OfferName "testoffer" -ResourceGroupName "testrg"

```

<span data-ttu-id="83455-113">Scollegare un piano da un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83455-113">Unlink a plan from an offer.</span></span>

## <span data-ttu-id="83455-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="83455-114">PARAMETERS</span></span>

### <span data-ttu-id="83455-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83455-115">-DefaultProfile</span></span>
<span data-ttu-id="83455-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="83455-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83455-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83455-117">-InputObject</span></span>
<span data-ttu-id="83455-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83455-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: UnlinkViaIdentity, UnlinkViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="83455-119">-MaxAcquisitionCount</span><span class="sxs-lookup"><span data-stu-id="83455-119">-MaxAcquisitionCount</span></span>
<span data-ttu-id="83455-120">Numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="83455-120">The maximum acquisition count by subscribers</span></span>

```yaml
Type: System.Int32
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="83455-121">-Offername</span><span class="sxs-lookup"><span data-stu-id="83455-121">-OfferName</span></span>
<span data-ttu-id="83455-122">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83455-122">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="83455-123">-PlanLink</span><span class="sxs-lookup"><span data-stu-id="83455-123">-PlanLink</span></span>
<span data-ttu-id="83455-124">Definizione per collegare e scollegare i piani per le offerte.</span><span class="sxs-lookup"><span data-stu-id="83455-124">Definition for linking and unlinking plans to offers.</span></span>
<span data-ttu-id="83455-125">Per costruire, vedere la sezione Note per le proprietà di PLANLINK e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="83455-125">To construct, see NOTES section for PLANLINK properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition
Parameter Sets: Unlink, UnlinkViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="83455-126">-PlanLinkType</span><span class="sxs-lookup"><span data-stu-id="83455-126">-PlanLinkType</span></span>
<span data-ttu-id="83455-127">Tipo di collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="83455-127">Type of the plan link.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Support.PlanLinkType
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="83455-128">-PlanName</span><span class="sxs-lookup"><span data-stu-id="83455-128">-PlanName</span></span>
<span data-ttu-id="83455-129">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="83455-129">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: UnlinkExpanded, UnlinkViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="83455-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83455-130">-ResourceGroupName</span></span>
<span data-ttu-id="83455-131">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="83455-131">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="83455-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83455-132">-SubscriptionId</span></span>
<span data-ttu-id="83455-133">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="83455-133">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Unlink, UnlinkExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="83455-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="83455-134">-Confirm</span></span>
<span data-ttu-id="83455-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83455-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83455-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83455-136">-WhatIf</span></span>
<span data-ttu-id="83455-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83455-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83455-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="83455-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83455-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83455-139">CommonParameters</span></span>
<span data-ttu-id="83455-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83455-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83455-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="83455-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83455-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="83455-142">INPUTS</span></span>

### <span data-ttu-id="83455-143">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanLinkDefinition</span><span class="sxs-lookup"><span data-stu-id="83455-143">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanLinkDefinition</span></span>

### <span data-ttu-id="83455-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="83455-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="83455-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="83455-145">OUTPUTS</span></span>

### <span data-ttu-id="83455-146">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="83455-146">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="83455-147">ALIAS</span><span class="sxs-lookup"><span data-stu-id="83455-147">ALIASES</span></span>

## <span data-ttu-id="83455-148">Note</span><span class="sxs-lookup"><span data-stu-id="83455-148">NOTES</span></span>

<span data-ttu-id="83455-149">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="83455-149">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83455-150">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83455-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="83455-151">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="83455-151">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83455-152">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="83455-152">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="83455-153">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="83455-153">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="83455-154">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="83455-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83455-155">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="83455-155">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="83455-156">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="83455-156">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="83455-157">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83455-157">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="83455-158">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="83455-158">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="83455-159">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="83455-159">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="83455-160">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="83455-160">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="83455-161">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="83455-161">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="83455-162">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="83455-162">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="83455-163">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="83455-163">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="83455-164">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="83455-164">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="83455-165">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="83455-165">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="83455-166">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="83455-166">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="83455-167">PLANLINK <IPlanLinkDefinition> : definizione per il collegamento e la disconnessione di piani alle offerte.</span><span class="sxs-lookup"><span data-stu-id="83455-167">PLANLINK <IPlanLinkDefinition>: Definition for linking and unlinking plans to offers.</span></span>
  - <span data-ttu-id="83455-168">`[MaxAcquisitionCount <Int32?>]`: Il numero massimo di acquisizioni per gli abbonati</span><span class="sxs-lookup"><span data-stu-id="83455-168">`[MaxAcquisitionCount <Int32?>]`: The maximum acquisition count by subscribers</span></span>
  - <span data-ttu-id="83455-169">`[PlanLinkType <PlanLinkType?>]`: Tipo del collegamento piano.</span><span class="sxs-lookup"><span data-stu-id="83455-169">`[PlanLinkType <PlanLinkType?>]`: Type of the plan link.</span></span>
  - <span data-ttu-id="83455-170">`[PlanName <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="83455-170">`[PlanName <String>]`: Name of the plan.</span></span>

## <span data-ttu-id="83455-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="83455-171">RELATED LINKS</span></span>

