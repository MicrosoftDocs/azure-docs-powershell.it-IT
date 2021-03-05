---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: 6812849fc8fe4aa8dab21f9bbcfc13891c45e0ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999853"
---
# <span data-ttu-id="a6562-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="a6562-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="a6562-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6562-102">SYNOPSIS</span></span>
<span data-ttu-id="a6562-103">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="a6562-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="a6562-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a6562-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a6562-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a6562-105">DESCRIPTION</span></span>
<span data-ttu-id="a6562-106">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="a6562-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="a6562-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a6562-107">EXAMPLES</span></span>

### <span data-ttu-id="a6562-108">Esempio 1: Calcolare, risolvere e convalidare le dipendenze delle risorse di spostamento nella raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="a6562-108">Example 1: Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 2/9/2021 2:05:04 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/c2ad006
                 6-6a69-45fe-aa70-193c240a9bc0
Message        : The resolve dependencies operation of one or more resources has failed. Check the move status of the resource for more details.
                     Possible Causes: The resolve dependencies operation of one ore more resources has failed.
                     Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : c2ad0066-6a69-45fe-aa70-193c240a9bc0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 2:05:00 AM
Status         : Succeeded
```

<span data-ttu-id="a6562-109">Calcolare, risolvere e convalidare le dipendenze delle risorse di spostamento nella raccolta Move.</span><span class="sxs-lookup"><span data-stu-id="a6562-109">Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>

## <span data-ttu-id="a6562-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6562-110">PARAMETERS</span></span>

### <span data-ttu-id="a6562-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a6562-111">-AsJob</span></span>
<span data-ttu-id="a6562-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="a6562-112">Run the command as a job</span></span>

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

### <span data-ttu-id="a6562-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6562-113">-DefaultProfile</span></span>
<span data-ttu-id="a6562-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a6562-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6562-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="a6562-115">-MoveCollectionName</span></span>
<span data-ttu-id="a6562-116">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="a6562-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="a6562-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="a6562-117">-NoWait</span></span>
<span data-ttu-id="a6562-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="a6562-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="a6562-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6562-119">-ResourceGroupName</span></span>
<span data-ttu-id="a6562-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a6562-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="a6562-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a6562-121">-SubscriptionId</span></span>
<span data-ttu-id="a6562-122">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="a6562-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="a6562-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6562-123">-Confirm</span></span>
<span data-ttu-id="a6562-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6562-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6562-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6562-125">-WhatIf</span></span>
<span data-ttu-id="a6562-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6562-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6562-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a6562-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6562-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6562-128">CommonParameters</span></span>
<span data-ttu-id="a6562-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6562-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6562-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6562-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6562-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="a6562-131">INPUTS</span></span>

## <span data-ttu-id="a6562-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a6562-132">OUTPUTS</span></span>

### <span data-ttu-id="a6562-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="a6562-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="a6562-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="a6562-134">NOTES</span></span>

<span data-ttu-id="a6562-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="a6562-135">ALIASES</span></span>

## <span data-ttu-id="a6562-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a6562-136">RELATED LINKS</span></span>

