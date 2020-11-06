---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/wait-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: a5de80561ee0b80c2ce825db26e1de5c6f46b80b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511940"
---
# <span data-ttu-id="9baa1-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9baa1-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="9baa1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9baa1-102">SYNOPSIS</span></span>
<span data-ttu-id="9baa1-103">Attende il completamento di un processo di backup.</span><span class="sxs-lookup"><span data-stu-id="9baa1-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9baa1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9baa1-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9baa1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9baa1-105">DESCRIPTION</span></span>
<span data-ttu-id="9baa1-106">Il cmdlet **wait-AzureRmBackupJob** attende il completamento di un processo di backup di Azure.</span><span class="sxs-lookup"><span data-stu-id="9baa1-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="9baa1-107">I processi di backup possono richiedere molto tempo.</span><span class="sxs-lookup"><span data-stu-id="9baa1-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="9baa1-108">Se si esegue un processo di backup come parte di uno script, è consigliabile forzare lo script ad attendere il completamento del processo prima che continui ad altre attività.</span><span class="sxs-lookup"><span data-stu-id="9baa1-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>
<span data-ttu-id="9baa1-109">Uno script che include questo cmdlet può essere più semplice di uno che esegue il polling del servizio di backup per lo stato del processo.</span><span class="sxs-lookup"><span data-stu-id="9baa1-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="9baa1-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9baa1-110">EXAMPLES</span></span>

## <span data-ttu-id="9baa1-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9baa1-111">PARAMETERS</span></span>

### <span data-ttu-id="9baa1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9baa1-112">-DefaultProfile</span></span>
<span data-ttu-id="9baa1-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="9baa1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9baa1-114">-Job</span><span class="sxs-lookup"><span data-stu-id="9baa1-114">-Job</span></span>
<span data-ttu-id="9baa1-115">Specifica un processo che questo cmdlet Annulla.</span><span class="sxs-lookup"><span data-stu-id="9baa1-115">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="9baa1-116">Per ottenere un oggetto **AzureRmBackupJob** , usa il cmdlet Get-AzureRmBackupJob.</span><span class="sxs-lookup"><span data-stu-id="9baa1-116">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9baa1-117">-TimeOut</span><span class="sxs-lookup"><span data-stu-id="9baa1-117">-TimeOut</span></span>
<span data-ttu-id="9baa1-118">Specifica il tempo massimo, in secondi, in cui questo cmdlet attende il completamento del processo.</span><span class="sxs-lookup"><span data-stu-id="9baa1-118">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="9baa1-119">È consigliabile specificare un valore di timeout.</span><span class="sxs-lookup"><span data-stu-id="9baa1-119">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9baa1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9baa1-120">CommonParameters</span></span>
<span data-ttu-id="9baa1-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9baa1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9baa1-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9baa1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9baa1-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9baa1-123">INPUTS</span></span>

### <span data-ttu-id="9baa1-124">System. Object</span><span class="sxs-lookup"><span data-stu-id="9baa1-124">System.Object</span></span>
<span data-ttu-id="9baa1-125">Parameters: Job (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9baa1-125">Parameters: Job (ByValue)</span></span>

## <span data-ttu-id="9baa1-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9baa1-126">OUTPUTS</span></span>

### <span data-ttu-id="9baa1-127">Microsoft. Azure. Commands. AzureBackup. Models. AzureRMBackupJob</span><span class="sxs-lookup"><span data-stu-id="9baa1-127">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob</span></span>

## <span data-ttu-id="9baa1-128">Note</span><span class="sxs-lookup"><span data-stu-id="9baa1-128">NOTES</span></span>

## <span data-ttu-id="9baa1-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9baa1-129">RELATED LINKS</span></span>

[<span data-ttu-id="9baa1-130">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9baa1-130">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="9baa1-131">Stop-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="9baa1-131">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


