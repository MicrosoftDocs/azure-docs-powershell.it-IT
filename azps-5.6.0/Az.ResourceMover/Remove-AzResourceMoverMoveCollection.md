---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999885"
---
# <span data-ttu-id="c6fd3-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="c6fd3-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="c6fd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6fd3-102">SYNOPSIS</span></span>
<span data-ttu-id="c6fd3-103">Elimina una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-103">Deletes a move collection.</span></span>

## <span data-ttu-id="c6fd3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c6fd3-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c6fd3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c6fd3-105">DESCRIPTION</span></span>
<span data-ttu-id="c6fd3-106">Elimina una raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-106">Deletes a move collection.</span></span>

## <span data-ttu-id="c6fd3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c6fd3-107">EXAMPLES</span></span>

### <span data-ttu-id="c6fd3-108">Esempio 1: Rimuovere la raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="c6fd3-109">Rimuovere la raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="c6fd3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6fd3-110">PARAMETERS</span></span>

### <span data-ttu-id="c6fd3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c6fd3-111">-AsJob</span></span>
<span data-ttu-id="c6fd3-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="c6fd3-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c6fd3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6fd3-113">-DefaultProfile</span></span>
<span data-ttu-id="c6fd3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c6fd3-115">-Name</span><span class="sxs-lookup"><span data-stu-id="c6fd3-115">-Name</span></span>
<span data-ttu-id="c6fd3-116">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="c6fd3-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c6fd3-117">-NoWait</span></span>
<span data-ttu-id="c6fd3-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="c6fd3-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c6fd3-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c6fd3-119">-PassThru</span></span>
<span data-ttu-id="c6fd3-120">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="c6fd3-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="c6fd3-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6fd3-121">-ResourceGroupName</span></span>
<span data-ttu-id="c6fd3-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="c6fd3-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c6fd3-123">-SubscriptionId</span></span>
<span data-ttu-id="c6fd3-124">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="c6fd3-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6fd3-125">-Confirm</span></span>
<span data-ttu-id="c6fd3-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6fd3-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6fd3-127">-WhatIf</span></span>
<span data-ttu-id="c6fd3-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6fd3-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6fd3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6fd3-130">CommonParameters</span></span>
<span data-ttu-id="c6fd3-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6fd3-132">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6fd3-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6fd3-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="c6fd3-133">INPUTS</span></span>

## <span data-ttu-id="c6fd3-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c6fd3-134">OUTPUTS</span></span>

### <span data-ttu-id="c6fd3-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="c6fd3-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="c6fd3-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="c6fd3-136">NOTES</span></span>

<span data-ttu-id="c6fd3-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="c6fd3-137">ALIASES</span></span>

## <span data-ttu-id="c6fd3-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c6fd3-138">RELATED LINKS</span></span>

