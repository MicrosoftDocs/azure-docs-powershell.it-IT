---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999854"
---
# <span data-ttu-id="0a795-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="0a795-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="0a795-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a795-102">SYNOPSIS</span></span>
<span data-ttu-id="0a795-103">Elimina una risorsa di spostamento dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="0a795-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="0a795-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0a795-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="0a795-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0a795-105">DESCRIPTION</span></span>
<span data-ttu-id="0a795-106">Elimina una risorsa di spostamento dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="0a795-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="0a795-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0a795-107">EXAMPLES</span></span>

### <span data-ttu-id="0a795-108">Esempio 1: Rimuovere una Rresource di spostamento dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="0a795-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="0a795-109">Rimuovere una risorsa di spostamento dalla raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="0a795-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="0a795-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0a795-110">PARAMETERS</span></span>

### <span data-ttu-id="0a795-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0a795-111">-AsJob</span></span>
<span data-ttu-id="0a795-112">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="0a795-112">Run the command as a job</span></span>

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

### <span data-ttu-id="0a795-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a795-113">-DefaultProfile</span></span>
<span data-ttu-id="0a795-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0a795-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a795-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="0a795-115">-MoveCollectionName</span></span>
<span data-ttu-id="0a795-116">Nome della raccolta di spostamento.</span><span class="sxs-lookup"><span data-stu-id="0a795-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="0a795-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0a795-117">-Name</span></span>
<span data-ttu-id="0a795-118">Nome della risorsa di spostamento.</span><span class="sxs-lookup"><span data-stu-id="0a795-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="0a795-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="0a795-119">-NoWait</span></span>
<span data-ttu-id="0a795-120">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="0a795-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="0a795-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0a795-121">-PassThru</span></span>
<span data-ttu-id="0a795-122">Restituisce true quando il comando ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="0a795-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="0a795-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a795-123">-ResourceGroupName</span></span>
<span data-ttu-id="0a795-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0a795-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="0a795-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="0a795-125">-SubscriptionId</span></span>
<span data-ttu-id="0a795-126">ID sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0a795-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="0a795-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0a795-127">-Confirm</span></span>
<span data-ttu-id="0a795-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0a795-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a795-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a795-129">-WhatIf</span></span>
<span data-ttu-id="0a795-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a795-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a795-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0a795-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a795-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a795-132">CommonParameters</span></span>
<span data-ttu-id="0a795-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a795-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a795-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0a795-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a795-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="0a795-135">INPUTS</span></span>

## <span data-ttu-id="0a795-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0a795-136">OUTPUTS</span></span>

### <span data-ttu-id="0a795-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="0a795-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="0a795-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="0a795-138">NOTES</span></span>

<span data-ttu-id="0a795-139">ALIAS</span><span class="sxs-lookup"><span data-stu-id="0a795-139">ALIASES</span></span>

## <span data-ttu-id="0a795-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0a795-140">RELATED LINKS</span></span>

