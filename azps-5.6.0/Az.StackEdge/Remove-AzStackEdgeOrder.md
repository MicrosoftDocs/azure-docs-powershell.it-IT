---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/remove-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeOrder.md
ms.openlocfilehash: 716beafc05c4746d0cfe76dce70109226b1f8f26
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005165"
---
# <span data-ttu-id="02f00-101">Remove-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="02f00-101">Remove-AzStackEdgeOrder</span></span>

## <span data-ttu-id="02f00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02f00-102">SYNOPSIS</span></span>
<span data-ttu-id="02f00-103">Rimuove l'ordine per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="02f00-103">Removes the order for a device.</span></span>

## <span data-ttu-id="02f00-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="02f00-104">SYNTAX</span></span>

### <span data-ttu-id="02f00-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="02f00-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f00-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f00-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeOrder -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02f00-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="02f00-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeOrder -InputObject <PSStackEdgeOrder> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02f00-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="02f00-108">DESCRIPTION</span></span>
<span data-ttu-id="02f00-109">Il cmdlet **Remove-AzStackEdgeOrder** elimina un ordine esistente per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="02f00-109">The **Remove-AzStackEdgeOrder** cmdlet deletes an existing order for a Stack Edge device.</span></span>

## <span data-ttu-id="02f00-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="02f00-110">EXAMPLES</span></span>

### <span data-ttu-id="02f00-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="02f00-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
```

## <span data-ttu-id="02f00-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="02f00-112">PARAMETERS</span></span>

### <span data-ttu-id="02f00-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02f00-113">-AsJob</span></span>
<span data-ttu-id="02f00-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="02f00-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="02f00-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f00-115">-DefaultProfile</span></span>
<span data-ttu-id="02f00-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="02f00-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f00-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="02f00-117">-DeviceName</span></span>
<span data-ttu-id="02f00-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="02f00-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f00-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02f00-119">-InputObject</span></span>
<span data-ttu-id="02f00-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="02f00-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02f00-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02f00-121">-PassThru</span></span>
<span data-ttu-id="02f00-122">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="02f00-122">returns true if successful</span></span>

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

### <span data-ttu-id="02f00-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02f00-123">-ResourceGroupName</span></span>
<span data-ttu-id="02f00-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="02f00-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f00-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02f00-125">-ResourceId</span></span>
<span data-ttu-id="02f00-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="02f00-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f00-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="02f00-127">-Confirm</span></span>
<span data-ttu-id="02f00-128">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02f00-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02f00-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02f00-129">-WhatIf</span></span>
<span data-ttu-id="02f00-130">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02f00-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02f00-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="02f00-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02f00-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f00-132">CommonParameters</span></span>
<span data-ttu-id="02f00-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f00-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f00-134">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="02f00-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f00-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="02f00-135">INPUTS</span></span>

### <span data-ttu-id="02f00-136">System.String</span><span class="sxs-lookup"><span data-stu-id="02f00-136">System.String</span></span>

### <span data-ttu-id="02f00-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="02f00-137">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="02f00-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="02f00-138">OUTPUTS</span></span>

### <span data-ttu-id="02f00-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="02f00-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="02f00-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="02f00-140">NOTES</span></span>

## <span data-ttu-id="02f00-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="02f00-141">RELATED LINKS</span></span>
