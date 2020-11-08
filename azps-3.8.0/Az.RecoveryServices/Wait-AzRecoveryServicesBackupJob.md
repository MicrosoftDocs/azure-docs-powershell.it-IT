---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/wait-azrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Wait-AzRecoveryServicesBackupJob.md
ms.openlocfilehash: d494169c989096ce562858c500289527479d42dd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021464"
---
# <span data-ttu-id="46470-101">Wait-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="46470-101">Wait-AzRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="46470-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="46470-102">SYNOPSIS</span></span>

<span data-ttu-id="46470-103">Attende il completamento di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="46470-103">Waits for a Backup job to finish.</span></span>

## <span data-ttu-id="46470-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="46470-104">SYNTAX</span></span>

```
Wait-AzRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46470-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="46470-105">DESCRIPTION</span></span>

<span data-ttu-id="46470-106">Il cmdlet **wait-AzRecoveryServicesBackupJob** attende il completamento di un processo di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="46470-106">The **Wait-AzRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="46470-107">I processi di backup possono richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="46470-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="46470-108">Se si esegue un processo di backup come parte di uno script, è consigliabile forzare lo script ad attendere il completamento del processo prima che continui ad altre attività.</span><span class="sxs-lookup"><span data-stu-id="46470-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="46470-109">Uno script che include questo cmdlet può essere più semplice di uno che esegue il polling del servizio di backup per lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="46470-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="46470-110">Imposta il contesto del Vault usando il parametro-VaultId.</span><span class="sxs-lookup"><span data-stu-id="46470-110">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="46470-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="46470-111">EXAMPLES</span></span>

### <span data-ttu-id="46470-112">Esempio 1: attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="46470-112">Example 1: Wait for a job to finish</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status InProgress -VaultId $vault.ID
PS C:\> Wait-AzRecoveryServicesBackupJob -Job $Jobs[0] -VaultId $vault.ID -Timeout 3600
```

<span data-ttu-id="46470-113">Questo script esegue il polling del primo processo che è attualmente in corso fino a quando il processo non è stato completato o il periodo di timeout di 1 ora è scaduto.</span><span class="sxs-lookup"><span data-stu-id="46470-113">This script polls the first job that is currently in progress until the job has completed or timeout period of 1 hour expired.</span></span>

## <span data-ttu-id="46470-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="46470-114">PARAMETERS</span></span>

### <span data-ttu-id="46470-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46470-115">-DefaultProfile</span></span>

<span data-ttu-id="46470-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="46470-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46470-117">-Job</span><span class="sxs-lookup"><span data-stu-id="46470-117">-Job</span></span>

<span data-ttu-id="46470-118">Specifica il processo da attendere.</span><span class="sxs-lookup"><span data-stu-id="46470-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="46470-119">Per ottenere un oggetto **BackupJob** , usa il cmdlet **Get-AzRecoveryServicesBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="46470-119">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="46470-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="46470-120">-Timeout</span></span>

<span data-ttu-id="46470-121">Specifica il tempo massimo, in secondi, in cui questo cmdlet attende il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="46470-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="46470-122">È consigliabile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="46470-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="46470-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="46470-123">-VaultId</span></span>

<span data-ttu-id="46470-124">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="46470-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="46470-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46470-125">CommonParameters</span></span>
<span data-ttu-id="46470-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46470-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46470-127">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="46470-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46470-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="46470-128">INPUTS</span></span>

### <span data-ttu-id="46470-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="46470-129">System.Object</span></span>

### <span data-ttu-id="46470-130">System. String</span><span class="sxs-lookup"><span data-stu-id="46470-130">System.String</span></span>

## <span data-ttu-id="46470-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="46470-131">OUTPUTS</span></span>

### <span data-ttu-id="46470-132">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="46470-132">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="46470-133">Note</span><span class="sxs-lookup"><span data-stu-id="46470-133">NOTES</span></span>

## <span data-ttu-id="46470-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="46470-134">RELATED LINKS</span></span>

[<span data-ttu-id="46470-135">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="46470-135">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
