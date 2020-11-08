---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleProfile.md
ms.openlocfilehash: f857f578ab3f0b8baacd0c5d392659ac09b0790f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193226"
---
# <span data-ttu-id="51ab1-101">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="51ab1-101">New-AzAutoscaleProfile</span></span>

## <span data-ttu-id="51ab1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="51ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="51ab1-103">Crea un profilo di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="51ab1-103">Creates an Autoscale profile.</span></span>

## <span data-ttu-id="51ab1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="51ab1-104">SYNTAX</span></span>

### <span data-ttu-id="51ab1-105">CreateWithoutScheduledTimes</span><span class="sxs-lookup"><span data-stu-id="51ab1-105">CreateWithoutScheduledTimes</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ab1-106">CreateWithFixedDateScheduling</span><span class="sxs-lookup"><span data-stu-id="51ab1-106">CreateWithFixedDateScheduling</span></span>
```
New-AzAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rule <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51ab1-107">CreateUsingRecurrentScheduling</span><span class="sxs-lookup"><span data-stu-id="51ab1-107">CreateUsingRecurrentScheduling</span></span>
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

## <span data-ttu-id="51ab1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="51ab1-108">DESCRIPTION</span></span>
<span data-ttu-id="51ab1-109">Il cmdlet **New-AzAutoscaleProfile** crea un profilo di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="51ab1-109">The **New-AzAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="51ab1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="51ab1-110">EXAMPLES</span></span>

### <span data-ttu-id="51ab1-111">Esempio 1: creare un profilo singolo con una data fissa</span><span class="sxs-lookup"><span data-stu-id="51ab1-111">Example 1: Create single profile with a fixed date</span></span>
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

<span data-ttu-id="51ab1-112">Il primo comando crea una regola di scalabilità denominata richieste e la archivia nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="51ab1-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="51ab1-113">Il secondo comando crea un profilo denominato Profile01 con una data fissa usando la regola in $Rule.</span><span class="sxs-lookup"><span data-stu-id="51ab1-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="51ab1-114">Esempio 2: creare un profilo con una programmazione</span><span class="sxs-lookup"><span data-stu-id="51ab1-114">Example 2: Create a profile with a schedule</span></span>
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

<span data-ttu-id="51ab1-115">Il primo comando crea una regola di scalabilità denominata richieste e la archivia nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="51ab1-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="51ab1-116">Il secondo comando crea un profilo denominato SecondProfileName con una programmazione ricorrente che usa la regola in $Rule.</span><span class="sxs-lookup"><span data-stu-id="51ab1-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="51ab1-117">Esempio 3: creare profili con due regole</span><span class="sxs-lookup"><span data-stu-id="51ab1-117">Example 3: Create profiles with two rules</span></span>
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

<span data-ttu-id="51ab1-118">I primi due comandi creano regole e li archiviano rispettivamente nelle variabili $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="51ab1-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>
<span data-ttu-id="51ab1-119">Il terzo comando crea un profilo denominato ProfileName usando le regole in Rule1 e Rule2 e lo archivia nella variabile $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="51ab1-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>
<span data-ttu-id="51ab1-120">Il comando finale crea un profilo denominato SecondProfileName usando le regole in Rule1 e Rule2 e lo archivia nella variabile $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="51ab1-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="51ab1-121">Esempio 4: creare un profilo senza pianificazione o data fissa</span><span class="sxs-lookup"><span data-stu-id="51ab1-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule -Name "ProfileName"
```

<span data-ttu-id="51ab1-122">Il primo comando crea una regola di scalabilità denominata richieste e la archivia nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="51ab1-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>
<span data-ttu-id="51ab1-123">Il secondo comando crea un profilo senza una pianificazione o una data fissa e lo archivia nella variabile $Profile.</span><span class="sxs-lookup"><span data-stu-id="51ab1-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="51ab1-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="51ab1-124">PARAMETERS</span></span>

### <span data-ttu-id="51ab1-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="51ab1-125">-DefaultCapacity</span></span>
<span data-ttu-id="51ab1-126">Specifica la capacità predefinita.</span><span class="sxs-lookup"><span data-stu-id="51ab1-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="51ab1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51ab1-127">-DefaultProfile</span></span>
<span data-ttu-id="51ab1-128">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="51ab1-128">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="51ab1-129">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="51ab1-129">-EndTimeWindow</span></span>
<span data-ttu-id="51ab1-130">Specifica la fine della finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="51ab1-130">Specifies the end of the time window.</span></span>

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

