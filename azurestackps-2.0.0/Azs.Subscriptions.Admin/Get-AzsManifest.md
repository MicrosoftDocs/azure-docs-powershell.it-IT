---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsmanifest
schema: 2.0.0
ms.openlocfilehash: 4e5ccedc67af31c19d35e5a91fad62ba46535ed7
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023088"
---
# <span data-ttu-id="079f5-101">Get-AzsManifest</span><span class="sxs-lookup"><span data-stu-id="079f5-101">Get-AzsManifest</span></span>

## <span data-ttu-id="079f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="079f5-102">SYNOPSIS</span></span>
<span data-ttu-id="079f5-103">Ottieni il manifesto specificato.</span><span class="sxs-lookup"><span data-stu-id="079f5-103">Get the specified manifest.</span></span>

## <span data-ttu-id="079f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="079f5-104">SYNTAX</span></span>

### <span data-ttu-id="079f5-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="079f5-105">List (Default)</span></span>
```
Get-AzsManifest [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="079f5-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="079f5-106">Get</span></span>
```
Get-AzsManifest -ManifestName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="079f5-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="079f5-107">GetViaIdentity</span></span>
```
Get-AzsManifest -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="079f5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="079f5-108">DESCRIPTION</span></span>
<span data-ttu-id="079f5-109">Ottieni il manifesto specificato.</span><span class="sxs-lookup"><span data-stu-id="079f5-109">Get the specified manifest.</span></span>

## <span data-ttu-id="079f5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="079f5-110">EXAMPLES</span></span>

### <span data-ttu-id="079f5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="079f5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsManifest

Name     : Microsoft-Authorization-Admin--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata

Name     : Microsoft-Authorization--redmond--Admin
Metadata : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ManifestMetadata
```

<span data-ttu-id="079f5-112">Elenca tutti i manifesti sotto la sottoscrizione corrente.</span><span class="sxs-lookup"><span data-stu-id="079f5-112">Lists all the manifests under the current subscription.</span></span>

## <span data-ttu-id="079f5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="079f5-113">PARAMETERS</span></span>

### <span data-ttu-id="079f5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="079f5-114">-DefaultProfile</span></span>
<span data-ttu-id="079f5-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="079f5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="079f5-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="079f5-116">-InputObject</span></span>
<span data-ttu-id="079f5-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="079f5-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="079f5-118">-Manifestoname</span><span class="sxs-lookup"><span data-stu-id="079f5-118">-ManifestName</span></span>
<span data-ttu-id="079f5-119">Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="079f5-119">The manifest name.</span></span>

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

### <span data-ttu-id="079f5-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="079f5-120">-SubscriptionId</span></span>
<span data-ttu-id="079f5-121">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="079f5-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="079f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="079f5-122">CommonParameters</span></span>
<span data-ttu-id="079f5-123">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="079f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="079f5-124">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="079f5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="079f5-125">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="079f5-125">INPUTS</span></span>

### <span data-ttu-id="079f5-126">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="079f5-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="079f5-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="079f5-127">OUTPUTS</span></span>

### <span data-ttu-id="079f5-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. imanif più</span><span class="sxs-lookup"><span data-stu-id="079f5-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IManifest</span></span>

<span data-ttu-id="079f5-129">ALIAS</span><span class="sxs-lookup"><span data-stu-id="079f5-129">ALIASES</span></span>

## <span data-ttu-id="079f5-130">Note</span><span class="sxs-lookup"><span data-stu-id="079f5-130">NOTES</span></span>

<span data-ttu-id="079f5-131">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="079f5-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="079f5-132">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="079f5-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="079f5-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="079f5-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="079f5-134">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="079f5-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="079f5-135">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="079f5-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="079f5-136">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="079f5-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="079f5-137">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="079f5-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="079f5-138">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="079f5-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="079f5-139">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="079f5-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="079f5-140">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="079f5-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="079f5-141">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="079f5-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="079f5-142">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="079f5-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="079f5-143">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="079f5-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="079f5-144">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="079f5-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="079f5-145">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="079f5-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="079f5-146">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="079f5-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="079f5-147">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="079f5-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="079f5-148">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="079f5-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="079f5-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="079f5-149">RELATED LINKS</span></span>

