---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSchedule.md
ms.openlocfilehash: 9f9cd5b779fcc4e1b9dd6f3df7ed0255adeaa3af
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201046"
---
# <span data-ttu-id="cd2a3-101">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd2a3-101">New-AzAutomationSchedule</span></span>

## <span data-ttu-id="cd2a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd2a3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd2a3-103">Crea una pianificazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="cd2a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cd2a3-104">SYNTAX</span></span>

### <span data-ttu-id="cd2a3-105">ByDaily (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cd2a3-105">ByDaily (Default)</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cd2a3-106">Disettimana</span><span class="sxs-lookup"><span data-stu-id="cd2a3-106">ByWeekly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd2a3-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="cd2a3-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd2a3-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="cd2a3-108">ByMonthlyDayOfWeek</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd2a3-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="cd2a3-109">ByOneTime</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ForUpdateConfiguration] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cd2a3-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="cd2a3-110">ByHourly</span></span>
```
New-AzAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ForUpdateConfiguration]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cd2a3-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cd2a3-111">DESCRIPTION</span></span>
<span data-ttu-id="cd2a3-112">Il cmdlet **New-AzAutomationSchedule** crea una pianificazione nell'automazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-112">The **New-AzAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="cd2a3-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cd2a3-113">EXAMPLES</span></span>

### <span data-ttu-id="cd2a3-114">Esempio 1: Creare una pianificazione che può essere pianificata una sola volta in locale</span><span class="sxs-lookup"><span data-stu-id="cd2a3-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\> $TimeZone = ([System.TimeZoneInfo]::Local).Id
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="cd2a3-115">Il primo comando recupera l'ID fuso orario dal sistema e lo archivia nella $TimeZone variabile.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="cd2a3-116">Il secondo comando crea una pianificazione che viene eseguita una sola volta alla data corrente alle 23:00 nel fuso orario specificato.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="cd2a3-117">Esempio 2: Creare una pianificazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="cd2a3-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DayInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cd2a3-118">Il primo comando crea un oggetto data usando il cmdlet **Get-Date** e quindi archivia l'oggetto nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="cd2a3-119">Specificare un'ora futura di almeno cinque minuti.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-119">Specify a time that is at least five minutes in the future.</span></span>
<span data-ttu-id="cd2a3-120">Il secondo comando crea un oggetto data usando il cmdlet **Get-Date** e quindi archivia l'oggetto nella $EndDate variabile.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="cd2a3-121">Il comando specifica un orario futuro.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-121">The command specifies a future time.</span></span>
<span data-ttu-id="cd2a3-122">Il comando finale crea una pianificazione giornaliera denominata Pianificazione02 in modo che inizi dal momento archiviato in $StartDate e scada al momento archiviato nel $EndDate.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-122">The final command creates a daily schedule named Schedule02 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

### <span data-ttu-id="cd2a3-123">Esempio 3: Creare una pianificazione ricorrente settimanale</span><span class="sxs-lookup"><span data-stu-id="cd2a3-123">Example 3: Create a weekly recurring schedule</span></span>
```
PS C:\> $StartTime = (Get-Date "13:00:00").AddDays(1)
PS C:\> [System.DayOfWeek[]]$WeekDays = @([System.DayOfWeek]::Monday..[System.DayOfWeek]::Friday)
PS C:\> New-AzAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule03" -StartTime $StartTime - WeekInterval 1 -DaysOfWeek $WeekDays -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="cd2a3-124">Il primo comando crea un oggetto data usando il cmdlet **Get-Date** e quindi archivia l'oggetto nella $StartDate variabile.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-124">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="cd2a3-125">Il secondo comando crea una matrice di giorni della settimana che contiene lunedì, martedì, mercoledì, giovedì e venerdì.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-125">The second command creates an array of week days that contains Monday, Tuesday, Wednesday, Thursday and Friday.</span></span>
<span data-ttu-id="cd2a3-126">Il comando finale crea una pianificazione giornaliera denominata Pianificazione03 che verrà eseguita ogni settimana dal lunedì al venerdì alle 13:00.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-126">The final command creates a daily schedule named Schedule03 that will run Monday to Friday each week at 13:00.</span></span> <span data-ttu-id="cd2a3-127">La pianificazione non scadrà mai.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-127">The schedule will never expire.</span></span>

