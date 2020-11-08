---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: 995d7296ef1e5b6f846d5343fd072909a877b1ec
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023245"
---
# <span data-ttu-id="e139a-101">Get-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e139a-101">Get-AzsOfferDelegation</span></span>

## <span data-ttu-id="e139a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e139a-102">SYNOPSIS</span></span>
<span data-ttu-id="e139a-103">Ottenere la delega offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="e139a-103">Get the specified offer delegation.</span></span>

## <span data-ttu-id="e139a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e139a-104">SYNTAX</span></span>

### <span data-ttu-id="e139a-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e139a-105">List (Default)</span></span>
```
Get-AzsOfferDelegation -OfferName <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e139a-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="e139a-106">Get</span></span>
```
Get-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="e139a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="e139a-107">GetViaIdentity</span></span>
```
Get-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="e139a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e139a-108">DESCRIPTION</span></span>
<span data-ttu-id="e139a-109">Ottenere la delega offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="e139a-109">Get the specified offer delegation.</span></span>

## <span data-ttu-id="e139a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e139a-110">EXAMPLES</span></span>

### <span data-ttu-id="e139a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e139a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsOfferDelegation -OfferName "delegatedoffer" -ResourceGroupName "testrg"

Id             : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/delegatedoffer/offerDelegations/offerdelegation
Location       : redmond
Name           : delegatedoffer/offerdelegation
SubscriptionId : dbc27112-f67a-4690-ba12-730f71cbb018
Tags           : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type           : Microsoft.Subscriptions.Admin/offers/offerDelegations
```

<span data-ttu-id="e139a-112">Ottenere l'elenco delle offerte Delegate.</span><span class="sxs-lookup"><span data-stu-id="e139a-112">Get the list of delegated offers.</span></span>

## <span data-ttu-id="e139a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e139a-113">PARAMETERS</span></span>

### <span data-ttu-id="e139a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e139a-114">-DefaultProfile</span></span>
<span data-ttu-id="e139a-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e139a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e139a-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e139a-116">-InputObject</span></span>
<span data-ttu-id="e139a-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="e139a-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="e139a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e139a-118">-Name</span></span>
<span data-ttu-id="e139a-119">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e139a-119">Name of a offer delegation.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e139a-120">-Offername</span><span class="sxs-lookup"><span data-stu-id="e139a-120">-OfferName</span></span>
<span data-ttu-id="e139a-121">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e139a-121">Name of an offer.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e139a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e139a-122">-ResourceGroupName</span></span>
<span data-ttu-id="e139a-123">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e139a-123">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e139a-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e139a-124">-SubscriptionId</span></span>
<span data-ttu-id="e139a-125">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e139a-125">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="e139a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e139a-126">CommonParameters</span></span>
<span data-ttu-id="e139a-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e139a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e139a-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e139a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e139a-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e139a-129">INPUTS</span></span>

### <span data-ttu-id="e139a-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="e139a-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="e139a-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e139a-131">OUTPUTS</span></span>

### <span data-ttu-id="e139a-132">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="e139a-132">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOfferDelegation</span></span>

<span data-ttu-id="e139a-133">ALIAS</span><span class="sxs-lookup"><span data-stu-id="e139a-133">ALIASES</span></span>

## <span data-ttu-id="e139a-134">Note</span><span class="sxs-lookup"><span data-stu-id="e139a-134">NOTES</span></span>

<span data-ttu-id="e139a-135">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="e139a-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="e139a-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="e139a-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="e139a-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="e139a-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="e139a-138">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="e139a-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="e139a-139">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="e139a-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="e139a-140">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="e139a-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="e139a-141">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="e139a-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="e139a-142">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="e139a-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="e139a-143">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e139a-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="e139a-144">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="e139a-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="e139a-145">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="e139a-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="e139a-146">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="e139a-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="e139a-147">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="e139a-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="e139a-148">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="e139a-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="e139a-149">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="e139a-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="e139a-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="e139a-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="e139a-151">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="e139a-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="e139a-152">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="e139a-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="e139a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e139a-153">RELATED LINKS</span></span>

