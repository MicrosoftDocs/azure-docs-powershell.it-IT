---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999981"
---
# <span data-ttu-id="1c6b6-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="1c6b6-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="1c6b6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c6b6-102">SYNOPSIS</span></span>
<span data-ttu-id="1c6b6-103">Esegue il commit del set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="1c6b6-104">L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="1c6b6-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="1c6b6-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c6b6-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c6b6-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1c6b6-107">DESCRIPTION</span></span>
<span data-ttu-id="1c6b6-108">Esegue il commit del set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="1c6b6-109">L'operazione di commit viene attivata su moveResources in moveState 'CommitPending' o 'CommitFailed', al completamento di moveResource moveState esegue una transizione a Committed.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="1c6b6-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="1c6b6-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c6b6-111">EXAMPLES</span></span>

### <span data-ttu-id="1c6b6-112">Esempio 1: Convalidare le dipendenze prima del commit delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="1c6b6-113">Convalidare le dipendenze prima di eseguire il commit delle risorse.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="1c6b6-114">Esempio 2: eseguire il commit del set di risorse nella raccolta move usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="1c6b6-115">Eseguire il commit del set di risorse nella raccolta move usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="1c6b6-116">Esempio 3: Eseguire il commit del set di risorse nella raccolta di spostamento usando "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="1c6b6-117">Eseguire il commit del set di risorse nella raccolta di spostamento usando "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="1c6b6-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c6b6-118">PARAMETERS</span></span>

### <span data-ttu-id="1c6b6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c6b6-119">-AsJob</span></span>
<span data-ttu-id="1c6b6-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="1c6b6-120">Run the command as a job</span></span>

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

### <span data-ttu-id="1c6b6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c6b6-121">-DefaultProfile</span></span>
<span data-ttu-id="1c6b6-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c6b6-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1c6b6-123">-MoveCollectionName</span></span>
<span data-ttu-id="1c6b6-124">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1c6b6-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="1c6b6-125">-MoveResource</span></span>
<span data-ttu-id="1c6b6-126">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="1c6b6-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="1c6b6-127">-MoveResourceInputType</span></span>
<span data-ttu-id="1c6b6-128">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="1c6b6-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1c6b6-129">-NoWait</span></span>
<span data-ttu-id="1c6b6-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="1c6b6-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c6b6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c6b6-131">-ResourceGroupName</span></span>
<span data-ttu-id="1c6b6-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1c6b6-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1c6b6-133">-SubscriptionId</span></span>
<span data-ttu-id="1c6b6-134">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="1c6b6-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="1c6b6-135">-ValidateOnly</span></span>
<span data-ttu-id="1c6b6-136">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="1c6b6-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c6b6-137">-Confirm</span></span>
<span data-ttu-id="1c6b6-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c6b6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c6b6-139">-WhatIf</span></span>
<span data-ttu-id="1c6b6-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c6b6-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c6b6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c6b6-142">CommonParameters</span></span>
<span data-ttu-id="1c6b6-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c6b6-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1c6b6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c6b6-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="1c6b6-145">INPUTS</span></span>

## <span data-ttu-id="1c6b6-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c6b6-146">OUTPUTS</span></span>

### <span data-ttu-id="1c6b6-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="1c6b6-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="1c6b6-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="1c6b6-148">NOTES</span></span>

<span data-ttu-id="1c6b6-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="1c6b6-149">ALIASES</span></span>

## <span data-ttu-id="1c6b6-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c6b6-150">RELATED LINKS</span></span>

