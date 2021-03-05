---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: d0f5d0d71f35df5bb36ea86a1ec20ca009256f67
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983182"
---
# <span data-ttu-id="9245b-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9245b-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9245b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9245b-102">SYNOPSIS</span></span>
<span data-ttu-id="9245b-103">Aggiorna una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="9245b-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="9245b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9245b-104">SYNTAX</span></span>

### <span data-ttu-id="9245b-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9245b-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9245b-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9245b-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="9245b-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="9245b-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9245b-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="9245b-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="9245b-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="9245b-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9245b-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="9245b-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9245b-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9245b-114">DESCRIPTION</span></span>
<span data-ttu-id="9245b-115">Il cmdlet **Set-AzDataBoxEdgeBandwidthSchedule** aggiorna una pianificazione bandwidth per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="9245b-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="9245b-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9245b-116">EXAMPLES</span></span>

### <span data-ttu-id="9245b-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9245b-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="9245b-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9245b-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="9245b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9245b-119">PARAMETERS</span></span>

### <span data-ttu-id="9245b-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9245b-120">-AsJob</span></span>
<span data-ttu-id="9245b-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9245b-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9245b-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="9245b-122">-Bandwidth</span></span>
<span data-ttu-id="9245b-123">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="9245b-123">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateByResourceIdParameterBandwidthSet, UpdateByInputObjectParameterBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="9245b-124">-DaysOfWeek</span></span>
<span data-ttu-id="9245b-125">Giorni programmatiDiSettimana</span><span class="sxs-lookup"><span data-stu-id="9245b-125">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9245b-126">-DefaultProfile</span></span>
<span data-ttu-id="9245b-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9245b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9245b-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9245b-128">-DeviceName</span></span>
<span data-ttu-id="9245b-129">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="9245b-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9245b-130">-InputObject</span></span>
<span data-ttu-id="9245b-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9245b-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-132">-Name</span><span class="sxs-lookup"><span data-stu-id="9245b-132">-Name</span></span>
<span data-ttu-id="9245b-133">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="9245b-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9245b-134">-ResourceGroupName</span></span>
<span data-ttu-id="9245b-135">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9245b-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9245b-136">-ResourceId</span></span>
<span data-ttu-id="9245b-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9245b-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="9245b-138">-StartTime</span></span>
<span data-ttu-id="9245b-139">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="9245b-139">Schedule Start Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="9245b-140">-StopTime</span></span>
<span data-ttu-id="9245b-141">Pianifica tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="9245b-141">Schedule Stop Time</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="9245b-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="9245b-143">Imposta larghezza di banda illimitata</span><span class="sxs-lookup"><span data-stu-id="9245b-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9245b-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9245b-144">-Confirm</span></span>
<span data-ttu-id="9245b-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9245b-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9245b-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9245b-146">-WhatIf</span></span>
<span data-ttu-id="9245b-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9245b-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9245b-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9245b-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9245b-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9245b-149">CommonParameters</span></span>
<span data-ttu-id="9245b-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9245b-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9245b-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9245b-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9245b-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="9245b-152">INPUTS</span></span>

### <span data-ttu-id="9245b-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="9245b-153">None</span></span>

## <span data-ttu-id="9245b-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9245b-154">OUTPUTS</span></span>

### <span data-ttu-id="9245b-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9245b-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9245b-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="9245b-156">NOTES</span></span>

## <span data-ttu-id="9245b-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9245b-157">RELATED LINKS</span></span>
