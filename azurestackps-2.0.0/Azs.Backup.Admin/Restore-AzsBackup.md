---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93864058"
---
# <span data-ttu-id="18050-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="18050-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="18050-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18050-102">SYNOPSIS</span></span>
<span data-ttu-id="18050-103">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="18050-103">Restore a backup.</span></span>

## <span data-ttu-id="18050-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18050-104">SYNTAX</span></span>

### <span data-ttu-id="18050-105">RestoreExpanded (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18050-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="18050-106">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="18050-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="18050-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="18050-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="18050-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="18050-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="18050-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18050-109">DESCRIPTION</span></span>
<span data-ttu-id="18050-110">Ripristinare un backup.</span><span class="sxs-lookup"><span data-stu-id="18050-110">Restore a backup.</span></span>

## <span data-ttu-id="18050-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18050-111">EXAMPLES</span></span>

### <span data-ttu-id="18050-112">Esempio 1: ripristino del backup</span><span class="sxs-lookup"><span data-stu-id="18050-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="18050-113">Eseguire il ripristino da un backup di Azure stack.</span><span class="sxs-lookup"><span data-stu-id="18050-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="18050-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18050-114">PARAMETERS</span></span>

### <span data-ttu-id="18050-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="18050-115">-AsJob</span></span>
<span data-ttu-id="18050-116">Eseguire il comando come processo</span><span class="sxs-lookup"><span data-stu-id="18050-116">Run the command as a job</span></span>

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

### <span data-ttu-id="18050-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="18050-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="18050-118">La password per il certificato di decrittazione.</span><span class="sxs-lookup"><span data-stu-id="18050-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="18050-119">-DecryptionCertPath</span></span>
<span data-ttu-id="18050-120">Percorso del file CERT di decrittografia con la chiave privata (PFX).</span><span class="sxs-lookup"><span data-stu-id="18050-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18050-121">-DefaultProfile</span></span>
<span data-ttu-id="18050-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="18050-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="18050-123">-Force</span><span class="sxs-lookup"><span data-stu-id="18050-123">-Force</span></span>
<span data-ttu-id="18050-124">Non chiedere conferma</span><span class="sxs-lookup"><span data-stu-id="18050-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="18050-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="18050-125">-InputObject</span></span>
<span data-ttu-id="18050-126">Parametro Identity da costruire, vedere la sezione Note per le proprietà di INPUTOBJECT e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="18050-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="18050-127">-Posizione</span><span class="sxs-lookup"><span data-stu-id="18050-127">-Location</span></span>
<span data-ttu-id="18050-128">Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="18050-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="18050-129">-Name</span></span>
<span data-ttu-id="18050-130">Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="18050-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-131">-NOWAIT</span><span class="sxs-lookup"><span data-stu-id="18050-131">-NoWait</span></span>
<span data-ttu-id="18050-132">Eseguire il comando in modo asincrono</span><span class="sxs-lookup"><span data-stu-id="18050-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="18050-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18050-133">-PassThru</span></span>
<span data-ttu-id="18050-134">Restituisce vero quando il comando riesce</span><span class="sxs-lookup"><span data-stu-id="18050-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="18050-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18050-135">-ResourceGroupName</span></span>
<span data-ttu-id="18050-136">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="18050-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="18050-137">-RestoreOption</span></span>
<span data-ttu-id="18050-138">Proprietà per le opzioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="18050-138">Properties for restore options.</span></span>
<span data-ttu-id="18050-139">Per costruire, vedere la sezione Note per le proprietà di RESTOREOPTION e creare una tabella hash.</span><span class="sxs-lookup"><span data-stu-id="18050-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-140">-RoleName</span><span class="sxs-lookup"><span data-stu-id="18050-140">-RoleName</span></span>
<span data-ttu-id="18050-141">Nome del ruolo di Azure stack per il ripristino, impostarlo su Empty per tutti i ruoli dell'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="18050-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="18050-142">-SubscriptionId</span></span>
<span data-ttu-id="18050-143">Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18050-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="18050-144">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="18050-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="18050-145">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18050-145">-Confirm</span></span>
<span data-ttu-id="18050-146">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18050-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18050-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18050-147">-WhatIf</span></span>
<span data-ttu-id="18050-148">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18050-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18050-149">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18050-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18050-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18050-150">CommonParameters</span></span>
<span data-ttu-id="18050-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18050-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18050-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="18050-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18050-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18050-153">INPUTS</span></span>

### <span data-ttu-id="18050-154">Microsoft. Azure. PowerShell. Cmdlets. BackupAdmin. Models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="18050-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="18050-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18050-155">OUTPUTS</span></span>

### <span data-ttu-id="18050-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18050-156">System.Boolean</span></span>



## <span data-ttu-id="18050-157">Note</span><span class="sxs-lookup"><span data-stu-id="18050-157">NOTES</span></span>

<span data-ttu-id="18050-158">Proprietà complesse dei parametri per creare i parametri descritti di seguito, Costruisci una tabella hash contenente le proprietà appropriate.</span><span class="sxs-lookup"><span data-stu-id="18050-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="18050-159">Per informazioni sulle tabelle hash, eseguire Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="18050-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="18050-160">INPUTOBJECT <IBackupAdminIdentity> : parametro Identity</span><span class="sxs-lookup"><span data-stu-id="18050-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="18050-161">`[Backup <String>]`: Nome del backup.</span><span class="sxs-lookup"><span data-stu-id="18050-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="18050-162">`[Id <String>]`: Percorso identità risorse</span><span class="sxs-lookup"><span data-stu-id="18050-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="18050-163">`[Location <String>]`: Nome del percorso di backup.</span><span class="sxs-lookup"><span data-stu-id="18050-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="18050-164">`[ResourceGroupName <String>]`: Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="18050-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="18050-165">`[SubscriptionId <String>]`: Credenziali di sottoscrizione che identificano in modo univoco l'abbonamento a Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="18050-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="18050-166">L'ID sottoscrizione fa parte dell'URI per ogni chiamata di servizio.</span><span class="sxs-lookup"><span data-stu-id="18050-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="18050-167">RESTOREOPTION <IRestoreOptions> : proprietà per le opzioni di ripristino.</span><span class="sxs-lookup"><span data-stu-id="18050-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="18050-168">`[DecryptionCertBase64 <String>]`: I dati non elaborati del file di certificato nella stringa Base64.</span><span class="sxs-lookup"><span data-stu-id="18050-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="18050-169">Questo dovrebbe essere il file PFX con la chiave privata.</span><span class="sxs-lookup"><span data-stu-id="18050-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="18050-170">`[DecryptionCertPassword <String>]`: La password per il certificato di decrittazione.</span><span class="sxs-lookup"><span data-stu-id="18050-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="18050-171">`[RoleName <String>]`: Nome del ruolo di Azure stack per il ripristino, impostarlo su Empty per tutti i ruoli dell'infrastruttura</span><span class="sxs-lookup"><span data-stu-id="18050-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="18050-172">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18050-172">RELATED LINKS</span></span>

