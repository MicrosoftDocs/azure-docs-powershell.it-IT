---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: c73a4c4bcc482b7e6e1281d0bc4ee6c29921b745
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023115"
---
# <span data-ttu-id="1f4b3-101">Get-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="1f4b3-101">Get-AzsAcquiredPlan</span></span>

## <span data-ttu-id="1f4b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f4b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1f4b3-103">Ottiene il piano specificato acquisito da un abbonamento che consuma l'offerta.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-103">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="1f4b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f4b3-104">SYNTAX</span></span>

### <span data-ttu-id="1f4b3-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f4b3-105">List (Default)</span></span>
```
Get-AzsAcquiredPlan -TargetSubscriptionId <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="1f4b3-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="1f4b3-106">Get</span></span>
```
Get-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1f4b3-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1f4b3-107">GetViaIdentity</span></span>
```
Get-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1f4b3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f4b3-108">DESCRIPTION</span></span>
<span data-ttu-id="1f4b3-109">Ottiene il piano specificato acquisito da un abbonamento che consuma l'offerta.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-109">Gets the specified plan acquired by a subscription consuming the offer.</span></span>

## <span data-ttu-id="1f4b3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f4b3-110">EXAMPLES</span></span>

### <span data-ttu-id="1f4b3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1f4b3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsAcquiredPlan -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

AcquisitionId       : 718c7f7c-4868-479a-98ce-5caaa8f158c1
AcquisitionTime     : 3/12/2020 11:16:08 PM
ExternalReferenceId : 
Id                  : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/acquiredPlan
                      s/718c7f7c-4868-479a-98ce-5caaa8f158c1
PlanId              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/plans/testplan
ProvisioningState   : Succeeded
```

<span data-ttu-id="1f4b3-112">Ottenere una raccolta di tutti i piani acquisiti a cui l'abbonamento ha accesso.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-112">Get a collection of all acquired plans that subscription has access to.</span></span>

## <span data-ttu-id="1f4b3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f4b3-113">PARAMETERS</span></span>

### <span data-ttu-id="1f4b3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f4b3-114">-DefaultProfile</span></span>
<span data-ttu-id="1f4b3-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f4b3-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f4b3-116">-InputObject</span></span>
<span data-ttu-id="1f4b3-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="1f4b3-118">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="1f4b3-118">-PlanAcquisitionId</span></span>
<span data-ttu-id="1f4b3-119">Identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="1f4b3-119">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="1f4b3-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f4b3-120">-SubscriptionId</span></span>
<span data-ttu-id="1f4b3-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1f4b3-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1f4b3-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="1f4b3-123">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="1f4b3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f4b3-124">CommonParameters</span></span>
<span data-ttu-id="1f4b3-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f4b3-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1f4b3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f4b3-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f4b3-127">INPUTS</span></span>

### <span data-ttu-id="1f4b3-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1f4b3-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="1f4b3-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f4b3-129">OUTPUTS</span></span>

### <span data-ttu-id="1f4b3-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IPlanAcquisition</span><span class="sxs-lookup"><span data-stu-id="1f4b3-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IPlanAcquisition</span></span>

<span data-ttu-id="1f4b3-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1f4b3-131">ALIASES</span></span>

<span data-ttu-id="1f4b3-132">Get-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="1f4b3-132">Get-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="1f4b3-133">Note</span><span class="sxs-lookup"><span data-stu-id="1f4b3-133">NOTES</span></span>

<span data-ttu-id="1f4b3-134">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1f4b3-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1f4b3-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="1f4b3-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1f4b3-137">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="1f4b3-138">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="1f4b3-139">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="1f4b3-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1f4b3-140">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="1f4b3-141">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="1f4b3-142">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="1f4b3-143">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="1f4b3-144">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="1f4b3-145">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="1f4b3-146">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="1f4b3-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="1f4b3-147">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="1f4b3-148">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="1f4b3-149">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="1f4b3-150">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="1f4b3-151">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="1f4b3-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="1f4b3-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f4b3-152">RELATED LINKS</span></span>

