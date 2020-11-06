---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 271426278c561ede4778e0ad69cf9ee4e6c0607e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506964"
---
# <span data-ttu-id="2b3f0-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2b3f0-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="2b3f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b3f0-102">SYNOPSIS</span></span>
<span data-ttu-id="2b3f0-103">Impostare la configurazione di backup nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="2b3f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b3f0-104">SYNTAX</span></span>

### <span data-ttu-id="2b3f0-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2b3f0-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2b3f0-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="2b3f0-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2b3f0-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b3f0-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2b3f0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b3f0-108">DESCRIPTION</span></span>
<span data-ttu-id="2b3f0-109">Impostare la configurazione di backup nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="2b3f0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b3f0-110">EXAMPLES</span></span>

### <span data-ttu-id="2b3f0-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2b3f0-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="2b3f0-112">Impostare la configurazione di backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="2b3f0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b3f0-113">PARAMETERS</span></span>

### <span data-ttu-id="2b3f0-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2b3f0-114">-AsJob</span></span>
<span data-ttu-id="2b3f0-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="2b3f0-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="2b3f0-117">Intervallo, in ore, per la frequenza con cui l'utilità di pianificazione accetta un backup.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="2b3f0-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="2b3f0-119">Periodo di conservazione, in giorni, per i backup nel percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="2b3f0-120">-EncryptionKey</span></span>
<span data-ttu-id="2b3f0-121">Chiave di crittografia usata per crittografare i backup.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b3f0-122">-InputObject</span></span>
<span data-ttu-id="2b3f0-123">Configurazione della posizione di backup restituita da Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="2b3f0-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="2b3f0-125">Se l'utilità di pianificazione di backup deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="2b3f0-126">-Location</span></span>
<span data-ttu-id="2b3f0-127">Posizione da configurare.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-128">-Password</span><span class="sxs-lookup"><span data-stu-id="2b3f0-128">-Password</span></span>
<span data-ttu-id="2b3f0-129">Password necessaria per accedere alla posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-130">-Path</span><span class="sxs-lookup"><span data-stu-id="2b3f0-130">-Path</span></span>
<span data-ttu-id="2b3f0-131">Posizione in cui verranno archiviati i backup.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b3f0-132">-ResourceGroupName</span></span>
<span data-ttu-id="2b3f0-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2b3f0-134">-ResourceId</span></span>
<span data-ttu-id="2b3f0-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-136">-Username</span><span class="sxs-lookup"><span data-stu-id="2b3f0-136">-Username</span></span>
<span data-ttu-id="2b3f0-137">Nome utente necessario per accedere alla posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="2b3f0-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b3f0-138">-Confirm</span></span>
<span data-ttu-id="2b3f0-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b3f0-140">-WhatIf</span></span>
<span data-ttu-id="2b3f0-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b3f0-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b3f0-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b3f0-143">CommonParameters</span></span>
<span data-ttu-id="2b3f0-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b3f0-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b3f0-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b3f0-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b3f0-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b3f0-146">INPUTS</span></span>

## <span data-ttu-id="2b3f0-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b3f0-147">OUTPUTS</span></span>

### <span data-ttu-id="2b3f0-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="2b3f0-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="2b3f0-149">Note</span><span class="sxs-lookup"><span data-stu-id="2b3f0-149">NOTES</span></span>

## <span data-ttu-id="2b3f0-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b3f0-150">RELATED LINKS</span></span>

