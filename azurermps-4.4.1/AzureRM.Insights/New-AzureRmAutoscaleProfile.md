---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleProfile.md
ms.openlocfilehash: a5cea42544f2f24ad6c1f1cc1ce64bf122e53440
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521238"
---
# <span data-ttu-id="f3de3-101">New-AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f3de3-101">New-AzureRmAutoscaleProfile</span></span>

## <span data-ttu-id="f3de3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3de3-102">SYNOPSIS</span></span>
<span data-ttu-id="f3de3-103">Crea un profilo di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="f3de3-103">Creates an Autoscale profile.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3de3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3de3-104">SYNTAX</span></span>

### <span data-ttu-id="f3de3-105">Parametri per New-AzureRmAutoscaleProfile cmdlet senza orari pianificati</span><span class="sxs-lookup"><span data-stu-id="f3de3-105">Parameters for New-AzureRmAutoscaleProfile cmdlet without scheduled times</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3de3-106">Parametri per New-AzureRmAutoscaleProfile cmdlet tramite la pianificazione della data di correzione</span><span class="sxs-lookup"><span data-stu-id="f3de3-106">Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -StartTimeWindow <DateTime> -EndTimeWindow <DateTime> -TimeWindowTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3de3-107">Parametri per New-AzureRmAutoscaleProfile cmdlet tramite la programmazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="f3de3-107">Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling</span></span>
```
New-AzureRmAutoscaleProfile -Name <String> -DefaultCapacity <String> -MaximumCapacity <String>
 -MinimumCapacity <String> -RecurrenceFrequency <RecurrenceFrequency>
 -ScheduleDays <System.Collections.Generic.List`1[System.String]>
 -ScheduleHours <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleMinutes <System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]>
 -ScheduleTimeZone <String>
 -Rules <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ScaleRule]>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3de3-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3de3-108">DESCRIPTION</span></span>
<span data-ttu-id="f3de3-109">Il cmdlet **New-AzureRmAutoscaleProfile** crea un profilo di scalabilità verticale.</span><span class="sxs-lookup"><span data-stu-id="f3de3-109">The **New-AzureRmAutoscaleProfile** cmdlet creates an Autoscale profile.</span></span>

## <span data-ttu-id="f3de3-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3de3-110">EXAMPLES</span></span>

### <span data-ttu-id="f3de3-111">Esempio 1: creare un profilo singolo con una data fissa</span><span class="sxs-lookup"><span data-stu-id="f3de3-111">Example 1: Create single profile with a fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule -Name "Profile01"
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : Microsoft.Azure.Management.Insights.Models.TimeWindow
Name       : adios
Recurrence : 
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="f3de3-112">Il primo comando crea una regola di scalabilità denominata richieste e la archivia nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="f3de3-112">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="f3de3-113">Il secondo comando crea un profilo denominato Profile01 con una data fissa usando la regola in $Rule.</span><span class="sxs-lookup"><span data-stu-id="f3de3-113">The second command creates a profile named Profile01 with a fixed date using the rule in $Rule.</span></span>

### <span data-ttu-id="f3de3-114">Esempio 2: creare un profilo con una programmazione</span><span class="sxs-lookup"><span data-stu-id="f3de3-114">Example 2: Create a profile with a schedule</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT
Capacity   : Microsoft.Azure.Management.Insights.Models.ScaleCapacity
FixedDate  : 
Name       : secondProfileName
Recurrence : Microsoft.Azure.Management.Insights.Models.Recurrence
Rules      : {Microsoft.Azure.Management.Insights.Models.ScaleRule, 
             Microsoft.Azure.Management.Insights.Models.ScaleRule}
