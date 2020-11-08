---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/move-azsusersubscription
schema: 2.0.0
ms.openlocfilehash: 51ad63ef1531e7494b3929b8508e88e988155081
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/24/2020
ms.locfileid: "94023296"
---
# <span data-ttu-id="649bd-101">Move-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="649bd-101">Move-AzsUserSubscription</span></span>

## <span data-ttu-id="649bd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="649bd-102">SYNOPSIS</span></span>
<span data-ttu-id="649bd-103">Trasferimento di abbonamenti tra offerte di provider Delegate.</span><span class="sxs-lookup"><span data-stu-id="649bd-103">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="649bd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="649bd-104">SYNTAX</span></span>

### <span data-ttu-id="649bd-105">MoveExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="649bd-105">MoveExpanded (Default)</span></span>
```
Move-AzsUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="649bd-106">Spostare</span><span class="sxs-lookup"><span data-stu-id="649bd-106">Move</span></span>
```
Move-AzsUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="649bd-107">MoveViaIdentity</span><span class="sxs-lookup"><span data-stu-id="649bd-107">MoveViaIdentity</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="649bd-108">MoveViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="649bd-108">MoveViaIdentityExpanded</span></span>
```
Move-AzsUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="649bd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="649bd-109">DESCRIPTION</span></span>
<span data-ttu-id="649bd-110">Trasferimento di abbonamenti tra offerte di provider Delegate.</span><span class="sxs-lookup"><span data-stu-id="649bd-110">Move subscriptions between delegated provider offers.</span></span>

## <span data-ttu-id="649bd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="649bd-111">EXAMPLES</span></span>

### <span data-ttu-id="649bd-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="649bd-112">Example 1</span></span>
```powershell
PS C:\> Move-AzsSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

{{ Add output here }}
```

<span data-ttu-id="649bd-113">Trasferire le sottoscrizioni degli utenti a un'offerta di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="649bd-113">Move user subscriptions to a delegated provider offer.</span></span>

### <span data-ttu-id="649bd-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="649bd-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where {$_.DelegatedProviderSubscriptionId -eq "798568b7-c6f1-4bf7-bb8f-2c8bebc7c777"} | Select -ExpandProperty Id
Move-AzsSubscription -ResourceId $resourceIds

{{ Add output here }}
```

<span data-ttu-id="649bd-115">Trasferire gli abbonamenti degli utenti da un provider delegato al provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="649bd-115">Move user subscriptions from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="649bd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="649bd-116">PARAMETERS</span></span>

### <span data-ttu-id="649bd-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="649bd-117">-AsJob</span></span>
<span data-ttu-id="649bd-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="649bd-118">Run the command as a job</span></span>

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

### <span data-ttu-id="649bd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="649bd-119">-DefaultProfile</span></span>
<span data-ttu-id="649bd-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="649bd-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="649bd-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="649bd-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="649bd-122">Identificatore dell'offerta del provider delegato (dal contesto di amministrazione) a cui devono essere spostati gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="649bd-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="649bd-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="649bd-123">-InputObject</span></span>
<span data-ttu-id="649bd-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="649bd-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: MoveViaIdentity, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="649bd-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="649bd-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="649bd-126">La definizione di azione per la creazione di abbonamenti, vedere la sezione Note per le proprietà di MOVESUBSCRIPTIONSDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="649bd-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Move, MoveViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="649bd-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="649bd-127">-NoWait</span></span>
<span data-ttu-id="649bd-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="649bd-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="649bd-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="649bd-129">-PassThru</span></span>
<span data-ttu-id="649bd-130">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="649bd-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="649bd-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="649bd-131">-ResourceId</span></span>
<span data-ttu-id="649bd-132">Una raccolta di abbonamenti per il passaggio all'offerta di provider delegati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="649bd-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MoveExpanded, MoveViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="649bd-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="649bd-133">-SubscriptionId</span></span>
<span data-ttu-id="649bd-134">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="649bd-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Move, MoveExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="649bd-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="649bd-135">-Confirm</span></span>
<span data-ttu-id="649bd-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="649bd-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="649bd-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="649bd-137">-WhatIf</span></span>
<span data-ttu-id="649bd-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="649bd-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="649bd-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="649bd-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="649bd-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="649bd-140">CommonParameters</span></span>
<span data-ttu-id="649bd-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="649bd-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="649bd-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="649bd-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="649bd-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="649bd-143">INPUTS</span></span>

### <span data-ttu-id="649bd-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="649bd-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="649bd-145">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="649bd-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="649bd-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="649bd-146">OUTPUTS</span></span>

### <span data-ttu-id="649bd-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="649bd-147">System.Boolean</span></span>

<span data-ttu-id="649bd-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="649bd-148">ALIASES</span></span>

## <span data-ttu-id="649bd-149">Note</span><span class="sxs-lookup"><span data-stu-id="649bd-149">NOTES</span></span>

<span data-ttu-id="649bd-150">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="649bd-150">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="649bd-151">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="649bd-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="649bd-152">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="649bd-152">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="649bd-153">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="649bd-153">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="649bd-154">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="649bd-154">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="649bd-155">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="649bd-155">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="649bd-156">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="649bd-156">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="649bd-157">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="649bd-157">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="649bd-158">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="649bd-158">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="649bd-159">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="649bd-159">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="649bd-160">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="649bd-160">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="649bd-161">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="649bd-161">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="649bd-162">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="649bd-162">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="649bd-163">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="649bd-163">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="649bd-164">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="649bd-164">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="649bd-165">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="649bd-165">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="649bd-166">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="649bd-166">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="649bd-167">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="649bd-167">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="649bd-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : definizione dell'azione per gli abbonamenti di movimento</span><span class="sxs-lookup"><span data-stu-id="649bd-168">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="649bd-169">`Resources <String[]>`: Raccolta di abbonamenti per il passaggio all'offerta di provider delegati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="649bd-169">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="649bd-170">`[TargetDelegatedProviderOffer <String>]`: Identificatore offerta provider delegati (dal contesto di amministrazione) a cui devono essere spostati gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="649bd-170">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="649bd-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="649bd-171">RELATED LINKS</span></span>