## <span data-ttu-id="cd2a3-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd2a3-128">PARAMETERS</span></span>

### <span data-ttu-id="cd2a3-129">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd2a3-129">-AutomationAccountName</span></span>
<span data-ttu-id="cd2a3-130">Specifica il nome di un account di automazione per cui questo cmdlet crea una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-130">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="cd2a3-131">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="cd2a3-131">-DayInterval</span></span>
<span data-ttu-id="cd2a3-132">Specifica un intervallo, in giorni, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-132">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="cd2a3-133">Se non si specifica questo parametro e non si specifica il parametro *OneTime,* il valore predefinito è 1 (1).</span><span class="sxs-lookup"><span data-stu-id="cd2a3-133">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="cd2a3-134">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="cd2a3-134">-DayOfWeek</span></span>
<span data-ttu-id="cd2a3-135">Specifica un elenco di giorni della settimana per la pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-135">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="cd2a3-136">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="cd2a3-136">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="cd2a3-137">Specifica l'occorrenza della settimana nel mese in cui viene eseguita la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-137">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="cd2a3-138">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="cd2a3-138">psdx_paramvalues</span></span>
- <span data-ttu-id="cd2a3-139">1</span><span class="sxs-lookup"><span data-stu-id="cd2a3-139">1</span></span>
- <span data-ttu-id="cd2a3-140">2</span><span class="sxs-lookup"><span data-stu-id="cd2a3-140">2</span></span>
- <span data-ttu-id="cd2a3-141">3</span><span class="sxs-lookup"><span data-stu-id="cd2a3-141">3</span></span>
- <span data-ttu-id="cd2a3-142">4</span><span class="sxs-lookup"><span data-stu-id="cd2a3-142">4</span></span>
- <span data-ttu-id="cd2a3-143">-1</span><span class="sxs-lookup"><span data-stu-id="cd2a3-143">-1</span></span>
- <span data-ttu-id="cd2a3-144">Prima di tutto</span><span class="sxs-lookup"><span data-stu-id="cd2a3-144">First</span></span>
- <span data-ttu-id="cd2a3-145">Secondo</span><span class="sxs-lookup"><span data-stu-id="cd2a3-145">Second</span></span>
- <span data-ttu-id="cd2a3-146">Terzo</span><span class="sxs-lookup"><span data-stu-id="cd2a3-146">Third</span></span>
- <span data-ttu-id="cd2a3-147">Quarto</span><span class="sxs-lookup"><span data-stu-id="cd2a3-147">Fourth</span></span>
- <span data-ttu-id="cd2a3-148">Ultimo giorno</span><span class="sxs-lookup"><span data-stu-id="cd2a3-148">LastDay</span></span>

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

### <span data-ttu-id="cd2a3-149">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="cd2a3-149">-DaysOfMonth</span></span>
<span data-ttu-id="cd2a3-150">Specifica un elenco di giorni del mese per la pianificazione mensile.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-150">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="cd2a3-151">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="cd2a3-151">-DaysOfWeek</span></span>
<span data-ttu-id="cd2a3-152">Specifica un elenco di giorni della settimana per la pianificazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-152">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="cd2a3-153">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd2a3-153">-DefaultProfile</span></span>
<span data-ttu-id="cd2a3-154">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="cd2a3-154">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd2a3-155">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="cd2a3-155">-Description</span></span>
<span data-ttu-id="cd2a3-156">Specifica una descrizione della programmazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-156">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="cd2a3-157">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="cd2a3-157">-ExpiryTime</span></span>
<span data-ttu-id="cd2a3-158">Specifica la data di scadenza di una pianificazione come **oggetto DateTime Schedule.**</span><span class="sxs-lookup"><span data-stu-id="cd2a3-158">Specifies the expiry time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="cd2a3-159">È possibile specificare una stringa che può essere convertita in **un valore DateTime Offset valido.**</span><span class="sxs-lookup"><span data-stu-id="cd2a3-159">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="cd2a3-160">-ForUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd2a3-160">-ForUpdateConfiguration</span></span>
<span data-ttu-id="cd2a3-161">Indica che l'oggetto pianificazione verrà usato per la pianificazione di una configurazione di aggiornamento software</span><span class="sxs-lookup"><span data-stu-id="cd2a3-161">Indicates that this schedule object will be used for scheduling a software update configuration</span></span>

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

