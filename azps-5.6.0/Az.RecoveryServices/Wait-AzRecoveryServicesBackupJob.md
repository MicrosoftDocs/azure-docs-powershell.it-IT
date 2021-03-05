---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: e0b3dc87ffdfc86f39f201b6384f38ce8ca1c70a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960142"
---
# <span data-ttu-id="6d7af-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6d7af-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="6d7af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d7af-102">SYNOPSIS</span></span>

<span data-ttu-id="6d7af-103">Attende il completamento di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="6d7af-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="6d7af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6d7af-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6d7af-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6d7af-105">DESCRIPTION</span></span>

<span data-ttu-id="6d7af-106">Il cmdlet **Wait-AzRecoveryServicesBackupJob** attende il completamento di un processo di Backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7af-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="6d7af-107">I processi di backup possono richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="6d7af-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="6d7af-108">Se si esegue un processo di backup come parte di uno script, è possibile forzare l'esecuzione dello script in attesa del completamento del processo prima che continui ad altre attività.</span><span class="sxs-lookup"><span data-stu-id="6d7af-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="6d7af-109">Uno script che include questo cmdlet può essere più semplice di uno che esegue il polling dello stato del processo nel servizio di backup.</span><span class="sxs-lookup"><span data-stu-id="6d7af-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="6d7af-110">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="6d7af-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="6d7af-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6d7af-111">EXAMPLES</span></span>

### <span data-ttu-id="6d7af-112">Esempio 1: Attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="6d7af-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="6d7af-113">Questo script esegue il polling del primo processo attualmente in corso finché il processo non viene completato o non scade il periodo di timeout di 1 ora.</span><span class="sxs-lookup"><span data-stu-id="6d7af-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="6d7af-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6d7af-114">PARAMETERS</span></span>

### <span data-ttu-id="6d7af-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d7af-115">-DefaultProfile</span></span>

<span data-ttu-id="6d7af-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6d7af-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d7af-117">-Job</span><span class="sxs-lookup"><span data-stu-id="6d7af-117">-Job</span></span>

<span data-ttu-id="6d7af-118">Specifica il processo da attendere.</span><span class="sxs-lookup"><span data-stu-id="6d7af-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="6d7af-119">Per ottenere un **oggetto BackupJob,** usare il cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="6d7af-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d7af-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="6d7af-120">-Timeout</span></span>

<span data-ttu-id="6d7af-121">Specifica il tempo massimo, in secondi, durante il quale il cmdlet attende il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="6d7af-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="6d7af-122">È consigliabile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="6d7af-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d7af-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6d7af-123">-VaultId</span></span>

<span data-ttu-id="6d7af-124">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="6d7af-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6d7af-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d7af-125">CommonParameters</span></span>
<span data-ttu-id="6d7af-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6d7af-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d7af-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6d7af-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d7af-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="6d7af-128">INPUTS</span></span>

### <span data-ttu-id="6d7af-129">System.Object</span><span class="sxs-lookup"><span data-stu-id="6d7af-129">System.Object</span></span>

### <span data-ttu-id="6d7af-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6d7af-130">System.String</span></span>

## <span data-ttu-id="6d7af-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6d7af-131">OUTPUTS</span></span>

### <span data-ttu-id="6d7af-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="6d7af-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="6d7af-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="6d7af-133">NOTES</span></span>

## <span data-ttu-id="6d7af-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6d7af-134">RELATED LINKS</span></span>

[<span data-ttu-id="6d7af-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="6d7af-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
