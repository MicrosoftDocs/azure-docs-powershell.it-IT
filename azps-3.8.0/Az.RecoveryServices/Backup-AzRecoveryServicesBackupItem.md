---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 04D7317E-2089-4197-909D-89F0CEC4851A
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/backup-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Backup-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: fb2b6c370ee7ce43c877bfac57b64a203e9238cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864379"
---
# <span data-ttu-id="49fe1-101">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="49fe1-101">Backup-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="49fe1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="49fe1-102">SYNOPSIS</span></span>

<span data-ttu-id="49fe1-103">Avvia un backup per un elemento di backup.</span><span class="sxs-lookup"><span data-stu-id="49fe1-103">Starts a backup for a Backup item.</span></span>

## <span data-ttu-id="49fe1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49fe1-104">SYNTAX</span></span>

```
Backup-AzRecoveryServicesBackupItem -Item <ItemBase> [-ExpiryDateTimeUTC <DateTime>] [-BackupType <BackupType>]
 [-EnableCompression] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="49fe1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="49fe1-105">DESCRIPTION</span></span>

<span data-ttu-id="49fe1-106">Il cmdlet **backup-AzRecoveryServicesBackupItem** avvia un backup per un elemento di backup di Azure protetto che non è legato alla pianificazione del backup.</span><span class="sxs-lookup"><span data-stu-id="49fe1-106">The **Backup-AzRecoveryServicesBackupItem** cmdlet starts a backup for a protected Azure Backup item that is not tied to the backup schedule.</span></span>
<span data-ttu-id="49fe1-107">È possibile eseguire un backup iniziale subito dopo l'abilitazione della protezione o avviare un backup dopo un errore di backup pianificato.</span><span class="sxs-lookup"><span data-stu-id="49fe1-107">You can do an initial backup immediately after you enable protection or start a backup after a scheduled backup fails.</span></span>
<span data-ttu-id="49fe1-108">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="49fe1-108">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="49fe1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49fe1-109">EXAMPLES</span></span>

### <span data-ttu-id="49fe1-110">Esempio 1: avviare un backup per un elemento di backup</span><span class="sxs-lookup"><span data-stu-id="49fe1-110">Example 1: Start a backup for a Backup item</span></span>

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

<span data-ttu-id="49fe1-111">Il primo comando ottiene il contenitore di backup di tipo AzureVM denominato pstestv2vm1 e lo archivia nella variabile $NamedContainer.</span><span class="sxs-lookup"><span data-stu-id="49fe1-111">The first command gets the Backup container of type AzureVM named pstestv2vm1, and then stores it in the $NamedContainer variable.</span></span>
<span data-ttu-id="49fe1-112">Il secondo comando ottiene l'elemento di backup corrispondente al contenitore in $NamedContainer e lo archivia nella variabile $Item.</span><span class="sxs-lookup"><span data-stu-id="49fe1-112">The second command gets the Backup item corresponding to the container in $NamedContainer, and then stores it in the $Item variable.</span></span>
<span data-ttu-id="49fe1-113">L'ultimo comando attiva il processo di backup per l'elemento di backup in $Item.</span><span class="sxs-lookup"><span data-stu-id="49fe1-113">The last command triggers the backup job for the Backup item in $Item.</span></span>

## <span data-ttu-id="49fe1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="49fe1-114">PARAMETERS</span></span>

### <span data-ttu-id="49fe1-115">-BackupType</span><span class="sxs-lookup"><span data-stu-id="49fe1-115">-BackupType</span></span>

<span data-ttu-id="49fe1-116">Tipo di backup da eseguire</span><span class="sxs-lookup"><span data-stu-id="49fe1-116">Type of backup to be performed</span></span>

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

### <span data-ttu-id="49fe1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49fe1-117">-DefaultProfile</span></span>

<span data-ttu-id="49fe1-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49fe1-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49fe1-119">-EnableCompression</span><span class="sxs-lookup"><span data-stu-id="49fe1-119">-EnableCompression</span></span>

<span data-ttu-id="49fe1-120">Se è necessaria l'abilitazione della compressione</span><span class="sxs-lookup"><span data-stu-id="49fe1-120">If enabling compression is required</span></span>

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

### <span data-ttu-id="49fe1-121">-ExpiryDateTimeUTC</span><span class="sxs-lookup"><span data-stu-id="49fe1-121">-ExpiryDateTimeUTC</span></span>

<span data-ttu-id="49fe1-122">Specifica un tempo di scadenza come oggetto **DateTime** .</span><span class="sxs-lookup"><span data-stu-id="49fe1-122">Specifies an expiry time as a **DateTime** object.</span></span>

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

### <span data-ttu-id="49fe1-123">-Elemento</span><span class="sxs-lookup"><span data-stu-id="49fe1-123">-Item</span></span>

<span data-ttu-id="49fe1-124">Specifica un elemento di backup per il quale questo cmdlet avvia un'operazione di backup.</span><span class="sxs-lookup"><span data-stu-id="49fe1-124">Specifies a Backup item for which this cmdlet starts a backup operation.</span></span>

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

### <span data-ttu-id="49fe1-125">-VaultId</span><span class="sxs-lookup"><span data-stu-id="49fe1-125">-VaultId</span></span>

<span data-ttu-id="49fe1-126">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="49fe1-126">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="49fe1-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="49fe1-127">-Confirm</span></span>

<span data-ttu-id="49fe1-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="49fe1-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="49fe1-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49fe1-129">-WhatIf</span></span>

<span data-ttu-id="49fe1-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49fe1-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="49fe1-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="49fe1-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="49fe1-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49fe1-132">CommonParameters</span></span>
<span data-ttu-id="49fe1-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49fe1-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49fe1-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="49fe1-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49fe1-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="49fe1-135">INPUTS</span></span>

### <span data-ttu-id="49fe1-136">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="49fe1-136">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="49fe1-137">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="49fe1-137">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="49fe1-138">System. String</span><span class="sxs-lookup"><span data-stu-id="49fe1-138">System.String</span></span>

## <span data-ttu-id="49fe1-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49fe1-139">OUTPUTS</span></span>

### <span data-ttu-id="49fe1-140">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="49fe1-140">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="49fe1-141">Note</span><span class="sxs-lookup"><span data-stu-id="49fe1-141">NOTES</span></span>

## <span data-ttu-id="49fe1-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49fe1-142">RELATED LINKS</span></span>

[<span data-ttu-id="49fe1-143">Get-AzRecoveryServicesBackupContainer</span><span class="sxs-lookup"><span data-stu-id="49fe1-143">Get-AzRecoveryServicesBackupContainer</span></span>](./Get-AzRecoveryServicesBackupContainer.md)

[<span data-ttu-id="49fe1-144">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="49fe1-144">Get-AzRecoveryServicesBackupItem</span></span>](./Get-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="49fe1-145">Ripristinare-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="49fe1-145">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
