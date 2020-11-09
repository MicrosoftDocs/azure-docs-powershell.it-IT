---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302497"
---
# <span data-ttu-id="d25fe-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="d25fe-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="d25fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d25fe-102">SYNOPSIS</span></span>
<span data-ttu-id="d25fe-103">Elimina il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="d25fe-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="d25fe-104">L'operazione di eliminazione viene attivata in moveResources in moveState "CommitPending" o "DiscardFailed", in un completamento positivo il moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="d25fe-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="d25fe-105">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="d25fe-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d25fe-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d25fe-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d25fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d25fe-107">DESCRIPTION</span></span>
<span data-ttu-id="d25fe-108">Elimina il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="d25fe-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="d25fe-109">L'operazione di eliminazione viene attivata in moveResources in moveState "CommitPending" o "DiscardFailed", in un completamento positivo il moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="d25fe-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="d25fe-110">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="d25fe-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d25fe-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d25fe-111">EXAMPLES</span></span>

### <span data-ttu-id="d25fe-112">Esempio 1: convalidare la dependecies prima dello scarto delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d25fe-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="d25fe-113">Convalidare la dependecies prima dello scarto delle risorse.</span><span class="sxs-lookup"><span data-stu-id="d25fe-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="d25fe-114">Esempio 2: Elimina il passaggio delle risorse usando "nome MoveResource" come input</span><span class="sxs-lookup"><span data-stu-id="d25fe-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="d25fe-115">Elimina il passaggio delle risorse usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="d25fe-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="d25fe-116">Esempio 3: Elimina il passaggio delle risorse con "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="d25fe-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="d25fe-117">Elimina il passaggio delle risorse usando "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="d25fe-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="d25fe-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d25fe-118">PARAMETERS</span></span>

### <span data-ttu-id="d25fe-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d25fe-119">-AsJob</span></span>
<span data-ttu-id="d25fe-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="d25fe-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d25fe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d25fe-121">-DefaultProfile</span></span>
<span data-ttu-id="d25fe-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d25fe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d25fe-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="d25fe-123">-MoveResource</span></span>
<span data-ttu-id="d25fe-124">Ottiene o imposta l'elenco di ID risorsa, per impostazione predefinita accetta sposta ID risorsa a meno che il tipo di input non venga attivato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="d25fe-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25fe-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="d25fe-125">-MoveResourceInputType</span></span>
<span data-ttu-id="d25fe-126">Definisce il tipo di input della risorsa Move.</span><span class="sxs-lookup"><span data-stu-id="d25fe-126">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25fe-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d25fe-127">-Name</span></span>
<span data-ttu-id="d25fe-128">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="d25fe-128">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25fe-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="d25fe-129">-NoWait</span></span>
<span data-ttu-id="d25fe-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="d25fe-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d25fe-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d25fe-131">-ResourceGroupName</span></span>
<span data-ttu-id="d25fe-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d25fe-132">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25fe-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d25fe-133">-SubscriptionId</span></span>
<span data-ttu-id="d25fe-134">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="d25fe-134">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d25fe-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="d25fe-135">-ValidateOnly</span></span>
<span data-ttu-id="d25fe-136">Ottiene o imposta un valore che indica se l'operazione deve essere eseguita solo prerequisito.</span><span class="sxs-lookup"><span data-stu-id="d25fe-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="d25fe-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d25fe-137">-Confirm</span></span>
<span data-ttu-id="d25fe-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d25fe-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d25fe-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d25fe-139">-WhatIf</span></span>
<span data-ttu-id="d25fe-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d25fe-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d25fe-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d25fe-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d25fe-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d25fe-142">CommonParameters</span></span>
<span data-ttu-id="d25fe-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d25fe-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d25fe-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d25fe-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d25fe-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d25fe-145">INPUTS</span></span>

## <span data-ttu-id="d25fe-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d25fe-146">OUTPUTS</span></span>

### <span data-ttu-id="d25fe-147">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d25fe-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="d25fe-148">Note</span><span class="sxs-lookup"><span data-stu-id="d25fe-148">NOTES</span></span>

<span data-ttu-id="d25fe-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="d25fe-149">ALIASES</span></span>

## <span data-ttu-id="d25fe-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d25fe-150">RELATED LINKS</span></span>