```

<span data-ttu-id="f3de3-115">Il primo comando crea una regola di scalabilità denominata richieste e la archivia nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="f3de3-115">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="f3de3-116">Il secondo comando crea un profilo denominato SecondProfileName con una programmazione ricorrente che usa la regola in $Rule.</span><span class="sxs-lookup"><span data-stu-id="f3de3-116">The second command creates a profile named SecondProfileName with a recurring schedule using the rule in $Rule.</span></span>

### <span data-ttu-id="f3de3-117">Esempio 3: creare profili con due regole</span><span class="sxs-lookup"><span data-stu-id="f3de3-117">Example 3: Create profiles with two rules</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "ProfileName"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Week -ScheduleDays "1" -ScheduleHours 5 -ScheduleMinutes 15 -ScheduleTimeZone UTC
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

<span data-ttu-id="f3de3-118">I primi due comandi creano regole e li archiviano rispettivamente nelle variabili $Rule 1 e $Rule 2.</span><span class="sxs-lookup"><span data-stu-id="f3de3-118">The first two commands create rules, and store them in the variables $Rule1 and $Rule2, respectively.</span></span>

<span data-ttu-id="f3de3-119">Il terzo comando crea un profilo denominato ProfileName usando le regole in Rule1 e Rule2 e lo archivia nella variabile $Profile 1.</span><span class="sxs-lookup"><span data-stu-id="f3de3-119">The third command creates a profile named ProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile1 variable.</span></span>

<span data-ttu-id="f3de3-120">Il comando finale crea un profilo denominato SecondProfileName usando le regole in Rule1 e Rule2 e lo archivia nella variabile $Profile 2.</span><span class="sxs-lookup"><span data-stu-id="f3de3-120">The final command creates a profile named SecondProfileName using the rules in Rule1 and Rule2, and then stores it in the $Profile2 variable.</span></span>

### <span data-ttu-id="f3de3-121">Esempio 4: creare un profilo senza pianificazione o data fissa</span><span class="sxs-lookup"><span data-stu-id="f3de3-121">Example 4: Create a profile with no schedule or fixed date</span></span>
```
PS C:\>$Rule = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Profile = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule -Name "ProfileName"
```

<span data-ttu-id="f3de3-122">Il primo comando crea una regola di scalabilità denominata richieste e la archivia nella variabile $Rule.</span><span class="sxs-lookup"><span data-stu-id="f3de3-122">The first command creates an Autoscale rule named Requests, and then stores it in the $Rule variable.</span></span>

<span data-ttu-id="f3de3-123">Il secondo comando crea un profilo senza una pianificazione o una data fissa e lo archivia nella variabile $Profile.</span><span class="sxs-lookup"><span data-stu-id="f3de3-123">The second command creates a profile without a schedule or a fixed date, and then stores it in the $Profile variable.</span></span>

## <span data-ttu-id="f3de3-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3de3-124">PARAMETERS</span></span>

### <span data-ttu-id="f3de3-125">-DefaultCapacity</span><span class="sxs-lookup"><span data-stu-id="f3de3-125">-DefaultCapacity</span></span>
<span data-ttu-id="f3de3-126">Specifica la capacità predefinita.</span><span class="sxs-lookup"><span data-stu-id="f3de3-126">Specifies the default capacity.</span></span>

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

### <span data-ttu-id="f3de3-127">-EndTimeWindow</span><span class="sxs-lookup"><span data-stu-id="f3de3-127">-EndTimeWindow</span></span>
<span data-ttu-id="f3de3-128">Specifica la fine della finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="f3de3-128">Specifies the end of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-129">-MaximumCapacity</span><span class="sxs-lookup"><span data-stu-id="f3de3-129">-MaximumCapacity</span></span>
<span data-ttu-id="f3de3-130">Specifica la capacità massima.</span><span class="sxs-lookup"><span data-stu-id="f3de3-130">Specifies the maximum capacity.</span></span>

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

### <span data-ttu-id="f3de3-131">-MinimumCapacity</span><span class="sxs-lookup"><span data-stu-id="f3de3-131">-MinimumCapacity</span></span>
<span data-ttu-id="f3de3-132">Specifica la capacità minima.</span><span class="sxs-lookup"><span data-stu-id="f3de3-132">Specifies the minimum capacity.</span></span>

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

### <span data-ttu-id="f3de3-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3de3-133">-Name</span></span>
<span data-ttu-id="f3de3-134">Specifica il nome del profilo da creare.</span><span class="sxs-lookup"><span data-stu-id="f3de3-134">Specifies the name of the profile to create.</span></span>

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

### <span data-ttu-id="f3de3-135">-RecurrenceFrequency</span><span class="sxs-lookup"><span data-stu-id="f3de3-135">-RecurrenceFrequency</span></span>
<span data-ttu-id="f3de3-136">Specifica la frequenza di ricorrenza.</span><span class="sxs-lookup"><span data-stu-id="f3de3-136">Specifies the frequency of recurrence.</span></span>
<span data-ttu-id="f3de3-137">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f3de3-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f3de3-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f3de3-138">None</span></span>
- <span data-ttu-id="f3de3-139">Secondo</span><span class="sxs-lookup"><span data-stu-id="f3de3-139">Second</span></span>
- <span data-ttu-id="f3de3-140">Minuto</span><span class="sxs-lookup"><span data-stu-id="f3de3-140">Minute</span></span>
- <span data-ttu-id="f3de3-141">Ora</span><span class="sxs-lookup"><span data-stu-id="f3de3-141">Hour</span></span>
- <span data-ttu-id="f3de3-142">Giorno</span><span class="sxs-lookup"><span data-stu-id="f3de3-142">Day</span></span>
- <span data-ttu-id="f3de3-143">Settimana</span><span class="sxs-lookup"><span data-stu-id="f3de3-143">Week</span></span>
- <span data-ttu-id="f3de3-144">Mese</span><span class="sxs-lookup"><span data-stu-id="f3de3-144">Month</span></span>
- <span data-ttu-id="f3de3-145">Anno</span><span class="sxs-lookup"><span data-stu-id="f3de3-145">Year</span></span>

<span data-ttu-id="f3de3-146">Non tutti questi valori sono supportati.</span><span class="sxs-lookup"><span data-stu-id="f3de3-146">Not all of these values are supported.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.RecurrenceFrequency
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 
Accepted values: None, Second, Minute, Hour, Day, Week, Month, Year

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-147">-Regole</span><span class="sxs-lookup"><span data-stu-id="f3de3-147">-Rules</span></span>
<span data-ttu-id="f3de3-148">Specifica l'elenco di regole da aggiungere al profilo.</span><span class="sxs-lookup"><span data-stu-id="f3de3-148">Specifies the list of rules to add to the profile.</span></span>

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

### <span data-ttu-id="f3de3-149">-ScheduleDays</span><span class="sxs-lookup"><span data-stu-id="f3de3-149">-ScheduleDays</span></span>
<span data-ttu-id="f3de3-150">Specifica i giorni pianificati.</span><span class="sxs-lookup"><span data-stu-id="f3de3-150">Specifies the scheduled days.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-151">-ScheduleHours</span><span class="sxs-lookup"><span data-stu-id="f3de3-151">-ScheduleHours</span></span>
<span data-ttu-id="f3de3-152">Specifica le ore pianificate.</span><span class="sxs-lookup"><span data-stu-id="f3de3-152">Specifies the scheduled hours.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-153">-ScheduleMinutes</span><span class="sxs-lookup"><span data-stu-id="f3de3-153">-ScheduleMinutes</span></span>
<span data-ttu-id="f3de3-154">Specifica i minuti pianificati.</span><span class="sxs-lookup"><span data-stu-id="f3de3-154">Specifies the scheduled minutes.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.Nullable`1[System.Int32]]
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-155">-ScheduleTimeZone</span><span class="sxs-lookup"><span data-stu-id="f3de3-155">-ScheduleTimeZone</span></span>
<span data-ttu-id="f3de3-156">Specifica il fuso orario della programmazione.</span><span class="sxs-lookup"><span data-stu-id="f3de3-156">Specifies the time zone of the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using recurrent scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-157">-StartTimeWindow</span><span class="sxs-lookup"><span data-stu-id="f3de3-157">-StartTimeWindow</span></span>
<span data-ttu-id="f3de3-158">Specifica l'inizio della finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="f3de3-158">Specifies the start of the time window.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-159">-TimeWindowTimeZone</span><span class="sxs-lookup"><span data-stu-id="f3de3-159">-TimeWindowTimeZone</span></span>
<span data-ttu-id="f3de3-160">Specifica il fuso orario della finestra temporale.</span><span class="sxs-lookup"><span data-stu-id="f3de3-160">Specifies the time zone of the time window.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for New-AzureRmAutoscaleProfile cmdlet using fix date scheduling
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-161">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3de3-161">-DefaultProfile</span></span>
<span data-ttu-id="f3de3-162">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3de3-162">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3de3-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3de3-163">CommonParameters</span></span>
<span data-ttu-id="f3de3-164">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3de3-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3de3-165">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3de3-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3de3-166">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3de3-166">INPUTS</span></span>

## <span data-ttu-id="f3de3-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3de3-167">OUTPUTS</span></span>

### <span data-ttu-id="f3de3-168">Microsoft. Azure. Management. monitor. Management. Models. AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="f3de3-168">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile</span></span>

## <span data-ttu-id="f3de3-169">Note</span><span class="sxs-lookup"><span data-stu-id="f3de3-169">NOTES</span></span>

## <span data-ttu-id="f3de3-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3de3-170">RELATED LINKS</span></span>

[<span data-ttu-id="f3de3-171">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f3de3-171">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="f3de3-172">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="f3de3-172">Get-AzureRmAutoscaleHistory</span></span>](./Get-AzureRmAutoscaleHistory.md)

[<span data-ttu-id="f3de3-173">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f3de3-173">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="f3de3-174">New-AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="f3de3-174">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="f3de3-175">Remove-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="f3de3-175">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


