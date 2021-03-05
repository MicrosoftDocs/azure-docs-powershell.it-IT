---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: 5e54501e6337943561489a80adf4e8789a55a394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999950"
---
# <span data-ttu-id="46c0b-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="46c0b-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="46c0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46c0b-102">SYNOPSIS</span></span>
<span data-ttu-id="46c0b-103">Elimina il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="46c0b-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="46c0b-104">L'operazione di eliminazione viene attivata su moveResources in moveState 'CommitPending' o 'DiscardFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="46c0b-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="46c0b-105">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="46c0b-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="46c0b-106">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46c0b-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="46c0b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="46c0b-107">DESCRIPTION</span></span>
<span data-ttu-id="46c0b-108">Elimina il set di risorse incluse nel corpo della richiesta.</span><span class="sxs-lookup"><span data-stu-id="46c0b-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="46c0b-109">L'operazione di eliminazione viene attivata su moveResources in moveState 'CommitPending' o 'DiscardFailed', al completamento di moveResource moveState esegue una transizione a MovePending.</span><span class="sxs-lookup"><span data-stu-id="46c0b-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="46c0b-110">Per aiutare l'utente a prerequisiti dell'operazione, il client può chiamare l'operazione con la proprietà validateOnly impostata su true.</span><span class="sxs-lookup"><span data-stu-id="46c0b-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="46c0b-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46c0b-111">EXAMPLES</span></span>

### <span data-ttu-id="46c0b-112">Esempio 1: Convalidare le dipendenze prima di eliminare le risorse.</span><span class="sxs-lookup"><span data-stu-id="46c0b-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:39:48 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:39:37 PM
Status         : Succeeded

```

<span data-ttu-id="46c0b-113">Verificare le dipendenze prima dell'eliminazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="46c0b-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="46c0b-114">Esempio 2: Elimina lo spostamento delle risorse usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="46c0b-114">Example 2: Discards the move of the resources using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:56:33 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:55:21 PM
Status         : Succeeded

```

<span data-ttu-id="46c0b-115">Elimina lo spostamento delle risorse usando "MoveResource Name" come input.</span><span class="sxs-lookup"><span data-stu-id="46c0b-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="46c0b-116">Esempio 3: Elimina lo spostamento delle risorse usando "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="46c0b-116">Example 3: Discards the move of the resources using "SourceARMID" as input.</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:01:32 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:00:00 PM
Status         : Succeeded


```

<span data-ttu-id="46c0b-117">Elimina lo spostamento delle risorse con "SourceARMID" come input.</span><span class="sxs-lookup"><span data-stu-id="46c0b-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="46c0b-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46c0b-118">PARAMETERS</span></span>

### <span data-ttu-id="46c0b-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="46c0b-119">-AsJob</span></span>
<span data-ttu-id="46c0b-120">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="46c0b-120">Run the command as a job</span></span>

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

### <span data-ttu-id="46c0b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46c0b-121">-DefaultProfile</span></span>
<span data-ttu-id="46c0b-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46c0b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46c0b-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="46c0b-123">-MoveResource</span></span>
<span data-ttu-id="46c0b-124">Ottiene o imposta l'elenco di ID della risorsa, per impostazione predefinita accetta id della risorsa di spostamento, a meno che il tipo di input non venga spostato tramite la proprietà moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="46c0b-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="46c0b-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="46c0b-125">-MoveResourceInputType</span></span>
<span data-ttu-id="46c0b-126">Definisce il tipo di input della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="46c0b-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="46c0b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="46c0b-127">-Name</span></span>
<span data-ttu-id="46c0b-128">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="46c0b-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="46c0b-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="46c0b-129">-NoWait</span></span>
<span data-ttu-id="46c0b-130">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="46c0b-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="46c0b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46c0b-131">-ResourceGroupName</span></span>
<span data-ttu-id="46c0b-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="46c0b-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="46c0b-133">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46c0b-133">-SubscriptionId</span></span>
<span data-ttu-id="46c0b-134">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="46c0b-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="46c0b-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="46c0b-135">-ValidateOnly</span></span>
<span data-ttu-id="46c0b-136">Ottiene o imposta un valore che indica se l'operazione deve eseguire solo i prerequisiti.</span><span class="sxs-lookup"><span data-stu-id="46c0b-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="46c0b-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="46c0b-137">-Confirm</span></span>
<span data-ttu-id="46c0b-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="46c0b-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46c0b-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46c0b-139">-WhatIf</span></span>
<span data-ttu-id="46c0b-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46c0b-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46c0b-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="46c0b-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46c0b-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46c0b-142">CommonParameters</span></span>
<span data-ttu-id="46c0b-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46c0b-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46c0b-144">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="46c0b-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46c0b-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="46c0b-145">INPUTS</span></span>

## <span data-ttu-id="46c0b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46c0b-146">OUTPUTS</span></span>

### <span data-ttu-id="46c0b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="46c0b-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="46c0b-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="46c0b-148">NOTES</span></span>

<span data-ttu-id="46c0b-149">ALIAS</span><span class="sxs-lookup"><span data-stu-id="46c0b-149">ALIASES</span></span>

## <span data-ttu-id="46c0b-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46c0b-150">RELATED LINKS</span></span>

