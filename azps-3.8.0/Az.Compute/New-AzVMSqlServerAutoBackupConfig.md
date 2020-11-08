---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 952a9160a20492fe49e7f79019ca68e3bc241e57
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019401"
---
# <span data-ttu-id="dbb01-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="dbb01-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="dbb01-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dbb01-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb01-103">Crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dbb01-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="dbb01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbb01-104">SYNTAX</span></span>

### <span data-ttu-id="dbb01-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="dbb01-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dbb01-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="dbb01-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbb01-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dbb01-107">DESCRIPTION</span></span>
<span data-ttu-id="dbb01-108">Il cmdlet **New-AzVMSqlServerAutoBackupConfig** crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dbb01-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="dbb01-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbb01-109">EXAMPLES</span></span>

### <span data-ttu-id="dbb01-110">Esempio 1: creare una configurazione di backup automatica usando l'URI di archiviazione e la chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="dbb01-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="dbb01-111">Questo comando crea un oggetto di configurazione di backup automatico specificando l'URI di archiviazione e la chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="dbb01-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="dbb01-112">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="dbb01-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="dbb01-113">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="dbb01-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="dbb01-114">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="dbb01-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="dbb01-115">Esempio 2: creare una configurazione di backup automatica tramite il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="dbb01-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="dbb01-116">Il primo comando crea un contesto di archiviazione e lo archivia nella variabile $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="dbb01-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="dbb01-117">Per altre informazioni, vedere New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="dbb01-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="dbb01-118">Il secondo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione in $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="dbb01-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="dbb01-119">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="dbb01-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="dbb01-120">Esempio 3: creare una configurazione di backup automatica tramite il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="dbb01-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="dbb01-121">Questo comando crea e archivia un oggetto di configurazione di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="dbb01-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="dbb01-122">Il comando specifica il contesto di archiviazione creato in un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="dbb01-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="dbb01-123">Il comando consente la crittografia con password.</span><span class="sxs-lookup"><span data-stu-id="dbb01-123">The command enables encryption with password.</span></span>
<span data-ttu-id="dbb01-124">La password è stata precedentemente archiviata come stringa sicura nella variabile $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="dbb01-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="dbb01-125">Per creare una stringa sicura, usa il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="dbb01-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="dbb01-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dbb01-126">PARAMETERS</span></span>

### <span data-ttu-id="dbb01-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="dbb01-127">-BackupScheduleType</span></span>
<span data-ttu-id="dbb01-128">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="dbb01-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="dbb01-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="dbb01-129">-BackupSystemDbs</span></span>
<span data-ttu-id="dbb01-130">Database di sistema di backup</span><span class="sxs-lookup"><span data-stu-id="dbb01-130">Backup system databases</span></span>

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

### <span data-ttu-id="dbb01-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="dbb01-131">-CertificatePassword</span></span>
<span data-ttu-id="dbb01-132">Specifica una password per crittografare il certificato usato per eseguire backup crittografati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dbb01-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="dbb01-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb01-133">-DefaultProfile</span></span>
<span data-ttu-id="dbb01-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbb01-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbb01-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="dbb01-135">-Enable</span></span>
<span data-ttu-id="dbb01-136">Indica che il backup automatizzato per la macchina virtuale di SQL Server è abilitato.</span><span class="sxs-lookup"><span data-stu-id="dbb01-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="dbb01-137">Se specifichi questo parametro, il backup automatizzato imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="dbb01-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="dbb01-138">In questo articolo vengono aggiornate le impostazioni di backup gestite per seguire questa programmazione.</span><span class="sxs-lookup"><span data-stu-id="dbb01-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="dbb01-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="dbb01-139">-EnableEncryption</span></span>
<span data-ttu-id="dbb01-140">Indica che questo cmdlet Abilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="dbb01-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="dbb01-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="dbb01-141">-FullBackupFrequency</span></span>
<span data-ttu-id="dbb01-142">Frequenza di backup completa di SQL Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="dbb01-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="dbb01-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="dbb01-143">-FullBackupStartHour</span></span>
<span data-ttu-id="dbb01-144">Ora del giorno (0-23) quando il backup completo di SQL Server dovrebbe iniziare</span><span class="sxs-lookup"><span data-stu-id="dbb01-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="dbb01-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="dbb01-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="dbb01-146">Finestra backup completo di SQL Server in ore</span><span class="sxs-lookup"><span data-stu-id="dbb01-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="dbb01-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="dbb01-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="dbb01-148">Frequenza di backup del log di SQL Server, una volta ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="dbb01-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="dbb01-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbb01-149">-ResourceGroupName</span></span>
<span data-ttu-id="dbb01-150">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="dbb01-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="dbb01-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="dbb01-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="dbb01-152">Specifica il numero di giorni per cui mantenere un backup.</span><span class="sxs-lookup"><span data-stu-id="dbb01-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="dbb01-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="dbb01-153">-StorageContext</span></span>
<span data-ttu-id="dbb01-154">Specifica l'account di archiviazione che verrà usato per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="dbb01-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="dbb01-155">Per ottenere un oggetto **AzureStorageContext** , usa il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="dbb01-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="dbb01-156">L'impostazione predefinita è l'account di archiviazione associato alla macchina virtuale di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="dbb01-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="dbb01-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="dbb01-157">-StorageKey</span></span>
<span data-ttu-id="dbb01-158">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="dbb01-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="dbb01-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="dbb01-159">-StorageUri</span></span>
<span data-ttu-id="dbb01-160">Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="dbb01-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="dbb01-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb01-161">CommonParameters</span></span>
<span data-ttu-id="dbb01-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbb01-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb01-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbb01-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb01-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dbb01-164">INPUTS</span></span>

### <span data-ttu-id="dbb01-165">System. String</span><span class="sxs-lookup"><span data-stu-id="dbb01-165">System.String</span></span>

### <span data-ttu-id="dbb01-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="dbb01-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="dbb01-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="dbb01-167">System.Int32</span></span>

### <span data-ttu-id="dbb01-168">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="dbb01-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="dbb01-169">System. Uri</span><span class="sxs-lookup"><span data-stu-id="dbb01-169">System.Uri</span></span>

### <span data-ttu-id="dbb01-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="dbb01-170">System.Security.SecureString</span></span>

### <span data-ttu-id="dbb01-171">System. Nullable ' 1 [[System. Int32, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="dbb01-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="dbb01-172">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbb01-172">OUTPUTS</span></span>

### <span data-ttu-id="dbb01-173">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="dbb01-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="dbb01-174">Note</span><span class="sxs-lookup"><span data-stu-id="dbb01-174">NOTES</span></span>

## <span data-ttu-id="dbb01-175">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbb01-175">RELATED LINKS</span></span>

[<span data-ttu-id="dbb01-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="dbb01-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="dbb01-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="dbb01-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


