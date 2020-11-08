---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 22C6845E-D7BD-4BBC-B373-394A23488A94
online version: ''
schema: 2.0.0
ms.openlocfilehash: a0695dc42d9c540e30ddf9ac55bd6fc136c84bff
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94023482"
---
# <span data-ttu-id="7677a-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span><span class="sxs-lookup"><span data-stu-id="7677a-101">New-AzureStorSimpleDeviceBackupScheduleUpdateConfig</span></span>

## <span data-ttu-id="7677a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7677a-102">SYNOPSIS</span></span>
<span data-ttu-id="7677a-103">Crea un oggetto di configurazione dell'aggiornamento della pianificazione di backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-103">Creates a backup schedule update configuration object.</span></span>

## <span data-ttu-id="7677a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7677a-104">SYNTAX</span></span>

```
New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id <String> -BackupType <String> -RecurrenceType <String>
 -RecurrenceValue <Int32> -RetentionCount <Int64> [-StartFromDateTime <String>] [-Enabled <Boolean>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7677a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7677a-105">DESCRIPTION</span></span>
<span data-ttu-id="7677a-106">Il cmdlet **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** crea un oggetto di configurazione **BackupScheduleUpdateRequest** .</span><span class="sxs-lookup"><span data-stu-id="7677a-106">The **New-AzureStorSimpleDeviceBackupScheduleUpdateConfig** cmdlet creates a **BackupScheduleUpdateRequest** configuration object.</span></span>
<span data-ttu-id="7677a-107">Usa questo oggetto Configuration per aggiornare i criteri di backup usando il cmdlet **set-AzureStorSimpleDeviceBackupPolicy** .</span><span class="sxs-lookup"><span data-stu-id="7677a-107">Use this configuration object to update a backup policy by using the **Set-AzureStorSimpleDeviceBackupPolicy** cmdlet.</span></span>

## <span data-ttu-id="7677a-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7677a-108">EXAMPLES</span></span>

### <span data-ttu-id="7677a-109">Esempio 1: creare una richiesta di aggiornamento della pianificazione</span><span class="sxs-lookup"><span data-stu-id="7677a-109">Example 1: Create a schedule update request</span></span>
```
PS C:\>New-AzureStorSimpleDeviceBackupScheduleUpdateConfig -Id "147f734d-a31a-4473-8501-6ba38be2cb30" -BackupType CloudSnapshot -RecurrenceType Hourly -RecurrenceValue 1 -RetentionCount 50 -Enabled $True
VERBOSE: ClientRequestId: ef346641-54b4-4273-8898-7f863e7c5b7e_PS


