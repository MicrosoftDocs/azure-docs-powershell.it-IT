---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189396"
---
# <span data-ttu-id="46ba7-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="46ba7-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="46ba7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="46ba7-103">Conferma il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="46ba7-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="46ba7-104">L'operazione di commit viene attivata in moveResources in moveState ' CommitPending ' o ' CommitFailed ', in un completamento positivo il moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="46ba7-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="46ba7-105">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="46ba7-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="46ba7-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46ba7-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46ba7-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46ba7-107">DESCRIPTION</span></span>
<span data-ttu-id="46ba7-108">Conferma il set di risorse incluso nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="46ba7-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="46ba7-109">L'operazione di commit viene attivata in moveResources in moveState ' CommitPending ' o ' CommitFailed ', in un completamento positivo il moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="46ba7-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="46ba7-110">Per aiutare l'utente a prerequisire l'operazione che il client può chiamare operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="46ba7-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="46ba7-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="46ba7-112">Esempio 1: convalidare la dependecies prima di eseguire il commit delle risorse</span><span class="sxs-lookup"><span data-stu-id="46ba7-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="46ba7-113">Convalidare dependecies prima di eseguire il commit delle risorse.</span><span class="sxs-lookup"><span data-stu-id="46ba7-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="46ba7-114">Esempio 2: eseguire il commit del set di risorse nella raccolta di mosse usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="46ba7-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="46ba7-115">Eseguire il commit del set di risorse nell'insieme Move usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="46ba7-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="46ba7-116">Esempio 3: eseguire il commit del set di risorse nella raccolta di mosse usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="46ba7-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="46ba7-117">Eseguire il commit del set di risorse nella raccolta di mosse usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="46ba7-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="46ba7-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46ba7-118">PARAMETERS</span></span>

### <span data-ttu-id="46ba7-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46ba7-119">-AsJob</span></span>
<span data-ttu-id="46ba7-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="46ba7-120">Run the command as a job</span></span>

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

### <span data-ttu-id="46ba7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46ba7-121">-DefaultProfile</span></span>
<span data-ttu-id="46ba7-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46ba7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46ba7-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="46ba7-123">-MoveCollectionName</span></span>
<span data-ttu-id="46ba7-124">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="46ba7-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="46ba7-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="46ba7-125">-MoveResource</span></span>
<span data-ttu-id="46ba7-126">Ottiene o imposta l'elenco di ID risorsa, per impostazione predefinita accetta sposta ID risorsa a meno che il tipo di input non venga attivato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="46ba7-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="46ba7-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="46ba7-127">-MoveResourceInputType</span></span>
<span data-ttu-id="46ba7-128">Definisce il tipo di input della risorsa Move.</span><span class="sxs-lookup"><span data-stu-id="46ba7-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="46ba7-129">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="46ba7-129">-NoWait</span></span>
<span data-ttu-id="46ba7-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="46ba7-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46ba7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46ba7-131">-ResourceGroupName</span></span>
<span data-ttu-id="46ba7-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="46ba7-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="46ba7-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46ba7-133">-SubscriptionId</span></span>
<span data-ttu-id="46ba7-134">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="46ba7-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="46ba7-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="46ba7-135">-ValidateOnly</span></span>
<span data-ttu-id="46ba7-136">Ottiene o imposta un valore che indica se l'operazione deve essere eseguita solo prerequisito.</span><span class="sxs-lookup"><span data-stu-id="46ba7-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="46ba7-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="46ba7-137">-Confirm</span></span>
<span data-ttu-id="46ba7-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46ba7-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46ba7-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46ba7-139">-WhatIf</span></span>
<span data-ttu-id="46ba7-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46ba7-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46ba7-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46ba7-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46ba7-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46ba7-142">CommonParameters</span></span>
<span data-ttu-id="46ba7-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46ba7-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46ba7-144">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46ba7-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46ba7-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46ba7-145">INPUTS</span></span>

## <span data-ttu-id="46ba7-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46ba7-146">OUTPUTS</span></span>

### <span data-ttu-id="46ba7-147">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="46ba7-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="46ba7-148">Note</span><span class="sxs-lookup"><span data-stu-id="46ba7-148">NOTES</span></span>

<span data-ttu-id="46ba7-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="46ba7-149">ALIASES</span></span>

## <span data-ttu-id="46ba7-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46ba7-150">RELATED LINKS</span></span>
