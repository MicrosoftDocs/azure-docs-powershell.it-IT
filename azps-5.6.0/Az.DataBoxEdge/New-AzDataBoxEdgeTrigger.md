---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/new-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 195be7fb51e947888c7c22911f4fb5177454731e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977149"
---
# <span data-ttu-id="ce7ef-101">New-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ce7ef-101">New-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="ce7ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce7ef-102">SYNOPSIS</span></span>
<span data-ttu-id="ce7ef-103">Configura un trigger nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="ce7ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce7ef-104">SYNTAX</span></span>

### <span data-ttu-id="ce7ef-105">FileEventTriggerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ce7ef-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7ef-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce7ef-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 -RoleName <String> [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7ef-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce7ef-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce7ef-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ce7ef-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzDataBoxEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce7ef-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ce7ef-109">DESCRIPTION</span></span>
<span data-ttu-id="ce7ef-110">Il cmdlet **New-AzDataBoxEdgeTrigger** configura un trigger nel dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-110">The **New-AzDataBoxEdgeTrigger** cmdlet configures a trigger on the Data Box Edge device.</span></span> 

## <span data-ttu-id="ce7ef-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce7ef-111">EXAMPLES</span></span>

### <span data-ttu-id="ce7ef-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce7ef-112">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="ce7ef-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce7ef-113">PARAMETERS</span></span>

### <span data-ttu-id="ce7ef-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ce7ef-114">-AsJob</span></span>
<span data-ttu-id="ce7ef-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ce7ef-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ce7ef-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce7ef-116">-DefaultProfile</span></span>
<span data-ttu-id="ce7ef-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ce7ef-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="ce7ef-118">-DeviceName</span></span>
<span data-ttu-id="ce7ef-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="ce7ef-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="ce7ef-120">-FileEvent</span></span>
<span data-ttu-id="ce7ef-121">Passare questo parametro per configurare Trigger evento file</span><span class="sxs-lookup"><span data-stu-id="ce7ef-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: FileEventTriggerParameterSet, FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ce7ef-122">-Name</span></span>
<span data-ttu-id="ce7ef-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="ce7ef-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="ce7ef-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="ce7ef-125">Passare questo parametro per configurare il trigger PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="ce7ef-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce7ef-126">-ResourceGroupName</span></span>
<span data-ttu-id="ce7ef-127">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ce7ef-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="ce7ef-128">-RoleName</span></span>
<span data-ttu-id="ce7ef-129">Ruolo di calcolo rispetto a cui verranno generati gli eventi.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-129">Compute role against which events will be raised.</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-130">-Pianificazione</span><span class="sxs-lookup"><span data-stu-id="ce7ef-130">-Schedule</span></span>
<span data-ttu-id="ce7ef-131">Frequenza periodica in cui deve essere elevato l'evento timer.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="ce7ef-132">Specificare una pianificazione in due giorni (tra 1 e 365), ore (tra 1 e 23) o minuti (tra 1 e 59).</span><span class="sxs-lookup"><span data-stu-id="ce7ef-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="ce7ef-133">-ShareId</span></span>
<span data-ttu-id="ce7ef-134">ID condivisione file da passare in Trigger Evento File</span><span class="sxs-lookup"><span data-stu-id="ce7ef-134">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="ce7ef-135">-ShareName</span></span>
<span data-ttu-id="ce7ef-136">ID condivisione file da passare in Trigger Evento File</span><span class="sxs-lookup"><span data-stu-id="ce7ef-136">File share ID to be passed in FileEvent Trigger</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ce7ef-137">-StartTime</span></span>
<span data-ttu-id="ce7ef-138">Ora del giorno che genera un trigger valido.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="ce7ef-139">La pianificazione viene calcolata con riferimento all'ora specificata fino a un massimo di secondi.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="ce7ef-140">Se il fuso orario non è specificato, verrà considerato nel fuso orario del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="ce7ef-141">Il valore verrà sempre restituito come ora UTC.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-141">The value will always be returned as UTC time.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="ce7ef-142">-Topic</span></span>
<span data-ttu-id="ce7ef-143">Argomento in cui gli eventi periodici vengono pubblicati in un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-143">Topic where periodic events are published to IoT device.</span></span>

```yaml
Type: System.String
Parameter Sets: PeriodicTimerTriggerParameterSet, PeriodicTimerTriggerResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce7ef-144">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ce7ef-144">-Confirm</span></span>
<span data-ttu-id="ce7ef-145">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce7ef-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce7ef-146">-WhatIf</span></span>
<span data-ttu-id="ce7ef-147">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce7ef-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce7ef-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce7ef-149">CommonParameters</span></span>
<span data-ttu-id="ce7ef-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce7ef-151">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce7ef-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce7ef-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="ce7ef-152">INPUTS</span></span>

### <span data-ttu-id="ce7ef-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ce7ef-153">None</span></span>

## <span data-ttu-id="ce7ef-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce7ef-154">OUTPUTS</span></span>

### <span data-ttu-id="ce7ef-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="ce7ef-155">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="ce7ef-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="ce7ef-156">NOTES</span></span>

## <span data-ttu-id="ce7ef-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce7ef-157">RELATED LINKS</span></span>
