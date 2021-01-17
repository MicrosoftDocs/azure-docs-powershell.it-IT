---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/stop-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Stop-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: 41234c91d5c833f15a4914d2af2de93c9c5bf288
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98378360"
---
# <span data-ttu-id="db55e-101">Stop-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="db55e-101">Stop-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="db55e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db55e-102">SYNOPSIS</span></span>
<span data-ttu-id="db55e-103">Annulla un processo in corso.</span><span class="sxs-lookup"><span data-stu-id="db55e-103">Cancels a running job.</span></span>

## <span data-ttu-id="db55e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db55e-104">SYNTAX</span></span>

### <span data-ttu-id="db55e-105">JobFilterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="db55e-105">JobFilterSet (Default)</span></span>
```
Stop-AzRecoveryServicesBackupJob [-Job] <JobBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="db55e-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="db55e-106">IdFilterSet</span></span>
```
Stop-AzRecoveryServicesBackupJob [-JobId] <String> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db55e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db55e-107">DESCRIPTION</span></span>
<span data-ttu-id="db55e-108">Il cmdlet **Stop-AzRecoveryServicesBackupJob** Annulla un processo di backup di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="db55e-108">The **Stop-AzRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="db55e-109">Questo cmdlet consente di arrestare un processo che impiega troppo tempo e blocca altre attività.</span><span class="sxs-lookup"><span data-stu-id="db55e-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="db55e-110">È possibile annullare solo i tipi di processo di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="db55e-110">You can cancel only Backup and Restore job types.</span></span>
<span data-ttu-id="db55e-111">Impostare il contesto del Vault usando il cmdlet Set-AzRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="db55e-111">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="db55e-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db55e-112">EXAMPLES</span></span>

### <span data-ttu-id="db55e-113">Esempio 1: interrompere un processo di backup</span><span class="sxs-lookup"><span data-stu-id="db55e-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="db55e-114">Il primo comando ottiene un processo di backup e quindi archivia il processo nella variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="db55e-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>
<span data-ttu-id="db55e-115">L'ultimo comando interrompe il processo specificando l'ID istanza del processo di backup in $Job.</span><span class="sxs-lookup"><span data-stu-id="db55e-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="db55e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db55e-116">PARAMETERS</span></span>

### <span data-ttu-id="db55e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db55e-117">-DefaultProfile</span></span>
<span data-ttu-id="db55e-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db55e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db55e-119">-Job</span><span class="sxs-lookup"><span data-stu-id="db55e-119">-Job</span></span>
<span data-ttu-id="db55e-120">Specifica un processo che questo cmdlet Annulla.</span><span class="sxs-lookup"><span data-stu-id="db55e-120">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="db55e-121">Per ottenere un oggetto **BackupJob** , usa il cmdlet Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="db55e-121">To obtain a **BackupJob** object, use the Get-AzRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase
Parameter Sets: JobFilterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db55e-122">-JobId</span><span class="sxs-lookup"><span data-stu-id="db55e-122">-JobId</span></span>
<span data-ttu-id="db55e-123">Specifica l'ID del processo da annullare.</span><span class="sxs-lookup"><span data-stu-id="db55e-123">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="db55e-124">L'ID è la proprietà InstanceId di un oggetto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="db55e-124">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="db55e-125">Per ottenere un oggetto **BackupJob** , USA Get-AzRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="db55e-125">To obtain an **BackupJob** object, use Get-AzRecoveryServicesBackupJob.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFilterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="db55e-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="db55e-126">-VaultId</span></span>
<span data-ttu-id="db55e-127">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="db55e-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="db55e-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="db55e-128">-Confirm</span></span>
<span data-ttu-id="db55e-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db55e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db55e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db55e-130">-WhatIf</span></span>
<span data-ttu-id="db55e-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="db55e-131">Shows what would happen if the cmdlet runs.</span></span>

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

### <span data-ttu-id="db55e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db55e-132">CommonParameters</span></span>
<span data-ttu-id="db55e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db55e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db55e-134">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db55e-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db55e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db55e-135">INPUTS</span></span>

### <span data-ttu-id="db55e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="db55e-136">System.String</span></span>

## <span data-ttu-id="db55e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db55e-137">OUTPUTS</span></span>

### <span data-ttu-id="db55e-138">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="db55e-138">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="db55e-139">Note</span><span class="sxs-lookup"><span data-stu-id="db55e-139">NOTES</span></span>

## <span data-ttu-id="db55e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db55e-140">RELATED LINKS</span></span>

[<span data-ttu-id="db55e-141">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="db55e-141">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)

[<span data-ttu-id="db55e-142">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="db55e-142">Wait-AzRecoveryServicesBackupJob</span></span>](./Wait-AzRecoveryServicesBackupJob.md)