### <span data-ttu-id="51ab1-131">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="51ab1-131">-MaximumCapacity</span></span>
<span data-ttu-id="51ab1-132">Specifica la capacità massima.</span><span class="sxs-lookup"><span data-stu-id="51ab1-132">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="51ab1-133">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="51ab1-133">-MinimumCapacity</span></span>
<span data-ttu-id="51ab1-134">Specifica la capacità minima.</span><span class="sxs-lookup"><span data-stu-id="51ab1-134">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="51ab1-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="51ab1-135">-Name</span></span>
<span data-ttu-id="51ab1-136">Specifica il nome del profilo da creare.</span><span class="sxs-lookup"><span data-stu-id="51ab1-136">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="51ab1-137">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="51ab1-137">-RecurrenceFrequency</span></span>
<span data-ttu-id="51ab1-138">Specifica la frequenza di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="51ab1-138">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="51ab1-139">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="51ab1-139">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="51ab1-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="51ab1-140">None</span></span>
- <span data-ttu-id="51ab1-141">Secondo</span><span class="sxs-lookup"><span data-stu-id="51ab1-141">Second</span></span>
- <span data-ttu-id="51ab1-142">Minuto</span><span class="sxs-lookup"><span data-stu-id="51ab1-142">Minute</span></span>
- <span data-ttu-id="51ab1-143">Ora</span><span class="sxs-lookup"><span data-stu-id="51ab1-143">Hour</span></span>
- <span data-ttu-id="51ab1-144">Giorno</span><span class="sxs-lookup"><span data-stu-id="51ab1-144">Day</span></span>
- <span data-ttu-id="51ab1-145">Settimana</span><span class="sxs-lookup"><span data-stu-id="51ab1-145">Week</span></span>
- <span data-ttu-id="51ab1-146">Mese</span><span class="sxs-lookup"><span data-stu-id="51ab1-146">Month</span></span>
- <span data-ttu-id="51ab1-147">Anno non tutti questi valori sono supportati.</span><span class="sxs-lookup"><span data-stu-id="51ab1-147">Year Not all of these values are supported.</span></span>

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

### <span data-ttu-id="51ab1-148">-Regola</span><span class="sxs-lookup"><span data-stu-id="51ab1-148">-Rule</span></span>
<span data-ttu-id="51ab1-149">Specifica l'elenco di regole da aggiungere al profilo.</span><span class="sxs-lookup"><span data-stu-id="51ab1-149">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="51ab1-150">-ScheduleDay</span><span class="sxs-lookup"><span data-stu-id="51ab1-150">-ScheduleDay</span></span>
<span data-ttu-id="51ab1-151">Specifica i giorni pianificati.</span><span class="sxs-lookup"><span data-stu-id="51ab1-151">Specifies the scheduled days.</span></span>

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

### <span data-ttu-id="51ab1-152">-ScheduleHour</span><span class="sxs-lookup"><span data-stu-id="51ab1-152">-ScheduleHour</span></span>
<span data-ttu-id="51ab1-153">Specifica le ore pianificate.</span><span class="sxs-lookup"><span data-stu-id="51ab1-153">Specifies the scheduled hours.</span></span>

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

### <span data-ttu-id="51ab1-154">-ScheduleMinute</span><span class="sxs-lookup"><span data-stu-id="51ab1-154">-ScheduleMinute</span></span>
<span data-ttu-id="51ab1-155">Specifica i minuti pianificati.</span><span class="sxs-lookup"><span data-stu-id="51ab1-155">Specifies the scheduled minutes.</span></span>

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

### <span data-ttu-id="51ab1-156">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="51ab1-156">-ScheduleTimeZone</span></span>
<span data-ttu-id="51ab1-157">Specifica il fuso orario della programmazione.</span><span class="sxs-lookup"><span data-stu-id="51ab1-157">Specifies the time zone of the schedule.</span></span>

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

### <span data-ttu-id="51ab1-158">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="51ab1-158">-StartTimeWindow</span></span>
<span data-ttu-id="51ab1-159">Specifica l'inizio della finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="51ab1-159">Specifies the start of the time window.</span></span>

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

### <span data-ttu-id="51ab1-160">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="51ab1-160">-TimeWindowTimeZone</span></span>
<span data-ttu-id="51ab1-161">Specifica il fuso orario della finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="51ab1-161">Specifies the time zone of the time window.</span></span>

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

### <span data-ttu-id="51ab1-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51ab1-162">CommonParameters</span></span>
<span data-ttu-id="51ab1-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51ab1-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51ab1-164">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="51ab1-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51ab1-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="51ab1-165">INPUTS</span></span>

### <span data-ttu-id="51ab1-166">System. String</span><span class="sxs-lookup"><span data-stu-id="51ab1-166">System.String</span></span>

### <span data-ttu-id="51ab1-167">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="51ab1-167">System.DateTime</span></span>

### <span data-ttu-id="51ab1-168">Microsoft. Azure. Management. monitor. Management. Models. RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="51ab1-168">Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency</span></span>

### <span data-ttu-id="51ab1-169">System. Collections. Generic. list ' 1 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="51ab1-169">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="51ab1-170">System. Collections. Generic. List `1[[System.Nullable` 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]], System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="51ab1-170">System.Collections.Generic.List`1[[System.Nullable`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]], System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="51ab1-171">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Management. monitor. Management. Models. ScaleRule, Microsoft. Azure. PowerShell. cmdlet. monitor, versione = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="51ab1-171">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="51ab1-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="51ab1-172">OUTPUTS</span></span>

### <span data-ttu-id="51ab1-173">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="51ab1-173">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="51ab1-174">Note</span><span class="sxs-lookup"><span data-stu-id="51ab1-174">NOTES</span></span>

## <span data-ttu-id="51ab1-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="51ab1-175">RELATED LINKS</span></span>

[<span data-ttu-id="51ab1-176">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="51ab1-176">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="51ab1-177">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="51ab1-177">Get-AzAutoscaleHistory</span></span>](./Get-AzAutoscaleHistory.md)

[<span data-ttu-id="51ab1-178">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="51ab1-178">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="51ab1-179">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="51ab1-179">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="51ab1-180">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="51ab1-180">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


