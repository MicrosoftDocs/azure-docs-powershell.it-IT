---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975918"
---
# <span data-ttu-id="b449b-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="b449b-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="b449b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b449b-102">SYNOPSIS</span></span>
<span data-ttu-id="b449b-103">Crea un oggetto configurazione per il SQL Server di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="b449b-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="b449b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b449b-104">SYNTAX</span></span>

### <span data-ttu-id="b449b-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b449b-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b449b-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="b449b-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b449b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="b449b-107">DESCRIPTION</span></span>
<span data-ttu-id="b449b-108">Il cmdlet **New-AzVMSqlServerAutoBackupConfig crea** un oggetto di configurazione per SQL Server di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="b449b-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="b449b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b449b-109">EXAMPLES</span></span>

### <span data-ttu-id="b449b-110">Esempio 1: Creare una configurazione di backup automatico con URI di archiviazione e chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="b449b-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="b449b-111">Questo comando crea un oggetto configurazione di backup automatico specificando URI di archiviazione e chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="b449b-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="b449b-112">Il backup automatico è abilitato e i backup automatici vengono mantenuti per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="b449b-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="b449b-113">Il comando archivia il risultato nella $AutoBackupConfig variabile.</span><span class="sxs-lookup"><span data-stu-id="b449b-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="b449b-114">È possibile specificare questo elemento di configurazione per altri cmdlet, ad esempio Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b449b-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="b449b-115">Esempio 2: Creare una configurazione di backup automatico usando il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="b449b-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="b449b-116">Il primo comando crea un contesto di archiviazione e quindi lo archivia nella $StorageContext variabile.</span><span class="sxs-lookup"><span data-stu-id="b449b-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="b449b-117">Per altre informazioni, vedere New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b449b-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="b449b-118">Il secondo comando crea un oggetto configurazione di backup automatico specificando il contesto di archiviazione in $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="b449b-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="b449b-119">Il backup automatico è abilitato e i backup automatici vengono mantenuti per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="b449b-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="b449b-120">Esempio 3: Creare una configurazione di backup automatico usando il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="b449b-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="b449b-121">Questo comando crea e archivia un oggetto configurazione di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="b449b-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="b449b-122">Il comando specifica il contesto di archiviazione creato in un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="b449b-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="b449b-123">Il comando abilita la crittografia con password.</span><span class="sxs-lookup"><span data-stu-id="b449b-123">The command enables encryption with password.</span></span>
<span data-ttu-id="b449b-124">La password in precedenza era archiviata come stringa sicura nella $CertificatePassword variabile.</span><span class="sxs-lookup"><span data-stu-id="b449b-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="b449b-125">Per creare una stringa sicura, usare il cmdlet ConvertTo-SecureString sicurezza.</span><span class="sxs-lookup"><span data-stu-id="b449b-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="b449b-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b449b-126">PARAMETERS</span></span>

### <span data-ttu-id="b449b-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="b449b-127">-BackupScheduleType</span></span>
<span data-ttu-id="b449b-128">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="b449b-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="b449b-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="b449b-129">-BackupSystemDbs</span></span>
<span data-ttu-id="b449b-130">Backup di database di sistema</span><span class="sxs-lookup"><span data-stu-id="b449b-130">Backup system databases</span></span>

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

### <span data-ttu-id="b449b-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="b449b-131">-CertificatePassword</span></span>
<span data-ttu-id="b449b-132">Specifica una password per crittografare il certificato usato per eseguire SQL Server backup crittografati.</span><span class="sxs-lookup"><span data-stu-id="b449b-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="b449b-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b449b-133">-DefaultProfile</span></span>
<span data-ttu-id="b449b-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b449b-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b449b-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="b449b-135">-Enable</span></span>
<span data-ttu-id="b449b-136">Indica che è abilitato il backup SQL Server della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b449b-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="b449b-137">Se si specifica questo parametro, il backup automatico imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="b449b-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="b449b-138">In questo modo, le impostazioni di Backup gestito vengono aggiornata in base a questa pianificazione.</span><span class="sxs-lookup"><span data-stu-id="b449b-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="b449b-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="b449b-139">-EnableEncryption</span></span>
<span data-ttu-id="b449b-140">Indica che questo cmdlet abilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="b449b-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="b449b-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="b449b-141">-FullBackupFrequency</span></span>
<span data-ttu-id="b449b-142">Frequenza di backup completo di Sql Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="b449b-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="b449b-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="b449b-143">-FullBackupStartHour</span></span>
<span data-ttu-id="b449b-144">Ora del giorno (0-23) in cui dovrebbe iniziare il backup completo di Sql Server</span><span class="sxs-lookup"><span data-stu-id="b449b-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="b449b-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="b449b-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="b449b-146">Finestra Backup completo di Sql Server in ore</span><span class="sxs-lookup"><span data-stu-id="b449b-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="b449b-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="b449b-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="b449b-148">Frequenza di backup del log di Sql Server ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="b449b-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="b449b-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b449b-149">-ResourceGroupName</span></span>
<span data-ttu-id="b449b-150">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="b449b-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="b449b-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="b449b-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="b449b-152">Specifica il numero di giorni per cui conservare un backup.</span><span class="sxs-lookup"><span data-stu-id="b449b-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="b449b-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="b449b-153">-StorageContext</span></span>
<span data-ttu-id="b449b-154">Specifica l'account di archiviazione che verrà usato per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="b449b-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="b449b-155">Per ottenere un **oggetto AzureStorageContext,** usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="b449b-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="b449b-156">L'impostazione predefinita è l'account di archiviazione associato alla macchina SQL Server virtuale.</span><span class="sxs-lookup"><span data-stu-id="b449b-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="b449b-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="b449b-157">-StorageKey</span></span>
<span data-ttu-id="b449b-158">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="b449b-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="b449b-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="b449b-159">-StorageUri</span></span>
<span data-ttu-id="b449b-160">Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="b449b-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="b449b-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b449b-161">CommonParameters</span></span>
<span data-ttu-id="b449b-162">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b449b-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b449b-163">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b449b-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b449b-164">INPUT</span><span class="sxs-lookup"><span data-stu-id="b449b-164">INPUTS</span></span>

### <span data-ttu-id="b449b-165">System.String</span><span class="sxs-lookup"><span data-stu-id="b449b-165">System.String</span></span>

### <span data-ttu-id="b449b-166">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="b449b-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="b449b-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="b449b-167">System.Int32</span></span>

### <span data-ttu-id="b449b-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b449b-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="b449b-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="b449b-169">System.Uri</span></span>

### <span data-ttu-id="b449b-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="b449b-170">System.Security.SecureString</span></span>

### <span data-ttu-id="b449b-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b449b-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="b449b-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b449b-172">OUTPUTS</span></span>

### <span data-ttu-id="b449b-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="b449b-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="b449b-174">NOTE</span><span class="sxs-lookup"><span data-stu-id="b449b-174">NOTES</span></span>

## <span data-ttu-id="b449b-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b449b-175">RELATED LINKS</span></span>

[<span data-ttu-id="b449b-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="b449b-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="b449b-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b449b-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


