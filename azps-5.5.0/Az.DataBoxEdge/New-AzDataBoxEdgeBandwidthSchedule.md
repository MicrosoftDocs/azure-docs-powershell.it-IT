---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: 68522dbd90593bdbc37afe333144431b997cc70c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188663"
---
# <span data-ttu-id="ca809-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ca809-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ca809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca809-102">SYNOPSIS</span></span>
<span data-ttu-id="ca809-103">Crea una nuova pianificazione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="ca809-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="ca809-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca809-104">SYNTAX</span></span>

### <span data-ttu-id="ca809-105">BandwidthParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca809-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca809-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca809-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca809-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ca809-107">DESCRIPTION</span></span>
<span data-ttu-id="ca809-108">Il cmdlet **New-AzDataBoxEdgeBandwidthSchedule** crea una nuova pianificazione della larghezza di banda per un dispositivo Data Box Edge per gestire l'utilizzo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="ca809-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="ca809-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca809-109">EXAMPLES</span></span>

### <span data-ttu-id="ca809-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca809-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="ca809-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ca809-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="ca809-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ca809-112">PARAMETERS</span></span>

### <span data-ttu-id="ca809-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca809-113">-AsJob</span></span>
<span data-ttu-id="ca809-114">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca809-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca809-115">-Bandwidth</span><span class="sxs-lookup"><span data-stu-id="ca809-115">-Bandwidth</span></span>
<span data-ttu-id="ca809-116">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="ca809-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="ca809-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ca809-117">-DaysOfWeek</span></span>
<span data-ttu-id="ca809-118">Giorni programmatiDiSettimana</span><span class="sxs-lookup"><span data-stu-id="ca809-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="ca809-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca809-119">-DefaultProfile</span></span>
<span data-ttu-id="ca809-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca809-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca809-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ca809-121">-DeviceName</span></span>
<span data-ttu-id="ca809-122">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca809-122">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca809-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ca809-123">-Name</span></span>
<span data-ttu-id="ca809-124">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="ca809-124">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca809-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca809-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca809-126">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ca809-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca809-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ca809-127">-StartTime</span></span>
<span data-ttu-id="ca809-128">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="ca809-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="ca809-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="ca809-129">-StopTime</span></span>
<span data-ttu-id="ca809-130">Pianifica tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="ca809-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="ca809-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="ca809-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="ca809-132">Imposta larghezza di banda illimitata, se è impostata su false, imposta il valore predefinito su 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="ca809-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UnlimitedBandwidthParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca809-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ca809-133">-Confirm</span></span>
<span data-ttu-id="ca809-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca809-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca809-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca809-135">-WhatIf</span></span>
<span data-ttu-id="ca809-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca809-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca809-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca809-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca809-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca809-138">CommonParameters</span></span>
<span data-ttu-id="ca809-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca809-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca809-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ca809-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca809-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="ca809-141">INPUTS</span></span>

### <span data-ttu-id="ca809-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ca809-142">None</span></span>

## <span data-ttu-id="ca809-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca809-143">OUTPUTS</span></span>

### <span data-ttu-id="ca809-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ca809-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ca809-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="ca809-145">NOTES</span></span>

## <span data-ttu-id="ca809-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca809-146">RELATED LINKS</span></span>
