---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: F671A7CC-2A27-460E-B064-2FBF1B9C6A0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/wait-azurermrecoveryservicesbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Wait-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 377250dcc8cbeb3727e7d2bf3f0dd0a8581d6401
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518607"
---
# <span data-ttu-id="31d35-101">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="31d35-101">Wait-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="31d35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31d35-102">SYNOPSIS</span></span>
<span data-ttu-id="31d35-103">Attende il completamento di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="31d35-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31d35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31d35-104">SYNTAX</span></span>

```
Wait-AzureRmRecoveryServicesBackupJob [-Job] <Object> [[-Timeout] <Int64>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31d35-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31d35-105">DESCRIPTION</span></span>
<span data-ttu-id="31d35-106">Il cmdlet **wait-AzureRmRecoveryServicesBackupJob** attende il completamento di un processo di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="31d35-106">The **Wait-AzureRmRecoveryServicesBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="31d35-107">I processi di backup possono richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="31d35-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="31d35-108">Se si esegue un processo di backup come parte di uno script, è consigliabile forzare lo script ad attendere il completamento del processo prima che continui ad altre attività.</span><span class="sxs-lookup"><span data-stu-id="31d35-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="31d35-109">Uno script che include questo cmdlet può essere più semplice di uno che esegue il polling del servizio di backup per lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="31d35-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>
<span data-ttu-id="31d35-110">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="31d35-110">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="31d35-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31d35-111">EXAMPLES</span></span>

### <span data-ttu-id="31d35-112">Esempio 1: attendere il completamento di un processo</span><span class="sxs-lookup"><span data-stu-id="31d35-112">Example 1: Wait for a job to finish</span></span>
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

<span data-ttu-id="31d35-113">Questo script esegue il polling del primo processo che è attualmente in corso fino al completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="31d35-113">This script polls the first job that is currently in progress until the job has completed.</span></span>

## <span data-ttu-id="31d35-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31d35-114">PARAMETERS</span></span>

### <span data-ttu-id="31d35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d35-115">-DefaultProfile</span></span>
<span data-ttu-id="31d35-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31d35-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d35-117">-Job</span><span class="sxs-lookup"><span data-stu-id="31d35-117">-Job</span></span>
<span data-ttu-id="31d35-118">Specifica il processo da attendere.</span><span class="sxs-lookup"><span data-stu-id="31d35-118">Specifies the job to wait for.</span></span>
<span data-ttu-id="31d35-119">Per ottenere un oggetto **BackupJob** , usa il cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="31d35-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="31d35-120">-Timeout</span><span class="sxs-lookup"><span data-stu-id="31d35-120">-Timeout</span></span>
<span data-ttu-id="31d35-121">Specifica il tempo massimo, in secondi, in cui questo cmdlet attende il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="31d35-121">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="31d35-122">È consigliabile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="31d35-122">It is recommended to specify a time-out value.</span></span>

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

### <span data-ttu-id="31d35-123">-VaultId</span><span class="sxs-lookup"><span data-stu-id="31d35-123">-VaultId</span></span>
<span data-ttu-id="31d35-124">ID ARM dell'archivio servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="31d35-124">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="31d35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d35-125">CommonParameters</span></span>
<span data-ttu-id="31d35-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31d35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d35-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d35-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d35-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31d35-128">INPUTS</span></span>

### <span data-ttu-id="31d35-129">System. Object</span><span class="sxs-lookup"><span data-stu-id="31d35-129">System.Object</span></span>
<span data-ttu-id="31d35-130">Parameters: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31d35-130">Parameters: Job (ByValue)</span></span>

### <span data-ttu-id="31d35-131">System. String</span><span class="sxs-lookup"><span data-stu-id="31d35-131">System.String</span></span>
<span data-ttu-id="31d35-132">Parametri: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="31d35-132">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="31d35-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31d35-133">OUTPUTS</span></span>

### <span data-ttu-id="31d35-134">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="31d35-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="31d35-135">Note</span><span class="sxs-lookup"><span data-stu-id="31d35-135">NOTES</span></span>

## <span data-ttu-id="31d35-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31d35-136">RELATED LINKS</span></span>

[<span data-ttu-id="31d35-137">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="31d35-137">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

