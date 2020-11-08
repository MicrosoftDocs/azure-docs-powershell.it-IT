---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/test-azsmoveusersubscription
schema: 2.0.0
ms.openlocfilehash: c0e80b7d0f17bf505c0b3bb8d22539afffea851a
ms.sourcegitcommit: 308ebca475d1c37624d7a10a2c02047594f44cdf
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/22/2020
ms.locfileid: "94023057"
---
# <span data-ttu-id="4dca5-101">Test-AzsMoveUserSubscription</span><span class="sxs-lookup"><span data-stu-id="4dca5-101">Test-AzsMoveUserSubscription</span></span>

## <span data-ttu-id="4dca5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4dca5-102">SYNOPSIS</span></span>
<span data-ttu-id="4dca5-103">Verificare che gli abbonamenti degli utenti possano essere spostati tra le offerte di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="4dca5-103">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="4dca5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4dca5-104">SYNTAX</span></span>

### <span data-ttu-id="4dca5-105">ValidateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4dca5-105">ValidateExpanded (Default)</span></span>
```
Test-AzsMoveUserSubscription -ResourceId <String[]> [-SubscriptionId <String>]
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4dca5-106">Convalidare</span><span class="sxs-lookup"><span data-stu-id="4dca5-106">Validate</span></span>
```
Test-AzsMoveUserSubscription -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="4dca5-107">ValidateViaIdentity</span><span class="sxs-lookup"><span data-stu-id="4dca5-107">ValidateViaIdentity</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity>
 -MoveSubscriptionsDefinition <IMoveSubscriptionsDefinition> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4dca5-108">ValidateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4dca5-108">ValidateViaIdentityExpanded</span></span>
```
Test-AzsMoveUserSubscription -InputObject <ISubscriptionsAdminIdentity> -ResourceId <String[]>
 [-DestinationDelegatedProviderOffer <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4dca5-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4dca5-109">DESCRIPTION</span></span>
<span data-ttu-id="4dca5-110">Verificare che gli abbonamenti degli utenti possano essere spostati tra le offerte di provider delegati.</span><span class="sxs-lookup"><span data-stu-id="4dca5-110">Validate that user subscriptions can be moved between delegated provider offers.</span></span>

## <span data-ttu-id="4dca5-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4dca5-111">EXAMPLES</span></span>

### <span data-ttu-id="4dca5-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4dca5-112">Example 1</span></span>
```powershell
PS C:\> Test-MoveUserSubscription \`
    -DestinationDelegatedProviderOffer "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/delegatedProviders/798568b7-c6f1-4bf7-bb8f-2c8bebc7c777/offers/ro1"
    -ResourceId "/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/ce4c7fdb-5a38-46f5-8bbc-b8b328a87ab6","/subscriptions/45ec4d39-8dea-4d26-a373-c176ec53717a/providers/Microsoft.Subscriptions.Admin/subscriptions/a0d1a71c-0b27-4e73-abfc-169512576f7d"

```

<span data-ttu-id="4dca5-113">Verificare che gli abbonamenti degli utenti possano essere spostati in un'offerta di provider delegata.</span><span class="sxs-lookup"><span data-stu-id="4dca5-113">Test that user subscriptions can be moved to a delegated provider offer.</span></span>

### <span data-ttu-id="4dca5-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4dca5-114">Example 2</span></span>
```powershell
PS C:\> $resourceIds = Get-AzsUserSubscription | where Displayname -eq "testsubscription" | Select -ExpandProperty Id
Test-MoveUserSubscription -ResourceId $resourceIds

```

<span data-ttu-id="4dca5-115">Verificare che gli abbonamenti degli utenti possano essere spostati da un provider delegato al provider predefinito.</span><span class="sxs-lookup"><span data-stu-id="4dca5-115">Test that user subscriptions can be moved from a delegated provider to the Default Provider.</span></span>

## <span data-ttu-id="4dca5-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4dca5-116">PARAMETERS</span></span>

### <span data-ttu-id="4dca5-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4dca5-117">-AsJob</span></span>
<span data-ttu-id="4dca5-118">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="4dca5-118">Run the command as a job</span></span>

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

### <span data-ttu-id="4dca5-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4dca5-119">-DefaultProfile</span></span>
<span data-ttu-id="4dca5-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4dca5-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4dca5-121">-DestinationDelegatedProviderOffer</span><span class="sxs-lookup"><span data-stu-id="4dca5-121">-DestinationDelegatedProviderOffer</span></span>
<span data-ttu-id="4dca5-122">Identificatore dell'offerta del provider delegato (dal contesto di amministrazione) a cui devono essere spostati gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="4dca5-122">The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

