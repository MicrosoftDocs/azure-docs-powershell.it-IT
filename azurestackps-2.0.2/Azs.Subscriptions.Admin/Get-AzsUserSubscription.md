---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: a36406499be15c53e9bfabd8aa9abf56b2afa1c7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030529"
---
# <span data-ttu-id="45792-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="45792-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="45792-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45792-102">SYNOPSIS</span></span>
<span data-ttu-id="45792-103">Ottenere un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="45792-103">Get a specified subscription.</span></span>

## <span data-ttu-id="45792-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45792-104">SYNTAX</span></span>

### <span data-ttu-id="45792-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="45792-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="45792-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="45792-106">Get</span></span>
```
Get-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="45792-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="45792-107">GetViaIdentity</span></span>
```
Get-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="45792-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45792-108">DESCRIPTION</span></span>
<span data-ttu-id="45792-109">Ottenere un abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="45792-109">Get a specified subscription.</span></span>

## <span data-ttu-id="45792-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45792-110">EXAMPLES</span></span>

### <span data-ttu-id="45792-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="45792-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsUserSubscription | Select-Object -First 1 | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : DRPTestffbffbe5-test-test-test-test-test-test
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ffbffbe5-8905-4f51-b2ed-4717049de782
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/DRPTestResourceGroup5056/providers/Microsoft.Subscriptions.Admin/offers/DRPTestOffer5056
Owner                           : user@microsoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ffbffbe5-8905-4f51-b2ed-4717049de782
TenantId                        : 76440dfb-c97c-4fee-8f6c-dff8ddbe816f
```

<span data-ttu-id="45792-112">Ottenere l'elenco degli abbonamenti agli utenti come operator.</span><span class="sxs-lookup"><span data-stu-id="45792-112">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="45792-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45792-113">PARAMETERS</span></span>

### <span data-ttu-id="45792-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45792-114">-DefaultProfile</span></span>
<span data-ttu-id="45792-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45792-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45792-116">-Filtro</span><span class="sxs-lookup"><span data-stu-id="45792-116">-Filter</span></span>
<span data-ttu-id="45792-117">Parametro di filtro OData.</span><span class="sxs-lookup"><span data-stu-id="45792-117">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="45792-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="45792-118">-InputObject</span></span>
<span data-ttu-id="45792-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="45792-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="45792-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45792-120">-SubscriptionId</span></span>
<span data-ttu-id="45792-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="45792-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="45792-122">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45792-122">-TargetSubscriptionId</span></span>
<span data-ttu-id="45792-123">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="45792-123">The target subscription ID.</span></span>

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

### <span data-ttu-id="45792-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45792-124">CommonParameters</span></span>
<span data-ttu-id="45792-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45792-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45792-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45792-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45792-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45792-127">INPUTS</span></span>

### <span data-ttu-id="45792-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="45792-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="45792-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45792-129">OUTPUTS</span></span>

### <span data-ttu-id="45792-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="45792-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="45792-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="45792-131">ALIASES</span></span>

## <span data-ttu-id="45792-132">Note</span><span class="sxs-lookup"><span data-stu-id="45792-132">NOTES</span></span>

<span data-ttu-id="45792-133">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="45792-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="45792-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="45792-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="45792-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="45792-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="45792-136">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="45792-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="45792-137">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="45792-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="45792-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="45792-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="45792-139">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="45792-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="45792-140">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="45792-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="45792-141">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="45792-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="45792-142">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="45792-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="45792-143">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="45792-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="45792-144">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="45792-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="45792-145">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="45792-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="45792-146">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="45792-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="45792-147">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="45792-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="45792-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="45792-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="45792-149">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="45792-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="45792-150">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="45792-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="45792-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45792-151">RELATED LINKS</span></span>

