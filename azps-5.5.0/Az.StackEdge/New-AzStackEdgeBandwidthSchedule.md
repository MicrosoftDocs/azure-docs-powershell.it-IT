---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190950"
---
# <span data-ttu-id="a96b1-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a96b1-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="a96b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a96b1-102">SYNOPSIS</span></span>
<span data-ttu-id="a96b1-103">Crea una nuova pianificazione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="a96b1-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="a96b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a96b1-104">SYNTAX</span></span>

### <span data-ttu-id="a96b1-105">UnlimitedBandwidthParameterSet (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a96b1-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a96b1-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="a96b1-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a96b1-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a96b1-107">DESCRIPTION</span></span>
<span data-ttu-id="a96b1-108">Il cmdlet **New-AzStackEdgeBandwidthSchedule** crea una nuova pianificazione della larghezza di banda per un dispositivo Stack Edge per gestire l'utilizzo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="a96b1-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="a96b1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a96b1-109">EXAMPLES</span></span>

### <span data-ttu-id="a96b1-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a96b1-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="a96b1-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a96b1-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="a96b1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a96b1-112">PARAMETERS</span></span>

### <span data-ttu-id="a96b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a96b1-113">-AsJob</span></span>
<span data-ttu-id="a96b1-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a96b1-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a96b1-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="a96b1-115">-Bandwidth</span></span>
<span data-ttu-id="a96b1-116">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="a96b1-116">Bandwidth in Mbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: BandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96b1-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="a96b1-117">-DaysOfWeek</span></span>
<span data-ttu-id="a96b1-118">Giorni programmatiDiSettimana</span><span class="sxs-lookup"><span data-stu-id="a96b1-118">Scheduled DaysOfWeek</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96b1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a96b1-119">-DefaultProfile</span></span>
<span data-ttu-id="a96b1-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a96b1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a96b1-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a96b1-121">-DeviceName</span></span>
<span data-ttu-id="a96b1-122">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="a96b1-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96b1-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a96b1-123">-Name</span></span>
<span data-ttu-id="a96b1-124">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="a96b1-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96b1-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a96b1-125">-ResourceGroupName</span></span>
<span data-ttu-id="a96b1-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a96b1-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a96b1-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="a96b1-127">-StartTime</span></span>
<span data-ttu-id="a96b1-128">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="a96b1-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="a96b1-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="a96b1-129">-StopTime</span></span>
<span data-ttu-id="a96b1-130">Pianifica tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="a96b1-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="a96b1-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="a96b1-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="a96b1-132">Imposta larghezza di banda illimitata</span><span class="sxs-lookup"><span data-stu-id="a96b1-132">Will Set Bandwidth as Unlimited</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a96b1-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a96b1-133">-Confirm</span></span>
<span data-ttu-id="a96b1-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a96b1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a96b1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a96b1-135">-WhatIf</span></span>
<span data-ttu-id="a96b1-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a96b1-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a96b1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a96b1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a96b1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a96b1-138">CommonParameters</span></span>
<span data-ttu-id="a96b1-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a96b1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a96b1-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a96b1-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a96b1-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="a96b1-141">INPUTS</span></span>

### <span data-ttu-id="a96b1-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a96b1-142">None</span></span>

## <span data-ttu-id="a96b1-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a96b1-143">OUTPUTS</span></span>

### <span data-ttu-id="a96b1-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="a96b1-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="a96b1-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="a96b1-145">NOTES</span></span>

## <span data-ttu-id="a96b1-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a96b1-146">RELATED LINKS</span></span>