```yaml
Type: System.String
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4dca5-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4dca5-123">-InputObject</span></span>
<span data-ttu-id="4dca5-124">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4dca5-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: ValidateViaIdentity, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4dca5-125">-MoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="4dca5-125">-MoveSubscriptionsDefinition</span></span>
<span data-ttu-id="4dca5-126">La definizione di azione per la creazione di abbonamenti, vedere la sezione Note per le proprietà di MOVESUBSCRIPTIONSDEFINITION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="4dca5-126">The move subscriptions action definition To construct, see NOTES section for MOVESUBSCRIPTIONSDEFINITION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition
Parameter Sets: Validate, ValidateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="4dca5-127">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="4dca5-127">-NoWait</span></span>
<span data-ttu-id="4dca5-128">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="4dca5-128">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4dca5-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4dca5-129">-PassThru</span></span>
<span data-ttu-id="4dca5-130">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="4dca5-130">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="4dca5-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4dca5-131">-ResourceId</span></span>
<span data-ttu-id="4dca5-132">Una raccolta di abbonamenti per il passaggio all'offerta di provider delegati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4dca5-132">A collection of subscriptions to move to the target delegated provider offer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ValidateExpanded, ValidateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4dca5-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4dca5-133">-SubscriptionId</span></span>
<span data-ttu-id="4dca5-134">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4dca5-134">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Validate, ValidateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="4dca5-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4dca5-135">-Confirm</span></span>
<span data-ttu-id="4dca5-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4dca5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4dca5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4dca5-137">-WhatIf</span></span>
<span data-ttu-id="4dca5-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4dca5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4dca5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4dca5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4dca5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4dca5-140">CommonParameters</span></span>
<span data-ttu-id="4dca5-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4dca5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4dca5-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4dca5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4dca5-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4dca5-143">INPUTS</span></span>

### <span data-ttu-id="4dca5-144">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. Api20151101. IMoveSubscriptionsDefinition</span><span class="sxs-lookup"><span data-stu-id="4dca5-144">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IMoveSubscriptionsDefinition</span></span>

### <span data-ttu-id="4dca5-145">Microsoft. Azure. PowerShell. Cmdlets. SubscriptionsAdmin. Models. ISubscriptionsAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="4dca5-145">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="4dca5-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4dca5-146">OUTPUTS</span></span>

### <span data-ttu-id="4dca5-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4dca5-147">System.Boolean</span></span>

<span data-ttu-id="4dca5-148">ALIAS</span><span class="sxs-lookup"><span data-stu-id="4dca5-148">ALIASES</span></span>

### <span data-ttu-id="4dca5-149">Test-AzsMoveSubscription</span><span class="sxs-lookup"><span data-stu-id="4dca5-149">Test-AzsMoveSubscription</span></span>

## <span data-ttu-id="4dca5-150">Note</span><span class="sxs-lookup"><span data-stu-id="4dca5-150">NOTES</span></span>

<span data-ttu-id="4dca5-151">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="4dca5-151">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4dca5-152">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4dca5-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="4dca5-153">INPUTOBJECT <ISubscriptionsAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="4dca5-153">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4dca5-154">`[DelegatedProvider <String>]`: Identificatore DelegatedProvider.</span><span class="sxs-lookup"><span data-stu-id="4dca5-154">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="4dca5-155">`[DelegatedProviderSubscriptionId <String>]`: Identificatore di abbonamento a provider delegati.</span><span class="sxs-lookup"><span data-stu-id="4dca5-155">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="4dca5-156">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="4dca5-156">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4dca5-157">`[Location <String>]`: La posizione di AzureStack.</span><span class="sxs-lookup"><span data-stu-id="4dca5-157">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="4dca5-158">`[ManifestName <String>]`: Nome manifesto.</span><span class="sxs-lookup"><span data-stu-id="4dca5-158">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="4dca5-159">`[Offer <String>]`: Nome di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="4dca5-159">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="4dca5-160">`[OfferDelegationName <String>]`: Nome della delega di un'offerta.</span><span class="sxs-lookup"><span data-stu-id="4dca5-160">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="4dca5-161">`[OperationsStatusName <String>]`: Nome stato operazione.</span><span class="sxs-lookup"><span data-stu-id="4dca5-161">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="4dca5-162">`[Plan <String>]`: Nome del piano.</span><span class="sxs-lookup"><span data-stu-id="4dca5-162">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="4dca5-163">`[PlanAcquisitionId <String>]`: L'identificatore di acquisizione del piano</span><span class="sxs-lookup"><span data-stu-id="4dca5-163">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="4dca5-164">`[Quota <String>]`: Nome della quota.</span><span class="sxs-lookup"><span data-stu-id="4dca5-164">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="4dca5-165">`[ResourceGroupName <String>]`: Il gruppo di risorse in cui si trova la risorsa.</span><span class="sxs-lookup"><span data-stu-id="4dca5-165">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="4dca5-166">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure. L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="4dca5-166">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="4dca5-167">`[TargetSubscriptionId <String>]`: ID abbonamento di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4dca5-167">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="4dca5-168">`[Tenant <String>]`: Nome del tenant della directory.</span><span class="sxs-lookup"><span data-stu-id="4dca5-168">`[Tenant <String>]`: Directory tenant name.</span></span>

<span data-ttu-id="4dca5-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition> : definizione dell'azione per gli abbonamenti di movimento</span><span class="sxs-lookup"><span data-stu-id="4dca5-169">MOVESUBSCRIPTIONSDEFINITION <IMoveSubscriptionsDefinition>: The move subscriptions action definition</span></span>
  - <span data-ttu-id="4dca5-170">`Resources <String[]>`: Raccolta di abbonamenti per il passaggio all'offerta di provider delegati di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4dca5-170">`Resources <String[]>`: A collection of subscriptions to move to the target delegated provider offer.</span></span>
  - <span data-ttu-id="4dca5-171">`[TargetDelegatedProviderOffer <String>]`: Identificatore offerta provider delegati (dal contesto di amministrazione) a cui devono essere spostati gli abbonamenti.</span><span class="sxs-lookup"><span data-stu-id="4dca5-171">`[TargetDelegatedProviderOffer <String>]`: The delegated provider offer identifier (from the Admin context) that the subscriptions to be moved to.</span></span>

## <span data-ttu-id="4dca5-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4dca5-172">RELATED LINKS</span></span>

