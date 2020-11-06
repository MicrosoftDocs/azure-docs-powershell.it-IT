---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 44C5AF58-ADC1-4BC6-9771-3FD8F0480106
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/stop-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Stop-AzureRmBackupJob.md
ms.openlocfilehash: 800b5c6e04e0842113db7fb3494815bcd97ebfb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511943"
---
# <span data-ttu-id="0ec82-101">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="0ec82-101">Stop-AzureRmBackupJob</span></span>

## <span data-ttu-id="0ec82-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ec82-102">SYNOPSIS</span></span>
<span data-ttu-id="0ec82-103">Annulla un processo di backup esistente.</span><span class="sxs-lookup"><span data-stu-id="0ec82-103">Cancels an existing Backup job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ec82-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ec82-104">SYNTAX</span></span>

### <span data-ttu-id="0ec82-105">IdFiltersSet</span><span class="sxs-lookup"><span data-stu-id="0ec82-105">IdFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Vault <AzureRMBackupVault> -JobID <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="0ec82-106">JobFiltersSet</span><span class="sxs-lookup"><span data-stu-id="0ec82-106">JobFiltersSet</span></span>
```
Stop-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ec82-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ec82-107">DESCRIPTION</span></span>
<span data-ttu-id="0ec82-108">Il cmdlet **Stop-AzureRmBackupJob** Annulla un processo di backup di Azure esistente.</span><span class="sxs-lookup"><span data-stu-id="0ec82-108">The **Stop-AzureRmBackupJob** cmdlet cancels an existing Azure Backup job.</span></span>
<span data-ttu-id="0ec82-109">Usa questo parametro per interrompere un processo che impiega troppo tempo e blocca altre attività.</span><span class="sxs-lookup"><span data-stu-id="0ec82-109">Use this parameter to stop a job that takes too long and blocks other activities.</span></span>
<span data-ttu-id="0ec82-110">È possibile annullare solo i tipi di processi seguenti:</span><span class="sxs-lookup"><span data-stu-id="0ec82-110">You can cancel only the following types of jobs:</span></span> 
- <span data-ttu-id="0ec82-111">Backup</span><span class="sxs-lookup"><span data-stu-id="0ec82-111">Backup</span></span>
- <span data-ttu-id="0ec82-112">Ripristinare</span><span class="sxs-lookup"><span data-stu-id="0ec82-112">Restore</span></span>

## <span data-ttu-id="0ec82-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ec82-113">EXAMPLES</span></span>

### <span data-ttu-id="0ec82-114">Esempio 1: arrestare un processo di backup usando un ID processo</span><span class="sxs-lookup"><span data-stu-id="0ec82-114">Example 1: Stop a backup job by using a job ID</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03" 
PS C:\> $Job = Get-AzureRmBackupJob -Vault $Vault -Operation Backup
PS C:\> Stop-AzureRmBackupJob -Vault $Vault -JobID $Job.InstanceId
```

<span data-ttu-id="0ec82-115">Il primo comando ottiene il Vault denominato Vault03 usando il cmdlet **Get-AzureRmBackupVault** .</span><span class="sxs-lookup"><span data-stu-id="0ec82-115">The first command gets the vault named Vault03 by using the **Get-AzureRmBackupVault** cmdlet.</span></span>
<span data-ttu-id="0ec82-116">Il comando Archivia l'oggetto nella variabile $Vault.</span><span class="sxs-lookup"><span data-stu-id="0ec82-116">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="0ec82-117">Il secondo comando ottiene un processo di backup dal Vault in $Vault usando il cmdlet **Get-AzureRmBackupJob** .</span><span class="sxs-lookup"><span data-stu-id="0ec82-117">The second command gets a backup job from the vault in $Vault by using the **Get-AzureRmBackupJob** cmdlet.</span></span>
<span data-ttu-id="0ec82-118">Il comando Archivia il processo nella variabile $Job.</span><span class="sxs-lookup"><span data-stu-id="0ec82-118">The command stores the job in the $Job variable.</span></span>
<span data-ttu-id="0ec82-119">In questo esempio è disponibile una sola operazione di backup nel Vault specificato.</span><span class="sxs-lookup"><span data-stu-id="0ec82-119">In this example, there is only one backup operation in the specified vault.</span></span>
<span data-ttu-id="0ec82-120">Il comando finale interrompe il processo con l'ID specificato.</span><span class="sxs-lookup"><span data-stu-id="0ec82-120">The final command stops the job that has the specified ID.</span></span>

