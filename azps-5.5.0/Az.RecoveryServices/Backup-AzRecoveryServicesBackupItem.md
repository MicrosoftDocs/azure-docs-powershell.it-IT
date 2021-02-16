---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178998"
---
# <span data-ttu-id="89e80-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89e80-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="89e80-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89e80-102">SYNOPSIS</span></span>

<span data-ttu-id="89e80-103">Avvia il backup di un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="89e80-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="89e80-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89e80-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="89e80-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="89e80-105">DESCRIPTION</span></span>

<span data-ttu-id="89e80-106">Il **cmdlet Backup-AzRecoveryServicesBackupItem accetta** un backup adhoc dell'elemento di backup protetto di Azure.</span><span class="sxs-lookup"><span data-stu-id="89e80-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="89e80-107">Con questo cmdlet è possibile eseguire un backup iniziale immediatamente dopo aver abilitato la protezione o avviare un backup se un backup pianificato non riesce.</span><span class="sxs-lookup"><span data-stu-id="89e80-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="89e80-108">Questo cmdlet può essere usato anche per la conservazione personalizzata con o senza data di scadenza. Per altre informazioni, vedere la Guida dei parametri di riferimento.</span><span class="sxs-lookup"><span data-stu-id="89e80-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="89e80-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89e80-109">EXAMPLES</span></span>

### <span data-ttu-id="89e80-110">Esempio 1: Avviare il backup di un elemento di backup</span><span class="sxs-lookup"><span data-stu-id="89e80-110">Example 1: Start a backup for a Backup item</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $NamedContainer = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "pstestv2vm1" -VaultId $vault.ID
PS C:\> $Item = Get-AzRecoveryServicesBackupItem -Container $NamedContainer -WorkloadType AzureVM -VaultId $vault.ID
PS C:\> $Job = Backup-AzRecoveryServicesBackupItem -Item $Item -VaultId $vault.ID
PS C:\> $Job
Operation        Status               StartTime            EndTime                   JOBID
------------     ---------            ------               ---------                 -------
pstestv2vm1      Backup               InProgress           4/23/2016 5:00:30 PM      cf4b3ef5-2fac-4c8e-a215-d2eba4124f27
```

<span data-ttu-id="89e80-111">Il primo comando ottiene il contenitore Backup del tipo AzureVM denominato pstestv2vm1 e quindi lo archivia nella variabile $NamedContainer variabile.</span><span class="sxs-lookup"><span data-stu-id="89e80-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="89e80-112">Il secondo comando recupera l'elemento di backup corrispondente al contenitore in $NamedContainer e quindi lo archivia nella $Item variabile.</span><span class="sxs-lookup"><span data-stu-id="89e80-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="89e80-113">L'ultimo comando attiva il processo di backup per l'elemento di backup in $Item.</span><span class="sxs-lookup"><span data-stu-id="89e80-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="89e80-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="89e80-114">Example 2</span></span>

<span data-ttu-id="89e80-115">Avvia il backup di un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="89e80-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="89e80-116">(autogenerated)</span><span class="sxs-lookup"><span data-stu-id="89e80-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="89e80-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89e80-117">PARAMETERS</span></span>

### <span data-ttu-id="89e80-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="89e80-118">-BackupType</span></span>

<span data-ttu-id="89e80-119">Tipo di backup da eseguire</span><span class="sxs-lookup"><span data-stu-id="89e80-119">Type of backup to be performed</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupType
Parameter Sets: (All)
Aliases:
Accepted values: Full, Differential, Log, CopyOnlyFull

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89e80-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89e80-120">-DefaultProfile</span></span>

<span data-ttu-id="89e80-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89e80-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89e80-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="89e80-122">-EnableCompression</span></span>

<span data-ttu-id="89e80-123">Se è necessaria l'abilitazione della compressione</span><span class="sxs-lookup"><span data-stu-id="89e80-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="89e80-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="89e80-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="89e80-125">Specifica una scadenza per il punto di ripristino come oggetto DateTime, se non viene assegnato un valore accetta il valore predefinito di 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="89e80-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="89e80-126">Applicabile a VM, SQL (solo per tipo di backup Copy-only-full), elementi di backup AFS.</span><span class="sxs-lookup"><span data-stu-id="89e80-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e80-127">-Item</span><span class="sxs-lookup"><span data-stu-id="89e80-127">-Item</span></span>

<span data-ttu-id="89e80-128">Specifica un elemento di backup per cui questo cmdlet avvia un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="89e80-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e80-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="89e80-129">-VaultId</span></span>

<span data-ttu-id="89e80-130">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="89e80-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="89e80-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="89e80-131">-Confirm</span></span>

<span data-ttu-id="89e80-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="89e80-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="89e80-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="89e80-133">-WhatIf</span></span>

<span data-ttu-id="89e80-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="89e80-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="89e80-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89e80-135">CommonParameters</span></span>
<span data-ttu-id="89e80-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89e80-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89e80-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89e80-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89e80-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="89e80-138">INPUTS</span></span>

### <span data-ttu-id="89e80-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="89e80-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="89e80-140">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="89e80-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="89e80-141">System.String</span><span class="sxs-lookup"><span data-stu-id="89e80-141">System.String</span></span>

## <span data-ttu-id="89e80-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89e80-142">OUTPUTS</span></span>

### <span data-ttu-id="89e80-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="89e80-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="89e80-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="89e80-144">NOTES</span></span>

## <span data-ttu-id="89e80-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89e80-145">RELATED LINKS</span></span>

[<span data-ttu-id="89e80-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="89e80-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="89e80-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89e80-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="89e80-148">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="89e80-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
