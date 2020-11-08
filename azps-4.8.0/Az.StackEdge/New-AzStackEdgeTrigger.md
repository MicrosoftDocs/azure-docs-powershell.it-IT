---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeTrigger.md
ms.openlocfilehash: d13498df4c91c8d31b8bfe2e19e9f7fa23f99998
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189230"
---
# <span data-ttu-id="51edf-101">New-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="51edf-101">New-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="51edf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51edf-102">SYNOPSIS</span></span>
<span data-ttu-id="51edf-103">Configura un trigger nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="51edf-103">Configures a trigger on the device.</span></span>

## <span data-ttu-id="51edf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51edf-104">SYNTAX</span></span>

### <span data-ttu-id="51edf-105">FileEventTriggerParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="51edf-105">FileEventTriggerParameterSet (Default)</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-FileEvent] -ShareName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="51edf-106">PeriodicTimerTriggerParameterSet</span><span class="sxs-lookup"><span data-stu-id="51edf-106">PeriodicTimerTriggerParameterSet</span></span>
```
New-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> -RoleName <String>
 [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>] -Schedule <String>
 -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51edf-107">FileEventTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51edf-107">FileEventTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-FileEvent] -ShareId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51edf-108">PeriodicTimerTriggerResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="51edf-108">PeriodicTimerTriggerResourceIdParameterSet</span></span>
```
New-AzStackEdgeTrigger [-PeriodicTimerEvent] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 -Schedule <String> -StartTime <DateTime> -Topic <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51edf-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51edf-109">DESCRIPTION</span></span>
<span data-ttu-id="51edf-110">Il cmdlet **New-AzStackEdgeTrigger** configura un trigger nel dispositivo dello stack Edge.</span><span class="sxs-lookup"><span data-stu-id="51edf-110">The **New-AzStackEdgeTrigger** cmdlet configures a trigger on the Stack Edge device.</span></span> 

## <span data-ttu-id="51edf-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51edf-111">EXAMPLES</span></span>

