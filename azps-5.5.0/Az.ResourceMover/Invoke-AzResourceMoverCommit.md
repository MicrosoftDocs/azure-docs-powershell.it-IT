---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201895"
---
# <span data-ttu-id="fa99a-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="fa99a-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="fa99a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa99a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa99a-103">Esegue il commit del set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa99a-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="fa99a-104">L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="fa99a-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="fa99a-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="fa99a-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="fa99a-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fa99a-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fa99a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fa99a-107">DESCRIPTION</span></span>
<span data-ttu-id="fa99a-108">Esegue il commit del set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="fa99a-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="fa99a-109">L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="fa99a-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="fa99a-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="fa99a-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="fa99a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fa99a-111">EXAMPLES</span></span>

### <span data-ttu-id="fa99a-112">Esempio 1: Convalidare le dipendenze prima del commit delle risorse</span><span class="sxs-lookup"><span data-stu-id="fa99a-112">Example 1: Validate the dependecies before commit of the resources</span></span>
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

<span data-ttu-id="fa99a-113">Convalidare le dipendenze prima di eseguire il commit delle risorse.</span><span class="sxs-lookup"><span data-stu-id="fa99a-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="fa99a-114">Esempio 2: Eseguire il commit del set di risorse nella raccolta move usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="fa99a-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="fa99a-115">Eseguire il commit del set di risorse nella raccolta move con "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="fa99a-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="fa99a-116">Esempio 3: Eseguire il commit del set di risorse nella raccolta di spostamento usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="fa99a-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="fa99a-117">Eseguire il commit del set di risorse nella raccolta di spostamento usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="fa99a-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="fa99a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa99a-118">PARAMETERS</span></span>

### <span data-ttu-id="fa99a-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fa99a-119">-AsJob</span></span>
<span data-ttu-id="fa99a-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="fa99a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="fa99a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa99a-121">-DefaultProfile</span></span>
<span data-ttu-id="fa99a-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fa99a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fa99a-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="fa99a-123">-MoveCollectionName</span></span>
<span data-ttu-id="fa99a-124">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="fa99a-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="fa99a-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="fa99a-125">-MoveResource</span></span>
<span data-ttu-id="fa99a-126">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="fa99a-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="fa99a-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="fa99a-127">-MoveResourceInputType</span></span>
<span data-ttu-id="fa99a-128">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="fa99a-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="fa99a-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fa99a-129">-NoWait</span></span>
<span data-ttu-id="fa99a-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="fa99a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fa99a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa99a-131">-ResourceGroupName</span></span>
<span data-ttu-id="fa99a-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fa99a-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="fa99a-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fa99a-133">-SubscriptionId</span></span>
<span data-ttu-id="fa99a-134">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="fa99a-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="fa99a-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="fa99a-135">-ValidateOnly</span></span>
<span data-ttu-id="fa99a-136">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="fa99a-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="fa99a-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fa99a-137">-Confirm</span></span>
<span data-ttu-id="fa99a-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa99a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa99a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa99a-139">-WhatIf</span></span>
<span data-ttu-id="fa99a-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa99a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa99a-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fa99a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa99a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa99a-142">CommonParameters</span></span>
<span data-ttu-id="fa99a-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa99a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa99a-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fa99a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa99a-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="fa99a-145">INPUTS</span></span>

## <span data-ttu-id="fa99a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fa99a-146">OUTPUTS</span></span>

### <span data-ttu-id="fa99a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="fa99a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="fa99a-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="fa99a-148">NOTES</span></span>

<span data-ttu-id="fa99a-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="fa99a-149">ALIASES</span></span>

## <span data-ttu-id="fa99a-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fa99a-150">RELATED LINKS</span></span>

