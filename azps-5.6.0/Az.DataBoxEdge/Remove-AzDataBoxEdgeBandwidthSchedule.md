---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/remove-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 6b30f79f7ef1e2819004c8ac7e9d3b6737bfb7d6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006974"
---
# <span data-ttu-id="942d3-101">Remove-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="942d3-101">Remove-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="942d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="942d3-102">SYNOPSIS</span></span>
<span data-ttu-id="942d3-103">Rimuove una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="942d3-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="942d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="942d3-104">SYNTAX</span></span>

### <span data-ttu-id="942d3-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="942d3-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942d3-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="942d3-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="942d3-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="942d3-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="942d3-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="942d3-108">DESCRIPTION</span></span>
<span data-ttu-id="942d3-109">Il cmdlet **Remove-AzDataBoxEdgeBandwidthSchedule** rimuove la pianificazione della larghezza di banda per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="942d3-109">The **Remove-AzDataBoxEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Data Box Edge device.</span></span> 

## <span data-ttu-id="942d3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="942d3-110">EXAMPLES</span></span>

### <span data-ttu-id="942d3-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="942d3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="942d3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="942d3-112">PARAMETERS</span></span>

### <span data-ttu-id="942d3-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="942d3-113">-AsJob</span></span>
<span data-ttu-id="942d3-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="942d3-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="942d3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="942d3-115">-DefaultProfile</span></span>
<span data-ttu-id="942d3-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="942d3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="942d3-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="942d3-117">-DeviceName</span></span>
<span data-ttu-id="942d3-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="942d3-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942d3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="942d3-119">-InputObject</span></span>
<span data-ttu-id="942d3-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="942d3-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="942d3-121">-Name</span><span class="sxs-lookup"><span data-stu-id="942d3-121">-Name</span></span>
<span data-ttu-id="942d3-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="942d3-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942d3-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="942d3-123">-PassThru</span></span>
<span data-ttu-id="942d3-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="942d3-124">returns true if successful</span></span>

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

### <span data-ttu-id="942d3-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="942d3-125">-ResourceGroupName</span></span>
<span data-ttu-id="942d3-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="942d3-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="942d3-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="942d3-127">-ResourceId</span></span>
<span data-ttu-id="942d3-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="942d3-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="942d3-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="942d3-129">-Confirm</span></span>
<span data-ttu-id="942d3-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="942d3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="942d3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="942d3-131">-WhatIf</span></span>
<span data-ttu-id="942d3-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="942d3-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="942d3-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="942d3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="942d3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="942d3-134">CommonParameters</span></span>
<span data-ttu-id="942d3-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="942d3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="942d3-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="942d3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="942d3-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="942d3-137">INPUTS</span></span>

### <span data-ttu-id="942d3-138">System.String</span><span class="sxs-lookup"><span data-stu-id="942d3-138">System.String</span></span>

### <span data-ttu-id="942d3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="942d3-139">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="942d3-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="942d3-140">OUTPUTS</span></span>

### <span data-ttu-id="942d3-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="942d3-141">System.Boolean</span></span>

## <span data-ttu-id="942d3-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="942d3-142">NOTES</span></span>

## <span data-ttu-id="942d3-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="942d3-143">RELATED LINKS</span></span>
