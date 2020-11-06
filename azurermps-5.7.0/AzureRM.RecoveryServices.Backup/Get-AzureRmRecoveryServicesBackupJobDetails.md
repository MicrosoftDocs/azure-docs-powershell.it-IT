---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupjobdetails
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupJobDetails.md
ms.openlocfilehash: 133a779a1227c74830fdae69b52db321a63a12e6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509752"
---
# <span data-ttu-id="93eb8-101">Get-AzureRmRecoveryServicesBackupJobDetails</span><span class="sxs-lookup"><span data-stu-id="93eb8-101">Get-AzureRmRecoveryServicesBackupJobDetails</span></span>

## <span data-ttu-id="93eb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93eb8-102">SYNOPSIS</span></span>
<span data-ttu-id="93eb8-103">Ottiene i dettagli per un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="93eb8-103">Gets details for a Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93eb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93eb8-104">SYNTAX</span></span>

### <span data-ttu-id="93eb8-105">JobFilterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="93eb8-105">JobFilterSet (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-Job] <JobBase> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93eb8-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="93eb8-106">IdFilterSet</span></span>
```
Get-AzureRmRecoveryServicesBackupJobDetails [-JobId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="93eb8-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93eb8-107">DESCRIPTION</span></span>
<span data-ttu-id="93eb8-108">Il cmdlet **Get-AzureRmRecoveryServicesBackupJobDetails** ottiene i dettagli del processo di backup di Azure per un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="93eb8-108">The **Get-AzureRmRecoveryServicesBackupJobDetails** cmdlet gets Azure Backup job details for a specified job.</span></span>

<span data-ttu-id="93eb8-109">Impostare il contesto del Vault usando il cmdlet Set-AzureRmRecoveryServicesVaultContext prima di usare il cmdlet corrente.</span><span class="sxs-lookup"><span data-stu-id="93eb8-109">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="93eb8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93eb8-110">EXAMPLES</span></span>

### <span data-ttu-id="93eb8-111">Esempio 1: ottenere i dettagli del processo di backup per i processi non riusciti</span><span class="sxs-lookup"><span data-stu-id="93eb8-111">Example 1: Get Backup job details for failed jobs</span></span>
```
PS C:\>$Jobs = Get-AzureRmRecoveryServicesBackupJob -Status Failed
PS C:\> $JobDetails = Get-AzureRmRecoveryServicesBackupJobDetails -Job $Jobs[0]
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="93eb8-112">Il primo comando consente di ottenere una matrice di processi non riusciti nel Vault e quindi di archiviarli nella matrice $Jobs.</span><span class="sxs-lookup"><span data-stu-id="93eb8-112">The first command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>

<span data-ttu-id="93eb8-113">Il secondo comando consente di ottenere i dettagli del processo per i processi non riusciti in $Jobs e quindi di archiviarli nella variabile $JobDetails.</span><span class="sxs-lookup"><span data-stu-id="93eb8-113">The second command gets the job details for the failed jobs in $Jobs, and then stores them in the $JobDetails variable.</span></span>

<span data-ttu-id="93eb8-114">Il comando finale Visualizza i dettagli degli errori per i processi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="93eb8-114">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="93eb8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93eb8-115">PARAMETERS</span></span>

### <span data-ttu-id="93eb8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93eb8-116">-DefaultProfile</span></span>
<span data-ttu-id="93eb8-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93eb8-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93eb8-118">-Job</span><span class="sxs-lookup"><span data-stu-id="93eb8-118">-Job</span></span>
<span data-ttu-id="93eb8-119">Specifica il processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="93eb8-119">Specifies the job to get.</span></span>
<span data-ttu-id="93eb8-120">Per ottenere un oggetto **BackupJob** , usa il cmdlet Get-AzureRmRecoveryServicesBackupJob.</span><span class="sxs-lookup"><span data-stu-id="93eb8-120">To obtain a **BackupJob** object, use the Get-AzureRmRecoveryServicesBackupJob cmdlet.</span></span>

```yaml
Type: JobBase
Parameter Sets: JobFilterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eb8-121">-JobId</span><span class="sxs-lookup"><span data-stu-id="93eb8-121">-JobId</span></span>
<span data-ttu-id="93eb8-122">Specifica l'ID di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="93eb8-122">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="93eb8-123">L'ID è la proprietà InstanceId di un oggetto **BackupJob** .</span><span class="sxs-lookup"><span data-stu-id="93eb8-123">The ID is the InstanceId property of a **BackupJob** object.</span></span>

```yaml
Type: String
Parameter Sets: IdFilterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="93eb8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93eb8-124">CommonParameters</span></span>
<span data-ttu-id="93eb8-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93eb8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93eb8-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93eb8-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93eb8-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93eb8-127">INPUTS</span></span>

### <span data-ttu-id="93eb8-128">Nessuno</span><span class="sxs-lookup"><span data-stu-id="93eb8-128">None</span></span>
<span data-ttu-id="93eb8-129">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="93eb8-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="93eb8-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93eb8-130">OUTPUTS</span></span>

### <span data-ttu-id="93eb8-131">Microsoft. Azure. Commands. RecoveryServices. backup. Cmdlets. Models. JobBase</span><span class="sxs-lookup"><span data-stu-id="93eb8-131">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="93eb8-132">Note</span><span class="sxs-lookup"><span data-stu-id="93eb8-132">NOTES</span></span>

## <span data-ttu-id="93eb8-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93eb8-133">RELATED LINKS</span></span>

[<span data-ttu-id="93eb8-134">Get-AzureRmRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="93eb8-134">Get-AzureRmRecoveryServicesBackupJob</span></span>](./Get-AzureRmRecoveryServicesBackupJob.md)


