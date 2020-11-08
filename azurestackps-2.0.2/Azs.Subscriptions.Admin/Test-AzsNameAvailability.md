---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsnameavailability
schema: 2.0.0
ms.openlocfilehash: d92c2558375a180c96ff20260977bdb38908fa61
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030606"
---
# <span data-ttu-id="43547-101">Test-AzsNameAvailability</span><span class="sxs-lookup"><span data-stu-id="43547-101">Test-AzsNameAvailability</span></span>

## <span data-ttu-id="43547-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43547-102">SYNOPSIS</span></span>
<span data-ttu-id="43547-103">Ottenere l'elenco degli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="43547-103">Get the list of subscriptions.</span></span>

## <span data-ttu-id="43547-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43547-104">SYNTAX</span></span>

### <span data-ttu-id="43547-105">CheckExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="43547-105">CheckExpanded (Default)</span></span>
```
Test-AzsNameAvailability [-SubscriptionId <String>] [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43547-106">Controllo</span><span class="sxs-lookup"><span data-stu-id="43547-106">Check</span></span>
```
Test-AzsNameAvailability -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43547-107">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="43547-107">CheckViaIdentity</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity>
 -NameAvailabilityDefinition <ICheckNameAvailabilityDefinition> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="43547-108">CheckViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="43547-108">CheckViaIdentityExpanded</span></span>
```
Test-AzsNameAvailability -InputObject <ISubscriptionsAdminIdentity> [-Name <String>] [-ResourceType <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="43547-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43547-109">DESCRIPTION</span></span>
<span data-ttu-id="43547-110">Ottenere l'elenco degli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="43547-110">Get the list of subscriptions.</span></span>

## <span data-ttu-id="43547-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43547-111">EXAMPLES</span></span>

### <span data-ttu-id="43547-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="43547-112">Example 1</span></span>
```powershell
PS C:\> Test-AzsNameAvailability -ResourceType "Microsoft.Subscriptions.Admin/offers" -Name "testoffer" | fl *

Message       : A resource of type 'Microsoft.Subscriptions.Admin/offers' with name 'testoffer' already exists. Please select a different name.
NameAvailable : False
Reason        : AlreadyExists
```

<span data-ttu-id="43547-113">Restituisce la disponibilità del tipo e del nome delle risorse di sottoscrizione specificati</span><span class="sxs-lookup"><span data-stu-id="43547-113">Returns the availability of the specified subscription resource type and name</span></span>

## <span data-ttu-id="43547-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43547-114">PARAMETERS</span></span>

### <span data-ttu-id="43547-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43547-115">-DefaultProfile</span></span>
<span data-ttu-id="43547-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43547-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43547-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="43547-117">-InputObject</span></span>
<span data-ttu-id="43547-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="43547-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity, CheckViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="43547-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="43547-119">-Name</span></span>
<span data-ttu-id="43547-120">Il nome della risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="43547-120">The resource name to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43547-121">-NameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="43547-121">-NameAvailabilityDefinition</span></span>
<span data-ttu-id="43547-122">Definizione dell'azione di disponibilità dei nomi di controllo.</span><span class="sxs-lookup"><span data-stu-id="43547-122">The check name availability action definition.</span></span>
<span data-ttu-id="43547-123">Per costruire, vedere la sezione Note per le proprietà di NAMEAVAILABILITYDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="43547-123">To construct, see NOTES section for NAMEAVAILABILITYDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition
Parameter Sets: Check, CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="43547-124">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="43547-124">-ResourceType</span></span>
<span data-ttu-id="43547-125">Tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="43547-125">The resource type to verify.</span></span>

```yaml
Type: System.String
Parameter Sets: CheckExpanded, CheckViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43547-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43547-126">-SubscriptionId</span></span>
<span data-ttu-id="43547-127">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="43547-127">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Check, CheckExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="43547-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43547-128">-Confirm</span></span>
<span data-ttu-id="43547-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43547-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43547-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43547-130">-WhatIf</span></span>
<span data-ttu-id="43547-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43547-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43547-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43547-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43547-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43547-133">CommonParameters</span></span>
<span data-ttu-id="43547-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43547-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43547-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43547-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43547-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43547-136">INPUTS</span></span>

### <span data-ttu-id="43547-137">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityDefinition</span><span class="sxs-lookup"><span data-stu-id="43547-137">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityDefinition</span></span>

### <span data-ttu-id="43547-138">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="43547-138">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="43547-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43547-139">OUTPUTS</span></span>

### <span data-ttu-id="43547-140">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ICheckNameAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="43547-140">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ICheckNameAvailabilityResponse</span></span>

<span data-ttu-id="43547-141">ALIAS</span><span class="sxs-lookup"><span data-stu-id="43547-141">ALIASES</span></span>

## <span data-ttu-id="43547-142">Note</span><span class="sxs-lookup"><span data-stu-id="43547-142">NOTES</span></span>

<span data-ttu-id="43547-143">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="43547-143">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="43547-144">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="43547-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="43547-145">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="43547-145">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="43547-146">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="43547-146">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="43547-147">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="43547-147">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="43547-148">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="43547-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="43547-149">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="43547-149">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="43547-150">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="43547-150">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="43547-151">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="43547-151">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="43547-152">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="43547-152">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="43547-153">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="43547-153">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="43547-154">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="43547-154">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="43547-155">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="43547-155">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="43547-156">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="43547-156">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="43547-157">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="43547-157">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="43547-158">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="43547-158">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="43547-159">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43547-159">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="43547-160">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="43547-160">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="43547-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition> : definizione dell'azione di disponibilità dei nomi di controllo.</span><span class="sxs-lookup"><span data-stu-id="43547-161">NAMEAVAILABILITYDEFINITION <ICheckNameAvailabilityDefinition>: The check name availability action definition.</span></span>
  - <span data-ttu-id="43547-162">`[Name <String>]`: Nome risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="43547-162">`[Name <String>]`: The resource name to verify.</span></span>
  - <span data-ttu-id="43547-163">`[ResourceType <String>]`: Il tipo di risorsa da verificare.</span><span class="sxs-lookup"><span data-stu-id="43547-163">`[ResourceType <String>]`: The resource type to verify.</span></span>

## <span data-ttu-id="43547-164">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43547-164">RELATED LINKS</span></span>

