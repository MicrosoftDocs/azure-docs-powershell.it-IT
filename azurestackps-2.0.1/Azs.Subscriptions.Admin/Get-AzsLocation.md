---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azslocation
schema: 2.0.0
ms.openlocfilehash: 431989f382d51b596cafc74d4cf229c6e803ccd6
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023333"
---
# <span data-ttu-id="c40bd-101">Get-AzsLocation</span><span class="sxs-lookup"><span data-stu-id="c40bd-101">Get-AzsLocation</span></span>

## <span data-ttu-id="c40bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c40bd-102">SYNOPSIS</span></span>
<span data-ttu-id="c40bd-103">Ottenere la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c40bd-103">Get the specified location.</span></span>

## <span data-ttu-id="c40bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c40bd-104">SYNTAX</span></span>

### <span data-ttu-id="c40bd-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c40bd-105">List (Default)</span></span>
```
Get-AzsLocation [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c40bd-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="c40bd-106">Get</span></span>
```
Get-AzsLocation -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="c40bd-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="c40bd-107">GetViaIdentity</span></span>
```
Get-AzsLocation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="c40bd-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c40bd-108">DESCRIPTION</span></span>
<span data-ttu-id="c40bd-109">Ottenere la posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="c40bd-109">Get the specified location.</span></span>

## <span data-ttu-id="c40bd-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c40bd-110">EXAMPLES</span></span>

### <span data-ttu-id="c40bd-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c40bd-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsLocation

DisplayName Latitude Longitude Name   
----------- -------- --------- ----   
redmond                        redmond
```

<span data-ttu-id="c40bd-112">Ottenere un elenco di tutte le posizioni di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c40bd-112">Get a list of all AzureStack locations.</span></span>

## <span data-ttu-id="c40bd-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c40bd-113">PARAMETERS</span></span>

### <span data-ttu-id="c40bd-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c40bd-114">-DefaultProfile</span></span>
<span data-ttu-id="c40bd-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c40bd-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c40bd-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c40bd-116">-InputObject</span></span>
<span data-ttu-id="c40bd-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="c40bd-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="c40bd-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c40bd-118">-Name</span></span>
<span data-ttu-id="c40bd-119">La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c40bd-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: Location

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="c40bd-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c40bd-120">-SubscriptionId</span></span>
<span data-ttu-id="c40bd-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c40bd-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c40bd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c40bd-122">CommonParameters</span></span>
<span data-ttu-id="c40bd-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c40bd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c40bd-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c40bd-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c40bd-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c40bd-125">INPUTS</span></span>

### <span data-ttu-id="c40bd-126">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="c40bd-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="c40bd-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c40bd-127">OUTPUTS</span></span>

### <span data-ttu-id="c40bd-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. ILocation</span><span class="sxs-lookup"><span data-stu-id="c40bd-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ILocation</span></span>

<span data-ttu-id="c40bd-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c40bd-129">ALIASES</span></span>

## <span data-ttu-id="c40bd-130">Note</span><span class="sxs-lookup"><span data-stu-id="c40bd-130">NOTES</span></span>

<span data-ttu-id="c40bd-131">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="c40bd-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c40bd-132">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c40bd-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="c40bd-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="c40bd-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="c40bd-134">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="c40bd-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="c40bd-135">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="c40bd-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="c40bd-136">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="c40bd-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="c40bd-137">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c40bd-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="c40bd-138">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="c40bd-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="c40bd-139">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="c40bd-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="c40bd-140">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="c40bd-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="c40bd-141">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="c40bd-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="c40bd-142">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="c40bd-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="c40bd-143">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="c40bd-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="c40bd-144">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="c40bd-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="c40bd-145">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="c40bd-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="c40bd-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="c40bd-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="c40bd-147">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="c40bd-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="c40bd-148">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="c40bd-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="c40bd-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c40bd-149">RELATED LINKS</span></span>

