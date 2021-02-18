---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 707A3E57-AF46-44B3-A491-89554900EF03
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupjobdetail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupJobDetail.md
ms.openlocfilehash: 6c12cccff6305c96bf2df037e32b8af35170454a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192983"
---
# <span data-ttu-id="2a1d3-101">Get-AzRecoveryServicesBackupJobDetail</span><span class="sxs-lookup"><span data-stu-id="2a1d3-101">Get-AzRecoveryServicesBackupJobDetail</span></span>

## <span data-ttu-id="2a1d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a1d3-102">SYNOPSIS</span></span>

<span data-ttu-id="2a1d3-103">Recupera i dettagli per un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-103">Gets details for a Backup job.</span></span>

## <span data-ttu-id="2a1d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a1d3-104">SYNTAX</span></span>

### <span data-ttu-id="2a1d3-105">JobFilterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2a1d3-105">JobFilterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-Job] <JobBase> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2a1d3-106">IdFilterSet</span><span class="sxs-lookup"><span data-stu-id="2a1d3-106">IdFilterSet</span></span>
```
Get-AzRecoveryServicesBackupJobDetail [-JobId] <String> [-UseSecondaryRegion]
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a1d3-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2a1d3-107">DESCRIPTION</span></span>

<span data-ttu-id="2a1d3-108">Il cmdlet **Get-AzRecoveryServicesBackupJobDetail** ottiene i dettagli del processo di Backup di Azure per un processo specificato.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-108">The **Get-AzRecoveryServicesBackupJobDetail** cmdlet gets Azure Backup job details for a specified job.</span></span>
<span data-ttu-id="2a1d3-109">Impostare il contesto del vault usando il parametro -VaultId.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-109">Set the vault context by using the -VaultId parameter.</span></span>

<span data-ttu-id="2a1d3-110">Avviso: **l'alias Get-AzRecoveryServicesBackupJobDetails** verrà rimosso in una versione successiva delle modifiche.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-110">Warning: **Get-AzRecoveryServicesBackupJobDetails** alias will be removed in a future breaking change release.</span></span>

## <span data-ttu-id="2a1d3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a1d3-111">EXAMPLES</span></span>

### <span data-ttu-id="2a1d3-112">Esempio 1: Ottenere i dettagli del processo di backup per i processi non riusciti</span><span class="sxs-lookup"><span data-stu-id="2a1d3-112">Example 1: Get Backup job details for failed jobs</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Jobs = Get-AzRecoveryServicesBackupJob -Status Failed -VaultId $vault.ID
PS C:\> $JobDetails = Get-AzRecoveryServicesBackupJobDetail -Job $Jobs[0] -VaultId $vault.ID
PS C:\> $JobDetails.ErrorDetails
```

<span data-ttu-id="2a1d3-113">Il primo comando recupera il vault pertinente.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-113">The first command fetches the relevant vault.</span></span> <span data-ttu-id="2a1d3-114">Il secondo comando recupera una matrice di processi non riusciti nel vault e quindi li archivia nella $Jobs matrice.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-114">The second command gets an array of failed jobs in the vault, and then stores them in the $Jobs array.</span></span>
<span data-ttu-id="2a1d3-115">Il terzo comando recupera i dettagli del primo processo non riuscito in $Jobs e quindi li archivia nella $JobDetails variabile.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-115">The third command gets the job details for the 1st failed job in $Jobs, and then stores them in the $JobDetails variable.</span></span>
<span data-ttu-id="2a1d3-116">Il comando finale visualizza i dettagli degli errori per i processi non riusciti.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-116">The final command displays error details for the failed jobs.</span></span>

## <span data-ttu-id="2a1d3-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a1d3-117">PARAMETERS</span></span>

### <span data-ttu-id="2a1d3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a1d3-118">-DefaultProfile</span></span>

<span data-ttu-id="2a1d3-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a1d3-120">-Job</span><span class="sxs-lookup"><span data-stu-id="2a1d3-120">-Job</span></span>

<span data-ttu-id="2a1d3-121">Specifica il processo da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-121">Specifies the job to get.</span></span>
<span data-ttu-id="2a1d3-122">Per ottenere un **oggetto BackupJob,** usare il cmdlet **Get-AzRecoveryServicesBackupJob.**</span><span class="sxs-lookup"><span data-stu-id="2a1d3-122">To obtain a **BackupJob** object, use the **Get-AzRecoveryServicesBackupJob** cmdlet.</span></span>

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

### <span data-ttu-id="2a1d3-123">-JobId</span><span class="sxs-lookup"><span data-stu-id="2a1d3-123">-JobId</span></span>

<span data-ttu-id="2a1d3-124">Specifica l'ID di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-124">Specifies the ID of a Backup job.</span></span>
<span data-ttu-id="2a1d3-125">L'ID è la proprietà JobId di un **oggetto Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase.**</span><span class="sxs-lookup"><span data-stu-id="2a1d3-125">The ID is the JobId property of a **Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase** object.</span></span>

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

### <span data-ttu-id="2a1d3-126">-VaultId</span><span class="sxs-lookup"><span data-stu-id="2a1d3-126">-VaultId</span></span>

<span data-ttu-id="2a1d3-127">ARM ID del Vault dei servizi di ripristino.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-127">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="2a1d3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a1d3-128">CommonParameters</span></span>
<span data-ttu-id="2a1d3-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a1d3-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a1d3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a1d3-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="2a1d3-131">INPUTS</span></span>

### <span data-ttu-id="2a1d3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="2a1d3-132">System.String</span></span>

## <span data-ttu-id="2a1d3-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a1d3-133">OUTPUTS</span></span>

### <span data-ttu-id="2a1d3-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="2a1d3-134">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="2a1d3-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="2a1d3-135">NOTES</span></span>

## <span data-ttu-id="2a1d3-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a1d3-136">RELATED LINKS</span></span>

[<span data-ttu-id="2a1d3-137">Get-AzRecoveryServicesBackupJob</span><span class="sxs-lookup"><span data-stu-id="2a1d3-137">Get-AzRecoveryServicesBackupJob</span></span>](./Get-AzRecoveryServicesBackupJob.md)
