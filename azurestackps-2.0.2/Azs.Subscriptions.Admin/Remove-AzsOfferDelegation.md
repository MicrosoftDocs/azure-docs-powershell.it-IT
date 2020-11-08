---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsofferdelegation
schema: 2.0.0
ms.openlocfilehash: e9de73f68501071bceb87c115c2c9882fc5ea988
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030392"
---
# <span data-ttu-id="f3a2f-101">Remove-AzsOfferDelegation</span><span class="sxs-lookup"><span data-stu-id="f3a2f-101">Remove-AzsOfferDelegation</span></span>

## <span data-ttu-id="f3a2f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3a2f-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a2f-103">Eliminare la delega offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-103">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="f3a2f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3a2f-104">SYNTAX</span></span>

### <span data-ttu-id="f3a2f-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f3a2f-105">Delete (Default)</span></span>
```
Remove-AzsOfferDelegation -Name <String> -OfferName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="f3a2f-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="f3a2f-106">DeleteViaIdentity</span></span>
```
Remove-AzsOfferDelegation -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3a2f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3a2f-107">DESCRIPTION</span></span>
<span data-ttu-id="f3a2f-108">Eliminare la delega offerta specificata.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-108">Delete the specified offer delegation.</span></span>

## <span data-ttu-id="f3a2f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3a2f-109">EXAMPLES</span></span>

### <span data-ttu-id="f3a2f-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f3a2f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsOfferDelegation -OfferName offer1 -ResourceGroupName rg1 -Name delegation1

{{ Add output here }}
```

<span data-ttu-id="f3a2f-111">Rimuove la delega dell'offerta</span><span class="sxs-lookup"><span data-stu-id="f3a2f-111">Removes the offer delegation</span></span>

## <span data-ttu-id="f3a2f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3a2f-112">PARAMETERS</span></span>

### <span data-ttu-id="f3a2f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a2f-113">-DefaultProfile</span></span>
<span data-ttu-id="f3a2f-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3a2f-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f3a2f-115">-InputObject</span></span>
<span data-ttu-id="f3a2f-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="f3a2f-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3a2f-117">-Name</span></span>
<span data-ttu-id="f3a2f-118">Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-118">Name of a offer delegation.</span></span>

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

### <span data-ttu-id="f3a2f-119">-Offername</span><span class="sxs-lookup"><span data-stu-id="f3a2f-119">-OfferName</span></span>
<span data-ttu-id="f3a2f-120">Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-120">Name of an offer.</span></span>

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

### <span data-ttu-id="f3a2f-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3a2f-121">-PassThru</span></span>
<span data-ttu-id="f3a2f-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="f3a2f-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3a2f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a2f-123">-ResourceGroupName</span></span>
<span data-ttu-id="f3a2f-124">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-124">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="f3a2f-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3a2f-125">-SubscriptionId</span></span>
<span data-ttu-id="f3a2f-126">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-126">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="f3a2f-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3a2f-127">-Confirm</span></span>
<span data-ttu-id="f3a2f-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a2f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a2f-129">-WhatIf</span></span>
<span data-ttu-id="f3a2f-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a2f-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a2f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a2f-132">CommonParameters</span></span>
<span data-ttu-id="f3a2f-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a2f-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3a2f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a2f-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3a2f-135">INPUTS</span></span>

### <span data-ttu-id="f3a2f-136">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="f3a2f-136">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="f3a2f-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3a2f-137">OUTPUTS</span></span>

### <span data-ttu-id="f3a2f-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f3a2f-138">System.Boolean</span></span>

<span data-ttu-id="f3a2f-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f3a2f-139">ALIASES</span></span>

## <span data-ttu-id="f3a2f-140">Note</span><span class="sxs-lookup"><span data-stu-id="f3a2f-140">NOTES</span></span>

<span data-ttu-id="f3a2f-141">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="f3a2f-142">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="f3a2f-143">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="f3a2f-143">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="f3a2f-144">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-144">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="f3a2f-145">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-145">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="f3a2f-146">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="f3a2f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="f3a2f-147">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-147">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="f3a2f-148">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-148">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="f3a2f-149">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-149">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="f3a2f-150">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-150">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="f3a2f-151">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-151">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="f3a2f-152">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-152">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="f3a2f-153">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="f3a2f-153">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="f3a2f-154">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-154">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="f3a2f-155">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-155">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="f3a2f-156">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-156">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="f3a2f-157">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-157">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="f3a2f-158">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="f3a2f-158">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="f3a2f-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3a2f-159">RELATED LINKS</span></span>

