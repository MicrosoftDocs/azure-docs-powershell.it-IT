---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: D28DD808-E8EF-4C71-A353-8BF1E458DF6F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9fcae4a0232331a020a716b3f7284b8f6dfc3212
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029681"
---
# <span data-ttu-id="0ccf6-101">New-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-101">New-AzureAutomationSchedule</span></span>

## <span data-ttu-id="0ccf6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ccf6-102">SYNOPSIS</span></span>

<span data-ttu-id="0ccf6-103">Crea una programmazione di automazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-103">Creates an Automation schedule.</span></span>

## <span data-ttu-id="0ccf6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ccf6-104">SYNTAX</span></span>

### <span data-ttu-id="0ccf6-105">ByDaily (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ccf6-105">ByDaily (Default)</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -DayInterval <Byte> -AutomationAccountName <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ccf6-106">ByOneTime</span><span class="sxs-lookup"><span data-stu-id="0ccf6-106">ByOneTime</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>] [-OneTime]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0ccf6-107">ByHourly</span><span class="sxs-lookup"><span data-stu-id="0ccf6-107">ByHourly</span></span>
```
New-AzureAutomationSchedule -Name <String> -StartTime <DateTimeOffset> [-Description <String>]
 [-ExpiryTime <DateTimeOffset>] -HourInterval <Byte> -AutomationAccountName <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0ccf6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ccf6-108">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="0ccf6-109">Il cmdlet **New-AzureAutomationSchedule** crea una pianificazione in Microsoft Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-109">The **New-AzureAutomationSchedule** cmdlet creates a schedule in Microsoft Azure Automation.</span></span>

## <span data-ttu-id="0ccf6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ccf6-110">EXAMPLES</span></span>

### <span data-ttu-id="0ccf6-111">Esempio 1: creare una pianificazione una tantum</span><span class="sxs-lookup"><span data-stu-id="0ccf6-111">Example 1: Create a one-time schedule</span></span>
```
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -StartTime "23:00" -OneTime
```

<span data-ttu-id="0ccf6-112">Il comando seguente crea una programmazione che viene eseguita una volta alla data corrente alle 11:00 PM.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-112">The following command creates a schedule that runs one time on the current date at 11:00 PM.</span></span>

### <span data-ttu-id="0ccf6-113">Esempio 2: creare una pianificazione ricorrente</span><span class="sxs-lookup"><span data-stu-id="0ccf6-113">Example 2: Create a recurring schedule</span></span>
```
PS C:\> $StartTime = Get-Date "13:00:00"
PS C:\> $EndTime = $StartTime.AddYears(1)
PS C:\> New-AzureAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule02" -StartTime $StartTime -ExpiryTime $EndTime -DailyInterval 1
```

<span data-ttu-id="0ccf6-114">I comandi seguenti creano una nuova pianificazione che viene eseguita a 1:00 PM ogni giorno per un anno a partire dal giorno corrente.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-114">The following commands create a new schedule that runs at 1:00 PM every day for one year starting on the current day.</span></span>

## <span data-ttu-id="0ccf6-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ccf6-115">PARAMETERS</span></span>

### <span data-ttu-id="0ccf6-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="0ccf6-116">-AutomationAccountName</span></span>
<span data-ttu-id="0ccf6-117">Specifica il nome di un account di automazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-117">Specifies the name of an Automation account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-118">-DayInterval</span><span class="sxs-lookup"><span data-stu-id="0ccf6-118">-DayInterval</span></span>
<span data-ttu-id="0ccf6-119">Specifica un intervallo, in giorni, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-119">Specifies an interval, in days, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByDaily
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-120">-Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ccf6-120">-Description</span></span>
<span data-ttu-id="0ccf6-121">Specifica una descrizione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-121">Specifies a description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-122">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="0ccf6-122">-ExpiryTime</span></span>
<span data-ttu-id="0ccf6-123">Specifica il periodo di scadenza di una programmazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-123">Specifies the expiry time of a schedule.</span></span>
<span data-ttu-id="0ccf6-124">Può essere fornita una stringa se può essere convertita in un valore **DateTime** valido.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-124">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: ByDaily, ByHourly
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-125">-HourInterval</span><span class="sxs-lookup"><span data-stu-id="0ccf6-125">-HourInterval</span></span>
<span data-ttu-id="0ccf6-126">Specifica un intervallo, in ore, per la programmazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-126">Specifies an interval, in hours, for the schedule.</span></span>

```yaml
Type: Byte
Parameter Sets: ByHourly
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ccf6-127">-Name</span></span>
<span data-ttu-id="0ccf6-128">Specifica un nome per la pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-128">Specifies a name for the schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-129">-Una tantum</span><span class="sxs-lookup"><span data-stu-id="0ccf6-129">-OneTime</span></span>
<span data-ttu-id="0ccf6-130">Indica che questa operazione crea una pianificazione una tantum.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-130">Indicates that this operation creates a one-time schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByOneTime
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-131">-Profile</span><span class="sxs-lookup"><span data-stu-id="0ccf6-131">-Profile</span></span>
<span data-ttu-id="0ccf6-132">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0ccf6-133">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-134">-StartTime</span><span class="sxs-lookup"><span data-stu-id="0ccf6-134">-StartTime</span></span>
<span data-ttu-id="0ccf6-135">Specifica l'ora di inizio di una pianificazione.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-135">Specifies the start time of a schedule.</span></span>
<span data-ttu-id="0ccf6-136">Può essere fornita una stringa se può essere convertita in un valore **DateTime** valido.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-136">A string can be provided if it can be converted to a valid **DateTime**.</span></span>

```yaml
Type: DateTimeOffset
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ccf6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ccf6-137">CommonParameters</span></span>
<span data-ttu-id="0ccf6-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ccf6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ccf6-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ccf6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ccf6-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ccf6-140">INPUTS</span></span>

## <span data-ttu-id="0ccf6-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ccf6-141">OUTPUTS</span></span>

### <span data-ttu-id="0ccf6-142">Microsoft. Azure. Commands. Automation. Model. Schedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-142">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

## <span data-ttu-id="0ccf6-143">Note</span><span class="sxs-lookup"><span data-stu-id="0ccf6-143">NOTES</span></span>

## <span data-ttu-id="0ccf6-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ccf6-144">RELATED LINKS</span></span>

[<span data-ttu-id="0ccf6-145">Get-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-145">Get-AzureAutomationSchedule</span></span>](./Get-AzureAutomationSchedule.md)

[<span data-ttu-id="0ccf6-146">Remove-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-146">Remove-AzureAutomationSchedule</span></span>](./Remove-AzureAutomationSchedule.md)

[<span data-ttu-id="0ccf6-147">Set-AzureAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="0ccf6-147">Set-AzureAutomationSchedule</span></span>](./Set-AzureAutomationSchedule.md)