BackupType     : CloudSnapshot
Id             : 147f734d-a31a-4473-8501-6ba38be2cb30
Recurrence     : Microsoft.WindowsAzure.Management.StorSimple.Models.ScheduleRecurrence
RetentionCount : 50
StartTime      : 2014-12-16T00:39:32+05:30
Status         : Enabled
```

<span data-ttu-id="7677a-110">Questo comando crea una richiesta di aggiornamento della pianificazione di backup per la pianificazione con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="7677a-110">This command creates a backup schedule update request for the schedule that has the specified ID.</span></span>
<span data-ttu-id="7677a-111">La richiesta consiste nell'eseguire la pianificazione di un backup snapshot del cloud che viene ripresentato ogni ora.</span><span class="sxs-lookup"><span data-stu-id="7677a-111">The request is to make the schedule a cloud snapshot backup that recurs every hour.</span></span>
<span data-ttu-id="7677a-112">I backup vengono conservati per 50 giorni.</span><span class="sxs-lookup"><span data-stu-id="7677a-112">The backups are kept for 50 days.</span></span>
<span data-ttu-id="7677a-113">Questa programmazione viene abilitata dall'ora predefinita, ovvero l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="7677a-113">This schedule is enabled from the default time, which is the current time.</span></span>

## <span data-ttu-id="7677a-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7677a-114">PARAMETERS</span></span>

### <span data-ttu-id="7677a-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="7677a-115">-BackupType</span></span>
<span data-ttu-id="7677a-116">Specifica il tipo di backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-116">Specifies the backup type.</span></span>
<span data-ttu-id="7677a-117">I valori validi sono: LocalSnapshot e CloudSnapshot.</span><span class="sxs-lookup"><span data-stu-id="7677a-117">Valid values are: LocalSnapshot and CloudSnapshot.</span></span>

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

### <span data-ttu-id="7677a-118">-Enabled</span><span class="sxs-lookup"><span data-stu-id="7677a-118">-Enabled</span></span>
<span data-ttu-id="7677a-119">Indica se abilitare la pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-119">Indicates whether to enable the backup schedule.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7677a-120">-ID</span><span class="sxs-lookup"><span data-stu-id="7677a-120">-Id</span></span>
<span data-ttu-id="7677a-121">Specifica l'ID istanza della pianificazione di backup da aggiornare.</span><span class="sxs-lookup"><span data-stu-id="7677a-121">Specifies the instance ID of the backup schedule to update.</span></span>

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

### <span data-ttu-id="7677a-122">-Profile</span><span class="sxs-lookup"><span data-stu-id="7677a-122">-Profile</span></span>
<span data-ttu-id="7677a-123">Specifica un profilo Azure.</span><span class="sxs-lookup"><span data-stu-id="7677a-123">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7677a-124">-RecurrenceType</span><span class="sxs-lookup"><span data-stu-id="7677a-124">-RecurrenceType</span></span>
<span data-ttu-id="7677a-125">Specifica il tipo di ricorrenza per la pianificazione di backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-125">Specifies the type of recurrence for this backup schedule.</span></span>
<span data-ttu-id="7677a-126">I valori validi sono:</span><span class="sxs-lookup"><span data-stu-id="7677a-126">Valid values are:</span></span> 

- <span data-ttu-id="7677a-127">Minuti</span><span class="sxs-lookup"><span data-stu-id="7677a-127">Minutes</span></span>
- <span data-ttu-id="7677a-128">Oraria</span><span class="sxs-lookup"><span data-stu-id="7677a-128">Hourly</span></span>
- <span data-ttu-id="7677a-129">Quotidiana</span><span class="sxs-lookup"><span data-stu-id="7677a-129">Daily</span></span>
- <span data-ttu-id="7677a-130">Settimanale</span><span class="sxs-lookup"><span data-stu-id="7677a-130">Weekly</span></span>

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

### <span data-ttu-id="7677a-131">-RecurrenceValue</span><span class="sxs-lookup"><span data-stu-id="7677a-131">-RecurrenceValue</span></span>
<span data-ttu-id="7677a-132">Specifica la frequenza con cui eseguire un backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-132">Specifies how often to make a backup.</span></span>
<span data-ttu-id="7677a-133">Questo parametro usa l'unità specificata dal parametro *RecurrenceType* .</span><span class="sxs-lookup"><span data-stu-id="7677a-133">This parameter uses the unit specified by the *RecurrenceType* parameter.</span></span>

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

### <span data-ttu-id="7677a-134">-RetentionCount</span><span class="sxs-lookup"><span data-stu-id="7677a-134">-RetentionCount</span></span>
<span data-ttu-id="7677a-135">Specifica il numero di giorni per conservare un backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-135">Specifies the number of days to keep a backup.</span></span>

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

### <span data-ttu-id="7677a-136">-StartFromDateTime</span><span class="sxs-lookup"><span data-stu-id="7677a-136">-StartFromDateTime</span></span>
<span data-ttu-id="7677a-137">Specifica la data da cui iniziare a eseguire i backup.</span><span class="sxs-lookup"><span data-stu-id="7677a-137">Specifies the date from which to start making backups.</span></span>
<span data-ttu-id="7677a-138">Il valore predefinito è l'ora corrente.</span><span class="sxs-lookup"><span data-stu-id="7677a-138">The default value is the current time.</span></span>

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

### <span data-ttu-id="7677a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7677a-139">CommonParameters</span></span>
<span data-ttu-id="7677a-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7677a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7677a-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7677a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7677a-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7677a-142">INPUTS</span></span>

### <span data-ttu-id="7677a-143">Nessuno</span><span class="sxs-lookup"><span data-stu-id="7677a-143">None</span></span>

## <span data-ttu-id="7677a-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7677a-144">OUTPUTS</span></span>

### <span data-ttu-id="7677a-145">BackupScheduleUpdateRequest</span><span class="sxs-lookup"><span data-stu-id="7677a-145">BackupScheduleUpdateRequest</span></span>
<span data-ttu-id="7677a-146">Questo cmdlet restituisce un oggetto **BackupScheduleUpdateRequest** che contiene informazioni sulle pianificazioni di backup aggiornate.</span><span class="sxs-lookup"><span data-stu-id="7677a-146">This cmdlet returns a **BackupScheduleUpdateRequest** object that contains information about updated backup schedules.</span></span>

## <span data-ttu-id="7677a-147">Note</span><span class="sxs-lookup"><span data-stu-id="7677a-147">NOTES</span></span>

## <span data-ttu-id="7677a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7677a-148">RELATED LINKS</span></span>

[<span data-ttu-id="7677a-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span><span class="sxs-lookup"><span data-stu-id="7677a-149">New-AzureStorSimpleDeviceBackupScheduleAddConfig</span></span>](./New-AzureStorSimpleDeviceBackupScheduleAddConfig.md)

[<span data-ttu-id="7677a-150">Set-AzureStorSimpleDeviceBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="7677a-150">Set-AzureStorSimpleDeviceBackupPolicy</span></span>](./Set-AzureStorSimpleDeviceBackupPolicy.md)


