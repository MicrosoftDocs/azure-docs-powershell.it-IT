---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 03fbbc38582bf301052074e674fa86abe97d6b61
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023156"
---
# <span data-ttu-id="9edc9-101">Remove-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="9edc9-101">Remove-AzsUserSubscription</span></span>

## <span data-ttu-id="9edc9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9edc9-102">SYNOPSIS</span></span>


## <span data-ttu-id="9edc9-103">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9edc9-103">SYNTAX</span></span>

### <span data-ttu-id="9edc9-104">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9edc9-104">Delete (Default)</span></span>
```
Remove-AzsUserSubscription -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Force] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9edc9-105">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9edc9-105">DeleteViaIdentity</span></span>
```
Remove-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Force]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9edc9-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9edc9-106">DESCRIPTION</span></span>


## <span data-ttu-id="9edc9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9edc9-107">EXAMPLES</span></span>

### <span data-ttu-id="9edc9-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9edc9-108">Example 1</span></span>
```powershell
PS C:\> Remove-AzsUserSubscription -SubscriptionId "c90173b1-de7a-4b1d-8600-b832b0e65946"

```

<span data-ttu-id="9edc9-109">Eliminare l'abbonamento al tenant specificato.</span><span class="sxs-lookup"><span data-stu-id="9edc9-109">Delete the specified tenant subscription.</span></span>

## <span data-ttu-id="9edc9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9edc9-110">PARAMETERS</span></span>

### <span data-ttu-id="9edc9-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9edc9-111">-DefaultProfile</span></span>


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

### <span data-ttu-id="9edc9-112">-Force</span><span class="sxs-lookup"><span data-stu-id="9edc9-112">-Force</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9edc9-113">-InputObject</span></span>
<span data-ttu-id="9edc9-114">Per costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="9edc9-114">To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9edc9-115">-PassThru</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-116">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9edc9-116">-SubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-117">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9edc9-117">-TargetSubscriptionId</span></span>


```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9edc9-118">-Confirm</span></span>
<span data-ttu-id="9edc9-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9edc9-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9edc9-120">-WhatIf</span></span>
<span data-ttu-id="9edc9-121">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9edc9-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9edc9-122">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9edc9-122">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="9edc9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9edc9-123">CommonParameters</span></span>
<span data-ttu-id="9edc9-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9edc9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9edc9-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9edc9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9edc9-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9edc9-126">INPUTS</span></span>

### <span data-ttu-id="9edc9-127">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="9edc9-127">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="9edc9-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9edc9-128">OUTPUTS</span></span>

### <span data-ttu-id="9edc9-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9edc9-129">System.Boolean</span></span>

<span data-ttu-id="9edc9-130">ALIAS</span><span class="sxs-lookup"><span data-stu-id="9edc9-130">ALIASES</span></span>

## <span data-ttu-id="9edc9-131">Note</span><span class="sxs-lookup"><span data-stu-id="9edc9-131">NOTES</span></span>

<span data-ttu-id="9edc9-132">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="9edc9-132">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9edc9-133">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9edc9-133">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="9edc9-134">INPUTOBJECT <ISubscriptionsAdminIdentity> :</span><span class="sxs-lookup"><span data-stu-id="9edc9-134">INPUTOBJECT <ISubscriptionsAdminIdentity>:</span></span> 
  - <span data-ttu-id="9edc9-135">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="9edc9-135">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="9edc9-136">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="9edc9-136">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="9edc9-137">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="9edc9-137">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9edc9-138">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="9edc9-138">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="9edc9-139">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="9edc9-139">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="9edc9-140">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edc9-140">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="9edc9-141">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="9edc9-141">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="9edc9-142">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="9edc9-142">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="9edc9-143">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="9edc9-143">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="9edc9-144">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="9edc9-144">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="9edc9-145">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="9edc9-145">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="9edc9-146">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="9edc9-146">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="9edc9-147">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="9edc9-147">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="9edc9-148">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9edc9-148">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="9edc9-149">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="9edc9-149">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="9edc9-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9edc9-150">RELATED LINKS</span></span>

