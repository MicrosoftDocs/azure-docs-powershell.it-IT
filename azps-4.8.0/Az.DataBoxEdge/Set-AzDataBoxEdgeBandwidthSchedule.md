---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/set-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Set-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 503f274b07b13bc19b4994f8b440ffc853f69bc5
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192546"
---
# <span data-ttu-id="297f1-101">Set-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="297f1-101">Set-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="297f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="297f1-102">SYNOPSIS</span></span>
<span data-ttu-id="297f1-103">Aggiorna una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="297f1-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="297f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="297f1-104">SYNTAX</span></span>

### <span data-ttu-id="297f1-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="297f1-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="297f1-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="297f1-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="297f1-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="297f1-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="297f1-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="297f1-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="297f1-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule -InputObject <PSDataBoxEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="297f1-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="297f1-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="297f1-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="297f1-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="297f1-114">DESCRIPTION</span></span>
<span data-ttu-id="297f1-115">Il cmdlet **set-AzDataBoxEdgeBandwidthSchedule** aggiorna una pianificazione della larghezza di banda per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="297f1-115">The **Set-AzDataBoxEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Data Box Edge device.</span></span>

## <span data-ttu-id="297f1-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="297f1-116">EXAMPLES</span></span>

### <span data-ttu-id="297f1-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="297f1-117">Example 1</span></span>
```powershell
PS C:\> Set-AzDataBoxEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="297f1-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="297f1-118">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="297f1-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="297f1-119">PARAMETERS</span></span>

### <span data-ttu-id="297f1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="297f1-120">-AsJob</span></span>
<span data-ttu-id="297f1-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="297f1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="297f1-122">-Larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="297f1-122">-Bandwidth</span></span>
<span data-ttu-id="297f1-123">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="297f1-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="297f1-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="297f1-124">-DaysOfWeek</span></span>
<span data-ttu-id="297f1-125">DaysOfWeek pianificato</span><span class="sxs-lookup"><span data-stu-id="297f1-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="297f1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="297f1-126">-DefaultProfile</span></span>
<span data-ttu-id="297f1-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="297f1-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="297f1-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="297f1-128">-DeviceName</span></span>
<span data-ttu-id="297f1-129">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="297f1-129">Device Name</span></span>

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

### <span data-ttu-id="297f1-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="297f1-130">-InputObject</span></span>
<span data-ttu-id="297f1-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="297f1-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="297f1-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="297f1-132">-Name</span></span>
<span data-ttu-id="297f1-133">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="297f1-133">Resource Name</span></span>

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

### <span data-ttu-id="297f1-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="297f1-134">-ResourceGroupName</span></span>
<span data-ttu-id="297f1-135">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="297f1-135">Resource Group Name</span></span>

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

### <span data-ttu-id="297f1-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="297f1-136">-ResourceId</span></span>
<span data-ttu-id="297f1-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="297f1-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="297f1-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="297f1-138">-StartTime</span></span>
<span data-ttu-id="297f1-139">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="297f1-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="297f1-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="297f1-140">-StopTime</span></span>
<span data-ttu-id="297f1-141">Pianificare il tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="297f1-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="297f1-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="297f1-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="297f1-143">Verrà impostata la larghezza di banda illimitata</span><span class="sxs-lookup"><span data-stu-id="297f1-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="297f1-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="297f1-144">-Confirm</span></span>
<span data-ttu-id="297f1-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="297f1-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="297f1-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="297f1-146">-WhatIf</span></span>
<span data-ttu-id="297f1-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="297f1-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="297f1-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="297f1-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="297f1-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="297f1-149">CommonParameters</span></span>
<span data-ttu-id="297f1-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="297f1-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="297f1-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="297f1-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="297f1-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="297f1-152">INPUTS</span></span>

### <span data-ttu-id="297f1-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="297f1-153">None</span></span>

## <span data-ttu-id="297f1-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="297f1-154">OUTPUTS</span></span>

### <span data-ttu-id="297f1-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="297f1-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="297f1-156">Note</span><span class="sxs-lookup"><span data-stu-id="297f1-156">NOTES</span></span>

## <span data-ttu-id="297f1-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="297f1-157">RELATED LINKS</span></span>