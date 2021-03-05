---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 17221e2d4f88e2f59ee13f73fb18132c01f6632e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994893"
---
# <span data-ttu-id="a08bb-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a08bb-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a08bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a08bb-102">SYNOPSIS</span></span>
<span data-ttu-id="a08bb-103">Aggiorna una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="a08bb-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="a08bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a08bb-104">SYNTAX</span></span>

### <span data-ttu-id="a08bb-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a08bb-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a08bb-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a08bb-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a08bb-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a08bb-114">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a08bb-114">DESCRIPTION</span></span>
<span data-ttu-id="a08bb-115">Il cmdlet **Set-AzStackEdgeBandwidthSchedule** aggiorna una pianificazione bandwidth per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="a08bb-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="a08bb-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a08bb-116">EXAMPLES</span></span>

### <span data-ttu-id="a08bb-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a08bb-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="a08bb-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a08bb-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="a08bb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a08bb-119">PARAMETERS</span></span>

### <span data-ttu-id="a08bb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a08bb-120">-AsJob</span></span>
<span data-ttu-id="a08bb-121">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a08bb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a08bb-122">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="a08bb-122">-Bandwidth</span></span>
<span data-ttu-id="a08bb-123">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="a08bb-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="a08bb-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a08bb-124">-DaysOfWeek</span></span>
<span data-ttu-id="a08bb-125">Giorni programmatiDiSettimana</span><span class="sxs-lookup"><span data-stu-id="a08bb-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="a08bb-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08bb-126">-DefaultProfile</span></span>
<span data-ttu-id="a08bb-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a08bb-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08bb-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a08bb-128">-DeviceName</span></span>
<span data-ttu-id="a08bb-129">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a08bb-129">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a08bb-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a08bb-130">-InputObject</span></span>
<span data-ttu-id="a08bb-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a08bb-131">Azure ResourceId</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule
Parameter Sets: UpdateByInputObjectParameterSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterBandwidthSet
Aliases: BandwidthSchedule

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a08bb-132">-Name</span><span class="sxs-lookup"><span data-stu-id="a08bb-132">-Name</span></span>
<span data-ttu-id="a08bb-133">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a08bb-133">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08bb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a08bb-134">-ResourceGroupName</span></span>
<span data-ttu-id="a08bb-135">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a08bb-135">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateByNameParameterUnlimitedBandwidthSet, UpdateByNameParameterBandwidthSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a08bb-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a08bb-136">-ResourceId</span></span>
<span data-ttu-id="a08bb-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a08bb-137">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet, UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByResourceIdParameterBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a08bb-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a08bb-138">-StartTime</span></span>
<span data-ttu-id="a08bb-139">Pianifica ora di inizio</span><span class="sxs-lookup"><span data-stu-id="a08bb-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="a08bb-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a08bb-140">-StopTime</span></span>
<span data-ttu-id="a08bb-141">Pianifica tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="a08bb-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="a08bb-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a08bb-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a08bb-143">Imposta larghezza di banda illimitata</span><span class="sxs-lookup"><span data-stu-id="a08bb-143">Will Set Unlimited Bandwidth</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateByResourceIdParameterUnlimitedBandwidthSet, UpdateByInputObjectParameterUnlimitedBandwidthSet, UpdateByNameParameterUnlimitedBandwidthSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a08bb-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a08bb-144">-Confirm</span></span>
<span data-ttu-id="a08bb-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a08bb-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a08bb-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a08bb-146">-WhatIf</span></span>
<span data-ttu-id="a08bb-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a08bb-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a08bb-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a08bb-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a08bb-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08bb-149">CommonParameters</span></span>
<span data-ttu-id="a08bb-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a08bb-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08bb-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a08bb-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08bb-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="a08bb-152">INPUTS</span></span>

### <span data-ttu-id="a08bb-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a08bb-153">None</span></span>

## <span data-ttu-id="a08bb-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a08bb-154">OUTPUTS</span></span>

### <span data-ttu-id="a08bb-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a08bb-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a08bb-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="a08bb-156">NOTES</span></span>

## <span data-ttu-id="a08bb-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a08bb-157">RELATED LINKS</span></span>
