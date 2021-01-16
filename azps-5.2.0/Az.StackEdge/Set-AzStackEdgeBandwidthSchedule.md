---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/set-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Set-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: db54799f13ca7524ccf42ade8b7e33c61a134ae9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358679"
---
# <span data-ttu-id="a8b19-101">Set-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a8b19-101">Set-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a8b19-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a8b19-102">SYNOPSIS</span></span>
<span data-ttu-id="a8b19-103">Aggiorna una pianificazione della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="a8b19-103">Updates a Bandwidth Schedule.</span></span>

## <span data-ttu-id="a8b19-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a8b19-104">SYNTAX</span></span>

### <span data-ttu-id="a8b19-105">UpdateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a8b19-105">UpdateByNameParameterSet (Default)</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-106">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-106">UpdateByResourceIdParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8b19-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-107">UpdateByResourceIdParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-108">UpdateByResourceIdParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-108">UpdateByResourceIdParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -ResourceId <String> [-StartTime <String>] [-StopTime <String>]
 [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-109">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-109">UpdateByInputObjectParameterSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-110">UpdateByInputObjectParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-111">UpdateByInputObjectParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-111">UpdateByInputObjectParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule -InputObject <PSStackEdgeBandWidthSchedule> [-StartTime <String>]
 [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-112">UpdateByNameParameterUnlimitedBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-112">UpdateByNameParameterUnlimitedBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8b19-113">UpdateByNameParameterBandwidthSet</span><span class="sxs-lookup"><span data-stu-id="a8b19-113">UpdateByNameParameterBandwidthSet</span></span>
```
Set-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-StartTime <String>] [-StopTime <String>] [-DaysOfWeek <String[]>] -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8b19-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a8b19-114">DESCRIPTION</span></span>
<span data-ttu-id="a8b19-115">Il cmdlet **set-AzStackEdgeBandwidthSchedule** aggiorna una pianificazione della larghezza di banda per un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="a8b19-115">The **Set-AzStackEdgeBandwidthSchedule** cmdlet updates a Bandwidth schedule for a Stack Edge device.</span></span>

## <span data-ttu-id="a8b19-116">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a8b19-116">EXAMPLES</span></span>

### <span data-ttu-id="a8b19-117">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a8b19-117">Example 1</span></span>
```powershell
PS C:\> Set-AzStackEdgeBandwidthSchedule  -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -UnlimitedBandwidth
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  12:00:00
```

### <span data-ttu-id="a8b19-118">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a8b19-118">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StopTime 21:00
Name                DaysOfWeek                    RateInMbps StartTime StopTime
----                ----------                    ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday      Unlimited  11:00:00  21:00:00
```

## <span data-ttu-id="a8b19-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a8b19-119">PARAMETERS</span></span>

### <span data-ttu-id="a8b19-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8b19-120">-AsJob</span></span>
<span data-ttu-id="a8b19-121">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a8b19-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8b19-122">-Larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="a8b19-122">-Bandwidth</span></span>
<span data-ttu-id="a8b19-123">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="a8b19-123">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="a8b19-124">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a8b19-124">-DaysOfWeek</span></span>
<span data-ttu-id="a8b19-125">DaysOfWeek pianificato</span><span class="sxs-lookup"><span data-stu-id="a8b19-125">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="a8b19-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8b19-126">-DefaultProfile</span></span>
<span data-ttu-id="a8b19-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a8b19-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8b19-128">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a8b19-128">-DeviceName</span></span>
<span data-ttu-id="a8b19-129">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a8b19-129">Device Name</span></span>

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

### <span data-ttu-id="a8b19-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a8b19-130">-InputObject</span></span>
<span data-ttu-id="a8b19-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8b19-131">Azure ResourceId</span></span>

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

### <span data-ttu-id="a8b19-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="a8b19-132">-Name</span></span>
<span data-ttu-id="a8b19-133">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a8b19-133">Resource Name</span></span>

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

### <span data-ttu-id="a8b19-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8b19-134">-ResourceGroupName</span></span>
<span data-ttu-id="a8b19-135">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a8b19-135">Resource Group Name</span></span>

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

### <span data-ttu-id="a8b19-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8b19-136">-ResourceId</span></span>
<span data-ttu-id="a8b19-137">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a8b19-137">Azure ResourceId</span></span>

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

### <span data-ttu-id="a8b19-138">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a8b19-138">-StartTime</span></span>
<span data-ttu-id="a8b19-139">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="a8b19-139">Schedule Start Time</span></span>

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

### <span data-ttu-id="a8b19-140">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a8b19-140">-StopTime</span></span>
<span data-ttu-id="a8b19-141">Pianificare il tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="a8b19-141">Schedule Stop Time</span></span>

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

### <span data-ttu-id="a8b19-142">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a8b19-142">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a8b19-143">Verrà impostata la larghezza di banda illimitata</span><span class="sxs-lookup"><span data-stu-id="a8b19-143">Will Set Unlimited Bandwidth</span></span>

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

### <span data-ttu-id="a8b19-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a8b19-144">-Confirm</span></span>
<span data-ttu-id="a8b19-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8b19-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8b19-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8b19-146">-WhatIf</span></span>
<span data-ttu-id="a8b19-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8b19-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a8b19-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a8b19-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8b19-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8b19-149">CommonParameters</span></span>
<span data-ttu-id="a8b19-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8b19-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8b19-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a8b19-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8b19-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a8b19-152">INPUTS</span></span>

### <span data-ttu-id="a8b19-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a8b19-153">None</span></span>

## <span data-ttu-id="a8b19-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a8b19-154">OUTPUTS</span></span>

### <span data-ttu-id="a8b19-155">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a8b19-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a8b19-156">Note</span><span class="sxs-lookup"><span data-stu-id="a8b19-156">NOTES</span></span>

## <span data-ttu-id="a8b19-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a8b19-157">RELATED LINKS</span></span>
