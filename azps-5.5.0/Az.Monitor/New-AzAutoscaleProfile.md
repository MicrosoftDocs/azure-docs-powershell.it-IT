---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: f857f578ab3f0b8baacd0c5d392659ac09b0790f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203478"
---
# <span data-ttu-id="d4e3f-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="d4e3f-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="d4e3f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4e3f-102">SYNOPSIS</span></span>
<span data-ttu-id="d4e3f-103">Crea un profilo di gradazione automatica.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="d4e3f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4e3f-104">SYNTAX</span></span>

### <span data-ttu-id="d4e3f-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="d4e3f-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4e3f-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="d4e3f-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d4e3f-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="d4e3f-107">CreateUsingRecurrentScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDay <System.Collections.Generic.List`1[System.String]>
 -ScheduleHour <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinute <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4e3f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d4e3f-108">DESCRIPTION</span></span>
<span data-ttu-id="d4e3f-109">Il cmdlet **New-AzAutoscaleProfile** crea un profilo di gradazione automatica.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="d4e3f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4e3f-110">EXAMPLES</span></span>

### <span data-ttu-id="d4e3f-111">Esempio 1: Creare un singolo profilo con una data fissa</span><span class="sxs-lookup"><span data-stu-id="d4e3f-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="d4e3f-112">Il primo comando crea una regola di gradazione automatica denominata Richieste, che viene quindi archiviata nella variabile $Rule automatica.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="d4e3f-113">Il secondo comando crea un profilo denominato Profile01 con una data fissa usando la regola in $Rule.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="d4e3f-114">Esempio 2: Creare un profilo con una pianificazione</span><span class="sxs-lookup"><span data-stu-id="d4e3f-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="d4e3f-115">Il primo comando crea una regola di gradazione automatica denominata Richieste, che viene quindi archiviata nella variabile $Rule automatica.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="d4e3f-116">Il secondo comando crea un profilo denominato SecondProfileName con una pianificazione ricorrente usando la regola in $Rule.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="d4e3f-117">Esempio 3: Creare profili con due regole</span><span class="sxs-lookup"><span data-stu-id="d4e3f-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDay "1" -ScheduleHour 5 -ScheduleMinute 15 -ScheduleTimeZone UTC
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : profileName
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="d4e3f-118">I primi due comandi creano regole e le archiviano rispettivamente nelle variabili $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="d4e3f-119">Il terzo comando crea un profilo denominato ProfileName usando le regole in Rule1 e Rule2 e quindi lo archivia nella variabile $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="d4e3f-120">Il comando finale crea un profilo denominato SecondProfileName usando le regole in Rule1 e Rule2 e quindi lo archivia nella variabile $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="d4e3f-121">Esempio 4: Creare un profilo senza programmazione o data fissa</span><span class="sxs-lookup"><span data-stu-id="d4e3f-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="d4e3f-122">Il primo comando crea una regola di gradazione automatica denominata Richieste, che viene quindi archiviata nella variabile $Rule automatica.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="d4e3f-123">Il secondo comando crea un profilo senza una pianificazione o una data fissa e quindi lo archivia nella $Profile variabile.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="d4e3f-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4e3f-124">PARAMETERS</span></span>

