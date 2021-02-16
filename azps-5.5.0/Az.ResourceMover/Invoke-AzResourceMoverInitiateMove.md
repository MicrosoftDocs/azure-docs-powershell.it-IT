---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186527"
---
# <span data-ttu-id="ae51d-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="ae51d-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="ae51d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae51d-102">SYNOPSIS</span></span>
<span data-ttu-id="ae51d-103">Sposta il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ae51d-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ae51d-104">L'operazione di spostamento viene attivata dopo che moveResources si trova nello stato moveState 'MovePending' o 'MoveFailed', al completamento di moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ae51d-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ae51d-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="ae51d-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ae51d-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae51d-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ae51d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ae51d-107">DESCRIPTION</span></span>
<span data-ttu-id="ae51d-108">Sposta il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="ae51d-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="ae51d-109">L'operazione di spostamento viene attivata dopo che moveResources si trova nello stato moveState 'MovePending' o 'MoveFailed', al completamento di moveResource moveState esegue una transizione a CommitPending.</span><span class="sxs-lookup"><span data-stu-id="ae51d-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="ae51d-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="ae51d-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ae51d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae51d-111">EXAMPLES</span></span>

### <span data-ttu-id="ae51d-112">Esempio 1: Convalidare le dipendenze prima di iniziare lo spostamento per le risorse.</span><span class="sxs-lookup"><span data-stu-id="ae51d-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
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

<span data-ttu-id="ae51d-113">Verificare le dipendenze prima di iniziare lo spostamento per le risorse.</span><span class="sxs-lookup"><span data-stu-id="ae51d-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="ae51d-114">Esempio 2: Iniziare lo spostamento per il set di risorse nella raccolta Move usando "MoveResource Name" come input</span><span class="sxs-lookup"><span data-stu-id="ae51d-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="ae51d-115">Iniziare lo spostamento per il set di risorse nella raccolta Move usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="ae51d-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="ae51d-116">Esempio 3: Iniziare lo spostamento per il set di risorse nella raccolta di spostamento usando "SourceARMID" come input</span><span class="sxs-lookup"><span data-stu-id="ae51d-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="ae51d-117">Iniziare lo spostamento per il set di risorse nella raccolta Sposta usando "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="ae51d-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="ae51d-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ae51d-118">PARAMETERS</span></span>

### <span data-ttu-id="ae51d-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae51d-119">-AsJob</span></span>
<span data-ttu-id="ae51d-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="ae51d-120">Run the command as a job</span></span>

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

### <span data-ttu-id="ae51d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae51d-121">-DefaultProfile</span></span>
<span data-ttu-id="ae51d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae51d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae51d-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ae51d-123">-MoveCollectionName</span></span>
<span data-ttu-id="ae51d-124">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="ae51d-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ae51d-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ae51d-125">-MoveResource</span></span>
<span data-ttu-id="ae51d-126">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="ae51d-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ae51d-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ae51d-127">-MoveResourceInputType</span></span>
<span data-ttu-id="ae51d-128">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="ae51d-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ae51d-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ae51d-129">-NoWait</span></span>
<span data-ttu-id="ae51d-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="ae51d-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ae51d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae51d-131">-ResourceGroupName</span></span>
<span data-ttu-id="ae51d-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae51d-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ae51d-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ae51d-133">-SubscriptionId</span></span>
<span data-ttu-id="ae51d-134">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="ae51d-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="ae51d-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ae51d-135">-ValidateOnly</span></span>
<span data-ttu-id="ae51d-136">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="ae51d-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ae51d-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ae51d-137">-Confirm</span></span>
<span data-ttu-id="ae51d-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae51d-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae51d-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae51d-139">-WhatIf</span></span>
<span data-ttu-id="ae51d-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae51d-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae51d-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae51d-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae51d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae51d-142">CommonParameters</span></span>
<span data-ttu-id="ae51d-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae51d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae51d-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ae51d-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae51d-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="ae51d-145">INPUTS</span></span>

## <span data-ttu-id="ae51d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae51d-146">OUTPUTS</span></span>

### <span data-ttu-id="ae51d-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ae51d-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="ae51d-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="ae51d-148">NOTES</span></span>

<span data-ttu-id="ae51d-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="ae51d-149">ALIASES</span></span>

## <span data-ttu-id="ae51d-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae51d-150">RELATED LINKS</span></span>

