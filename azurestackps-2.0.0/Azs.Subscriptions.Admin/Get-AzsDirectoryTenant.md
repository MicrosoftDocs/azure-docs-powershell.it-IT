---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdirectorytenant
schema: 2.0.0
ms.openlocfilehash: f516562b6bc4a136c64a15fa1f128cd1bda502d9
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023090"
---
# <span data-ttu-id="93589-101">Get-AzsDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="93589-101">Get-AzsDirectoryTenant</span></span>

## <span data-ttu-id="93589-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93589-102">SYNOPSIS</span></span>
<span data-ttu-id="93589-103">Ottenere un tenant della directory per nome.</span><span class="sxs-lookup"><span data-stu-id="93589-103">Get a directory tenant by name.</span></span>

## <span data-ttu-id="93589-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93589-104">SYNTAX</span></span>

### <span data-ttu-id="93589-105">Elenco (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93589-105">List (Default)</span></span>
```
Get-AzsDirectoryTenant -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="93589-106">Ottieni</span><span class="sxs-lookup"><span data-stu-id="93589-106">Get</span></span>
```
Get-AzsDirectoryTenant -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="93589-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="93589-107">GetViaIdentity</span></span>
```
Get-AzsDirectoryTenant -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="93589-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93589-108">DESCRIPTION</span></span>
<span data-ttu-id="93589-109">Ottenere un tenant della directory per nome.</span><span class="sxs-lookup"><span data-stu-id="93589-109">Get a directory tenant by name.</span></span>

## <span data-ttu-id="93589-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93589-110">EXAMPLES</span></span>

### <span data-ttu-id="93589-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93589-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDirectoryTenant -ResourceGroupName 'system.redmond'

Location Name                           Type                                          
-------- ----                           ----                                          
redmond  azurestack01.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
redmond  azurestack02.onmicrosoft.com Microsoft.Subscriptions.Admin/directoryTenants
```

<span data-ttu-id="93589-112">Elenca tutti i tenant della directory sotto l'abbonamento corrente e il nome del gruppo di risorse assegnato.</span><span class="sxs-lookup"><span data-stu-id="93589-112">Lists all the directory tenants under the current subscription and given resource group name.</span></span>

## <span data-ttu-id="93589-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93589-113">PARAMETERS</span></span>

### <span data-ttu-id="93589-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93589-114">-DefaultProfile</span></span>
<span data-ttu-id="93589-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93589-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93589-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="93589-116">-InputObject</span></span>
<span data-ttu-id="93589-117">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="93589-117">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="93589-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="93589-118">-Name</span></span>
<span data-ttu-id="93589-119">Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="93589-119">Directory tenant name.</span></span>

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

### <span data-ttu-id="93589-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93589-120">-ResourceGroupName</span></span>
<span data-ttu-id="93589-121">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="93589-121">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="93589-122">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="93589-122">-SubscriptionId</span></span>
<span data-ttu-id="93589-123">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="93589-123">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="93589-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93589-124">CommonParameters</span></span>
<span data-ttu-id="93589-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93589-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93589-126">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93589-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93589-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93589-127">INPUTS</span></span>

### <span data-ttu-id="93589-128">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="93589-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="93589-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93589-129">OUTPUTS</span></span>

### <span data-ttu-id="93589-130">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IDirectoryTenant</span><span class="sxs-lookup"><span data-stu-id="93589-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IDirectoryTenant</span></span>

<span data-ttu-id="93589-131">ALIAS</span><span class="sxs-lookup"><span data-stu-id="93589-131">ALIASES</span></span>

## <span data-ttu-id="93589-132">Note</span><span class="sxs-lookup"><span data-stu-id="93589-132">NOTES</span></span>

<span data-ttu-id="93589-133">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="93589-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="93589-134">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="93589-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="93589-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="93589-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="93589-136">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="93589-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="93589-137">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="93589-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="93589-138">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="93589-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="93589-139">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="93589-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="93589-140">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="93589-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="93589-141">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="93589-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="93589-142">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="93589-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="93589-143">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="93589-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="93589-144">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="93589-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="93589-145">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="93589-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="93589-146">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="93589-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="93589-147">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="93589-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="93589-148">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="93589-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="93589-149">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="93589-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="93589-150">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="93589-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="93589-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93589-151">RELATED LINKS</span></span>

