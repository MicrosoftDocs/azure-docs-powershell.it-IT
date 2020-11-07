---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: CB621890-EF8A-4F14-8F18-D8806E624DAB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationSchedule.md
ms.openlocfilehash: d82e63d21e18b7fb75282da9ac12be7644b0535a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686347"
---
# <span data-ttu-id="ae93b-101">New-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ae93b-101">New-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="ae93b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae93b-102">SYNOPSIS</span></span>
<span data-ttu-id="ae93b-103">Crea una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-103">Creates an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae93b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae93b-104">SYNTAX</span></span>

### <span data-ttu-id="ae93b-105">ByDaily (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae93b-105">ByDaily (Default)</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae93b-106">ByWeekly</span><span class="sxs-lookup"><span data-stu-id="ae93b-106">ByWeekly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfWeek <DayOfWeek[]>] [-ExpiryTime <DateTimeOffset>] -WeekInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae93b-107">ByMonthlyDaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="ae93b-107">ByMonthlyDaysOfMonth</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DaysOfMonth <DaysOfMonth[]>] [-ExpiryTime <DateTimeOffset>] -MonthInterval <Byte> [-TimeZone <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae93b-108">ByMonthlyDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ae93b-108">ByMonthlyDayOfWeek</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-DayOfWeek <DayOfWeek>] [-DayOfWeekOccurrence <DayOfWeekOccurrence>] [-ExpiryTime <DateTimeOffset>]
 -MonthInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae93b-109">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="ae93b-109">ByOneTime</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>] [-OneTime]
 [-TimeZone <String>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae93b-110">ByHourly</span><span class="sxs-lookup"><span data-stu-id="ae93b-110">ByHourly</span></span>
```
New-AzureRmAutomationSchedule [-Name] <String> [-StartTime] <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> [-TimeZone <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae93b-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae93b-111">DESCRIPTION</span></span>
<span data-ttu-id="ae93b-112">Il cmdlet **New-AzureRmAutomationSchedule** crea una pianificazione in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="ae93b-112">The **New-AzureRmAutomationSchedule** cmdlet creates a schedule in Azure Automation.</span></span>

## <span data-ttu-id="ae93b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae93b-113">EXAMPLES</span></span>

### <span data-ttu-id="ae93b-114">Esempio 1: creare una pianificazione unica in ora locale</span><span class="sxs-lookup"><span data-stu-id="ae93b-114">Example 1: Create a one-time schedule in local time</span></span>
```
PS C:\>$TimeZone = ([System.TimeZoneInfo]::Local)Id
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime -ResourceGroupName "ResourceGroup01" -TimeZone $TimeZone
```

<span data-ttu-id="ae93b-115">Il primo comando ottiene l'ID del fuso orario dal sistema e lo archivia nella variabile $TimeZone.</span><span class="sxs-lookup"><span data-stu-id="ae93b-115">The first command gets the time zone ID from the system and stores it in the $TimeZone variable.</span></span>
<span data-ttu-id="ae93b-116">Il secondo comando crea una programmazione che viene eseguita una volta alla data corrente in 11:00 PM nel fuso orario specificato.</span><span class="sxs-lookup"><span data-stu-id="ae93b-116">The second command creates a schedule that runs one time on the current date at 11:00 PM in the specified time zone..</span></span>

### <span data-ttu-id="ae93b-117">Esempio 2: creare una pianificazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="ae93b-117">Example 2: Create a recurring schedule</span></span>
```
PS C:\>$StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1 -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ae93b-118">Il primo comando crea un oggetto Date usando il cmdlet **get-date** e quindi archivia l'oggetto nella variabile $StartDate.</span><span class="sxs-lookup"><span data-stu-id="ae93b-118">The first command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $StartDate variable.</span></span>
<span data-ttu-id="ae93b-119">Specificare un periodo di almeno cinque minuti per il futuro.</span><span class="sxs-lookup"><span data-stu-id="ae93b-119">Specify a time that is at least five minutes in the future.</span></span>

<span data-ttu-id="ae93b-120">Il secondo comando crea un oggetto Date usando il cmdlet **get-date** e quindi archivia l'oggetto nella variabile $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ae93b-120">The second command creates a date object by using the **Get-Date** cmdlet, and then stores the object in the $EndDate variable.</span></span>
<span data-ttu-id="ae93b-121">Il comando specifica un'ora futura.</span><span class="sxs-lookup"><span data-stu-id="ae93b-121">The command specifies a future time.</span></span>

<span data-ttu-id="ae93b-122">Il comando finale crea una programmazione giornaliera denominata Schedule01 per iniziare all'ora archiviata in $StartDate e scade all'ora archiviata in $EndDate.</span><span class="sxs-lookup"><span data-stu-id="ae93b-122">The final command creates a daily schedule named Schedule01 to begin at the time stored in $StartDate and expire at the time stored in $EndDate.</span></span>

## <span data-ttu-id="ae93b-123">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae93b-123">PARAMETERS</span></span>

### <span data-ttu-id="ae93b-124">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ae93b-124">-AutomationAccountName</span></span>
<span data-ttu-id="ae93b-125">Specifica il nome di un account di automazione per cui questo cmdlet crea una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-125">Specifies the name of an Automation account for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="ae93b-126">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="ae93b-126">-DayInterval</span></span>
<span data-ttu-id="ae93b-127">Specifica un intervallo, in giorni, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-127">Specifies an interval, in days, for the schedule.</span></span>
<span data-ttu-id="ae93b-128">Se non specifichi questo parametro e non *specifichi il parametro una volta* , il valore predefinito è uno (1).</span><span class="sxs-lookup"><span data-stu-id="ae93b-128">If you do not specify this parameter, and you do not specify the *OneTime* parameter, the default value is one (1).</span></span>

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

### <span data-ttu-id="ae93b-129">-DayOfWeek</span><span class="sxs-lookup"><span data-stu-id="ae93b-129">-DayOfWeek</span></span>
<span data-ttu-id="ae93b-130">Specifica un elenco di giorni della settimana per la programmazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="ae93b-130">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="ae93b-131">-DayOfWeekOccurrence</span><span class="sxs-lookup"><span data-stu-id="ae93b-131">-DayOfWeekOccurrence</span></span>
<span data-ttu-id="ae93b-132">Specifica l'occorrenza della settimana entro il mese in cui viene eseguita la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-132">Specifies the occurrence of the week within the month that the schedule runs.</span></span>
<span data-ttu-id="ae93b-133">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="ae93b-133">psdx_paramvalues</span></span>

- <span data-ttu-id="ae93b-134">1</span><span class="sxs-lookup"><span data-stu-id="ae93b-134">1</span></span>
- <span data-ttu-id="ae93b-135">2</span><span class="sxs-lookup"><span data-stu-id="ae93b-135">2</span></span>
- <span data-ttu-id="ae93b-136">3</span><span class="sxs-lookup"><span data-stu-id="ae93b-136">3</span></span>
- <span data-ttu-id="ae93b-137">4</span><span class="sxs-lookup"><span data-stu-id="ae93b-137">4</span></span>
- <span data-ttu-id="ae93b-138">-1</span><span class="sxs-lookup"><span data-stu-id="ae93b-138">-1</span></span>
- <span data-ttu-id="ae93b-139">Prima</span><span class="sxs-lookup"><span data-stu-id="ae93b-139">First</span></span>
- <span data-ttu-id="ae93b-140">Secondo</span><span class="sxs-lookup"><span data-stu-id="ae93b-140">Second</span></span>
- <span data-ttu-id="ae93b-141">Terze</span><span class="sxs-lookup"><span data-stu-id="ae93b-141">Third</span></span>
- <span data-ttu-id="ae93b-142">Quarto</span><span class="sxs-lookup"><span data-stu-id="ae93b-142">Fourth</span></span>
- <span data-ttu-id="ae93b-143">LastDay</span><span class="sxs-lookup"><span data-stu-id="ae93b-143">LastDay</span></span>

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

### <span data-ttu-id="ae93b-144">-DaysOfMonth</span><span class="sxs-lookup"><span data-stu-id="ae93b-144">-DaysOfMonth</span></span>
<span data-ttu-id="ae93b-145">Specifica un elenco di giorni del mese per la programmazione mensile.</span><span class="sxs-lookup"><span data-stu-id="ae93b-145">Specifies a list of days of the month for the monthly schedule.</span></span>

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

### <span data-ttu-id="ae93b-146">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="ae93b-146">-DaysOfWeek</span></span>
<span data-ttu-id="ae93b-147">Specifica un elenco di giorni della settimana per la programmazione settimanale.</span><span class="sxs-lookup"><span data-stu-id="ae93b-147">Specifies a list of days of the week for the weekly schedule.</span></span>

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

### <span data-ttu-id="ae93b-148">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae93b-148">-Description</span></span>
<span data-ttu-id="ae93b-149">Specifica una descrizione per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-149">Specifies a description for the schedule.</span></span>

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

### <span data-ttu-id="ae93b-150">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="ae93b-150">-ExpiryTime</span></span>
<span data-ttu-id="ae93b-151">Specifica il periodo di scadenza di una pianificazione come oggetto **DateTimeOffest** .</span><span class="sxs-lookup"><span data-stu-id="ae93b-151">Specifies the expiry time of a schedule as a **DateTimeOffest** object.</span></span>
<span data-ttu-id="ae93b-152">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="ae93b-152">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>

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

### <span data-ttu-id="ae93b-153">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="ae93b-153">-HourInterval</span></span>
<span data-ttu-id="ae93b-154">Specifica un intervallo, in ore, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-154">Specifies an interval, in hours, for the schedule.</span></span>

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

### <span data-ttu-id="ae93b-155">-MonthInterval</span><span class="sxs-lookup"><span data-stu-id="ae93b-155">-MonthInterval</span></span>
<span data-ttu-id="ae93b-156">Specifica un intervallo, in mesi, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-156">Specifies an interval, in Months, for the schedule.</span></span>

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

### <span data-ttu-id="ae93b-157">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae93b-157">-Name</span></span>
<span data-ttu-id="ae93b-158">Specifica un nome per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-158">Specifies a name for the schedule.</span></span>

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

### <span data-ttu-id="ae93b-159">-Una tantum</span><span class="sxs-lookup"><span data-stu-id="ae93b-159">-OneTime</span></span>
<span data-ttu-id="ae93b-160">Specifica che il cmdlet crea una pianificazione una tantum.</span><span class="sxs-lookup"><span data-stu-id="ae93b-160">Specifies that the cmdlet creates a one-time schedule.</span></span>

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

### <span data-ttu-id="ae93b-161">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae93b-161">-ResourceGroupName</span></span>
<span data-ttu-id="ae93b-162">Specifica il nome di un gruppo di risorse per cui questo cmdlet crea una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-162">Specifies the name of a resource group for which this cmdlet creates a schedule.</span></span>

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

### <span data-ttu-id="ae93b-163">-StartTime</span><span class="sxs-lookup"><span data-stu-id="ae93b-163">-StartTime</span></span>
<span data-ttu-id="ae93b-164">Specifica l'ora di inizio di una pianificazione come oggetto **DateTimeOffset** .</span><span class="sxs-lookup"><span data-stu-id="ae93b-164">Specifies the start time of a schedule as a **DateTimeOffset** object.</span></span>
<span data-ttu-id="ae93b-165">Puoi specificare una stringa che può essere convertita in un valore **DateTimeOffset** valido.</span><span class="sxs-lookup"><span data-stu-id="ae93b-165">You can specify a string that can be converted to a valid **DateTimeOffset**.</span></span>
<span data-ttu-id="ae93b-166">.</span><span class="sxs-lookup"><span data-stu-id="ae93b-166">.</span></span> <span data-ttu-id="ae93b-167">Se viene specificato il parametro *TimeZone* , l'offset verrà ignorato e viene usato il fuso orario specificato.</span><span class="sxs-lookup"><span data-stu-id="ae93b-167">If the *TimeZone* parameter is specified, the offset will be ignored and the time zone specified is used.</span></span>

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

### <span data-ttu-id="ae93b-168">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="ae93b-168">-TimeZone</span></span>
<span data-ttu-id="ae93b-169">Specifica il fuso orario per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-169">Specifies the time zone for the schedule.</span></span>
<span data-ttu-id="ae93b-170">Questa stringa può essere l'ID IANA o l'ID del fuso orario di Windows.</span><span class="sxs-lookup"><span data-stu-id="ae93b-170">This string can be the IANA ID or the Windows Time Zone ID.</span></span>

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

### <span data-ttu-id="ae93b-171">-WeekInterval</span><span class="sxs-lookup"><span data-stu-id="ae93b-171">-WeekInterval</span></span>
<span data-ttu-id="ae93b-172">Specifica un intervallo, in settimane, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="ae93b-172">Specifies an interval, in weeks, for the schedule.</span></span>

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

### <span data-ttu-id="ae93b-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae93b-173">-DefaultProfile</span></span>
<span data-ttu-id="ae93b-174">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae93b-174">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae93b-175">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae93b-175">CommonParameters</span></span>
<span data-ttu-id="ae93b-176">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae93b-176">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae93b-177">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae93b-177">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae93b-178">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae93b-178">INPUTS</span></span>

## <span data-ttu-id="ae93b-179">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae93b-179">OUTPUTS</span></span>

### <span data-ttu-id="ae93b-180">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="ae93b-180">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="ae93b-181">Note</span><span class="sxs-lookup"><span data-stu-id="ae93b-181">NOTES</span></span>

## <span data-ttu-id="ae93b-182">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae93b-182">RELATED LINKS</span></span>

[<span data-ttu-id="ae93b-183">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ae93b-183">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ae93b-184">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ae93b-184">Remove-AzureRmAutomationSchedule</span></span>](./Remove-AzureRMAutomationSchedule.md)

[<span data-ttu-id="ae93b-185">Set-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="ae93b-185">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


