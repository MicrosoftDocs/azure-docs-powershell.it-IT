---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 4ae0f9c046cc1383dddeb790e8277dc2429b173b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201016"
---
# <span data-ttu-id="4c2f1-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4c2f1-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="4c2f1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c2f1-102">SYNOPSIS</span></span>

<span data-ttu-id="4c2f1-103">Avvia un backup per un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="4c2f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c2f1-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c2f1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c2f1-105">DESCRIPTION</span></span>

<span data-ttu-id="4c2f1-106">Il cmdlet **backup-AzRecoveryServicesBackupItem** accetta un backup ad hoc di elementi di backup di Azure protetti.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet takes an adhoc backup of protected Azure backup item.</span></span> <span data-ttu-id="4c2f1-107">L'uso di questo cmdlet consente di eseguire un backup iniziale subito dopo l'abilitazione della protezione o di avviare un backup se non è possibile eseguire un backup pianificato.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-107">Using this cmdlet you can do an initial backup immediately after you enable protection or start a backup if a scheduled backup fails.</span></span> <span data-ttu-id="4c2f1-108">Questo cmdlet può essere usato anche per la conservazione personalizzata con o senza data di scadenza: vedere il testo della Guida parametri per ulteriori dettagli.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-108">This cmdlet can also be used for custom retention with or without expiry date - refer parameters help text for more details.</span></span> 

## <span data-ttu-id="4c2f1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c2f1-109">EXAMPLES</span></span>

### <span data-ttu-id="4c2f1-110">Esempio 1: avviare un backup per un elemento di backup</span><span class="sxs-lookup"><span data-stu-id="4c2f1-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="4c2f1-111">Il primo comando ottiene il contenitore di backup di tipo AzureVM denominato pstestv2vm1 e lo archivia nella variabile $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="4c2f1-112">Il secondo comando ottiene l'elemento di backup corrispondente al contenitore in $NamedContainer e lo archivia nella variabile $Item.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="4c2f1-113">L'ultimo comando attiva il processo di backup per l'elemento di backup in $Item.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

### <span data-ttu-id="4c2f1-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c2f1-114">Example 2</span></span>

<span data-ttu-id="4c2f1-115">Avvia un backup per un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-115">Starts a backup for a Backup item.</span></span> <span data-ttu-id="4c2f1-116">AutoGenerated</span><span class="sxs-lookup"><span data-stu-id="4c2f1-116">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Backup-AzRecoveryServicesBackupItem -ExpiryDateTimeUTC <DateTime> -Item $Item -VaultId $vault.ID
```

## <span data-ttu-id="4c2f1-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c2f1-117">PARAMETERS</span></span>

### <span data-ttu-id="4c2f1-118">-BackupType</span><span class="sxs-lookup"><span data-stu-id="4c2f1-118">-BackupType</span></span>

<span data-ttu-id="4c2f1-119">Tipo di backup da eseguire</span><span class="sxs-lookup"><span data-stu-id="4c2f1-119">Type of backup to be performed</span></span>

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

### <span data-ttu-id="4c2f1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c2f1-120">-DefaultProfile</span></span>

<span data-ttu-id="4c2f1-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c2f1-122">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="4c2f1-122">-EnableCompression</span></span>

<span data-ttu-id="4c2f1-123">Se è necessaria l'abilitazione della compressione</span><span class="sxs-lookup"><span data-stu-id="4c2f1-123">If enabling compression is required</span></span>

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

### <span data-ttu-id="4c2f1-124">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="4c2f1-124">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="4c2f1-125">Specifica un tempo di scadenza per il punto di recupero come oggetto DateTime, se non viene specificato il valore predefinito di 30 giorni.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-125">Specifies an expiry time for the Recovery point as a DateTime object, if nothing is given it takes the default value of  30 days.</span></span> <span data-ttu-id="4c2f1-126">Applicabile a VM, SQL (solo per il tipo di backup completo di sola copia), gli elementi di backup AFS.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-126">Applicable to VM, SQL (for only Copy-only-full backup type), AFS backup items.</span></span>

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

### <span data-ttu-id="4c2f1-127">-Elemento</span><span class="sxs-lookup"><span data-stu-id="4c2f1-127">-Item</span></span>

<span data-ttu-id="4c2f1-128">Specifica un elemento di backup per il quale questo cmdlet avvia un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-128">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="4c2f1-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="4c2f1-129">-VaultId</span></span>

<span data-ttu-id="4c2f1-130">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-130">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="4c2f1-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c2f1-131">-Confirm</span></span>

<span data-ttu-id="4c2f1-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c2f1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c2f1-133">-WhatIf</span></span>

<span data-ttu-id="4c2f1-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-134">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="4c2f1-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c2f1-135">CommonParameters</span></span>
<span data-ttu-id="4c2f1-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c2f1-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c2f1-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c2f1-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c2f1-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c2f1-138">INPUTS</span></span>

### <span data-ttu-id="4c2f1-139">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="4c2f1-139">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="4c2f1-140">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4c2f1-140">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="4c2f1-141">System. String</span><span class="sxs-lookup"><span data-stu-id="4c2f1-141">System.String</span></span>

## <span data-ttu-id="4c2f1-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c2f1-142">OUTPUTS</span></span>

### <span data-ttu-id="4c2f1-143">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="4c2f1-143">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="4c2f1-144">Note</span><span class="sxs-lookup"><span data-stu-id="4c2f1-144">NOTES</span></span>

## <span data-ttu-id="4c2f1-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c2f1-145">RELATED LINKS</span></span>

[<span data-ttu-id="4c2f1-146">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="4c2f1-146">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="4c2f1-147">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4c2f1-147">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="4c2f1-148">Ripristinare-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="4c2f1-148">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
