---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 14026F0E-4959-4150-A31F-A94BC56ED808
online version: https://docs.microsoft.com/powershell/module/az.batch/set-azbatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchJobSchedule.md
ms.openlocfilehash: cf4512bc0d219c164be6543d5633a43c9052cc4e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004621"
---
# <span data-ttu-id="14d94-101">Set-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-101">Set-AzBatchJobSchedule</span></span>

## <span data-ttu-id="14d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14d94-102">SYNOPSIS</span></span>
<span data-ttu-id="14d94-103">Imposta la pianificazione di un processo.</span><span class="sxs-lookup"><span data-stu-id="14d94-103">Sets a job schedule.</span></span>

## <span data-ttu-id="14d94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14d94-104">SYNTAX</span></span>

```
Set-AzBatchJobSchedule [-JobSchedule] <PSCloudJobSchedule> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14d94-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="14d94-105">DESCRIPTION</span></span>
<span data-ttu-id="14d94-106">Il cmdlet **Set-AzBatchJobSchedule** imposta una pianificazione di processo nel servizio batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="14d94-106">The **Set-AzBatchJobSchedule** cmdlet sets a job schedule in the Azure Batch service.</span></span>

## <span data-ttu-id="14d94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14d94-107">EXAMPLES</span></span>

### <span data-ttu-id="14d94-108">Esempio 1: Aggiornare la pianificazione di un processo</span><span class="sxs-lookup"><span data-stu-id="14d94-108">Example 1: Update a job schedule</span></span>
```
PS C:\> $JobSchedule = Get-AzBatchJobSchedule -Id "MyJobSchedule" -BatchContext $Context
PS C:\> $JobSchedule.Schedule.RecurrenceInterval = New-TimeSpan -Days 2
PS C:\> Set-AzBatchJobSchedule -JobSchedule $Job -BatchContext $Context
```

<span data-ttu-id="14d94-109">Il primo comando ottiene un processo con **Get-AzBatchJobSchedule** e quindi lo archivia nella $JobSchedule variabile.</span><span class="sxs-lookup"><span data-stu-id="14d94-109">The first command gets a job by using **Get-AzBatchJobSchedule**, and then stores it in the $JobSchedule variable.</span></span>
<span data-ttu-id="14d94-110">Il secondo comando modifica l'intervallo di ricorrenza `$JobSchedule.Schedule` sull'oggetto.</span><span class="sxs-lookup"><span data-stu-id="14d94-110">The second command modifies the recurrence interval on the `$JobSchedule.Schedule` object.</span></span>
<span data-ttu-id="14d94-111">Il comando finale aggiorna il servizio batch in modo che corrisponda all'oggetto locale in $JobSchedule.</span><span class="sxs-lookup"><span data-stu-id="14d94-111">The final command updates the Batch service to match the local object in $JobSchedule.</span></span>

## <span data-ttu-id="14d94-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="14d94-112">PARAMETERS</span></span>

### <span data-ttu-id="14d94-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="14d94-113">-BatchContext</span></span>
<span data-ttu-id="14d94-114">Specifica **l'istanza BatchAccountContext** che questo cmdlet usa per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="14d94-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="14d94-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere BatchAccountContext, verrà usata l'autenticazione di Azure Active Directory quando si interagisce con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="14d94-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="14d94-116">Per usare invece l'autenticazione della chiave condivisa, usare il cmdlet Get-AzBatchAccountKey per ottenere un oggetto BatchAccountContext con le relative chiavi di accesso popolate.</span><span class="sxs-lookup"><span data-stu-id="14d94-116">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="14d94-117">Quando si usa l'autenticazione con chiave condivisa, per impostazione predefinita viene usata la chiave di accesso primario.</span><span class="sxs-lookup"><span data-stu-id="14d94-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="14d94-118">Per modificare la chiave da usare, impostare la proprietà BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="14d94-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d94-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14d94-119">-DefaultProfile</span></span>
<span data-ttu-id="14d94-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14d94-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14d94-121">-JobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-121">-JobSchedule</span></span>
<span data-ttu-id="14d94-122">Specifica un oggetto **PSCloudJobSchedule** che rappresenta una pianificazione di processo.</span><span class="sxs-lookup"><span data-stu-id="14d94-122">Specifies a **PSCloudJobSchedule** object that represents a job schedule.</span></span>
<span data-ttu-id="14d94-123">Per ottenere un **oggetto PSCloudJobSchedule,** usare il cmdlet Get-AzBatchJobSchedule.</span><span class="sxs-lookup"><span data-stu-id="14d94-123">To obtain a **PSCloudJobSchedule** object, use the Get-AzBatchJobSchedule cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14d94-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14d94-124">CommonParameters</span></span>
<span data-ttu-id="14d94-125">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14d94-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14d94-126">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="14d94-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14d94-127">INPUT</span><span class="sxs-lookup"><span data-stu-id="14d94-127">INPUTS</span></span>

### <span data-ttu-id="14d94-128">Microsoft.Azure.Commands.Batch. Models.PSCloudJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-128">Microsoft.Azure.Commands.Batch.Models.PSCloudJobSchedule</span></span>

### <span data-ttu-id="14d94-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="14d94-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="14d94-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14d94-130">OUTPUTS</span></span>

### <span data-ttu-id="14d94-131">System.Void</span><span class="sxs-lookup"><span data-stu-id="14d94-131">System.Void</span></span>

## <span data-ttu-id="14d94-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="14d94-132">NOTES</span></span>

## <span data-ttu-id="14d94-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14d94-133">RELATED LINKS</span></span>

[<span data-ttu-id="14d94-134">Disable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-134">Disable-AzBatchJobSchedule</span></span>](./Disable-AzBatchJobSchedule.md)

[<span data-ttu-id="14d94-135">Enable-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-135">Enable-AzBatchJobSchedule</span></span>](./Enable-AzBatchJobSchedule.md)

[<span data-ttu-id="14d94-136">Get-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-136">Get-AzBatchJobSchedule</span></span>](./Get-AzBatchJobSchedule.md)

[<span data-ttu-id="14d94-137">New-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-137">New-AzBatchJobSchedule</span></span>](./New-AzBatchJobSchedule.md)

[<span data-ttu-id="14d94-138">Remove-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-138">Remove-AzBatchJobSchedule</span></span>](./Remove-AzBatchJobSchedule.md)

[<span data-ttu-id="14d94-139">Stop-AzBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="14d94-139">Stop-AzBatchJobSchedule</span></span>](./Stop-AzBatchJobSchedule.md)


