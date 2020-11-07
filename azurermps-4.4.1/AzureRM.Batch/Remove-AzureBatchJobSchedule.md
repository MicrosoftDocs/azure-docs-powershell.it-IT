---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 97FA5983-0D73-4336-99DA-46E5992F06DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchJobSchedule.md
ms.openlocfilehash: 673d9e5034b1e7c97d3b6b7cfdd6f89e9a79a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686232"
---
# <span data-ttu-id="4e2b8-101">Remove-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-101">Remove-AzureBatchJobSchedule</span></span>

## <span data-ttu-id="4e2b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4e2b8-102">SYNOPSIS</span></span>
<span data-ttu-id="4e2b8-103">Rimuove la pianificazione di un processo batch.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-103">Removes a Batch job schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4e2b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4e2b8-104">SYNTAX</span></span>

```
Remove-AzureBatchJobSchedule [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e2b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4e2b8-105">DESCRIPTION</span></span>
<span data-ttu-id="4e2b8-106">Il cmdlet **Remove-AzureBatchJobSchedule** rimuove una pianificazione dei processi batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-106">The **Remove-AzureBatchJobSchedule** cmdlet removes an Azure Batch job schedule.</span></span>

## <span data-ttu-id="4e2b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4e2b8-107">EXAMPLES</span></span>

## <span data-ttu-id="4e2b8-108">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4e2b8-108">PARAMETERS</span></span>

### <span data-ttu-id="4e2b8-109">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="4e2b8-109">-BatchContext</span></span>
<span data-ttu-id="4e2b8-110">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-110">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="4e2b8-111">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-111">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="4e2b8-112">-Force</span><span class="sxs-lookup"><span data-stu-id="4e2b8-112">-Force</span></span>
<span data-ttu-id="4e2b8-113">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-113">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e2b8-114">-ID</span><span class="sxs-lookup"><span data-stu-id="4e2b8-114">-Id</span></span>
<span data-ttu-id="4e2b8-115">Specifica l'ID della pianificazione del processo da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-115">Specifies the ID of the job schedule to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4e2b8-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4e2b8-116">-Confirm</span></span>
<span data-ttu-id="4e2b8-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e2b8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e2b8-118">-WhatIf</span></span>
<span data-ttu-id="4e2b8-119">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e2b8-120">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-120">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e2b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e2b8-121">-DefaultProfile</span></span>
<span data-ttu-id="4e2b8-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4e2b8-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e2b8-123">CommonParameters</span></span>
<span data-ttu-id="4e2b8-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e2b8-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e2b8-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e2b8-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e2b8-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4e2b8-126">INPUTS</span></span>

### <span data-ttu-id="4e2b8-127">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="4e2b8-127">BatchAccountContext</span></span>
<span data-ttu-id="4e2b8-128">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="4e2b8-128">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="4e2b8-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4e2b8-129">OUTPUTS</span></span>

## <span data-ttu-id="4e2b8-130">Note</span><span class="sxs-lookup"><span data-stu-id="4e2b8-130">NOTES</span></span>

## <span data-ttu-id="4e2b8-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4e2b8-131">RELATED LINKS</span></span>

[<span data-ttu-id="4e2b8-132">Disable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-132">Disable-AzureBatchJobSchedule</span></span>](./Disable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4e2b8-133">Enable-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-133">Enable-AzureBatchJobSchedule</span></span>](./Enable-AzureBatchJobSchedule.md)

[<span data-ttu-id="4e2b8-134">Get-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-134">Get-AzureBatchJobSchedule</span></span>](./Get-AzureBatchJobSchedule.md)

[<span data-ttu-id="4e2b8-135">New-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-135">New-AzureBatchJobSchedule</span></span>](./New-AzureBatchJobSchedule.md)

[<span data-ttu-id="4e2b8-136">Set-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-136">Set-AzureBatchJobSchedule</span></span>](./Set-AzureBatchJobSchedule.md)

[<span data-ttu-id="4e2b8-137">Stop-AzureBatchJobSchedule</span><span class="sxs-lookup"><span data-stu-id="4e2b8-137">Stop-AzureBatchJobSchedule</span></span>](./Stop-AzureBatchJobSchedule.md)


