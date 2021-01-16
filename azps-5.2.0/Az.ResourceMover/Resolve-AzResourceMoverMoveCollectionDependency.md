---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353740"
---
# <span data-ttu-id="43f38-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="43f38-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="43f38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43f38-102">SYNOPSIS</span></span>
<span data-ttu-id="43f38-103">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="43f38-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="43f38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43f38-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="43f38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f38-105">DESCRIPTION</span></span>
<span data-ttu-id="43f38-106">Calcola, risolve e convalida le dipendenze di moveResources nella raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="43f38-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="43f38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43f38-107">EXAMPLES</span></span>

### <span data-ttu-id="43f38-108">Esempio 1: calcola, risolve e convalida le dipendenze di moveresources nella raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="43f38-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="43f38-109">Calcola, risolve e convalida le dipendenze di moveresources nella raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="43f38-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="43f38-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43f38-110">PARAMETERS</span></span>

### <span data-ttu-id="43f38-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="43f38-111">-AsJob</span></span>
<span data-ttu-id="43f38-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="43f38-112">Run the command as a job</span></span>

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

### <span data-ttu-id="43f38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f38-113">-DefaultProfile</span></span>
<span data-ttu-id="43f38-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="43f38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="43f38-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="43f38-115">-MoveCollectionName</span></span>
<span data-ttu-id="43f38-116">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="43f38-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="43f38-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="43f38-117">-NoWait</span></span>
<span data-ttu-id="43f38-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="43f38-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="43f38-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f38-119">-ResourceGroupName</span></span>
<span data-ttu-id="43f38-120">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="43f38-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="43f38-121">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="43f38-121">-SubscriptionId</span></span>
<span data-ttu-id="43f38-122">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="43f38-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="43f38-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43f38-123">-Confirm</span></span>
<span data-ttu-id="43f38-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f38-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f38-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f38-125">-WhatIf</span></span>
<span data-ttu-id="43f38-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43f38-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f38-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43f38-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f38-128">CommonParameters</span></span>
<span data-ttu-id="43f38-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f38-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="43f38-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f38-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43f38-131">INPUTS</span></span>

## <span data-ttu-id="43f38-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43f38-132">OUTPUTS</span></span>

### <span data-ttu-id="43f38-133">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="43f38-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="43f38-134">Note</span><span class="sxs-lookup"><span data-stu-id="43f38-134">NOTES</span></span>

<span data-ttu-id="43f38-135">ALIAS</span><span class="sxs-lookup"><span data-stu-id="43f38-135">ALIASES</span></span>

## <span data-ttu-id="43f38-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43f38-136">RELATED LINKS</span></span>