### <span data-ttu-id="cd2a3-162">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="cd2a3-162">-HourInterval</span></span>
<span data-ttu-id="cd2a3-163">Specifica un intervallo, in ore, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-163">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="cd2a3-164">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="cd2a3-164">-MonthInterval</span></span>
<span data-ttu-id="cd2a3-165">Specifica un intervallo, in mesi, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-165">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="cd2a3-166">-Name</span><span class="sxs-lookup"><span data-stu-id="cd2a3-166">-Name</span></span>
<span data-ttu-id="cd2a3-167">Specifica un nome per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-167">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="cd2a3-168">-OneTime</span><span class="sxs-lookup"><span data-stu-id="cd2a3-168">-OneTime</span></span>
<span data-ttu-id="cd2a3-169">Specifica che il cmdlet crea una pianificazione una sola volta.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-169">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="cd2a3-170">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd2a3-170">-ResourceGroupName</span></span>
<span data-ttu-id="cd2a3-171">Specifica il nome di un gruppo di risorse per cui questo cmdlet crea una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-171">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="cd2a3-172">-StartTime</span><span class="sxs-lookup"><span data-stu-id="cd2a3-172">-StartTime</span></span>
<span data-ttu-id="cd2a3-173">Specifica l'ora di inizio di una pianificazione come **oggetto DateTime Schedule.**</span><span class="sxs-lookup"><span data-stu-id="cd2a3-173">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="cd2a3-174">È possibile specificare una stringa che può essere convertita in **un valore DateTime Offset valido.**</span><span class="sxs-lookup"><span data-stu-id="cd2a3-174">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="cd2a3-175">Se si specifica il parametro *TimeZone,* l'offset verrà ignorato e verrà usato il fuso orario specificato.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-175">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="cd2a3-176">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="cd2a3-176">-TimeZone</span></span>
<span data-ttu-id="cd2a3-177">Specifica il fuso orario per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-177">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="cd2a3-178">Può essere l'ID IANA o l'ID del fuso orario di Windows.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-178">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="cd2a3-179">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="cd2a3-179">-WeekInterval</span></span>
<span data-ttu-id="cd2a3-180">Specifica un intervallo, in settimane, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-180">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="cd2a3-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd2a3-181">CommonParameters</span></span>
<span data-ttu-id="cd2a3-182">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd2a3-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd2a3-183">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd2a3-183">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd2a3-184">INPUT</span><span class="sxs-lookup"><span data-stu-id="cd2a3-184">INPUTS</span></span>

### <span data-ttu-id="cd2a3-185">System.String</span><span class="sxs-lookup"><span data-stu-id="cd2a3-185">System.String</span></span>

### <span data-ttu-id="cd2a3-186">System.DateTime Offset</span><span class="sxs-lookup"><span data-stu-id="cd2a3-186">System.DateTimeOffset</span></span>

### <span data-ttu-id="cd2a3-187">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="cd2a3-187">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="cd2a3-188">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cd2a3-188">OUTPUTS</span></span>

### <span data-ttu-id="cd2a3-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="cd2a3-189">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="cd2a3-190">NOTE</span><span class="sxs-lookup"><span data-stu-id="cd2a3-190">NOTES</span></span>

## <span data-ttu-id="cd2a3-191">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cd2a3-191">RELATED LINKS</span></span>

[<span data-ttu-id="cd2a3-192">Get-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd2a3-192">Get-AzAutomationSchedule</span></span>](./Get-AzAutomationSchedule.md)

[<span data-ttu-id="cd2a3-193">Remove-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd2a3-193">Remove-AzAutomationSchedule</span></span>](./Remove-AzAutomationSchedule.md)

[<span data-ttu-id="cd2a3-194">Set-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="cd2a3-194">Set-AzAutomationSchedule</span></span>](./Set-AzAutomationSchedule.md)


