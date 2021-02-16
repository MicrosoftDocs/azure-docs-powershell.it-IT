---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: f3f38feff8b6d855121a6772cfb56ef0b57cebfd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209122"
---
# <span data-ttu-id="47e91-101">Remove-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="47e91-101">Remove-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="47e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47e91-102">SYNOPSIS</span></span>
<span data-ttu-id="47e91-103">Rimuove una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="47e91-103">Removes a Bandwidth Schedule.</span></span>

## <span data-ttu-id="47e91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="47e91-104">SYNTAX</span></span>

### <span data-ttu-id="47e91-105">DeleteByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="47e91-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e91-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47e91-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47e91-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47e91-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47e91-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="47e91-108">DESCRIPTION</span></span>
<span data-ttu-id="47e91-109">Il cmdlet **Remove-AzStackEdgeBandwidthSchedule** rimuove la pianificazione della larghezza di banda per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="47e91-109">The **Remove-AzStackEdgeBandwidthSchedule** cmdlet removes the Bandwidth schedule for a Stack Edge device.</span></span> 

## <span data-ttu-id="47e91-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="47e91-110">EXAMPLES</span></span>

### <span data-ttu-id="47e91-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="47e91-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule
```

## <span data-ttu-id="47e91-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="47e91-112">PARAMETERS</span></span>

### <span data-ttu-id="47e91-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="47e91-113">-AsJob</span></span>
<span data-ttu-id="47e91-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="47e91-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="47e91-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47e91-115">-DefaultProfile</span></span>
<span data-ttu-id="47e91-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="47e91-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47e91-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="47e91-117">-DeviceName</span></span>
<span data-ttu-id="47e91-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="47e91-118">Device Name</span></span>

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

### <span data-ttu-id="47e91-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="47e91-119">-InputObject</span></span>
<span data-ttu-id="47e91-120">Oggetto Input</span><span class="sxs-lookup"><span data-stu-id="47e91-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="47e91-121">-Name</span><span class="sxs-lookup"><span data-stu-id="47e91-121">-Name</span></span>
<span data-ttu-id="47e91-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="47e91-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47e91-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47e91-123">-PassThru</span></span>
<span data-ttu-id="47e91-124">restituisce true se ha esito positivo</span><span class="sxs-lookup"><span data-stu-id="47e91-124">returns true if successful</span></span>

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

### <span data-ttu-id="47e91-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47e91-125">-ResourceGroupName</span></span>
<span data-ttu-id="47e91-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="47e91-126">Resource Group Name</span></span>

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

### <span data-ttu-id="47e91-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47e91-127">-ResourceId</span></span>
<span data-ttu-id="47e91-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="47e91-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="47e91-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="47e91-129">-Confirm</span></span>
<span data-ttu-id="47e91-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47e91-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47e91-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47e91-131">-WhatIf</span></span>
<span data-ttu-id="47e91-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47e91-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47e91-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="47e91-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47e91-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47e91-134">CommonParameters</span></span>
<span data-ttu-id="47e91-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47e91-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47e91-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="47e91-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47e91-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="47e91-137">INPUTS</span></span>

### <span data-ttu-id="47e91-138">System.String</span><span class="sxs-lookup"><span data-stu-id="47e91-138">System.String</span></span>

### <span data-ttu-id="47e91-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="47e91-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="47e91-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="47e91-140">OUTPUTS</span></span>

### <span data-ttu-id="47e91-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="47e91-141">System.Boolean</span></span>

## <span data-ttu-id="47e91-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="47e91-142">NOTES</span></span>

## <span data-ttu-id="47e91-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="47e91-143">RELATED LINKS</span></span>
