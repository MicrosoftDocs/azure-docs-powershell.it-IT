---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: ee7321f6021c6e4b2f56209d6c6a7fd5a6ff79a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685025"
---
# <span data-ttu-id="1bd15-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1bd15-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="1bd15-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1bd15-102">SYNOPSIS</span></span>
<span data-ttu-id="1bd15-103">Crea una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="1bd15-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1bd15-104">SYNTAX</span></span>

### <span data-ttu-id="1bd15-105">ByDaily (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1bd15-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="1bd15-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="1bd15-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bd15-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="1bd15-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bd15-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="1bd15-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bd15-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="1bd15-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1bd15-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="1bd15-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1bd15-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bd15-111">DESCRIPTION</span></span>
<span data-ttu-id="1bd15-112">Il cmdlet **New-AzAutomationSchedule** crea una pianificazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1bd15-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="1bd15-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1bd15-113">EXAMPLES</span></span>

### <span data-ttu-id="1bd15-114">Esempio 1: creare una pianificazione unica in ora locale</span><span class="sxs-lookup"><span data-stu-id="1bd15-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="1bd15-115">Il primo comando ottiene l'ID del fuso orario dal sistema e lo archivia nella variabile $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="1bd15-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="1bd15-116">Il secondo comando crea una programmazione che viene eseguita una volta alla data corrente in 11:00 PM nel fuso orario specificato.</span><span class="sxs-lookup"><span data-stu-id="1bd15-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="1bd15-117">Esempio 2: creare una pianificazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="1bd15-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1bd15-118">Il primo comando crea un oggetto Date usando il cmdlet **get-date** e quindi archivia l'oggetto nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="1bd15-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="1bd15-119">Specificare un periodo di almeno cinque minuti per il futuro.</span><span class="sxs-lookup"><span data-stu-id="1bd15-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="1bd15-120">Il secondo comando crea un oggetto Date usando il cmdlet **get-date** e quindi archivia l'oggetto nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="1bd15-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="1bd15-121">Il comando specifica un'ora futura.</span><span class="sxs-lookup"><span data-stu-id="1bd15-121">The command specifies a future time.</span></span>
<span data-ttu-id="1bd15-122">Il comando finale crea una programmazione giornaliera denominata Schedule02 per iniziare all'ora archiviata in $StartDate e scade all'ora archiviata in $EndDate.</span><span class="sxs-lookup"><span data-stu-id="1bd15-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="1bd15-123">Esempio 3: creare una programmazione periodica settimanale</span><span class="sxs-lookup"><span data-stu-id="1bd15-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="1bd15-124">Il primo comando crea un oggetto Date usando il cmdlet **get-date** e quindi archivia l'oggetto nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="1bd15-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="1bd15-125">Il secondo comando crea una matrice di giorni della settimana che contiene lunedì, martedì, mercoledì, giovedì e venerdì.</span><span class="sxs-lookup"><span data-stu-id="1bd15-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="1bd15-126">Il comando finale crea una programmazione giornaliera denominata Schedule03 che verrà eseguita dal lunedì al venerdì ogni settimana alle 13:00.</span><span class="sxs-lookup"><span data-stu-id="1bd15-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="1bd15-127">La programmazione non scadrà mai.</span><span class="sxs-lookup"><span data-stu-id="1bd15-127">The schedule will never expire.</span></span>

## <span data-ttu-id="1bd15-128">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1bd15-128">PARAMETERS</span></span>

