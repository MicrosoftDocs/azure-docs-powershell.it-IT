---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 651c1cd08f8a2c711a4a0cec16ddb965ccfa8211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509708"
---
# <span data-ttu-id="ce6d2-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ce6d2-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="ce6d2-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="ce6d2-103">Attende il completamento di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce6d2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce6d2-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce6d2-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce6d2-105">DESCRIPTION</span></span>
<span data-ttu-id="ce6d2-106">Il cmdlet **wait-AzureRmRecoveryServicesBackupJob** attende il completamento di un processo di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="ce6d2-107">I processi di backup possono richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="ce6d2-108">Se si esegue un processo di backup come parte di uno script, è consigliabile forzare lo script ad attendere il completamento del processo prima che continui ad altre attività.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="ce6d2-109">Uno script che include questo cmdlet può essere più semplice di uno che esegue il polling del servizio di backup per lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

<span data-ttu-id="ce6d2-110">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ce6d2-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce6d2-111">EXAMPLES</span></span>

### <span data-ttu-id="ce6d2-112">Esempio 1: attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="ce6d2-112">Example 1: Wait for a job to finish</span></span>
```
PS C:\>
$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status InProgress
    $Job = $Jobs[0]
    while ( $Job.Status -ne Completed )
    {
       Write-Host "Waiting for completion..."
       Start-Sleep -Seconds 10
       $Job = Get-AzureRmBackAzureRmRecoveryServicesBackupJob -Job $Job
    }
   Write-Host "Done!"
    Waiting for completion... 
    Waiting for completion... 
    Waiting for completion... 
    Done!
```

<span data-ttu-id="ce6d2-113">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="ce6d2-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce6d2-114">PARAMETERS</span></span>

### <span data-ttu-id="ce6d2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce6d2-115">-DefaultProfile</span></span>
<span data-ttu-id="ce6d2-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d2-117">-Job</span><span class="sxs-lookup"><span data-stu-id="ce6d2-117">-Job</span></span>
<span data-ttu-id="ce6d2-118">Specifica il processo da attendere.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="ce6d2-119">Per ottenere un oggetto **BackupJob** , usa il cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d2-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="ce6d2-120">-Timeout</span></span>
<span data-ttu-id="ce6d2-121">Specifica il tempo massimo, in secondi, in cui questo cmdlet attende il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="ce6d2-122">È consigliabile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-122">It is recommended to specify a time-out value.</span></span>

```yaml
Type: Int64
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce6d2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce6d2-123">CommonParameters</span></span>
<span data-ttu-id="ce6d2-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce6d2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce6d2-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce6d2-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce6d2-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce6d2-126">INPUTS</span></span>

### <span data-ttu-id="ce6d2-127">Oggetto</span><span class="sxs-lookup"><span data-stu-id="ce6d2-127">Object</span></span>
<span data-ttu-id="ce6d2-128">Il parametro "Job" accetta il valore di tipo "Object" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="ce6d2-128">Parameter 'Job' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="ce6d2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce6d2-129">OUTPUTS</span></span>

### <span data-ttu-id="ce6d2-130">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ce6d2-130">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

### <span data-ttu-id="ce6d2-131">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase]</span><span class="sxs-lookup"><span data-stu-id="ce6d2-131">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase]</span></span>

## <span data-ttu-id="ce6d2-132">Note</span><span class="sxs-lookup"><span data-stu-id="ce6d2-132">NOTES</span></span>

## <span data-ttu-id="ce6d2-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce6d2-133">RELATED LINKS</span></span>

[<span data-ttu-id="ce6d2-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="ce6d2-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

