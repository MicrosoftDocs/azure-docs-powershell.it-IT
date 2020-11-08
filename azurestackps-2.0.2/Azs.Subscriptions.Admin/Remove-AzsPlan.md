---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030390"
---
# <span data-ttu-id="35d66-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="35d66-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="35d66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35d66-102">SYNOPSIS</span></span>
<span data-ttu-id="35d66-103">Eliminare il piano specificato.</span><span class="sxs-lookup"><span data-stu-id="35d66-103">Delete the specified plan.</span></span>

## <span data-ttu-id="35d66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35d66-104">SYNTAX</span></span>

### <span data-ttu-id="35d66-105">Elimina (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35d66-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="35d66-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="35d66-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="35d66-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35d66-107">DESCRIPTION</span></span>
<span data-ttu-id="35d66-108">Eliminare il piano specificato.</span><span class="sxs-lookup"><span data-stu-id="35d66-108">Delete the specified plan.</span></span>

## <span data-ttu-id="35d66-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35d66-109">EXAMPLES</span></span>

### <span data-ttu-id="35d66-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="35d66-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="35d66-111">Eliminare il piano specificato</span><span class="sxs-lookup"><span data-stu-id="35d66-111">Delete the specified plan</span></span>

## <span data-ttu-id="35d66-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35d66-112">PARAMETERS</span></span>

### <span data-ttu-id="35d66-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35d66-113">-DefaultProfile</span></span>
<span data-ttu-id="35d66-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35d66-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35d66-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35d66-115">-InputObject</span></span>
<span data-ttu-id="35d66-116">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="35d66-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="35d66-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="35d66-117">-Name</span></span>
<span data-ttu-id="35d66-118">Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="35d66-118">Name of the plan.</span></span>

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

### <span data-ttu-id="35d66-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35d66-119">-PassThru</span></span>
<span data-ttu-id="35d66-120">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="35d66-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="35d66-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35d66-121">-ResourceGroupName</span></span>
<span data-ttu-id="35d66-122">Gruppo risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="35d66-122">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="35d66-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="35d66-123">-SubscriptionId</span></span>
<span data-ttu-id="35d66-124">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="35d66-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="35d66-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="35d66-125">-Confirm</span></span>
<span data-ttu-id="35d66-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35d66-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35d66-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35d66-127">-WhatIf</span></span>
<span data-ttu-id="35d66-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35d66-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35d66-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="35d66-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35d66-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35d66-130">CommonParameters</span></span>
<span data-ttu-id="35d66-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35d66-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35d66-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35d66-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35d66-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35d66-133">INPUTS</span></span>

### <span data-ttu-id="35d66-134">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="35d66-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="35d66-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35d66-135">OUTPUTS</span></span>

### <span data-ttu-id="35d66-136">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="35d66-136">System.Boolean</span></span>

<span data-ttu-id="35d66-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="35d66-137">ALIASES</span></span>

## <span data-ttu-id="35d66-138">Note</span><span class="sxs-lookup"><span data-stu-id="35d66-138">NOTES</span></span>

<span data-ttu-id="35d66-139">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="35d66-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="35d66-140">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="35d66-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="35d66-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="35d66-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="35d66-142">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="35d66-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="35d66-143">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="35d66-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="35d66-144">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="35d66-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="35d66-145">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="35d66-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="35d66-146">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="35d66-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="35d66-147">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="35d66-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="35d66-148">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="35d66-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="35d66-149">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="35d66-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="35d66-150">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="35d66-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="35d66-151">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="35d66-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="35d66-152">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="35d66-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="35d66-153">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="35d66-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="35d66-154">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="35d66-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="35d66-155">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="35d66-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="35d66-156">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="35d66-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="35d66-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35d66-157">RELATED LINKS</span></span>

