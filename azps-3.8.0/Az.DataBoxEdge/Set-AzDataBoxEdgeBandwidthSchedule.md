---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022514"
---
# <span data-ttu-id="7d1ea-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="7d1ea-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="7d1ea-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d1ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7d1ea-103">Aggiorna una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="7d1ea-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d1ea-104">SYNTAX</span></span>

### <span data-ttu-id="7d1ea-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d1ea-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d1ea-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="7d1ea-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d1ea-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d1ea-114">DESCRIPTION</span></span>
<span data-ttu-id="7d1ea-115">Il cmdlet **set-AzDataBoxEdgeBandwidthSchedule** aggiorna una pianificazione della larghezza di banda per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="7d1ea-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d1ea-116">EXAMPLES</span></span>

### <span data-ttu-id="7d1ea-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d1ea-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="7d1ea-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d1ea-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="7d1ea-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d1ea-119">PARAMETERS</span></span>

### <span data-ttu-id="7d1ea-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d1ea-120">-AsJob</span></span>
<span data-ttu-id="7d1ea-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7d1ea-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d1ea-122">-Larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="7d1ea-122">-Bandwidth</span></span>
<span data-ttu-id="7d1ea-123">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="7d1ea-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="7d1ea-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="7d1ea-124">-DaysOfWeek</span></span>
<span data-ttu-id="7d1ea-125">DaysOfWeek pianificato</span><span class="sxs-lookup"><span data-stu-id="7d1ea-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="7d1ea-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d1ea-126">-DefaultProfile</span></span>
<span data-ttu-id="7d1ea-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d1ea-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="7d1ea-128">-DeviceName</span></span>
<span data-ttu-id="7d1ea-129">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d1ea-129">Device Name</span></span>

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

### <span data-ttu-id="7d1ea-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d1ea-130">-InputObject</span></span>
<span data-ttu-id="7d1ea-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1ea-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="7d1ea-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d1ea-132">-Name</span></span>
<span data-ttu-id="7d1ea-133">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="7d1ea-133">Resource Name</span></span>

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

### <span data-ttu-id="7d1ea-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d1ea-134">-ResourceGroupName</span></span>
<span data-ttu-id="7d1ea-135">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="7d1ea-135">Resource Group Name</span></span>

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

### <span data-ttu-id="7d1ea-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1ea-136">-ResourceId</span></span>
<span data-ttu-id="7d1ea-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d1ea-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="7d1ea-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="7d1ea-138">-StartTime</span></span>
<span data-ttu-id="7d1ea-139">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="7d1ea-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="7d1ea-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="7d1ea-140">-StopTime</span></span>
<span data-ttu-id="7d1ea-141">Pianificare il tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="7d1ea-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="7d1ea-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="7d1ea-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="7d1ea-143">Verrà impostata la larghezza di banda illimitata</span><span class="sxs-lookup"><span data-stu-id="7d1ea-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="7d1ea-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d1ea-144">-Confirm</span></span>
<span data-ttu-id="7d1ea-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d1ea-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d1ea-146">-WhatIf</span></span>
<span data-ttu-id="7d1ea-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7d1ea-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d1ea-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d1ea-149">CommonParameters</span></span>
<span data-ttu-id="7d1ea-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d1ea-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d1ea-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7d1ea-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d1ea-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d1ea-152">INPUTS</span></span>

### <span data-ttu-id="7d1ea-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7d1ea-153">None</span></span>

## <span data-ttu-id="7d1ea-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d1ea-154">OUTPUTS</span></span>

### <span data-ttu-id="7d1ea-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="7d1ea-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="7d1ea-156">Note</span><span class="sxs-lookup"><span data-stu-id="7d1ea-156">NOTES</span></span>

## <span data-ttu-id="7d1ea-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d1ea-157">RELATED LINKS</span></span>
