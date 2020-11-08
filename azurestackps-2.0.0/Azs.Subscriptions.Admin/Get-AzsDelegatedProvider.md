---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023093"
---
# <span data-ttu-id="b653b-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="b653b-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="b653b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b653b-102">SYNOPSIS</span></span>
<span data-ttu-id="b653b-103">Ottenere il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="b653b-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="b653b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b653b-104">SYNTAX</span></span>

### <span data-ttu-id="b653b-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b653b-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b653b-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="b653b-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b653b-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b653b-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b653b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b653b-108">DESCRIPTION</span></span>
<span data-ttu-id="b653b-109">Ottenere il provider delegato specificato.</span><span class="sxs-lookup"><span data-stu-id="b653b-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="b653b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b653b-110">EXAMPLES</span></span>

### <span data-ttu-id="b653b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b653b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="b653b-112">Ottenere un provider delegato specifico.</span><span class="sxs-lookup"><span data-stu-id="b653b-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="b653b-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b653b-113">PARAMETERS</span></span>

### <span data-ttu-id="b653b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b653b-114">-DefaultProfile</span></span>
<span data-ttu-id="b653b-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b653b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b653b-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="b653b-116">-DelegatedProviderId</span></span>
<span data-ttu-id="b653b-117">Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="b653b-117">DelegatedProvider identifier.</span></span>

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

### <span data-ttu-id="b653b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b653b-118">-InputObject</span></span>
<span data-ttu-id="b653b-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="b653b-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b653b-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b653b-120">-SubscriptionId</span></span>
<span data-ttu-id="b653b-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b653b-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b653b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b653b-122">CommonParameters</span></span>
<span data-ttu-id="b653b-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b653b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b653b-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b653b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b653b-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b653b-125">INPUTS</span></span>

### <span data-ttu-id="b653b-126">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="b653b-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="b653b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b653b-127">OUTPUTS</span></span>

### <span data-ttu-id="b653b-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="b653b-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="b653b-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b653b-129">ALIASES</span></span>

## <span data-ttu-id="b653b-130">Note</span><span class="sxs-lookup"><span data-stu-id="b653b-130">NOTES</span></span>

<span data-ttu-id="b653b-131">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="b653b-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b653b-132">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b653b-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="b653b-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="b653b-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b653b-134">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="b653b-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="b653b-135">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="b653b-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="b653b-136">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="b653b-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b653b-137">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="b653b-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="b653b-138">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="b653b-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="b653b-139">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="b653b-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="b653b-140">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="b653b-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="b653b-141">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="b653b-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="b653b-142">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="b653b-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="b653b-143">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="b653b-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="b653b-144">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="b653b-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="b653b-145">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="b653b-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="b653b-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="b653b-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="b653b-147">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="b653b-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="b653b-148">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="b653b-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="b653b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b653b-149">RELATED LINKS</span></span>

