---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183719"
---
# <span data-ttu-id="2b569-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="2b569-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="2b569-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b569-102">SYNOPSIS</span></span>
<span data-ttu-id="2b569-103">Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="2b569-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="2b569-104">L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="2b569-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="2b569-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="2b569-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="2b569-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b569-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2b569-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2b569-107">DESCRIPTION</span></span>
<span data-ttu-id="2b569-108">Avvia la preparazione per il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="2b569-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="2b569-109">L'operazione di preparazione si trova su moveResources che si trova in moveState 'PreparePending' o 'PrepareFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="2b569-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="2b569-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="2b569-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="2b569-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b569-111">EXAMPLES</span></span>

### <span data-ttu-id="2b569-112">Esempio 1: Convalidare le dipendenze prima di prepararsi per le risorse</span><span class="sxs-lookup"><span data-stu-id="2b569-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="2b569-113">Verificare le dipendenze prima di prepararsi per le risorse.</span><span class="sxs-lookup"><span data-stu-id="2b569-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="2b569-114">Esempio 2: Iniziare a preparare il set di risorse nella raccolta di spostamento usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="2b569-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="2b569-115">Iniziare a preparare l'insieme di risorse nella raccolta di spostamento usando come input "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="2b569-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="2b569-116">Esempio 3: Iniziare a preparare il set di risorse nella raccolta di spostamento usando "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="2b569-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="2b569-117">Iniziare a preparare l'insieme di risorse nella raccolta di spostamento usando "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="2b569-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="2b569-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2b569-118">PARAMETERS</span></span>

### <span data-ttu-id="2b569-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b569-119">-AsJob</span></span>
<span data-ttu-id="2b569-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="2b569-120">Run the command as a job</span></span>

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

### <span data-ttu-id="2b569-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b569-121">-DefaultProfile</span></span>
<span data-ttu-id="2b569-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b569-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b569-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2b569-123">-MoveCollectionName</span></span>
<span data-ttu-id="2b569-124">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="2b569-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="2b569-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="2b569-125">-MoveResource</span></span>
<span data-ttu-id="2b569-126">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="2b569-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="2b569-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="2b569-127">-MoveResourceInputType</span></span>
<span data-ttu-id="2b569-128">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="2b569-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="2b569-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2b569-129">-NoWait</span></span>
<span data-ttu-id="2b569-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="2b569-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2b569-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b569-131">-ResourceGroupName</span></span>
<span data-ttu-id="2b569-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b569-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="2b569-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b569-133">-SubscriptionId</span></span>
<span data-ttu-id="2b569-134">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="2b569-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="2b569-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="2b569-135">-ValidateOnly</span></span>
<span data-ttu-id="2b569-136">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="2b569-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="2b569-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2b569-137">-Confirm</span></span>
<span data-ttu-id="2b569-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b569-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b569-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b569-139">-WhatIf</span></span>
<span data-ttu-id="2b569-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b569-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b569-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b569-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b569-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b569-142">CommonParameters</span></span>
<span data-ttu-id="2b569-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b569-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b569-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2b569-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b569-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="2b569-145">INPUTS</span></span>

## <span data-ttu-id="2b569-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b569-146">OUTPUTS</span></span>

### <span data-ttu-id="2b569-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="2b569-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="2b569-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="2b569-148">NOTES</span></span>

<span data-ttu-id="2b569-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="2b569-149">ALIASES</span></span>

## <span data-ttu-id="2b569-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b569-150">RELATED LINKS</span></span>

