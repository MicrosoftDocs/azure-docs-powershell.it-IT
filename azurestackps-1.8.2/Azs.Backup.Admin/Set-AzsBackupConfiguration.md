---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/08/2020
ms.locfileid: "94030264"
---
# <span data-ttu-id="0fdf1-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="0fdf1-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="0fdf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0fdf1-102">SYNOPSIS</span></span>
<span data-ttu-id="0fdf1-103">Impostare la configurazione di backup nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="0fdf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0fdf1-104">SYNTAX</span></span>

### <span data-ttu-id="0fdf1-105">Update (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0fdf1-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fdf1-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="0fdf1-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0fdf1-107">ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fdf1-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0fdf1-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0fdf1-108">DESCRIPTION</span></span>
<span data-ttu-id="0fdf1-109">Impostare la configurazione di backup nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="0fdf1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0fdf1-110">EXAMPLES</span></span>

### <span data-ttu-id="0fdf1-111">--------------------------ESEMPIO 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="0fdf1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="0fdf1-112">Impostare la configurazione di backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="0fdf1-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0fdf1-113">PARAMETERS</span></span>

### <span data-ttu-id="0fdf1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0fdf1-114">-AsJob</span></span>
<span data-ttu-id="0fdf1-115">Esegui asincrono come processo e Restituisci l'oggetto processo.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0fdf1-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="0fdf1-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="0fdf1-117">Intervallo, in ore, per la frequenza con cui l'utilità di pianificazione accetta un backup.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="0fdf1-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="0fdf1-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="0fdf1-119">Periodo di conservazione, in giorni, per i backup nel percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="0fdf1-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="0fdf1-120">-EncryptionKey</span></span>
<span data-ttu-id="0fdf1-121">Chiave di crittografia usata per crittografare i backup.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-121">Encryption key used to encrypt backups.</span></span>

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

### <span data-ttu-id="0fdf1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0fdf1-122">-InputObject</span></span>
<span data-ttu-id="0fdf1-123">Configurazione della posizione di backup restituita da Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

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

### <span data-ttu-id="0fdf1-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="0fdf1-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="0fdf1-125">Se l'utilità di pianificazione di backup deve essere abilitata.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-125">Whether the backup scheduler should be enabled.</span></span>

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

### <span data-ttu-id="0fdf1-126">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0fdf1-126">-Location</span></span>
<span data-ttu-id="0fdf1-127">Posizione da configurare.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-127">Location to configure.</span></span>

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

### <span data-ttu-id="0fdf1-128">-Password</span><span class="sxs-lookup"><span data-stu-id="0fdf1-128">-Password</span></span>
<span data-ttu-id="0fdf1-129">Password necessaria per accedere alla posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="0fdf1-130">-Path</span><span class="sxs-lookup"><span data-stu-id="0fdf1-130">-Path</span></span>
<span data-ttu-id="0fdf1-131">Posizione in cui verranno archiviati i backup.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-131">Location where backups will be stored.</span></span>

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

### <span data-ttu-id="0fdf1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fdf1-132">-ResourceGroupName</span></span>
<span data-ttu-id="0fdf1-133">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="0fdf1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fdf1-134">-ResourceId</span></span>
<span data-ttu-id="0fdf1-135">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-135">The resource id.</span></span>

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

### <span data-ttu-id="0fdf1-136">-Username</span><span class="sxs-lookup"><span data-stu-id="0fdf1-136">-Username</span></span>
<span data-ttu-id="0fdf1-137">Nome utente necessario per accedere alla posizione di backup.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="0fdf1-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0fdf1-138">-Confirm</span></span>
<span data-ttu-id="0fdf1-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0fdf1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fdf1-140">-WhatIf</span></span>
<span data-ttu-id="0fdf1-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fdf1-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0fdf1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fdf1-143">CommonParameters</span></span>
<span data-ttu-id="0fdf1-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0fdf1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fdf1-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0fdf1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fdf1-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0fdf1-146">INPUTS</span></span>

## <span data-ttu-id="0fdf1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0fdf1-147">OUTPUTS</span></span>

### <span data-ttu-id="0fdf1-148">Microsoft. AzureStack. Management. backup. admin. Models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="0fdf1-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="0fdf1-149">Note</span><span class="sxs-lookup"><span data-stu-id="0fdf1-149">NOTES</span></span>

## <span data-ttu-id="0fdf1-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0fdf1-150">RELATED LINKS</span></span>

