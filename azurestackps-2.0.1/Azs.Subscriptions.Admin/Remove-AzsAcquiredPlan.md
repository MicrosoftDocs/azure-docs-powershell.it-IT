---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsacquiredplan
schema: 2.0.0
ms.openlocfilehash: 80a4353497d0c7894a8c0ac4d95e57e56a6211a1
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023136"
---
# <span data-ttu-id="a61ab-101">Remove-AzsAcquiredPlan</span><span class="sxs-lookup"><span data-stu-id="a61ab-101">Remove-AzsAcquiredPlan</span></span>

## <span data-ttu-id="a61ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a61ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a61ab-103">Elimina un piano acquisito.</span><span class="sxs-lookup"><span data-stu-id="a61ab-103">Deletes an acquired plan.</span></span>

## <span data-ttu-id="a61ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a61ab-104">SYNTAX</span></span>

### <span data-ttu-id="a61ab-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a61ab-105">Delete (Default)</span></span>
```
Remove-AzsAcquiredPlan -PlanAcquisitionId <String> -TargetSubscriptionId <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="a61ab-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a61ab-106">DeleteViaIdentity</span></span>
```
Remove-AzsAcquiredPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="a61ab-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a61ab-107">DESCRIPTION</span></span>
<span data-ttu-id="a61ab-108">Elimina un piano acquisito.</span><span class="sxs-lookup"><span data-stu-id="a61ab-108">Deletes an acquired plan.</span></span>

## <span data-ttu-id="a61ab-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a61ab-109">EXAMPLES</span></span>

### <span data-ttu-id="a61ab-110">Esempio 1:</span><span class="sxs-lookup"><span data-stu-id="a61ab-110">Example 1:</span></span>
```powershell
PS C:\> Remove-AzsAcquiredPlan -PlanAcquisitionId "718c7f7c-4868-479a-98ce-5caaa8f158c2" -TargetSubscriptionId "d77ed1d7-cb62-4658-a777-386a8ae523dd"

```

<span data-ttu-id="a61ab-111">Eliminare un piano acquisito.</span><span class="sxs-lookup"><span data-stu-id="a61ab-111">Delete an acquired plan.</span></span>

## <span data-ttu-id="a61ab-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a61ab-112">PARAMETERS</span></span>

### <span data-ttu-id="a61ab-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a61ab-113">-DefaultProfile</span></span>
<span data-ttu-id="a61ab-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a61ab-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a61ab-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a61ab-115">-InputObject</span></span>
<span data-ttu-id="a61ab-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="a61ab-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a61ab-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a61ab-117">-PassThru</span></span>
<span data-ttu-id="a61ab-118">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="a61ab-118">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="a61ab-119">-PlanAcquisitionId</span><span class="sxs-lookup"><span data-stu-id="a61ab-119">-PlanAcquisitionId</span></span>
<span data-ttu-id="a61ab-120">Identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="a61ab-120">The plan acquisition Identifier</span></span>

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

### <span data-ttu-id="a61ab-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a61ab-121">-SubscriptionId</span></span>
<span data-ttu-id="a61ab-122">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a61ab-122">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a61ab-123">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a61ab-123">-TargetSubscriptionId</span></span>
<span data-ttu-id="a61ab-124">ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a61ab-124">The target subscription ID.</span></span>

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

### <span data-ttu-id="a61ab-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a61ab-125">-Confirm</span></span>
<span data-ttu-id="a61ab-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a61ab-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a61ab-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a61ab-127">-WhatIf</span></span>
<span data-ttu-id="a61ab-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a61ab-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a61ab-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a61ab-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a61ab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a61ab-130">CommonParameters</span></span>
<span data-ttu-id="a61ab-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a61ab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a61ab-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a61ab-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a61ab-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a61ab-133">INPUTS</span></span>

### <span data-ttu-id="a61ab-134">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="a61ab-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="a61ab-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a61ab-135">OUTPUTS</span></span>

### <span data-ttu-id="a61ab-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a61ab-136">System.Boolean</span></span>

<span data-ttu-id="a61ab-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a61ab-137">ALIASES</span></span>

### <span data-ttu-id="a61ab-138">Remove-AzsSubscriptionPlan</span><span class="sxs-lookup"><span data-stu-id="a61ab-138">Remove-AzsSubscriptionPlan</span></span>

## <span data-ttu-id="a61ab-139">Note</span><span class="sxs-lookup"><span data-stu-id="a61ab-139">NOTES</span></span>

<span data-ttu-id="a61ab-140">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="a61ab-140">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a61ab-141">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a61ab-141">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a61ab-142">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="a61ab-142">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a61ab-143">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="a61ab-143">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="a61ab-144">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="a61ab-144">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="a61ab-145">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="a61ab-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a61ab-146">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="a61ab-146">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="a61ab-147">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="a61ab-147">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="a61ab-148">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a61ab-148">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="a61ab-149">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="a61ab-149">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="a61ab-150">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="a61ab-150">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="a61ab-151">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="a61ab-151">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="a61ab-152">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="a61ab-152">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="a61ab-153">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="a61ab-153">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="a61ab-154">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="a61ab-154">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="a61ab-155">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="a61ab-155">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="a61ab-156">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="a61ab-156">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="a61ab-157">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="a61ab-157">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="a61ab-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a61ab-158">RELATED LINKS</span></span>

