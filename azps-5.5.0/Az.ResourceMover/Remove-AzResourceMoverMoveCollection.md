---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183703"
---
# <span data-ttu-id="f3769-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="f3769-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="f3769-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3769-102">SYNOPSIS</span></span>
<span data-ttu-id="f3769-103">Elimina una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="f3769-103">Deletes a move collection.</span></span>

## <span data-ttu-id="f3769-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3769-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="f3769-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f3769-105">DESCRIPTION</span></span>
<span data-ttu-id="f3769-106">Elimina una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="f3769-106">Deletes a move collection.</span></span>

## <span data-ttu-id="f3769-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3769-107">EXAMPLES</span></span>

### <span data-ttu-id="f3769-108">Esempio 1: Rimuovere la raccolta di spostamento dalla sottoscrizione specificata</span><span class="sxs-lookup"><span data-stu-id="f3769-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="f3769-109">Rimuovere la raccolta di spostamento dalla sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="f3769-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="f3769-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3769-110">PARAMETERS</span></span>

### <span data-ttu-id="f3769-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3769-111">-AsJob</span></span>
<span data-ttu-id="f3769-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="f3769-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f3769-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3769-113">-DefaultProfile</span></span>
<span data-ttu-id="f3769-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3769-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3769-115">-Name</span><span class="sxs-lookup"><span data-stu-id="f3769-115">-Name</span></span>
<span data-ttu-id="f3769-116">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="f3769-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="f3769-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="f3769-117">-NoWait</span></span>
<span data-ttu-id="f3769-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="f3769-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f3769-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3769-119">-PassThru</span></span>
<span data-ttu-id="f3769-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="f3769-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="f3769-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3769-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3769-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f3769-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f3769-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f3769-123">-SubscriptionId</span></span>
<span data-ttu-id="f3769-124">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f3769-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="f3769-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3769-125">-Confirm</span></span>
<span data-ttu-id="f3769-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3769-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3769-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3769-127">-WhatIf</span></span>
<span data-ttu-id="f3769-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3769-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3769-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3769-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3769-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3769-130">CommonParameters</span></span>
<span data-ttu-id="f3769-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3769-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3769-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f3769-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3769-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="f3769-133">INPUTS</span></span>

## <span data-ttu-id="f3769-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3769-134">OUTPUTS</span></span>

### <span data-ttu-id="f3769-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f3769-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="f3769-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="f3769-136">NOTES</span></span>

<span data-ttu-id="f3769-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="f3769-137">ALIASES</span></span>

## <span data-ttu-id="f3769-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3769-138">RELATED LINKS</span></span>

