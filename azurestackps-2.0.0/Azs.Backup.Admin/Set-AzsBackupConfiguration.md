---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93864049"
---
# <span data-ttu-id="8c6de-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="8c6de-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="8c6de-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8c6de-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6de-103">Aggiornare un percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-103">Update a backup location.</span></span>

## <span data-ttu-id="8c6de-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8c6de-104">SYNTAX</span></span>

### <span data-ttu-id="8c6de-105">UpdateExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8c6de-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="8c6de-106">Aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8c6de-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8c6de-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8c6de-107">DESCRIPTION</span></span>
<span data-ttu-id="8c6de-108">Aggiornare un percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-108">Update a backup location.</span></span>

## <span data-ttu-id="8c6de-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8c6de-109">EXAMPLES</span></span>

### <span data-ttu-id="8c6de-110">Esempio 1: impostare la configurazione di backup</span><span class="sxs-lookup"><span data-stu-id="8c6de-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="8c6de-111">Impostare la configurazione di backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="8c6de-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="8c6de-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8c6de-112">PARAMETERS</span></span>

### <span data-ttu-id="8c6de-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c6de-113">-AsJob</span></span>
<span data-ttu-id="8c6de-114">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="8c6de-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-115">-Backup</span><span class="sxs-lookup"><span data-stu-id="8c6de-115">-Backup</span></span>
<span data-ttu-id="8c6de-116">Informazioni sul percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-116">Information about the backup location.</span></span>
<span data-ttu-id="8c6de-117">Per costruire, vedere la sezione Note per le proprietà di BACKUP e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="8c6de-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="8c6de-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="8c6de-119">Intervallo, in ore, per la frequenza con cui l'utilità di pianificazione accetta un backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="8c6de-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="8c6de-121">Periodo di conservazione, in giorni, per gli schienali nel percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8c6de-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6de-122">-DefaultProfile</span></span>
<span data-ttu-id="8c6de-123">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6de-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="8c6de-124">-EncryptionCertPath</span></span>
<span data-ttu-id="8c6de-125">Percorso del file CERT di crittografia con chiave pubblica (con estensione CER).</span><span class="sxs-lookup"><span data-stu-id="8c6de-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="8c6de-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="8c6de-127">True se l'utilità di pianificazione di backup è abilitata.</span><span class="sxs-lookup"><span data-stu-id="8c6de-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-128">-Posizione</span><span class="sxs-lookup"><span data-stu-id="8c6de-128">-Location</span></span>
<span data-ttu-id="8c6de-129">Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-130">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="8c6de-130">-NoWait</span></span>
<span data-ttu-id="8c6de-131">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="8c6de-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-132">-Password</span><span class="sxs-lookup"><span data-stu-id="8c6de-132">-Password</span></span>
<span data-ttu-id="8c6de-133">Password per accedere alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8c6de-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-134">-Path</span><span class="sxs-lookup"><span data-stu-id="8c6de-134">-Path</span></span>
<span data-ttu-id="8c6de-135">Percorso della posizione di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8c6de-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6de-136">-ResourceGroupName</span></span>
<span data-ttu-id="8c6de-137">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8c6de-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8c6de-138">-SubscriptionId</span></span>
<span data-ttu-id="8c6de-139">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6de-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c6de-140">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="8c6de-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="8c6de-141">-Tag</span></span>
<span data-ttu-id="8c6de-142">Elenco di coppie di valori chiave.</span><span class="sxs-lookup"><span data-stu-id="8c6de-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="8c6de-143">-UserName</span></span>
<span data-ttu-id="8c6de-144">Nome utente per accedere alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8c6de-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8c6de-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8c6de-145">-Confirm</span></span>
<span data-ttu-id="8c6de-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c6de-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c6de-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c6de-147">-WhatIf</span></span>
<span data-ttu-id="8c6de-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c6de-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c6de-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8c6de-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c6de-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6de-150">CommonParameters</span></span>
<span data-ttu-id="8c6de-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6de-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6de-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c6de-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6de-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8c6de-153">INPUTS</span></span>

### <span data-ttu-id="8c6de-154">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="8c6de-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="8c6de-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8c6de-155">OUTPUTS</span></span>

### <span data-ttu-id="8c6de-156">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="8c6de-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="8c6de-157">Note</span><span class="sxs-lookup"><span data-stu-id="8c6de-157">NOTES</span></span>

<span data-ttu-id="8c6de-158">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="8c6de-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c6de-159">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c6de-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8c6de-160">BACKUP <IBackupLocation> : informazioni sul percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="8c6de-161">`[Location <String>]`: Posizione della risorsa.</span><span class="sxs-lookup"><span data-stu-id="8c6de-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="8c6de-162">`[Tag <IResourceTags>]`: Elenco di coppie di valori chiave.</span><span class="sxs-lookup"><span data-stu-id="8c6de-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="8c6de-163">`[(Any) <String>]`: Indica che qualsiasi proprietà può essere aggiunta a questo oggetto.</span><span class="sxs-lookup"><span data-stu-id="8c6de-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="8c6de-164">`[BackupFrequencyInHours <Int32?>]`: Intervallo, in ore, per la frequenza con cui l'utilità di pianificazione accetta un backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="8c6de-165">`[BackupRetentionPeriodInDays <Int32?>]`: Periodo di conservazione, in giorni, per gli schienali nel percorso di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="8c6de-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="8c6de-166">`[EncryptionCertBase64 <String>]`: Dati non elaborati Base64 per il certificato di crittografia di backup.</span><span class="sxs-lookup"><span data-stu-id="8c6de-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="8c6de-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True se l'utilità di pianificazione backup è abilitata.</span><span class="sxs-lookup"><span data-stu-id="8c6de-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="8c6de-168">`[Password <String>]`: Password per accedere alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8c6de-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="8c6de-169">`[Path <String>]`: Percorso della posizione di aggiornamento</span><span class="sxs-lookup"><span data-stu-id="8c6de-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="8c6de-170">`[UserName <String>]`: Nomeutente per accedere alla posizione.</span><span class="sxs-lookup"><span data-stu-id="8c6de-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="8c6de-171">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8c6de-171">RELATED LINKS</span></span>

