---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302484"
---
# <span data-ttu-id="45472-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="45472-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="45472-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="45472-102">SYNOPSIS</span></span>
<span data-ttu-id="45472-103">Elimina una risorsa di trasferimento dalla raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="45472-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="45472-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="45472-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="45472-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="45472-105">DESCRIPTION</span></span>
<span data-ttu-id="45472-106">Elimina una risorsa di trasferimento dalla raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="45472-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="45472-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="45472-107">EXAMPLES</span></span>

### <span data-ttu-id="45472-108">Esempio 1: rimuovere la risorsa dalla raccolta Move</span><span class="sxs-lookup"><span data-stu-id="45472-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="45472-109">Rimuovere la risorsa dall'insieme Move all'interno della sottoscrizione specificata.</span><span class="sxs-lookup"><span data-stu-id="45472-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="45472-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="45472-110">PARAMETERS</span></span>

### <span data-ttu-id="45472-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="45472-111">-AsJob</span></span>
<span data-ttu-id="45472-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="45472-112">Run the command as a job</span></span>

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

### <span data-ttu-id="45472-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45472-113">-DefaultProfile</span></span>
<span data-ttu-id="45472-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="45472-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45472-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="45472-115">-MoveCollectionName</span></span>
<span data-ttu-id="45472-116">Il nome della raccolta di mosse.</span><span class="sxs-lookup"><span data-stu-id="45472-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="45472-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="45472-117">-Name</span></span>
<span data-ttu-id="45472-118">Il nome della risorsa di trasferimento.</span><span class="sxs-lookup"><span data-stu-id="45472-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45472-119">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="45472-119">-NoWait</span></span>
<span data-ttu-id="45472-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="45472-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="45472-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="45472-121">-PassThru</span></span>
<span data-ttu-id="45472-122">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="45472-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="45472-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45472-123">-ResourceGroupName</span></span>
<span data-ttu-id="45472-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="45472-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="45472-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="45472-125">-SubscriptionId</span></span>
<span data-ttu-id="45472-126">ID abbonamento.</span><span class="sxs-lookup"><span data-stu-id="45472-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="45472-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="45472-127">-Confirm</span></span>
<span data-ttu-id="45472-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45472-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45472-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45472-129">-WhatIf</span></span>
<span data-ttu-id="45472-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45472-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="45472-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="45472-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45472-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45472-132">CommonParameters</span></span>
<span data-ttu-id="45472-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45472-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45472-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45472-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45472-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="45472-135">INPUTS</span></span>

## <span data-ttu-id="45472-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="45472-136">OUTPUTS</span></span>

### <span data-ttu-id="45472-137">Microsoft. Azure. PowerShell. Cmdlets. ResourceMover. Models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="45472-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="45472-138">Note</span><span class="sxs-lookup"><span data-stu-id="45472-138">NOTES</span></span>

<span data-ttu-id="45472-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="45472-139">ALIASES</span></span>

## <span data-ttu-id="45472-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="45472-140">RELATED LINKS</span></span>