### <span data-ttu-id="51edf-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="51edf-112">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName -PeriodicTimerEvent -Name periodic-trigger -RoleName IOTRole -Schedule "00:00" -StartTime "2019-10-28 12:00:00" -Topic sample-topic
Name                  Kind               
----                  ----               
periodic-trigger      PeriodicTimerEvent
```

## <span data-ttu-id="51edf-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51edf-113">PARAMETERS</span></span>

### <span data-ttu-id="51edf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="51edf-114">-AsJob</span></span>
<span data-ttu-id="51edf-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="51edf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="51edf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51edf-116">-DefaultProfile</span></span>
<span data-ttu-id="51edf-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="51edf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51edf-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="51edf-118">-DeviceName</span></span>
<span data-ttu-id="51edf-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="51edf-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51edf-120">-FileEvent</span><span class="sxs-lookup"><span data-stu-id="51edf-120">-FileEvent</span></span>
<span data-ttu-id="51edf-121">Passare questo parametro switch per configurare il trigger fileEvent</span><span class="sxs-lookup"><span data-stu-id="51edf-121">Pass this switch parameter to configure FileEvent Trigger</span></span>

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

### <span data-ttu-id="51edf-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="51edf-122">-Name</span></span>
<span data-ttu-id="51edf-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="51edf-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51edf-124">-PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="51edf-124">-PeriodicTimerEvent</span></span>
<span data-ttu-id="51edf-125">Passare questo parametro switch per configurare il trigger PeriodicTimerEvent</span><span class="sxs-lookup"><span data-stu-id="51edf-125">Pass this switch parameter to configure PeriodicTimerEvent Trigger</span></span>

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

### <span data-ttu-id="51edf-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51edf-126">-ResourceGroupName</span></span>
<span data-ttu-id="51edf-127">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="51edf-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FileEventTriggerParameterSet, PeriodicTimerTriggerParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="51edf-128">-RoleName</span><span class="sxs-lookup"><span data-stu-id="51edf-128">-RoleName</span></span>
<span data-ttu-id="51edf-129">Ruolo di calcolo in base a quali eventi verranno generati.</span><span class="sxs-lookup"><span data-stu-id="51edf-129">Compute role against which events will be raised.</span></span>

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

### <span data-ttu-id="51edf-130">-Programmazione</span><span class="sxs-lookup"><span data-stu-id="51edf-130">-Schedule</span></span>
<span data-ttu-id="51edf-131">Frequenza periodica a cui deve essere generato l'evento timer.</span><span class="sxs-lookup"><span data-stu-id="51edf-131">Periodic frequency at which timer event needs to be raised.</span></span> <span data-ttu-id="51edf-132">Specificare una programmazione in giorni (compreso tra 1 e 365), ore (compreso tra 1 e 23) o minuti (compreso tra 1 e 59).</span><span class="sxs-lookup"><span data-stu-id="51edf-132">Specify a schedule in either days (between 1 and 365) , hours (between 1 and 23), or minutes (between 1 and 59).</span></span>

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

### <span data-ttu-id="51edf-133">-ShareId</span><span class="sxs-lookup"><span data-stu-id="51edf-133">-ShareId</span></span>
<span data-ttu-id="51edf-134">ID condivisione file da passare nel trigger fileEvent</span><span class="sxs-lookup"><span data-stu-id="51edf-134">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="51edf-135">-ShareName</span><span class="sxs-lookup"><span data-stu-id="51edf-135">-ShareName</span></span>
<span data-ttu-id="51edf-136">ID condivisione file da passare nel trigger fileEvent</span><span class="sxs-lookup"><span data-stu-id="51edf-136">File share ID to be passed in FileEvent Trigger</span></span>

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

### <span data-ttu-id="51edf-137">-StartTime</span><span class="sxs-lookup"><span data-stu-id="51edf-137">-StartTime</span></span>
<span data-ttu-id="51edf-138">L'ora del giorno che genera un trigger valido.</span><span class="sxs-lookup"><span data-stu-id="51edf-138">The time of the day that results in a valid trigger.</span></span> <span data-ttu-id="51edf-139">La programmazione viene calcolata con il riferimento all'ora specificata fino a secondi.</span><span class="sxs-lookup"><span data-stu-id="51edf-139">Schedule is computed with reference to the time specified up to seconds.</span></span> <span data-ttu-id="51edf-140">Se il fuso orario non è specificato, l'ora verrà considerata in Device TimeZone.</span><span class="sxs-lookup"><span data-stu-id="51edf-140">If timezone is not specified the time will considered to be in device timezone.</span></span> <span data-ttu-id="51edf-141">Il valore verrà sempre restituito come ora UTC.</span><span class="sxs-lookup"><span data-stu-id="51edf-141">The value will always be returned as UTC time.</span></span>

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

### <span data-ttu-id="51edf-142">-Topic</span><span class="sxs-lookup"><span data-stu-id="51edf-142">-Topic</span></span>
<span data-ttu-id="51edf-143">Argomento in cui gli eventi periodici vengono pubblicati nel dispositivo degli anni.</span><span class="sxs-lookup"><span data-stu-id="51edf-143">Topic where periodic events are published to IoT device.</span></span>

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

### <span data-ttu-id="51edf-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="51edf-144">-Confirm</span></span>
<span data-ttu-id="51edf-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51edf-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51edf-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51edf-146">-WhatIf</span></span>
<span data-ttu-id="51edf-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51edf-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51edf-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="51edf-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51edf-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51edf-149">CommonParameters</span></span>
<span data-ttu-id="51edf-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51edf-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51edf-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51edf-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51edf-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51edf-152">INPUTS</span></span>

### <span data-ttu-id="51edf-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51edf-153">None</span></span>

## <span data-ttu-id="51edf-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51edf-154">OUTPUTS</span></span>

### <span data-ttu-id="51edf-155">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="51edf-155">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="51edf-156">Note</span><span class="sxs-lookup"><span data-stu-id="51edf-156">NOTES</span></span>

## <span data-ttu-id="51edf-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51edf-157">RELATED LINKS</span></span>