### <span data-ttu-id="1bd15-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1bd15-129">-AutomationAccountName</span></span>
<span data-ttu-id="1bd15-130">Specifica il nome di un account di automazione per cui questo cmdlet crea una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="1bd15-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="1bd15-131">-DayInterval</span></span>
<span data-ttu-id="1bd15-132">Specifica un intervallo, in giorni, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="1bd15-133">Se non specifichi questo parametro e non *specifichi il parametro una volta* , il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="1bd15-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByDaily
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="1bd15-134">-DayOfWeek</span></span>
<span data-ttu-id="1bd15-135">Specifica un elenco di giorni della settimana per la programmazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="1bd15-135">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.Nullable`1[System.DayOfWeek]
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="1bd15-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="1bd15-137">Specifica l'occorrenza della settimana entro il mese in cui viene eseguita la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="1bd15-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="1bd15-138">psdx_paramvalues</span></span>
- <span data-ttu-id="1bd15-139">1</span><span class="sxs-lookup"><span data-stu-id="1bd15-139">1</span></span>
- <span data-ttu-id="1bd15-140">2</span><span class="sxs-lookup"><span data-stu-id="1bd15-140">2</span></span>
- <span data-ttu-id="1bd15-141">3</span><span class="sxs-lookup"><span data-stu-id="1bd15-141">3</span></span>
- <span data-ttu-id="1bd15-142">4</span><span class="sxs-lookup"><span data-stu-id="1bd15-142">4</span></span>
- <span data-ttu-id="1bd15-143">-1</span><span class="sxs-lookup"><span data-stu-id="1bd15-143">-1</span></span>
- <span data-ttu-id="1bd15-144">Prima</span><span class="sxs-lookup"><span data-stu-id="1bd15-144">First</span></span>
- <span data-ttu-id="1bd15-145">Secondo</span><span class="sxs-lookup"><span data-stu-id="1bd15-145">Second</span></span>
- <span data-ttu-id="1bd15-146">Terze</span><span class="sxs-lookup"><span data-stu-id="1bd15-146">Third</span></span>
- <span data-ttu-id="1bd15-147">Quarto</span><span class="sxs-lookup"><span data-stu-id="1bd15-147">Fourth</span></span>
- <span data-ttu-id="1bd15-148">LastDay</span><span class="sxs-lookup"><span data-stu-id="1bd15-148">LastDay</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DayOfWeekOccurrence
Parameter Sets: ByMonthlyDayOfWeek
Aliases:
Accepted values: First, Second, Third, Fourth, Last

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="1bd15-149">-DaysOfMonth</span></span>
<span data-ttu-id="1bd15-150">Specifica un elenco di giorni del mese per la programmazione mensile.</span><span class="sxs-lookup"><span data-stu-id="1bd15-150">Specifies a list of days of the month for the monthly schedule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Cmdlet.DaysOfMonth[]
Parameter Sets: ByMonthlyDaysOfMonth
Aliases:
Accepted values: One, Two, Three, Four, Five, Six, Seventh, Eighth, Ninth, Tenth, Eleventh, Twelfth, Thirteenth, Fourteenth, Fifteenth, Sixteenth, Seventeenth, Eighteenth, Nineteenth, Twentieth, TwentyFirst, TwentySecond, TwentyThird, TwentyFourth, TwentyFifth, TwentySixth, TwentySeventh, TwentyEighth, TwentyNinth, Thirtieth, ThirtyFirst, LastDay

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="1bd15-151">-DaysOfWeek</span></span>
<span data-ttu-id="1bd15-152">Specifica un elenco di giorni della settimana per la programmazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="1bd15-152">Specifies a list of days of the week for the weekly schedule.</span></span>

```yaml
Type: System.DayOfWeek[]
Parameter Sets: ByWeekly
Aliases:
Accepted values: Sunday, Monday, Tuesday, Wednesday, Thursday, Friday, Saturday

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1bd15-153">-DefaultProfile</span></span>
<span data-ttu-id="1bd15-154">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1bd15-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1bd15-155">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="1bd15-155">-Description</span></span>
<span data-ttu-id="1bd15-156">Specifica una descrizione per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-156">Specifies a description for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1bd15-157">-ExpiryTime</span></span>
<span data-ttu-id="1bd15-158">Specifica il periodo di scadenza di una pianificazione come oggetto **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="1bd15-158">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="1bd15-159">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="1bd15-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByDaily, ByWeekly, ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek, ByHourly
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="1bd15-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="1bd15-161">Indica che questo oggetto pianificazione verrà usato per la pianificazione di una configurazione di aggiornamento software</span><span class="sxs-lookup"><span data-stu-id="1bd15-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="1bd15-162">-HourInterval</span></span>
<span data-ttu-id="1bd15-163">Specifica un intervallo, in ore, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-163">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByHourly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="1bd15-164">-MonthInterval</span></span>
<span data-ttu-id="1bd15-165">Specifica un intervallo, in mesi, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-165">Specifies an interval, in Months, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByMonthlyDaysOfMonth, ByMonthlyDayOfWeek
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-166">-Nome</span><span class="sxs-lookup"><span data-stu-id="1bd15-166">-Name</span></span>
<span data-ttu-id="1bd15-167">Specifica un nome per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-167">Specifies a name for the schedule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-168">-Una tantum</span><span class="sxs-lookup"><span data-stu-id="1bd15-168">-OneTime</span></span>
<span data-ttu-id="1bd15-169">Specifica che il cmdlet crea una pianificazione una tantum.</span><span class="sxs-lookup"><span data-stu-id="1bd15-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByOneTime
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bd15-170">-ResourceGroupName</span></span>
<span data-ttu-id="1bd15-171">Specifica il nome di un gruppo di risorse per cui questo cmdlet crea una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="1bd15-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1bd15-172">-StartTime</span></span>
<span data-ttu-id="1bd15-173">Specifica l'ora di inizio di una pianificazione come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="1bd15-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="1bd15-174">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="1bd15-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="1bd15-175">Se viene specificato il parametro *TimeZone* , l'offset verrà ignorato e viene usato il fuso orario specificato.</span><span class="sxs-lookup"><span data-stu-id="1bd15-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="1bd15-176">-TimeZone</span></span>
<span data-ttu-id="1bd15-177">Specifica il fuso orario per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="1bd15-178">Questa stringa può essere l'ID IANA o l'ID del fuso orario di Windows.</span><span class="sxs-lookup"><span data-stu-id="1bd15-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="1bd15-179">-WeekInterval</span></span>
<span data-ttu-id="1bd15-180">Specifica un intervallo, in settimane, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="1bd15-180">Specifies an interval, in weeks, for the schedule.</span></span>

```yaml
Type: System.Byte
Parameter Sets: ByWeekly
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1bd15-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bd15-181">CommonParameters</span></span>
<span data-ttu-id="1bd15-182">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bd15-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bd15-183">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bd15-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bd15-184">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1bd15-184">INPUTS</span></span>

### <span data-ttu-id="1bd15-185">System. String</span><span class="sxs-lookup"><span data-stu-id="1bd15-185">System.String</span></span>

### <span data-ttu-id="1bd15-186">System. DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="1bd15-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="1bd15-187">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1bd15-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1bd15-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1bd15-188">OUTPUTS</span></span>

### <span data-ttu-id="1bd15-189">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="1bd15-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="1bd15-190">Note</span><span class="sxs-lookup"><span data-stu-id="1bd15-190">NOTES</span></span>

## <span data-ttu-id="1bd15-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1bd15-191">RELATED LINKS</span></span>

[<span data-ttu-id="1bd15-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1bd15-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="1bd15-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1bd15-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="1bd15-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="1bd15-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)