### <span data-ttu-id="d4e3f-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="d4e3f-125">-DefaultCapacity</span></span>
<span data-ttu-id="d4e3f-126">Specifica la capacità predefinita.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-126">Specifies the default capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4e3f-127">-DefaultProfile</span></span>
<span data-ttu-id="d4e3f-128">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="d4e3f-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4e3f-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="d4e3f-129">-EndTimeWindow</span></span>
<span data-ttu-id="d4e3f-130">Specifica la fine dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-130">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="d4e3f-131">-MaximumCapacity</span></span>
<span data-ttu-id="d4e3f-132">Specifica la capacità massima.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-132">Specifies the maximum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="d4e3f-133">-MinimumCapacity</span></span>
<span data-ttu-id="d4e3f-134">Specifica la capacità minima.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-134">Specifies the minimum capacity.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-135">-Name</span><span class="sxs-lookup"><span data-stu-id="d4e3f-135">-Name</span></span>
<span data-ttu-id="d4e3f-136">Specifica il nome del profilo da creare.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-136">Specifies the name of the profile to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="d4e3f-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="d4e3f-138">Specifica la frequenza di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="d4e3f-139">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="d4e3f-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="d4e3f-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d4e3f-140">None</span></span>
- <span data-ttu-id="d4e3f-141">Secondo</span><span class="sxs-lookup"><span data-stu-id="d4e3f-141">Second</span></span>
- <span data-ttu-id="d4e3f-142">Minuto</span><span class="sxs-lookup"><span data-stu-id="d4e3f-142">Minute</span></span>
- <span data-ttu-id="d4e3f-143">Ora</span><span class="sxs-lookup"><span data-stu-id="d4e3f-143">Hour</span></span>
- <span data-ttu-id="d4e3f-144">Giorno</span><span class="sxs-lookup"><span data-stu-id="d4e3f-144">Day</span></span>
- <span data-ttu-id="d4e3f-145">Settimana</span><span class="sxs-lookup"><span data-stu-id="d4e3f-145">Week</span></span>
- <span data-ttu-id="d4e3f-146">Mese</span><span class="sxs-lookup"><span data-stu-id="d4e3f-146">Month</span></span>
- <span data-ttu-id="d4e3f-147">Anno Non tutti questi valori sono supportati.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-147">Year Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-148">-Rule</span><span class="sxs-lookup"><span data-stu-id="d4e3f-148">-Rule</span></span>
<span data-ttu-id="d4e3f-149">Specifica l'elenco di regole da aggiungere al profilo.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-149">Specifies the list of rules to add to the profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="d4e3f-150">-ScheduleDay</span></span>
<span data-ttu-id="d4e3f-151">Specifica i giorni pianificati.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-151">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="d4e3f-152">-ScheduleHour</span></span>
<span data-ttu-id="d4e3f-153">Specifica le ore pianificate.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-153">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="d4e3f-154">-ScheduleMinute</span></span>
<span data-ttu-id="d4e3f-155">Specifica i minuti pianificati.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-155">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="d4e3f-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="d4e3f-157">Specifica il fuso orario della pianificazione.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-157">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateUsingRecurrentScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="d4e3f-158">-StartTimeWindow</span></span>
<span data-ttu-id="d4e3f-159">Specifica l'inizio dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-159">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="d4e3f-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="d4e3f-161">Specifica il fuso orario dell'intervallo di tempo.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-161">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithFixedDateScheduling
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4e3f-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4e3f-162">CommonParameters</span></span>
<span data-ttu-id="d4e3f-163">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4e3f-164">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d4e3f-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4e3f-165">INPUT</span><span class="sxs-lookup"><span data-stu-id="d4e3f-165">INPUTS</span></span>

### <span data-ttu-id="d4e3f-166">System.String</span><span class="sxs-lookup"><span data-stu-id="d4e3f-166">System.String</span></span>

### <span data-ttu-id="d4e3f-167">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="d4e3f-167">System.DateTime</span></span>

### <span data-ttu-id="d4e3f-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="d4e3f-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="d4e3f-169">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e3f-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d4e3f-170">System.Collections.generic.List `1[[System.Nullable` 1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="d4e3f-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="d4e3f-171">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="d4e3f-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d4e3f-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4e3f-172">OUTPUTS</span></span>

### <span data-ttu-id="d4e3f-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="d4e3f-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="d4e3f-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="d4e3f-174">NOTES</span></span>

## <span data-ttu-id="d4e3f-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4e3f-175">RELATED LINKS</span></span>

[<span data-ttu-id="d4e3f-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d4e3f-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="d4e3f-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="d4e3f-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="d4e3f-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d4e3f-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="d4e3f-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="d4e3f-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="d4e3f-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="d4e3f-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


