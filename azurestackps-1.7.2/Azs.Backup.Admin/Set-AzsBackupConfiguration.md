---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858713"
---
# <span data-ttu-id="5c923-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="5c923-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="5c923-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5c923-102">SYNOPSIS</span></span>
<span data-ttu-id="5c923-103">Impostare la configurazione di backup nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c923-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="5c923-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5c923-104">SYNTAX</span></span>

### <span data-ttu-id="5c923-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5c923-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c923-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="5c923-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5c923-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c923-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5c923-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5c923-108">DESCRIPTION</span></span>
<span data-ttu-id="5c923-109">Impostare la configurazione di backup nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="5c923-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="5c923-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5c923-110">EXAMPLES</span></span>

### <span data-ttu-id="5c923-111">ESEMPIO 1</span><span class="sxs-lookup"><span data-stu-id="5c923-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="5c923-112">Impostare la configurazione di backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="5c923-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="5c923-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5c923-113">PARAMETERS</span></span>

### <span data-ttu-id="5c923-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c923-114">-AsJob</span></span>
<span data-ttu-id="5c923-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="5c923-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="5c923-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="5c923-117">Intervallo, in ore, per la frequenza con cui l'utilità di pianificazione accetta un backup.</span><span class="sxs-lookup"><span data-stu-id="5c923-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="5c923-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="5c923-119">Periodo di conservazione, in giorni, per i backup nel percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="5c923-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="5c923-120">-EncryptionCertPath</span></span>
<span data-ttu-id="5c923-121">Percorso del file CERT di crittografia con chiave pubblica (con estensione CER).</span><span class="sxs-lookup"><span data-stu-id="5c923-121">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c923-122">-InputObject</span></span>
<span data-ttu-id="5c923-123">Configurazione della posizione di backup restituita da Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5c923-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="5c923-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="5c923-125">Se l'utilità di pianificazione di backup deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="5c923-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="5c923-126">-Location</span></span>
<span data-ttu-id="5c923-127">Posizione da configurare.</span><span class="sxs-lookup"><span data-stu-id="5c923-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-128">-Password</span><span class="sxs-lookup"><span data-stu-id="5c923-128">-Password</span></span>
<span data-ttu-id="5c923-129">Password necessaria per accedere alla posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="5c923-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-130">-Path</span><span class="sxs-lookup"><span data-stu-id="5c923-130">-Path</span></span>
<span data-ttu-id="5c923-131">Posizione in cui verranno archiviati i backup.</span><span class="sxs-lookup"><span data-stu-id="5c923-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c923-132">-ResourceGroupName</span></span>
<span data-ttu-id="5c923-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5c923-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c923-134">-ResourceId</span></span>
<span data-ttu-id="5c923-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="5c923-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-136">-Username</span><span class="sxs-lookup"><span data-stu-id="5c923-136">-Username</span></span>
<span data-ttu-id="5c923-137">Nome utente necessario per accedere alla posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="5c923-137">Username required to access backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5c923-138">-Confirm</span></span>
<span data-ttu-id="5c923-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c923-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c923-140">-WhatIf</span></span>
<span data-ttu-id="5c923-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c923-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c923-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5c923-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c923-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c923-143">CommonParameters</span></span>
<span data-ttu-id="5c923-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c923-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c923-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c923-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c923-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5c923-146">INPUTS</span></span>

## <span data-ttu-id="5c923-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5c923-147">OUTPUTS</span></span>

### <span data-ttu-id="5c923-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="5c923-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="5c923-149">Note</span><span class="sxs-lookup"><span data-stu-id="5c923-149">NOTES</span></span>

## <span data-ttu-id="5c923-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5c923-150">RELATED LINKS</span></span>
