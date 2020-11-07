---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e15e6ee6186dc19f9f85264548c1b735ea242b98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863242"
---
# <span data-ttu-id="ca3ee-101">New-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ca3ee-101">New-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="ca3ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca3ee-102">SYNOPSIS</span></span>
<span data-ttu-id="ca3ee-103">Crea una nuova pianificazione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="ca3ee-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="ca3ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca3ee-104">SYNTAX</span></span>

### <span data-ttu-id="ca3ee-105">BandwidthParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca3ee-105">BandwidthParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca3ee-106">UnlimitedBandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="ca3ee-106">UnlimitedBandwidthParameterSet</span></span>
```
New-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -UnlimitedBandwidth <Boolean> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca3ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca3ee-107">DESCRIPTION</span></span>
<span data-ttu-id="ca3ee-108">Il cmdlet **New-AzDataBoxEdgeBandwidthSchedule** crea una nuova pianificazione della larghezza di banda per un dispositivo Edge della casella dati per facilitare la gestione dell'utilizzo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="ca3ee-108">The **New-AzDataBoxEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Data Box Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="ca3ee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca3ee-109">EXAMPLES</span></span>

### <span data-ttu-id="ca3ee-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ca3ee-110">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="ca3ee-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ca3ee-111">Example 2</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="ca3ee-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca3ee-112">PARAMETERS</span></span>

### <span data-ttu-id="ca3ee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ca3ee-113">-AsJob</span></span>
<span data-ttu-id="ca3ee-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ca3ee-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ca3ee-115">-Larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="ca3ee-115">-Bandwidth</span></span>
<span data-ttu-id="ca3ee-116">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="ca3ee-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="ca3ee-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ca3ee-117">-DaysOfWeek</span></span>
<span data-ttu-id="ca3ee-118">DaysOfWeek pianificato</span><span class="sxs-lookup"><span data-stu-id="ca3ee-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="ca3ee-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca3ee-119">-DefaultProfile</span></span>
<span data-ttu-id="ca3ee-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca3ee-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca3ee-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ca3ee-121">-DeviceName</span></span>
<span data-ttu-id="ca3ee-122">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="ca3ee-122">Device Name</span></span>

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

### <span data-ttu-id="ca3ee-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ca3ee-123">-Name</span></span>
<span data-ttu-id="ca3ee-124">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="ca3ee-124">Resource Name</span></span>

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

### <span data-ttu-id="ca3ee-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca3ee-125">-ResourceGroupName</span></span>
<span data-ttu-id="ca3ee-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="ca3ee-126">Resource Group Name</span></span>

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

### <span data-ttu-id="ca3ee-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ca3ee-127">-StartTime</span></span>
<span data-ttu-id="ca3ee-128">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="ca3ee-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="ca3ee-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="ca3ee-129">-StopTime</span></span>
<span data-ttu-id="ca3ee-130">Pianificare il tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="ca3ee-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="ca3ee-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="ca3ee-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="ca3ee-132">Imposta la larghezza di banda illimitata, se impostato su false imposta il valore predefinito come 20 Mbps</span><span class="sxs-lookup"><span data-stu-id="ca3ee-132">Will Set Unlimited Bandwidth, if set to false will set default value as 20 Mbps</span></span>

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

### <span data-ttu-id="ca3ee-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca3ee-133">-Confirm</span></span>
<span data-ttu-id="ca3ee-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca3ee-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca3ee-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca3ee-135">-WhatIf</span></span>
<span data-ttu-id="ca3ee-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3ee-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ca3ee-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca3ee-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca3ee-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca3ee-138">CommonParameters</span></span>
<span data-ttu-id="ca3ee-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca3ee-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca3ee-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca3ee-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca3ee-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca3ee-141">INPUTS</span></span>

### <span data-ttu-id="ca3ee-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ca3ee-142">None</span></span>

## <span data-ttu-id="ca3ee-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca3ee-143">OUTPUTS</span></span>

### <span data-ttu-id="ca3ee-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="ca3ee-144">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="ca3ee-145">Note</span><span class="sxs-lookup"><span data-stu-id="ca3ee-145">NOTES</span></span>

## <span data-ttu-id="ca3ee-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca3ee-146">RELATED LINKS</span></span>
