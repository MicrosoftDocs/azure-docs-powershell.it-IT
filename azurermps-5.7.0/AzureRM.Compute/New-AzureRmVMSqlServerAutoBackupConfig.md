---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508352"
---
# <span data-ttu-id="6cc46-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="6cc46-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="6cc46-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6cc46-102">SYNOPSIS</span></span>
<span data-ttu-id="6cc46-103">Crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6cc46-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cc46-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6cc46-104">SYNTAX</span></span>

### <span data-ttu-id="6cc46-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6cc46-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="6cc46-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="6cc46-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="6cc46-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6cc46-107">DESCRIPTION</span></span>
<span data-ttu-id="6cc46-108">Il cmdlet **New-AzureVMSqlServerAutoBackupConfig** crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6cc46-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="6cc46-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6cc46-109">EXAMPLES</span></span>

### <span data-ttu-id="6cc46-110">Esempio 1: creare una configurazione di backup automatica usando l'URI di archiviazione e la chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="6cc46-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="6cc46-111">Questo comando crea un oggetto di configurazione di backup automatico specificando l'URI di archiviazione e la chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="6cc46-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="6cc46-112">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="6cc46-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="6cc46-113">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="6cc46-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="6cc46-114">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="6cc46-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="6cc46-115">Esempio 2: creare una configurazione di backup automatica tramite il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="6cc46-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="6cc46-116">Il primo comando crea un contesto di archiviazione e lo archivia nella variabile $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="6cc46-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="6cc46-117">Per altre informazioni, vedere New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6cc46-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="6cc46-118">Il secondo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione in $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="6cc46-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="6cc46-119">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="6cc46-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="6cc46-120">Esempio 3: creare una configurazione di backup automatica tramite il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="6cc46-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="6cc46-121">Questo comando crea e archivia un oggetto di configurazione di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="6cc46-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="6cc46-122">Il comando specifica il contesto di archiviazione creato in un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="6cc46-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="6cc46-123">Il comando consente la crittografia con password.</span><span class="sxs-lookup"><span data-stu-id="6cc46-123">The command enables encryption with password.</span></span>
<span data-ttu-id="6cc46-124">La password è stata precedentemente archiviata come stringa sicura nella variabile $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="6cc46-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="6cc46-125">Per creare una stringa sicura, usa il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="6cc46-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="6cc46-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6cc46-126">PARAMETERS</span></span>

### <span data-ttu-id="6cc46-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="6cc46-127">-BackupScheduleType</span></span>
<span data-ttu-id="6cc46-128">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="6cc46-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="6cc46-129">-BackupSystemDbs</span></span>
<span data-ttu-id="6cc46-130">Database di sistema di backup</span><span class="sxs-lookup"><span data-stu-id="6cc46-130">Backup system databases</span></span>

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

### <span data-ttu-id="6cc46-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="6cc46-131">-CertificatePassword</span></span>
<span data-ttu-id="6cc46-132">Specifica una password per crittografare il certificato usato per eseguire backup crittografati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6cc46-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-133">-Enable</span><span class="sxs-lookup"><span data-stu-id="6cc46-133">-Enable</span></span>
<span data-ttu-id="6cc46-134">Indica che il backup automatizzato per la macchina virtuale di SQL Server è abilitato.</span><span class="sxs-lookup"><span data-stu-id="6cc46-134">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="6cc46-135">Se specifichi questo parametro, il backup automatizzato imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="6cc46-135">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="6cc46-136">In questo articolo vengono aggiornate le impostazioni di backup gestite per seguire questa programmazione.</span><span class="sxs-lookup"><span data-stu-id="6cc46-136">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-137">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="6cc46-137">-EnableEncryption</span></span>
<span data-ttu-id="6cc46-138">Indica che questo cmdlet Abilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="6cc46-138">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-139">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="6cc46-139">-FullBackupFrequency</span></span>
<span data-ttu-id="6cc46-140">Frequenza di backup completa di SQL Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="6cc46-140">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-141">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="6cc46-141">-FullBackupStartHour</span></span>
<span data-ttu-id="6cc46-142">Ora del giorno (0-23) quando il backup completo di SQL Server dovrebbe iniziare</span><span class="sxs-lookup"><span data-stu-id="6cc46-142">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="6cc46-143">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="6cc46-143">-FullBackupWindowInHours</span></span>
<span data-ttu-id="6cc46-144">Finestra backup completo di SQL Server in ore</span><span class="sxs-lookup"><span data-stu-id="6cc46-144">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="6cc46-145">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="6cc46-145">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="6cc46-146">Frequenza di backup del log di SQL Server, una volta ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="6cc46-146">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="6cc46-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cc46-147">-ResourceGroupName</span></span>
<span data-ttu-id="6cc46-148">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="6cc46-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-149">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="6cc46-149">-RetentionPeriodInDays</span></span>
<span data-ttu-id="6cc46-150">Specifica il numero di giorni per cui mantenere un backup.</span><span class="sxs-lookup"><span data-stu-id="6cc46-150">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-151">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="6cc46-151">-StorageContext</span></span>
<span data-ttu-id="6cc46-152">Specifica l'account di archiviazione che verrà usato per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="6cc46-152">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="6cc46-153">Per ottenere un oggetto **AzureStorageContext** , usa il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6cc46-153">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="6cc46-154">L'impostazione predefinita è l'account di archiviazione associato alla macchina virtuale di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6cc46-154">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cc46-155">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="6cc46-155">-StorageKey</span></span>
<span data-ttu-id="6cc46-156">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="6cc46-156">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="6cc46-157">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="6cc46-157">-StorageUri</span></span>
<span data-ttu-id="6cc46-158">Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="6cc46-158">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="6cc46-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cc46-159">CommonParameters</span></span>
<span data-ttu-id="6cc46-160">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cc46-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cc46-161">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cc46-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cc46-162">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6cc46-162">INPUTS</span></span>

### <span data-ttu-id="6cc46-163">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6cc46-163">None</span></span>
<span data-ttu-id="6cc46-164">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="6cc46-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cc46-165">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6cc46-165">OUTPUTS</span></span>

## <span data-ttu-id="6cc46-166">Note</span><span class="sxs-lookup"><span data-stu-id="6cc46-166">NOTES</span></span>

## <span data-ttu-id="6cc46-167">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6cc46-167">RELATED LINKS</span></span>

[<span data-ttu-id="6cc46-168">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="6cc46-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="6cc46-169">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6cc46-169">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


