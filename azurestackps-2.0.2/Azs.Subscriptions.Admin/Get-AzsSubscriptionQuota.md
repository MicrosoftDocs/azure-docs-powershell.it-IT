---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azssubscriptionquota
schema: 2.0.0
ms.openlocfilehash: 8e1c03393c1d276f5c93425250bf7202e49022d8
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030527"
---
# <span data-ttu-id="cab93-101">Get-AzsSubscriptionQuota</span><span class="sxs-lookup"><span data-stu-id="cab93-101">Get-AzsSubscriptionQuota</span></span>

## <span data-ttu-id="cab93-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cab93-102">SYNOPSIS</span></span>
<span data-ttu-id="cab93-103">Ottiene una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="cab93-103">Gets a quota by name.</span></span>

## <span data-ttu-id="cab93-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cab93-104">SYNTAX</span></span>

### <span data-ttu-id="cab93-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cab93-105">List (Default)</span></span>
```
Get-AzsSubscriptionQuota [-Location <String>] [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="cab93-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cab93-106">Get</span></span>
```
Get-AzsSubscriptionQuota -Quota <String> [-Location <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cab93-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cab93-107">GetViaIdentity</span></span>
```
Get-AzsSubscriptionQuota -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cab93-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cab93-108">DESCRIPTION</span></span>
<span data-ttu-id="cab93-109">Ottiene una quota per nome.</span><span class="sxs-lookup"><span data-stu-id="cab93-109">Gets a quota by name.</span></span>

## <span data-ttu-id="cab93-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cab93-110">EXAMPLES</span></span>

### <span data-ttu-id="cab93-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cab93-111">Example 1</span></span>
```powershell

```

<span data-ttu-id="cab93-112">Ottenere l'elenco delle quote del provider di risorse di sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="cab93-112">Get the list of subscription resource provider quotas.</span></span>

## <span data-ttu-id="cab93-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cab93-113">PARAMETERS</span></span>

### <span data-ttu-id="cab93-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cab93-114">-DefaultProfile</span></span>
<span data-ttu-id="cab93-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cab93-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cab93-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cab93-116">-InputObject</span></span>
<span data-ttu-id="cab93-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cab93-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cab93-118">-Posizione</span><span class="sxs-lookup"><span data-stu-id="cab93-118">-Location</span></span>
<span data-ttu-id="cab93-119">La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="cab93-119">The AzureStack location.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cab93-120">-Quota</span><span class="sxs-lookup"><span data-stu-id="cab93-120">-Quota</span></span>
<span data-ttu-id="cab93-121">Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="cab93-121">Name of the quota.</span></span>

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

### <span data-ttu-id="cab93-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cab93-122">-SubscriptionId</span></span>
<span data-ttu-id="cab93-123">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cab93-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cab93-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cab93-124">CommonParameters</span></span>
<span data-ttu-id="cab93-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cab93-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cab93-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cab93-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cab93-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cab93-127">INPUTS</span></span>

### <span data-ttu-id="cab93-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cab93-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="cab93-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cab93-129">OUTPUTS</span></span>

### <span data-ttu-id="cab93-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IQuota</span><span class="sxs-lookup"><span data-stu-id="cab93-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IQuota</span></span>

<span data-ttu-id="cab93-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cab93-131">ALIASES</span></span>

<span data-ttu-id="cab93-132">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="cab93-132">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="cab93-133">Note</span><span class="sxs-lookup"><span data-stu-id="cab93-133">NOTES</span></span>

<span data-ttu-id="cab93-134">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cab93-134">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cab93-135">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cab93-135">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cab93-136">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cab93-136">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cab93-137">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="cab93-137">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="cab93-138">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="cab93-138">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="cab93-139">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cab93-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cab93-140">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="cab93-140">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="cab93-141">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="cab93-141">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="cab93-142">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="cab93-142">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="cab93-143">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="cab93-143">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="cab93-144">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="cab93-144">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="cab93-145">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="cab93-145">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="cab93-146">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="cab93-146">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="cab93-147">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="cab93-147">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cab93-148">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cab93-148">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="cab93-149">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cab93-149">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cab93-150">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cab93-150">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="cab93-151">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="cab93-151">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="cab93-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cab93-152">RELATED LINKS</span></span>

