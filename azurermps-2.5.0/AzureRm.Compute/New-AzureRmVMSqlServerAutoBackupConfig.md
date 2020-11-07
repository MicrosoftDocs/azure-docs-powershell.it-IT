---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
ms.openlocfilehash: bb00a3e4fc953510d2ec32b7c213d07d6c8801c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866911"
---
# <span data-ttu-id="5c64c-101">New-AzureRmVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="5c64c-101">New-AzureRmVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="5c64c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c64c-102">SYNOPSIS</span></span>
<span data-ttu-id="5c64c-103">Crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c64c-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5c64c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c64c-104">SYNTAX</span></span>

### <span data-ttu-id="5c64c-105">StorageUriSqlServerAutoBackup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c64c-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5c64c-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="5c64c-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c64c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c64c-107">DESCRIPTION</span></span>
<span data-ttu-id="5c64c-108">Il cmdlet **New-AzureRmVMSqlServerAutoBackupConfig** crea un oggetto Configuration per il backup automatico di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c64c-108">The **New-AzureRmVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="5c64c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c64c-109">EXAMPLES</span></span>

### <span data-ttu-id="5c64c-110">Esempio 1: creare una configurazione di backup automatica usando l'URI di archiviazione e la chiave dell'account</span><span class="sxs-lookup"><span data-stu-id="5c64c-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="5c64c-111">Questo comando crea un oggetto di configurazione di backup automatico specificando l'URI di archiviazione e la chiave dell'account.</span><span class="sxs-lookup"><span data-stu-id="5c64c-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="5c64c-112">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="5c64c-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="5c64c-113">Il comando Archivia il risultato nella variabile $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5c64c-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="5c64c-114">Puoi specificare questo elemento di configurazione per altri cmdlet, ad esempio il cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="5c64c-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="5c64c-115">Esempio 2: creare una configurazione di backup automatica tramite il contesto di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5c64c-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="5c64c-116">Il primo comando crea un contesto di archiviazione e lo archivia nella variabile $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="5c64c-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="5c64c-117">Per altre informazioni, vedere New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5c64c-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="5c64c-118">Il secondo comando crea un oggetto di configurazione di backup automatico specificando il contesto di archiviazione in $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="5c64c-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="5c64c-119">Il backup automatico è abilitato e i backup automatici vengono conservati per 10 giorni.</span><span class="sxs-lookup"><span data-stu-id="5c64c-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="5c64c-120">Esempio 3: creare una configurazione di backup automatica tramite il contesto di archiviazione con crittografia e password</span><span class="sxs-lookup"><span data-stu-id="5c64c-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="5c64c-121">Questo comando crea e archivia un oggetto di configurazione di backup automatico.</span><span class="sxs-lookup"><span data-stu-id="5c64c-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="5c64c-122">Il comando specifica il contesto di archiviazione creato in un esempio precedente.</span><span class="sxs-lookup"><span data-stu-id="5c64c-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="5c64c-123">Il comando consente la crittografia con password.</span><span class="sxs-lookup"><span data-stu-id="5c64c-123">The command enables encryption with password.</span></span>
<span data-ttu-id="5c64c-124">La password è stata precedentemente archiviata come stringa sicura nella variabile $CertificatePassword.</span><span class="sxs-lookup"><span data-stu-id="5c64c-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="5c64c-125">Per creare una stringa sicura, usa il cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="5c64c-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="5c64c-126">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c64c-126">PARAMETERS</span></span>

### <span data-ttu-id="5c64c-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="5c64c-127">-BackupScheduleType</span></span>
<span data-ttu-id="5c64c-128">Tipo di pianificazione del backup, manuale o automatizzato</span><span class="sxs-lookup"><span data-stu-id="5c64c-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="5c64c-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="5c64c-129">-BackupSystemDbs</span></span>
<span data-ttu-id="5c64c-130">Database di sistema di backup</span><span class="sxs-lookup"><span data-stu-id="5c64c-130">Backup system databases</span></span>

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