### <span data-ttu-id="0ec82-121">Esempio 2: arrestare tutte le operazioni di ripristino</span><span class="sxs-lookup"><span data-stu-id="0ec82-121">Example 2: Stop all Restore operations</span></span>
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Operation Restore | Stop-AzureRmBackupJob
```

<span data-ttu-id="0ec82-122">Questo comando ottiene tutte le operazioni di ripristino nel Vault in $Vault e quindi le passa al cmdlet corrente usando l'operatore pipeline.</span><span class="sxs-lookup"><span data-stu-id="0ec82-122">This command gets all the restore operations in the vault in $Vault, and then passes them to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="0ec82-123">Il cmdlet corrente arresta ogni processo.</span><span class="sxs-lookup"><span data-stu-id="0ec82-123">The current cmdlet stops each job.</span></span>

## <span data-ttu-id="0ec82-124">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ec82-124">PARAMETERS</span></span>

### <span data-ttu-id="0ec82-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ec82-125">-DefaultProfile</span></span>
<span data-ttu-id="0ec82-126">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0ec82-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ec82-127">-Job</span><span class="sxs-lookup"><span data-stu-id="0ec82-127">-Job</span></span>
<span data-ttu-id="0ec82-128">Specifica un processo che questo cmdlet Annulla.</span><span class="sxs-lookup"><span data-stu-id="0ec82-128">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="0ec82-129">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="0ec82-129">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ec82-130">-JobID</span><span class="sxs-lookup"><span data-stu-id="0ec82-130">-JobID</span></span>
<span data-ttu-id="0ec82-131">Specifica un processo che questo cmdlet Annulla.</span><span class="sxs-lookup"><span data-stu-id="0ec82-131">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="0ec82-132">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="0ec82-132">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ec82-133">-Vault</span><span class="sxs-lookup"><span data-stu-id="0ec82-133">-Vault</span></span>
<span data-ttu-id="0ec82-134">Specifica il Vault di backup in cui questo cmdlet Annulla un processo.</span><span class="sxs-lookup"><span data-stu-id="0ec82-134">Specifies the Backup vault in which this cmdlet cancels a job.</span></span>
<span data-ttu-id="0ec82-135">Per ottenere un oggetto **AzureRmBackupVault** , usa il cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="0ec82-135">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: IdFiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ec82-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ec82-136">CommonParameters</span></span>
<span data-ttu-id="0ec82-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ec82-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ec82-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ec82-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ec82-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ec82-139">INPUTS</span></span>

### <span data-ttu-id="0ec82-140">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="0ec82-140">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>
<span data-ttu-id="0ec82-141">Parameters: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="0ec82-141">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="0ec82-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ec82-142">OUTPUTS</span></span>

### <span data-ttu-id="0ec82-143">System. void</span><span class="sxs-lookup"><span data-stu-id="0ec82-143">System.Void</span></span>

## <span data-ttu-id="0ec82-144">Note</span><span class="sxs-lookup"><span data-stu-id="0ec82-144">NOTES</span></span>

## <span data-ttu-id="0ec82-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ec82-145">RELATED LINKS</span></span>

[<span data-ttu-id="0ec82-146">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="0ec82-146">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="0ec82-147">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="0ec82-147">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="0ec82-148">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="0ec82-148">Wait-AzureRmBackupJob</span></span>](./Wait-AzureRmBackupJob.md)


