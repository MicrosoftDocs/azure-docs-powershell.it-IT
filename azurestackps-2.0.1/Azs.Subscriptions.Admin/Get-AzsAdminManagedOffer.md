---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsadminmanagedoffer
schema: 2.0.0
ms.openlocfilehash: 79cac7a530a9aedc1e53120b29eb2dd8cb73489b
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023117"
---
# <span data-ttu-id="f45bf-101">Get-AzsAdminManagedOffer</span><span class="sxs-lookup"><span data-stu-id="f45bf-101">Get-AzsAdminManagedOffer</span></span>

## <span data-ttu-id="f45bf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f45bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f45bf-103">Ottenere l'offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="f45bf-103">Get the specified offer.</span></span>

## <span data-ttu-id="f45bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f45bf-104">SYNTAX</span></span>

### <span data-ttu-id="f45bf-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f45bf-105">List (Default)</span></span>
```
Get-AzsAdminManagedOffer [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f45bf-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="f45bf-106">Get</span></span>
```
Get-AzsAdminManagedOffer -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="f45bf-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f45bf-107">GetViaIdentity</span></span>
```
Get-AzsAdminManagedOffer -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="f45bf-108">List1</span><span class="sxs-lookup"><span data-stu-id="f45bf-108">List1</span></span>
```
Get-AzsAdminManagedOffer -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="f45bf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f45bf-109">DESCRIPTION</span></span>
<span data-ttu-id="f45bf-110">Ottenere l'offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="f45bf-110">Get the specified offer.</span></span>

## <span data-ttu-id="f45bf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f45bf-111">EXAMPLES</span></span>

### <span data-ttu-id="f45bf-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f45bf-112">Example 1</span></span>
```powershell
PS C:\> Get-AzsAdminManagedOffer -Name "testoffer" -ResourceGroupName "testrg"

AddonPlans                 : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/addonplan}
BasePlanIds                : {/subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/plans/testplan}
Description                : 
DisplayName                : testoffer
ExternalReferenceId        : 
Id                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/testrg/providers/Microsoft.Subscriptions.Admin/offers/testoffer
Location                   : redmond
MaxSubscriptionsPerAccount : 0
Name                       : testoffer
PropertiesName             : testoffer
State                      : Private
SubscriptionCount          : 0
Tags                       : Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ResourceTags
Type                       : Microsoft.Subscriptions.Admin/offers
```

<span data-ttu-id="f45bf-113">Ottenere l'offerta per nome e ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45bf-113">Get offer by Name and ResourceGroupName</span></span>

## <span data-ttu-id="f45bf-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f45bf-114">PARAMETERS</span></span>

### <span data-ttu-id="f45bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f45bf-115">-DefaultProfile</span></span>
<span data-ttu-id="f45bf-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f45bf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f45bf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f45bf-117">-InputObject</span></span>
<span data-ttu-id="f45bf-118">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f45bf-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f45bf-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="f45bf-119">-Name</span></span>
<span data-ttu-id="f45bf-120">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f45bf-120">Name of an offer.</span></span>

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

### <span data-ttu-id="f45bf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f45bf-121">-ResourceGroupName</span></span>
<span data-ttu-id="f45bf-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f45bf-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f45bf-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f45bf-123">-SubscriptionId</span></span>
<span data-ttu-id="f45bf-124">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f45bf-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="f45bf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f45bf-125">CommonParameters</span></span>
<span data-ttu-id="f45bf-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f45bf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f45bf-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f45bf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f45bf-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f45bf-128">INPUTS</span></span>

### <span data-ttu-id="f45bf-129">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f45bf-129">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f45bf-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f45bf-130">OUTPUTS</span></span>

### <span data-ttu-id="f45bf-131">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IOffer</span><span class="sxs-lookup"><span data-stu-id="f45bf-131">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IOffer</span></span>

<span data-ttu-id="f45bf-132">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f45bf-132">ALIASES</span></span>

<span data-ttu-id="f45bf-133">Get-AzsManagedOffer</span><span class="sxs-lookup"><span data-stu-id="f45bf-133">Get-AzsManagedOffer</span></span>

## <span data-ttu-id="f45bf-134">Note</span><span class="sxs-lookup"><span data-stu-id="f45bf-134">NOTES</span></span>

<span data-ttu-id="f45bf-135">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f45bf-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f45bf-136">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f45bf-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f45bf-137">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f45bf-137">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f45bf-138">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="f45bf-138">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f45bf-139">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="f45bf-139">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f45bf-140">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f45bf-140">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f45bf-141">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="f45bf-141">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f45bf-142">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="f45bf-142">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f45bf-143">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f45bf-143">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f45bf-144">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f45bf-144">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f45bf-145">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="f45bf-145">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f45bf-146">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="f45bf-146">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f45bf-147">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="f45bf-147">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f45bf-148">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="f45bf-148">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f45bf-149">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f45bf-149">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f45bf-150">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f45bf-150">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f45bf-151">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f45bf-151">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f45bf-152">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="f45bf-152">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f45bf-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f45bf-153">RELATED LINKS</span></span>

