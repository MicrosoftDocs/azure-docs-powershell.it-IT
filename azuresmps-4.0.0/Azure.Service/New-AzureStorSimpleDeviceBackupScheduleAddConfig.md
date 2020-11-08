---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: EE7EC812-640B-4672-B23C-673F912F0EDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 945d06ddc1be6d2b0864b0421a5a087e14d98218
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023486"
---
# <span data-ttu-id="57a2e-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="57a2e-101">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>

## <span data-ttu-id="57a2e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="57a2e-102">SYNOPSIS</span></span>
<span data-ttu-id="57a2e-103">Crea un oggetto di configurazione della pianificazione di backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-103">Creates a backup schedule configuration object.</span></span>

## <span data-ttu-id="57a2e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="57a2e-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] -Enabled <Boolean>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="57a2e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57a2e-105">DESCRIPTION</span></span>
<span data-ttu-id="57a2e-106">Il cmdlet **New-AzureStorSimpleDeviceBackupScheduleAddConfig** crea un oggetto di configurazione **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="57a2e-106">The **New-AzureStorSimpleDeviceBackupScheduleAddConfig** cmdlet creates a **BackupScheduleBase** configuration object.</span></span>
<span data-ttu-id="57a2e-107">Usa questo oggetto Configuration per creare nuovi criteri di backup usando il cmdlet **New-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="57a2e-107">Use this configuration object to create new backup policy by using the **New-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="57a2e-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="57a2e-108">EXAMPLES</span></span>

### <span data-ttu-id="57a2e-109">Esempio 1: creare un oggetto di configurazione di backup</span><span class="sxs-lookup"><span data-stu-id="57a2e-109">Example 1: Create a backup configuration object</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleAddConfig -BackupType CloudSnapshot -RecurrenceType Daily -RecurrenceValue 1 -RetentionCount 100 -Enabled $True
VERBOSE: ClientRequestId: 426a79ee-fed3-4d3d-9123-e371f83222b3_PS


BackupType     : CloudSnapshot
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 100
StartTime      : 2014-12-16T00:37:19+05:30
Status         : Enabled
```

<span data-ttu-id="57a2e-110">Questo comando crea un oggetto di base per la pianificazione di backup per i backup snapshot cloud.</span><span class="sxs-lookup"><span data-stu-id="57a2e-110">This command creates a backup schedule base object for cloud snapshot backups.</span></span>
<span data-ttu-id="57a2e-111">Il backup viene eseguito ogni giorno e i backup vengono conservati per 100 giorni.</span><span class="sxs-lookup"><span data-stu-id="57a2e-111">The backup occurs every day, and the backups are kept for 100 days.</span></span>
<span data-ttu-id="57a2e-112">Questa programmazione viene abilitata dall'ora predefinita, ovvero l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="57a2e-112">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="57a2e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="57a2e-113">PARAMETERS</span></span>

### <span data-ttu-id="57a2e-114">-BackupType</span><span class="sxs-lookup"><span data-stu-id="57a2e-114">-BackupType</span></span>
<span data-ttu-id="57a2e-115">Specifica il tipo di backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-115">Specifies the backup type.</span></span>
<span data-ttu-id="57a2e-116">I valori validi sono: LocalSnapshot e CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="57a2e-116">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a2e-117">-Enabled</span><span class="sxs-lookup"><span data-stu-id="57a2e-117">-Enabled</span></span>
<span data-ttu-id="57a2e-118">Indica se abilitare la pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-118">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a2e-119">-Profile</span><span class="sxs-lookup"><span data-stu-id="57a2e-119">-Profile</span></span>
<span data-ttu-id="57a2e-120">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="57a2e-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="57a2e-121">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="57a2e-121">-RecurrenceType</span></span>
<span data-ttu-id="57a2e-122">Specifica il tipo di ricorrenza per la pianificazione di backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-122">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="57a2e-123">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="57a2e-123">Valid values are:</span></span> 

- <span data-ttu-id="57a2e-124">Minuti</span><span class="sxs-lookup"><span data-stu-id="57a2e-124">Minutes</span></span>
- <span data-ttu-id="57a2e-125">Oraria</span><span class="sxs-lookup"><span data-stu-id="57a2e-125">Hourly</span></span>
- <span data-ttu-id="57a2e-126">Quotidiana</span><span class="sxs-lookup"><span data-stu-id="57a2e-126">Daily</span></span>
- <span data-ttu-id="57a2e-127">Settimanale</span><span class="sxs-lookup"><span data-stu-id="57a2e-127">Weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a2e-128">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="57a2e-128">-RecurrenceValue</span></span>
<span data-ttu-id="57a2e-129">Specifica la frequenza con cui eseguire un backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-129">Specifies how often to make a backup.</span></span>
<span data-ttu-id="57a2e-130">Questo parametro usa l'unità specificata dal parametro *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="57a2e-130">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a2e-131">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="57a2e-131">-RetentionCount</span></span>
<span data-ttu-id="57a2e-132">Specifica il numero di giorni per conservare un backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-132">Specifies the number of days to keep a backup.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a2e-133">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="57a2e-133">-StartFromDateTime</span></span>
<span data-ttu-id="57a2e-134">Specifica la data da cui iniziare a eseguire i backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-134">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="57a2e-135">Il valore predefinito è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="57a2e-135">The default value is the current time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57a2e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57a2e-136">CommonParameters</span></span>
<span data-ttu-id="57a2e-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="57a2e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57a2e-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="57a2e-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57a2e-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="57a2e-139">INPUTS</span></span>

### <span data-ttu-id="57a2e-140">Nessuno</span><span class="sxs-lookup"><span data-stu-id="57a2e-140">None</span></span>

## <span data-ttu-id="57a2e-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="57a2e-141">OUTPUTS</span></span>

### <span data-ttu-id="57a2e-142">BackupScheduleBase</span><span class="sxs-lookup"><span data-stu-id="57a2e-142">BackupScheduleBase</span></span>
<span data-ttu-id="57a2e-143">Questo cmdlet restituisce un oggetto **BackupScheduleBase** .</span><span class="sxs-lookup"><span data-stu-id="57a2e-143">This cmdlet returns a **BackupScheduleBase** object.</span></span>
<span data-ttu-id="57a2e-144">Usare un **BackupScheduleBase** per creare nuovi criteri di backup.</span><span class="sxs-lookup"><span data-stu-id="57a2e-144">Use a **BackupScheduleBase** to construct new backup policy.</span></span>

## <span data-ttu-id="57a2e-145">Note</span><span class="sxs-lookup"><span data-stu-id="57a2e-145">NOTES</span></span>

## <span data-ttu-id="57a2e-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="57a2e-146">RELATED LINKS</span></span>

[<span data-ttu-id="57a2e-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="57a2e-147">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleUpdateConfig.md)

[<span data-ttu-id="57a2e-148">New-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="57a2e-148">New-AzureStorSimpleDeviceBackupPolicy</span></span>](./New-AzureStorSimpleDeviceBackupPolicy.md)


