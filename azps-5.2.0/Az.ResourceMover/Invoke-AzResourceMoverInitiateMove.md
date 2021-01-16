---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349120"
---
# <span data-ttu-id="b717f-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="b717f-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="b717f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b717f-102">SYNOPSIS</span></span>
<span data-ttu-id="b717f-103">Sposta il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="b717f-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="b717f-104">L'operazione di movimento viene attivata dopo che il moveResources si trova in moveState ' MovePending ' o ' MoveFailed ', in seguito a un completamento positivo il moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="b717f-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="b717f-105">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="b717f-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b717f-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b717f-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b717f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b717f-107">DESCRIPTION</span></span>
<span data-ttu-id="b717f-108">Sposta il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="b717f-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="b717f-109">L'operazione di movimento viene attivata dopo che il moveResources si trova in moveState ' MovePending ' o ' MoveFailed ', in seguito a un completamento positivo il moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="b717f-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="b717f-110">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="b717f-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="b717f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b717f-111">EXAMPLES</span></span>

### <span data-ttu-id="b717f-112">Esempio 1: convalidare la dependecies prima di avviare lo stato di trasferimento per le risorse.</span><span class="sxs-lookup"><span data-stu-id="b717f-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="b717f-113">Convalidare dependecies prima di avviare lo stato di trasferimento per le risorse.</span><span class="sxs-lookup"><span data-stu-id="b717f-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="b717f-114">Esempio 2: avviare lo stato di trasferimento per il set di risorse nella raccolta di mosse usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="b717f-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="b717f-115">Avviare lo stato di trasferimento per il set di risorse nella raccolta di mosse usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="b717f-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="b717f-116">Esempio 3: avviare lo stato di trasferimento per il set di risorse nella raccolta di mosse usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="b717f-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="b717f-117">Avviare lo stato di trasferimento per il set di risorse nella raccolta di mosse usando "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="b717f-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="b717f-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b717f-118">PARAMETERS</span></span>

### <span data-ttu-id="b717f-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b717f-119">-AsJob</span></span>
<span data-ttu-id="b717f-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="b717f-120">Run the command as a job</span></span>

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

### <span data-ttu-id="b717f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b717f-121">-DefaultProfile</span></span>
<span data-ttu-id="b717f-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b717f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b717f-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="b717f-123">-MoveCollectionName</span></span>
<span data-ttu-id="b717f-124">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="b717f-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="b717f-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="b717f-125">-MoveResource</span></span>
<span data-ttu-id="b717f-126">Ottiene o imposta l'elenco di ID risorsa, per impostazione predefinita accetta sposta ID risorsa a meno che il tipo di input non venga attivato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="b717f-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="b717f-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="b717f-127">-MoveResourceInputType</span></span>
<span data-ttu-id="b717f-128">Definisce il tipo di input della risorsa Move.</span><span class="sxs-lookup"><span data-stu-id="b717f-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="b717f-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="b717f-129">-NoWait</span></span>
<span data-ttu-id="b717f-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="b717f-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b717f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b717f-131">-ResourceGroupName</span></span>
<span data-ttu-id="b717f-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b717f-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="b717f-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b717f-133">-SubscriptionId</span></span>
<span data-ttu-id="b717f-134">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b717f-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="b717f-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="b717f-135">-ValidateOnly</span></span>
<span data-ttu-id="b717f-136">Ottiene o imposta un valore che indica se l'operazione deve essere eseguita solo prerequisito.</span><span class="sxs-lookup"><span data-stu-id="b717f-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="b717f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b717f-137">-Confirm</span></span>
<span data-ttu-id="b717f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b717f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b717f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b717f-139">-WhatIf</span></span>
<span data-ttu-id="b717f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b717f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b717f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b717f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b717f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b717f-142">CommonParameters</span></span>
<span data-ttu-id="b717f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b717f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b717f-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b717f-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b717f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b717f-145">INPUTS</span></span>

## <span data-ttu-id="b717f-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b717f-146">OUTPUTS</span></span>

### <span data-ttu-id="b717f-147">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="b717f-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="b717f-148">Note</span><span class="sxs-lookup"><span data-stu-id="b717f-148">NOTES</span></span>

<span data-ttu-id="b717f-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="b717f-149">ALIASES</span></span>

## <span data-ttu-id="b717f-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b717f-150">RELATED LINKS</span></span>

