---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 7C79BFF1-41E1-472D-AF67-1C3B39AB7548
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/enable-azbatchjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Enable-AzBatchJob.md
ms.openlocfilehash: 608d4aaba26b6f9631d4f1c35e889ac5a7480154
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865623"
---
# <span data-ttu-id="2c495-101">Enable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2c495-101">Enable-AzBatchJob</span></span>

## <span data-ttu-id="2c495-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2c495-102">SYNOPSIS</span></span>
<span data-ttu-id="2c495-103">Abilita un processo batch.</span><span class="sxs-lookup"><span data-stu-id="2c495-103">Enables a Batch job.</span></span>

## <span data-ttu-id="2c495-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2c495-104">SYNTAX</span></span>

```
Enable-AzBatchJob [-Id] <String> -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2c495-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2c495-105">DESCRIPTION</span></span>
<span data-ttu-id="2c495-106">Il cmdlet **Enable-AzBatchJob** Abilita un processo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="2c495-106">The **Enable-AzBatchJob** cmdlet enables an Azure Batch job.</span></span>
<span data-ttu-id="2c495-107">Dopo l'abilitazione di un processo, le nuove attività possono essere eseguite.</span><span class="sxs-lookup"><span data-stu-id="2c495-107">After you enable a job, new tasks can run.</span></span>

## <span data-ttu-id="2c495-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2c495-108">EXAMPLES</span></span>

### <span data-ttu-id="2c495-109">Esempio 1: abilitare un processo batch</span><span class="sxs-lookup"><span data-stu-id="2c495-109">Example 1: Enable a Batch job</span></span>
```
PS C:\>Enable-AzBatchJob -Id "Job-000001" -BatchContext $Context
```

<span data-ttu-id="2c495-110">Questo comando consente di abilitare il processo con ID Job-000001.</span><span class="sxs-lookup"><span data-stu-id="2c495-110">This command enables the job that has the ID Job-000001.</span></span>
<span data-ttu-id="2c495-111">Usa il cmdlet Get-AzBatchAccountKeys per assegnare un contesto alla variabile $Context.</span><span class="sxs-lookup"><span data-stu-id="2c495-111">Use the Get-AzBatchAccountKeys cmdlet to assign a context to the $Context variable.</span></span>

## <span data-ttu-id="2c495-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2c495-112">PARAMETERS</span></span>

### <span data-ttu-id="2c495-113">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="2c495-113">-BatchContext</span></span>
<span data-ttu-id="2c495-114">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2c495-114">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="2c495-115">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="2c495-115">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="2c495-116">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="2c495-116">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="2c495-117">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="2c495-117">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="2c495-118">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="2c495-118">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="2c495-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c495-119">-DefaultProfile</span></span>
<span data-ttu-id="2c495-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2c495-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c495-121">-ID</span><span class="sxs-lookup"><span data-stu-id="2c495-121">-Id</span></span>
<span data-ttu-id="2c495-122">Specifica l'ID del processo abilitato da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c495-122">Specifies the ID of the job that this cmdlet enables.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c495-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c495-123">CommonParameters</span></span>
<span data-ttu-id="2c495-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c495-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c495-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c495-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c495-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2c495-126">INPUTS</span></span>

### <span data-ttu-id="2c495-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2c495-127">System.String</span></span>

### <span data-ttu-id="2c495-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="2c495-128">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="2c495-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2c495-129">OUTPUTS</span></span>

### <span data-ttu-id="2c495-130">System. void</span><span class="sxs-lookup"><span data-stu-id="2c495-130">System.Void</span></span>

## <span data-ttu-id="2c495-131">Note</span><span class="sxs-lookup"><span data-stu-id="2c495-131">NOTES</span></span>

## <span data-ttu-id="2c495-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2c495-132">RELATED LINKS</span></span>

[<span data-ttu-id="2c495-133">Disable-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2c495-133">Disable-AzBatchJob</span></span>](./Disable-AzBatchJob.md)

[<span data-ttu-id="2c495-134">Get-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2c495-134">Get-AzBatchJob</span></span>](./Get-AzBatchJob.md)

[<span data-ttu-id="2c495-135">New-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2c495-135">New-AzBatchJob</span></span>](./New-AzBatchJob.md)

[<span data-ttu-id="2c495-136">Remove-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2c495-136">Remove-AzBatchJob</span></span>](./Remove-AzBatchJob.md)

[<span data-ttu-id="2c495-137">Stop-AzBatchJob</span><span class="sxs-lookup"><span data-stu-id="2c495-137">Stop-AzBatchJob</span></span>](./Stop-AzBatchJob.md)

[<span data-ttu-id="2c495-138">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="2c495-138">Azure Batch Cmdlets</span></span>](/powershell/module/az.batch)


