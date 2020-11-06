---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurebatchjobschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 2e474462983f15c0d58f8ada60b907c100508c6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514552"
---
# <span data-ttu-id="0b7ae-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="0b7ae-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0b7ae-102">SYNOPSIS</span></span>
<span data-ttu-id="0b7ae-103">Rimuove la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0b7ae-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b7ae-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0b7ae-105">DESCRIPTION</span></span>
<span data-ttu-id="0b7ae-106">Il cmdlet **Remove-AzureBatchJobSchedule** rimuove una pianificazione dei processi batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="0b7ae-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-107">EXAMPLES</span></span>

## <span data-ttu-id="0b7ae-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-108">PARAMETERS</span></span>

### <span data-ttu-id="0b7ae-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0b7ae-109">-BatchContext</span></span>
<span data-ttu-id="0b7ae-110">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0b7ae-111">Se si usa il cmdlet Get-AzureRmBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-111">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="0b7ae-112">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzureRmBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-112">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="0b7ae-113">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-113">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="0b7ae-114">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-114">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7ae-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b7ae-115">-DefaultProfile</span></span>
<span data-ttu-id="0b7ae-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0b7ae-117">-Force</span><span class="sxs-lookup"><span data-stu-id="0b7ae-117">-Force</span></span>
<span data-ttu-id="0b7ae-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7ae-119">-ID</span><span class="sxs-lookup"><span data-stu-id="0b7ae-119">-Id</span></span>
<span data-ttu-id="0b7ae-120">Specifica l'ID della pianificazione del processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-120">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0b7ae-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0b7ae-121">-Confirm</span></span>
<span data-ttu-id="0b7ae-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7ae-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b7ae-123">-WhatIf</span></span>
<span data-ttu-id="0b7ae-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b7ae-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0b7ae-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b7ae-126">CommonParameters</span></span>
<span data-ttu-id="0b7ae-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b7ae-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b7ae-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b7ae-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b7ae-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-129">INPUTS</span></span>

### <span data-ttu-id="0b7ae-130">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0b7ae-130">BatchAccountContext</span></span>
<span data-ttu-id="0b7ae-131">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0b7ae-131">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="0b7ae-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b7ae-132">OUTPUTS</span></span>

## <span data-ttu-id="0b7ae-133">Note</span><span class="sxs-lookup"><span data-stu-id="0b7ae-133">NOTES</span></span>

## <span data-ttu-id="0b7ae-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b7ae-134">RELATED LINKS</span></span>

[<span data-ttu-id="0b7ae-135">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-135">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0b7ae-136">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-136">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="0b7ae-137">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-137">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="0b7ae-138">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-138">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="0b7ae-139">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-139">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="0b7ae-140">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="0b7ae-140">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


