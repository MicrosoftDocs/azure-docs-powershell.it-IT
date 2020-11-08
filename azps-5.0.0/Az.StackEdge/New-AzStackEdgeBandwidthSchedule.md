---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 27d1f77db385c04e50b67b9aa3a8d8d6bf921485
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203042"
---
# <span data-ttu-id="d8717-101">New-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d8717-101">New-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="d8717-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8717-102">SYNOPSIS</span></span>
<span data-ttu-id="d8717-103">Crea una nuova pianificazione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="d8717-103">Creates a new Bandwidth schedule</span></span>

## <span data-ttu-id="d8717-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8717-104">SYNTAX</span></span>

### <span data-ttu-id="d8717-105">UnlimitedBandwidthParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8717-105">UnlimitedBandwidthParameterSet (Default)</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> [-UnlimitedBandwidth] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8717-106">BandwidthParameterSet</span><span class="sxs-lookup"><span data-stu-id="d8717-106">BandwidthParameterSet</span></span>
```
New-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -StartTime <String> -StopTime <String> -DaysOfWeek <String[]> -Bandwidth <Int32> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8717-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8717-107">DESCRIPTION</span></span>
<span data-ttu-id="d8717-108">Il cmdlet **New-AzStackEdgeBandwidthSchedule** crea una nuova pianificazione della larghezza di banda per un dispositivo Edge dello stack per facilitare la gestione dell'utilizzo della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="d8717-108">The **New-AzStackEdgeBandwidthSchedule** cmdlet creates a new Bandwidth Schedule for a Stack Edge device to help manage the Bandwidth usage.</span></span>

## <span data-ttu-id="d8717-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8717-109">EXAMPLES</span></span>

### <span data-ttu-id="d8717-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8717-110">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthSchedule -StartTime 11:00 -StopTime 12:00 -Bandwidth 30
Name                DaysOfWeek                  RateInMbps StartTime StopTime
----                ----------                  ---------- --------- --------
bandwidthSchedule  Sunday, Tuesday, Saturday    30         11:00:00  12:00:00
```

### <span data-ttu-id="d8717-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d8717-111">Example 2</span></span>
```powershell
PS C:\> New-AzStackEdgeBandwidthSchedule  -Days Sunday,Tuesday,Saturday -ResourceGroupName resourceGroupName -DeviceName deviceName -Name bandwidthScheduleUnlimited -StartTime 11:00 -StopTime 12:00 -UnlimitedBandwidth
Name                          DaysOfWeek                RateInMbps  StartTime    StopTime
----------------              ----------------------    ----------- -----------  ---------
bandwidthScheduleUnlimited  Sunday,Tuesday,Saturday     unlimited   11:00:00     12:00:00
```

## <span data-ttu-id="d8717-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8717-112">PARAMETERS</span></span>

### <span data-ttu-id="d8717-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8717-113">-AsJob</span></span>
<span data-ttu-id="d8717-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d8717-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d8717-115">-Larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="d8717-115">-Bandwidth</span></span>
<span data-ttu-id="d8717-116">Larghezza di banda in Mbps</span><span class="sxs-lookup"><span data-stu-id="d8717-116">Bandwidth in Mbps</span></span>

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

### <span data-ttu-id="d8717-117">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="d8717-117">-DaysOfWeek</span></span>
<span data-ttu-id="d8717-118">DaysOfWeek pianificato</span><span class="sxs-lookup"><span data-stu-id="d8717-118">Scheduled DaysOfWeek</span></span>

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

### <span data-ttu-id="d8717-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8717-119">-DefaultProfile</span></span>
<span data-ttu-id="d8717-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8717-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8717-121">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d8717-121">-DeviceName</span></span>
<span data-ttu-id="d8717-122">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="d8717-122">Device Name</span></span>

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

### <span data-ttu-id="d8717-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8717-123">-Name</span></span>
<span data-ttu-id="d8717-124">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="d8717-124">Resource Name</span></span>

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

### <span data-ttu-id="d8717-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8717-125">-ResourceGroupName</span></span>
<span data-ttu-id="d8717-126">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="d8717-126">Resource Group Name</span></span>

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

### <span data-ttu-id="d8717-127">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d8717-127">-StartTime</span></span>
<span data-ttu-id="d8717-128">Pianificare l'ora di inizio</span><span class="sxs-lookup"><span data-stu-id="d8717-128">Schedule Start Time</span></span>

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

### <span data-ttu-id="d8717-129">-StopTime</span><span class="sxs-lookup"><span data-stu-id="d8717-129">-StopTime</span></span>
<span data-ttu-id="d8717-130">Pianificare il tempo di interruzione</span><span class="sxs-lookup"><span data-stu-id="d8717-130">Schedule Stop Time</span></span>

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

### <span data-ttu-id="d8717-131">-UnlimitedBandwidth</span><span class="sxs-lookup"><span data-stu-id="d8717-131">-UnlimitedBandwidth</span></span>
<span data-ttu-id="d8717-132">La larghezza di banda viene impostata come illimitata</span><span class="sxs-lookup"><span data-stu-id="d8717-132">Will Set Bandwidth as Unlimited</span></span>

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

### <span data-ttu-id="d8717-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8717-133">-Confirm</span></span>
<span data-ttu-id="d8717-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8717-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8717-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8717-135">-WhatIf</span></span>
<span data-ttu-id="d8717-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8717-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d8717-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8717-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8717-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8717-138">CommonParameters</span></span>
<span data-ttu-id="d8717-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8717-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8717-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8717-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8717-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8717-141">INPUTS</span></span>

### <span data-ttu-id="d8717-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d8717-142">None</span></span>

## <span data-ttu-id="d8717-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8717-143">OUTPUTS</span></span>

### <span data-ttu-id="d8717-144">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="d8717-144">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="d8717-145">Note</span><span class="sxs-lookup"><span data-stu-id="d8717-145">NOTES</span></span>

## <span data-ttu-id="d8717-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8717-146">RELATED LINKS</span></span>
