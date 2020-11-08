---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/18/2020
ms.locfileid: "94029661"
---
# <span data-ttu-id="3b8fe-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="3b8fe-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="3b8fe-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b8fe-102">SYNOPSIS</span></span>
<span data-ttu-id="3b8fe-103">Crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="3b8fe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b8fe-104">SYNTAX</span></span>

### <span data-ttu-id="3b8fe-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3b8fe-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="3b8fe-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="3b8fe-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3b8fe-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b8fe-107">DESCRIPTION</span></span>
<span data-ttu-id="3b8fe-108">Il cmdlet **New-AzureVMSqlServerAutoBackupConfig** crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="3b8fe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b8fe-109">EXAMPLES</span></span>

### <span data-ttu-id="3b8fe-110">Esempio 1: creare una configurazione di backup automatico usando l'URI di archiviazione e la chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="3b8fe-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="3b8fe-111">Questo comando crea un oggetto di configurazione di backup automatico specificando l'URL di archiviazione e la chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="3b8fe-112">Esempio 2: creare una configurazione di backup automatico usando il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3b8fe-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="3b8fe-113">Questo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="3b8fe-114">Esempio 3: creare una configurazione di backup automatico usando il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="3b8fe-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="3b8fe-115">Questo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione e abilitando l'opzione di crittografia con la password.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="3b8fe-116">CertificatePassword ist archiviato nella variabile denominata $CertPasswd.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="3b8fe-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b8fe-117">PARAMETERS</span></span>

### <span data-ttu-id="3b8fe-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="3b8fe-118">-BackupScheduleType</span></span>
<span data-ttu-id="3b8fe-119">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="3b8fe-119">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="3b8fe-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="3b8fe-120">-BackupSystemDbs</span></span>
<span data-ttu-id="3b8fe-121">Database di sistema di backup</span><span class="sxs-lookup"><span data-stu-id="3b8fe-121">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="3b8fe-122">-CertificatePassword</span></span>
<span data-ttu-id="3b8fe-123">Specifica una password per crittografare il certificato usato per eseguire backup crittografati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="3b8fe-124">-Enable</span></span>
<span data-ttu-id="3b8fe-125">Indica che il backup automatizzato per la macchina virtuale di SQL Server è abilitato.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="3b8fe-126">Se si usa questo parametro, il backup automatizzato imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="3b8fe-127">In questo articolo vengono aggiornate le impostazioni di backup gestite per seguire questa programmazione.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="3b8fe-128">-EnableEncryption</span></span>
<span data-ttu-id="3b8fe-129">Indica che la crittografia è abilitata.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="3b8fe-130">-FullBackupFrequency</span></span>
<span data-ttu-id="3b8fe-131">Frequenza di backup completa di SQL Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="3b8fe-131">Sql Server Full Backup frequency, daily or week</span></span>

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

### <span data-ttu-id="3b8fe-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="3b8fe-132">-FullBackupStartHour</span></span>
<span data-ttu-id="3b8fe-133">Ora del giorno (0-23) quando il backup completo di SQL Server dovrebbe iniziare</span><span class="sxs-lookup"><span data-stu-id="3b8fe-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="3b8fe-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="3b8fe-135">Finestra backup completo di SQL Server in ore</span><span class="sxs-lookup"><span data-stu-id="3b8fe-135">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="3b8fe-136">-InformationAction</span></span>
<span data-ttu-id="3b8fe-137">Specifica il modo in cui questo cmdlet risponde a un evento informativo.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3b8fe-138">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="3b8fe-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3b8fe-139">Continuare</span><span class="sxs-lookup"><span data-stu-id="3b8fe-139">Continue</span></span>
- <span data-ttu-id="3b8fe-140">Ignora</span><span class="sxs-lookup"><span data-stu-id="3b8fe-140">Ignore</span></span>
- <span data-ttu-id="3b8fe-141">Informarsi</span><span class="sxs-lookup"><span data-stu-id="3b8fe-141">Inquire</span></span>
- <span data-ttu-id="3b8fe-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3b8fe-142">SilentlyContinue</span></span>
- <span data-ttu-id="3b8fe-143">Stop</span><span class="sxs-lookup"><span data-stu-id="3b8fe-143">Stop</span></span>
- <span data-ttu-id="3b8fe-144">Sospensione</span><span class="sxs-lookup"><span data-stu-id="3b8fe-144">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3b8fe-145">-InformationVariable</span></span>
<span data-ttu-id="3b8fe-146">Specifica una variabile di informazioni.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-146">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="3b8fe-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="3b8fe-148">Frequenza di backup del log di SQL Server, una volta ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="3b8fe-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-149">-Profile</span><span class="sxs-lookup"><span data-stu-id="3b8fe-149">-Profile</span></span>
<span data-ttu-id="3b8fe-150">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3b8fe-151">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3b8fe-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="3b8fe-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="3b8fe-153">Specifica la lunghezza del periodo di conservazione in giorni.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="3b8fe-154">-StorageContext</span></span>
<span data-ttu-id="3b8fe-155">Specifica l'account di archiviazione da usare per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="3b8fe-156">Il valore predefinito è l'account di archiviazione associato alla macchina virtuale di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="3b8fe-157">-StorageKey</span></span>
<span data-ttu-id="3b8fe-158">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="3b8fe-159">-StorageUri</span></span>
<span data-ttu-id="3b8fe-160">Specifica un URI per l'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-160">Specifies a URI to the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b8fe-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b8fe-161">CommonParameters</span></span>
<span data-ttu-id="3b8fe-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b8fe-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b8fe-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b8fe-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b8fe-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b8fe-164">INPUTS</span></span>

## <span data-ttu-id="3b8fe-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b8fe-165">OUTPUTS</span></span>

## <span data-ttu-id="3b8fe-166">Note</span><span class="sxs-lookup"><span data-stu-id="3b8fe-166">NOTES</span></span>

## <span data-ttu-id="3b8fe-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b8fe-167">RELATED LINKS</span></span>

[<span data-ttu-id="3b8fe-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="3b8fe-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


