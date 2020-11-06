---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: A8FDC5A3-F309-49B3-B417-8E0A1535BAF4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Stop-AzureRmRecoveryServicesBackupJob.md
ms.openlocfilehash: 63d90aa5f98f6710702a70e9609c7625626e34c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521157"
---
# <span data-ttu-id="d0cbd-101">Stop-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d0cbd-101">Stop-AzureRmRecoveryServicesBackupJob</span></span>

## <span data-ttu-id="d0cbd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d0cbd-102">SYNOPSIS</span></span>
<span data-ttu-id="d0cbd-103">Annulla un processo in corso.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-103">Cancels a running job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0cbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0cbd-104">SYNTAX</span></span>

### <span data-ttu-id="d0cbd-105">JobFilterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0cbd-105">JobFilterSet (Default)</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0cbd-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="d0cbd-106">IdFilterSet</span></span>
```
Stop-AzureRmRecoveryServicesBackupJob [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0cbd-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d0cbd-107">DESCRIPTION</span></span>
<span data-ttu-id="d0cbd-108">Il cmdlet **Stop-AzureRmRecoveryServicesBackupJob** Annulla un processo di backup di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-108">The **Stop-AzureRmRecoveryServicesBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="d0cbd-109">Questo cmdlet consente di arrestare un processo che impiega troppo tempo e blocca altre attività.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-109">Use this cmdlet to stop a job that takes too long and blocks other activities.</span></span>

<span data-ttu-id="d0cbd-110">È possibile annullare solo i tipi di processo di backup e ripristino.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-110">You can cancel only Backup and Restore job types.</span></span>

<span data-ttu-id="d0cbd-111">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="d0cbd-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0cbd-112">EXAMPLES</span></span>

### <span data-ttu-id="d0cbd-113">Esempio 1: interrompere un processo di backup</span><span class="sxs-lookup"><span data-stu-id="d0cbd-113">Example 1: Stop a backup job</span></span>
```
PS C:\>$Job = Get-AzureRmRecoveryServicesBackupJob -Operation Backup
PS C:\> Stop-AzureRmRecoveryServicesBackupJob -JobID $Job.InstanceId
```

<span data-ttu-id="d0cbd-114">Il primo comando ottiene un processo di backup e quindi archivia il processo nella variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-114">The first command gets a backup job, and then stores the job in the $Job variable.</span></span>

<span data-ttu-id="d0cbd-115">L'ultimo comando interrompe il processo specificando l'ID istanza del processo di backup in $Job.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-115">The last command stops the job by specifying the Instance ID of the backup job in $Job.</span></span>

## <span data-ttu-id="d0cbd-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d0cbd-116">PARAMETERS</span></span>

### <span data-ttu-id="d0cbd-117">-Job</span><span class="sxs-lookup"><span data-stu-id="d0cbd-117">-Job</span></span>
<span data-ttu-id="d0cbd-118">Specifica un processo che questo cmdlet Annulla.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-118">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="d0cbd-119">Per ottenere un oggetto **BackupJob** , usa il cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-119">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

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

### <span data-ttu-id="d0cbd-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="d0cbd-120">-JobId</span></span>
<span data-ttu-id="d0cbd-121">Specifica l'ID del processo da annullare.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-121">Specifies the ID of the job to cancel.</span></span>
<span data-ttu-id="d0cbd-122">L'ID è la proprietà InstanceId di un oggetto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="d0cbd-122">The ID is the InstanceId property of a **BackupJob** object.</span></span>
<span data-ttu-id="d0cbd-123">Per ottenere un oggetto **BackupJob** , USA Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-123">To obtain an **BackupJob** object, use Get-AzureRmRecoveryServicesBackupJob.</span></span>

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

### <span data-ttu-id="d0cbd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0cbd-124">-DefaultProfile</span></span>
<span data-ttu-id="d0cbd-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0cbd-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0cbd-126">CommonParameters</span></span>
<span data-ttu-id="d0cbd-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0cbd-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0cbd-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0cbd-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0cbd-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d0cbd-129">INPUTS</span></span>

## <span data-ttu-id="d0cbd-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0cbd-130">OUTPUTS</span></span>

### <span data-ttu-id="d0cbd-131">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="d0cbd-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="d0cbd-132">Note</span><span class="sxs-lookup"><span data-stu-id="d0cbd-132">NOTES</span></span>

## <span data-ttu-id="d0cbd-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0cbd-133">RELATED LINKS</span></span>

[<span data-ttu-id="d0cbd-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d0cbd-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)

[<span data-ttu-id="d0cbd-135">Wait-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="d0cbd-135">Wait-AzureRmRecoveryServicesBackupJob</span></span>](./Wait-AzureRmRecoveryServicesBackupJob.md)


