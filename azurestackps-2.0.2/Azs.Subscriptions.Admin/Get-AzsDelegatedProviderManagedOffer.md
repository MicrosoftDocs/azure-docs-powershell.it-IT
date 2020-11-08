---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovidermanagedoffer
schema: 2.0.0
ms.openlocfilehash: 238fe2a9c3f0cf1d4fdefc5a09231066152cfe60
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030615"
---
# <span data-ttu-id="cd744-101">Get-AzsDelegatedProviderManagedOffer</span><span class="sxs-lookup"><span data-stu-id="cd744-101">Get-AzsDelegatedProviderManagedOffer</span></span>

## <span data-ttu-id="cd744-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cd744-102">SYNOPSIS</span></span>
<span data-ttu-id="cd744-103">Ottenere l'offerta del provider delegata specificata.</span><span class="sxs-lookup"><span data-stu-id="cd744-103">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="cd744-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd744-104">SYNTAX</span></span>

### <span data-ttu-id="cd744-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd744-105">List (Default)</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd744-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="cd744-106">Get</span></span>
```
Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId <String> -Name <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd744-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cd744-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProviderManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd744-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd744-108">DESCRIPTION</span></span>
<span data-ttu-id="cd744-109">Ottenere l'offerta del provider delegata specificata.</span><span class="sxs-lookup"><span data-stu-id="cd744-109">Get the specified delegated provider offer.</span></span>

## <span data-ttu-id="cd744-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd744-110">EXAMPLES</span></span>

### <span data-ttu-id="cd744-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cd744-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProviderManagedOffer -DelegatedProviderSubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

{{ Add output here }}
```

<span data-ttu-id="cd744-112">Ottenere l'elenco dei provider delegati offerti.</span><span class="sxs-lookup"><span data-stu-id="cd744-112">Get the list of delegated provider offers.</span></span>

## <span data-ttu-id="cd744-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cd744-113">PARAMETERS</span></span>

### <span data-ttu-id="cd744-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd744-114">-DefaultProfile</span></span>
<span data-ttu-id="cd744-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cd744-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd744-116">-DelegatedProviderSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd744-116">-DelegatedProviderSubscriptionId</span></span>
<span data-ttu-id="cd744-117">Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="cd744-117">Delegated provider subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases: DelegatedProviderId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="cd744-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd744-118">-InputObject</span></span>
<span data-ttu-id="cd744-119">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="cd744-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="cd744-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="cd744-120">-Name</span></span>
<span data-ttu-id="cd744-121">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="cd744-121">Name of an offer.</span></span>

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

### <span data-ttu-id="cd744-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd744-122">-SubscriptionId</span></span>
<span data-ttu-id="cd744-123">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cd744-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="cd744-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd744-124">CommonParameters</span></span>
<span data-ttu-id="cd744-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd744-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd744-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd744-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd744-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cd744-127">INPUTS</span></span>

### <span data-ttu-id="cd744-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="cd744-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="cd744-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd744-129">OUTPUTS</span></span>

### <span data-ttu-id="cd744-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="cd744-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDelegatedProviderOffer</span></span>

<span data-ttu-id="cd744-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="cd744-131">ALIASES</span></span>

## <span data-ttu-id="cd744-132">Note</span><span class="sxs-lookup"><span data-stu-id="cd744-132">NOTES</span></span>

<span data-ttu-id="cd744-133">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="cd744-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cd744-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cd744-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="cd744-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="cd744-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cd744-136">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="cd744-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="cd744-137">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="cd744-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="cd744-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="cd744-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cd744-139">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="cd744-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="cd744-140">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="cd744-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="cd744-141">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="cd744-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="cd744-142">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="cd744-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="cd744-143">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="cd744-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="cd744-144">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="cd744-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="cd744-145">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="cd744-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="cd744-146">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="cd744-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="cd744-147">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="cd744-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="cd744-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="cd744-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="cd744-149">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cd744-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="cd744-150">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="cd744-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="cd744-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd744-151">RELATED LINKS</span></span>

