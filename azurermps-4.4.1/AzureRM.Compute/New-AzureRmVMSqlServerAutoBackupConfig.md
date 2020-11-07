---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688360"
---
# <span data-ttu-id="1b209-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="1b209-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="1b209-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b209-102">SYNOPSIS</span></span>
<span data-ttu-id="1b209-103">Crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b209-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b209-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b209-104">SYNTAX</span></span>

### <span data-ttu-id="1b209-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b209-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="1b209-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="1b209-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="1b209-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b209-107">DESCRIPTION</span></span>
<span data-ttu-id="1b209-108">Il cmdlet **New-AzureVMSqlServerAutoBackupConfig** crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b209-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="1b209-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b209-109">EXAMPLES</span></span>

### <span data-ttu-id="1b209-110">Esempio 1: creare una configurazione di backup automatica usando l'URI di archiviazione e la chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="1b209-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="1b209-111">Questo comando crea un oggetto di configurazione di backup automatico specificando l'URI di archiviazione e la chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="1b209-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="1b209-112">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="1b209-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="1b209-113">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="1b209-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="1b209-114">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="1b209-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="1b209-115">Esempio 2: creare una configurazione di backup automatica tramite il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1b209-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="1b209-116">Il primo comando crea un contesto di archiviazione e lo archivia nella variabile $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b209-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="1b209-117">Per altre informazioni, vedere New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b209-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="1b209-118">Il secondo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione in $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b209-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="1b209-119">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="1b209-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="1b209-120">Esempio 3: creare una configurazione di backup automatica tramite il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="1b209-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="1b209-121">Questo comando crea e archivia un oggetto di configurazione di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="1b209-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="1b209-122">Il comando specifica il contesto di archiviazione creato in un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="1b209-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="1b209-123">Il comando consente la crittografia con password.</span><span class="sxs-lookup"><span data-stu-id="1b209-123">The command enables encryption with password.</span></span>
<span data-ttu-id="1b209-124">La password è stata precedentemente archiviata come stringa sicura nella variabile $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="1b209-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="1b209-125">Per creare una stringa sicura, usa il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="1b209-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="1b209-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b209-126">PARAMETERS</span></span>

### <span data-ttu-id="1b209-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="1b209-127">-Enable</span></span>
<span data-ttu-id="1b209-128">Indica che il backup automatizzato per la macchina virtuale di SQL Server è abilitato.</span><span class="sxs-lookup"><span data-stu-id="1b209-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="1b209-129">Se specifichi questo parametro, il backup automatizzato imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="1b209-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="1b209-130">In questo articolo vengono aggiornate le impostazioni di backup gestite per seguire questa programmazione.</span><span class="sxs-lookup"><span data-stu-id="1b209-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="1b209-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="1b209-132">Specifica il numero di giorni per cui mantenere un backup.</span><span class="sxs-lookup"><span data-stu-id="1b209-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="1b209-133">-EnableEncryption</span></span>
<span data-ttu-id="1b209-134">Indica che questo cmdlet Abilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="1b209-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="1b209-135">-CertificatePassword</span></span>
<span data-ttu-id="1b209-136">Specifica una password per crittografare il certificato usato per eseguire backup crittografati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b209-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="1b209-137">-StorageUri</span></span>
<span data-ttu-id="1b209-138">Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="1b209-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="1b209-139">-StorageKey</span></span>
<span data-ttu-id="1b209-140">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="1b209-140">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="1b209-141">-Profile</span></span>
<span data-ttu-id="1b209-142">Specifica il profilo Azure da cui viene letto il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b209-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="1b209-143">Se non specifichi un profilo, questo cmdlet viene letto dal profilo predefinito locale.</span><span class="sxs-lookup"><span data-stu-id="1b209-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="1b209-144">-InformationAction</span></span>
<span data-ttu-id="1b209-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="1b209-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="1b209-146">-InformationVariable</span></span>
<span data-ttu-id="1b209-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="1b209-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="1b209-148">-StorageContext</span></span>
<span data-ttu-id="1b209-149">Specifica l'account di archiviazione che verrà usato per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="1b209-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="1b209-150">Per ottenere un oggetto **AzureStorageContext** , usa il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b209-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="1b209-151">L'impostazione predefinita è l'account di archiviazione associato alla macchina virtuale di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="1b209-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="1b209-152">-BackupScheduleType</span></span>
<span data-ttu-id="1b209-153">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="1b209-153">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="1b209-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="1b209-154">-BackupSystemDbs</span></span>
<span data-ttu-id="1b209-155">Database di sistema di backup</span><span class="sxs-lookup"><span data-stu-id="1b209-155">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="1b209-156">-FullBackupFrequency</span></span>
<span data-ttu-id="1b209-157">Frequenza di backup completa di SQL Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="1b209-157">Sql Server Full Backup frequency, daily or week</span></span>

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

### <span data-ttu-id="1b209-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="1b209-158">-FullBackupStartHour</span></span>
<span data-ttu-id="1b209-159">Ora del giorno (0-23) quando il backup completo di SQL Server dovrebbe iniziare</span><span class="sxs-lookup"><span data-stu-id="1b209-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="1b209-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="1b209-161">Finestra backup completo di SQL Server in ore</span><span class="sxs-lookup"><span data-stu-id="1b209-161">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="1b209-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="1b209-163">Frequenza di backup del log di SQL Server, una volta ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="1b209-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b209-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b209-164">CommonParameters</span></span>
<span data-ttu-id="1b209-165">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b209-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b209-166">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b209-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b209-167">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b209-167">INPUTS</span></span>

## <span data-ttu-id="1b209-168">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b209-168">OUTPUTS</span></span>

## <span data-ttu-id="1b209-169">Note</span><span class="sxs-lookup"><span data-stu-id="1b209-169">NOTES</span></span>

## <span data-ttu-id="1b209-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b209-170">RELATED LINKS</span></span>

[<span data-ttu-id="1b209-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="1b209-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="1b209-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="1b209-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)