### <span data-ttu-id="5c64c-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="5c64c-131">-CertificatePassword</span></span>
<span data-ttu-id="5c64c-132">Specifica una password per crittografare il certificato usato per eseguire backup crittografati di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c64c-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="5c64c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c64c-133">-DefaultProfile</span></span>
<span data-ttu-id="5c64c-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5c64c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c64c-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="5c64c-135">-Enable</span></span>
<span data-ttu-id="5c64c-136">Indica che il backup automatizzato per la macchina virtuale di SQL Server è abilitato.</span><span class="sxs-lookup"><span data-stu-id="5c64c-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="5c64c-137">Se specifichi questo parametro, il backup automatizzato imposta una pianificazione di backup per tutti i database correnti e nuovi.</span><span class="sxs-lookup"><span data-stu-id="5c64c-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="5c64c-138">In questo articolo vengono aggiornate le impostazioni di backup gestite per seguire questa programmazione.</span><span class="sxs-lookup"><span data-stu-id="5c64c-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="5c64c-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="5c64c-139">-EnableEncryption</span></span>
<span data-ttu-id="5c64c-140">Indica che questo cmdlet Abilita la crittografia.</span><span class="sxs-lookup"><span data-stu-id="5c64c-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="5c64c-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="5c64c-141">-FullBackupFrequency</span></span>
<span data-ttu-id="5c64c-142">Frequenza di backup completa di SQL Server, giornaliera o settimanale</span><span class="sxs-lookup"><span data-stu-id="5c64c-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="5c64c-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="5c64c-143">-FullBackupStartHour</span></span>
<span data-ttu-id="5c64c-144">Ora del giorno (0-23) quando il backup completo di SQL Server dovrebbe iniziare</span><span class="sxs-lookup"><span data-stu-id="5c64c-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="5c64c-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="5c64c-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="5c64c-146">Finestra backup completo di SQL Server in ore</span><span class="sxs-lookup"><span data-stu-id="5c64c-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="5c64c-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="5c64c-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="5c64c-148">Frequenza di backup del log di SQL Server, una volta ogni 1-60 minuti</span><span class="sxs-lookup"><span data-stu-id="5c64c-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="5c64c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c64c-149">-ResourceGroupName</span></span>
<span data-ttu-id="5c64c-150">Specifica il nome del gruppo di risorse della macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="5c64c-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5c64c-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5c64c-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="5c64c-152">Specifica il numero di giorni per cui mantenere un backup.</span><span class="sxs-lookup"><span data-stu-id="5c64c-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="5c64c-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="5c64c-153">-StorageContext</span></span>
<span data-ttu-id="5c64c-154">Specifica l'account di archiviazione che verrà usato per archiviare i backup.</span><span class="sxs-lookup"><span data-stu-id="5c64c-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="5c64c-155">Per ottenere un oggetto **AzureStorageContext** , usa il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5c64c-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="5c64c-156">L'impostazione predefinita è l'account di archiviazione associato alla macchina virtuale di SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c64c-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c64c-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="5c64c-157">-StorageKey</span></span>
<span data-ttu-id="5c64c-158">Specifica la chiave di archiviazione dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="5c64c-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="5c64c-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="5c64c-159">-StorageUri</span></span>
<span data-ttu-id="5c64c-160">Specifica l'URI (Uniform Resource Identifier) dell'account di archiviazione BLOB.</span><span class="sxs-lookup"><span data-stu-id="5c64c-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="5c64c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c64c-161">CommonParameters</span></span>
<span data-ttu-id="5c64c-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c64c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c64c-163">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c64c-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c64c-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c64c-164">INPUTS</span></span>

### <span data-ttu-id="5c64c-165">Nessuno</span><span class="sxs-lookup"><span data-stu-id="5c64c-165">None</span></span>
<span data-ttu-id="5c64c-166">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="5c64c-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5c64c-167">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c64c-167">OUTPUTS</span></span>

### <span data-ttu-id="5c64c-168">Microsoft. Azure. Commands. Compute. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5c64c-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="5c64c-169">Note</span><span class="sxs-lookup"><span data-stu-id="5c64c-169">NOTES</span></span>

## <span data-ttu-id="5c64c-170">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c64c-170">RELATED LINKS</span></span>



[<span data-ttu-id="5c64c-171">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5c64c-171">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


