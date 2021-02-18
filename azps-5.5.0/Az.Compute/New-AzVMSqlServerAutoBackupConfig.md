---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 952a9160a20492fe49e7f79019ca68e3bc241e57
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181567"
---
# <span data-ttu-id="876a3-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="876a3-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="876a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="876a3-102">SYNOPSIS</span></span>
<span data-ttu-id="876a3-103">Crea un oggetto configurazione per il SQL Server di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="876a3-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="876a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="876a3-104">SYNTAX</span></span>

### <span data-ttu-id="876a3-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="876a3-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="876a3-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="876a3-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="876a3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="876a3-107">DESCRIPTION</span></span>
<span data-ttu-id="876a3-108">Il cmdlet **New-AzVMSqlServerAutoBackupConfig crea** un oggetto di configurazione per SQL Server di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="876a3-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="876a3-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="876a3-109">EXAMPLES</span></span>

### <span data-ttu-id="876a3-110">Esempio 1: Creare una configurazione di backup automatico con URI di archiviazione e chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="876a3-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="876a3-111">Questo comando crea un oggetto configurazione di backup automatico specificando URI di archiviazione e chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="876a3-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="876a3-112">Il backup automatico è abilitato e i backup automatici vengono mantenuti per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="876a3-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="876a3-113">Il comando archivia il risultato nella $AutoBackupConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="876a3-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="876a3-114">È possibile specificare questo elemento di configurazione per altri cmdlet, ad esempio Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="876a3-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="876a3-115">Esempio 2: Creare una configurazione di backup automatico usando il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="876a3-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="876a3-116">Il primo comando crea un contesto di archiviazione e quindi lo archivia nella $StorageContext variabile.</span><span class="sxs-lookup"><span data-stu-id="876a3-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="876a3-117">Per altre informazioni, vedere New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="876a3-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="876a3-118">Il secondo comando crea un oggetto configurazione di backup automatico specificando il contesto di archiviazione $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="876a3-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="876a3-119">Il backup automatico è abilitato e i backup automatici vengono mantenuti per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="876a3-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="876a3-120">Esempio 3: Creare una configurazione di backup automatico usando il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="876a3-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="876a3-121">Questo comando crea e archivia un oggetto configurazione di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="876a3-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="876a3-122">Il comando specifica il contesto di archiviazione creato in un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="876a3-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="876a3-123">Il comando abilita la crittografia con password.</span><span class="sxs-lookup"><span data-stu-id="876a3-123">The command enables encryption with password.</span></span>
<span data-ttu-id="876a3-124">La password in precedenza era archiviata come stringa sicura nella $CertificatePassword variabile.</span><span class="sxs-lookup"><span data-stu-id="876a3-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="876a3-125">Per creare una stringa sicura, usare il cmdlet ConvertTo-SecureString sicurezza.</span><span class="sxs-lookup"><span data-stu-id="876a3-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="876a3-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="876a3-126">PARAMETERS</span></span>

### <span data-ttu-id="876a3-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="876a3-127">-BackupScheduleType</span></span>
<span data-ttu-id="876a3-128">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="876a3-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="876a3-129">-BackupSystemDbs</span></span>
<span data-ttu-id="876a3-130">Backup di database di sistema</span><span class="sxs-lookup"><span data-stu-id="876a3-130">Backup system databases</span></span>

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

### <span data-ttu-id="876a3-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="876a3-131">-CertificatePassword</span></span>
<span data-ttu-id="876a3-132">Specifica una password per crittografare il certificato usato per eseguire SQL Server backup crittografati.</span><span class="sxs-lookup"><span data-stu-id="876a3-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="876a3-133">-DefaultProfile</span></span>
<span data-ttu-id="876a3-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="876a3-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="876a3-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="876a3-135">-Enable</span></span>
<span data-ttu-id="876a3-136">Indica che è abilitato il backup SQL Server della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="876a3-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="876a3-137">Se si specifica questo parametro, il backup automatico imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="876a3-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="876a3-138">In questo modo, le impostazioni di Backup gestito vengono aggiornata in base a questa pianificazione.</span><span class="sxs-lookup"><span data-stu-id="876a3-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="876a3-139">-EnableEncryption</span></span>
<span data-ttu-id="876a3-140">Indica che questo cmdlet abilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="876a3-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="876a3-141">-FullBackupFrequency</span></span>
<span data-ttu-id="876a3-142">Frequenza di backup completo di Sql Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="876a3-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="876a3-143">-FullBackupStartHour</span></span>
<span data-ttu-id="876a3-144">Ora del giorno (0-23) in cui dovrebbe iniziare il backup completo di Sql Server</span><span class="sxs-lookup"><span data-stu-id="876a3-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="876a3-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="876a3-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="876a3-146">Finestra Backup completo di Sql Server in ore</span><span class="sxs-lookup"><span data-stu-id="876a3-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="876a3-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="876a3-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="876a3-148">Frequenza di backup del log di Sql Server ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="876a3-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="876a3-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="876a3-149">-ResourceGroupName</span></span>
<span data-ttu-id="876a3-150">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="876a3-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="876a3-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="876a3-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="876a3-152">Specifica il numero di giorni per cui conservare un backup.</span><span class="sxs-lookup"><span data-stu-id="876a3-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="876a3-153">-StorageContext</span></span>
<span data-ttu-id="876a3-154">Specifica l'account di archiviazione che verrà usato per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="876a3-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="876a3-155">Per ottenere un **oggetto AzureStorageContext,** usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="876a3-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="876a3-156">L'impostazione predefinita è l'account di archiviazione associato alla macchina SQL Server virtuale.</span><span class="sxs-lookup"><span data-stu-id="876a3-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="876a3-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="876a3-157">-StorageKey</span></span>
<span data-ttu-id="876a3-158">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="876a3-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="876a3-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="876a3-159">-StorageUri</span></span>
<span data-ttu-id="876a3-160">Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="876a3-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="876a3-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="876a3-161">CommonParameters</span></span>
<span data-ttu-id="876a3-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="876a3-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="876a3-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="876a3-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="876a3-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="876a3-164">INPUTS</span></span>

### <span data-ttu-id="876a3-165">System.String</span><span class="sxs-lookup"><span data-stu-id="876a3-165">System.String</span></span>

### <span data-ttu-id="876a3-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="876a3-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="876a3-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="876a3-167">System.Int32</span></span>

### <span data-ttu-id="876a3-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="876a3-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="876a3-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="876a3-169">System.Uri</span></span>

### <span data-ttu-id="876a3-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="876a3-170">System.Security.SecureString</span></span>

### <span data-ttu-id="876a3-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="876a3-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="876a3-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="876a3-172">OUTPUTS</span></span>

### <span data-ttu-id="876a3-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="876a3-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="876a3-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="876a3-174">NOTES</span></span>

## <span data-ttu-id="876a3-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="876a3-175">RELATED LINKS</span></span>

[<span data-ttu-id="876a3-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="876a3-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="876a3-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="876a3-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


