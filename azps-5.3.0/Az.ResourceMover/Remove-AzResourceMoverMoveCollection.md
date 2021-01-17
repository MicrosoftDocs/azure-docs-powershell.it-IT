---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474329"
---
# <span data-ttu-id="6358c-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="6358c-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="6358c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6358c-102">SYNOPSIS</span></span>
<span data-ttu-id="6358c-103">Elimina una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="6358c-103">Deletes a move collection.</span></span>

## <span data-ttu-id="6358c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6358c-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6358c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6358c-105">DESCRIPTION</span></span>
<span data-ttu-id="6358c-106">Elimina una raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="6358c-106">Deletes a move collection.</span></span>

## <span data-ttu-id="6358c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6358c-107">EXAMPLES</span></span>

### <span data-ttu-id="6358c-108">Esempio 1: rimuovere la raccolta di mosse dall'abbonamento specificato</span><span class="sxs-lookup"><span data-stu-id="6358c-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
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

<span data-ttu-id="6358c-109">Rimuovere la raccolta di mosse dall'abbonamento specificato.</span><span class="sxs-lookup"><span data-stu-id="6358c-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="6358c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6358c-110">PARAMETERS</span></span>

### <span data-ttu-id="6358c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6358c-111">-AsJob</span></span>
<span data-ttu-id="6358c-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="6358c-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6358c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6358c-113">-DefaultProfile</span></span>
<span data-ttu-id="6358c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6358c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6358c-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="6358c-115">-Name</span></span>
<span data-ttu-id="6358c-116">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="6358c-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="6358c-117">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="6358c-117">-NoWait</span></span>
<span data-ttu-id="6358c-118">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="6358c-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6358c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6358c-119">-PassThru</span></span>
<span data-ttu-id="6358c-120">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="6358c-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="6358c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6358c-121">-ResourceGroupName</span></span>
<span data-ttu-id="6358c-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6358c-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="6358c-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6358c-123">-SubscriptionId</span></span>
<span data-ttu-id="6358c-124">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="6358c-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="6358c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6358c-125">-Confirm</span></span>
<span data-ttu-id="6358c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6358c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6358c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6358c-127">-WhatIf</span></span>
<span data-ttu-id="6358c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6358c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6358c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6358c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6358c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6358c-130">CommonParameters</span></span>
<span data-ttu-id="6358c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6358c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6358c-132">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6358c-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6358c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6358c-133">INPUTS</span></span>

## <span data-ttu-id="6358c-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6358c-134">OUTPUTS</span></span>

### <span data-ttu-id="6358c-135">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="6358c-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="6358c-136">Note</span><span class="sxs-lookup"><span data-stu-id="6358c-136">NOTES</span></span>

<span data-ttu-id="6358c-137">ALIAS</span><span class="sxs-lookup"><span data-stu-id="6358c-137">ALIASES</span></span>

## <span data-ttu-id="6358c-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6358c-138">RELATED LINKS</span></span>

