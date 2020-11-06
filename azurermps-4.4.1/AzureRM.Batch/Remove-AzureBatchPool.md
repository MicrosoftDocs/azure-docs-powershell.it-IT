---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DB0A8E4B-AD3F-4BAC-A0B2-031913E019D4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchPool.md
ms.openlocfilehash: 01098a20ebb754d4445a85dd5a6bb0d327453234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517028"
---
# <span data-ttu-id="93ef3-101">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="93ef3-101">Remove-AzureBatchPool</span></span>

## <span data-ttu-id="93ef3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="93ef3-102">SYNOPSIS</span></span>
<span data-ttu-id="93ef3-103">Elimina il pool di batch specificato.</span><span class="sxs-lookup"><span data-stu-id="93ef3-103">Deletes the specified Batch pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="93ef3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93ef3-104">SYNTAX</span></span>

```
Remove-AzureBatchPool [-Id] <String> [-Force] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93ef3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="93ef3-105">DESCRIPTION</span></span>
<span data-ttu-id="93ef3-106">Il cmdlet **Remove-AzureBatchPool** Elimina il pool di batch di Azure specificato.</span><span class="sxs-lookup"><span data-stu-id="93ef3-106">The **Remove-AzureBatchPool** cmdlet deletes the specified Azure Batch pool.</span></span>
<span data-ttu-id="93ef3-107">Viene richiesto di confermare a meno che non si usi il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="93ef3-107">You are prompted for confirmation unless you use the *Force* parameter.</span></span>

## <span data-ttu-id="93ef3-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93ef3-108">EXAMPLES</span></span>

### <span data-ttu-id="93ef3-109">Esempio 1: eliminare un pool di batch per ID pool</span><span class="sxs-lookup"><span data-stu-id="93ef3-109">Example 1: Delete a Batch pool by pool ID</span></span>
```
PS C:\>Remove-AzureBatchPool -Id "MyPool" -BatchContext $Context
```

<span data-ttu-id="93ef3-110">Questo comando Elimina il pool con ID pool.</span><span class="sxs-lookup"><span data-stu-id="93ef3-110">This command deletes the pool with ID MyPool.</span></span>
<span data-ttu-id="93ef3-111">All'utente viene richiesta la conferma prima che venga applicata l'operazione di eliminazione.</span><span class="sxs-lookup"><span data-stu-id="93ef3-111">The user is prompted for confirmation before the delete operation takes place.</span></span>

### <span data-ttu-id="93ef3-112">Esempio 2: eliminare tutti i pool di batch per forza</span><span class="sxs-lookup"><span data-stu-id="93ef3-112">Example 2: Delete all Batch pools by force</span></span>
```
PS C:\>Get-AzureBatchPool -BatchContext $Context | Remove-AzureBatchPool -Force -BatchContext $Context
```

<span data-ttu-id="93ef3-113">Questo comando Elimina tutti i pool di batch.</span><span class="sxs-lookup"><span data-stu-id="93ef3-113">This command deletes all Batch pools.</span></span>
<span data-ttu-id="93ef3-114">Dato che il parametro *Force* è presente, il messaggio di conferma viene soppresso.</span><span class="sxs-lookup"><span data-stu-id="93ef3-114">Because the *Force* parameter is present, the confirmation prompt is suppressed.</span></span>

## <span data-ttu-id="93ef3-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="93ef3-115">PARAMETERS</span></span>

### <span data-ttu-id="93ef3-116">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="93ef3-116">-BatchContext</span></span>
<span data-ttu-id="93ef3-117">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="93ef3-117">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="93ef3-118">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="93ef3-118">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="93ef3-119">-Force</span><span class="sxs-lookup"><span data-stu-id="93ef3-119">-Force</span></span>
<span data-ttu-id="93ef3-120">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="93ef3-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="93ef3-121">-ID</span><span class="sxs-lookup"><span data-stu-id="93ef3-121">-Id</span></span>
<span data-ttu-id="93ef3-122">Specifica l'ID del pool da eliminare.</span><span class="sxs-lookup"><span data-stu-id="93ef3-122">Specifies the ID of the pool to delete.</span></span>
<span data-ttu-id="93ef3-123">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="93ef3-123">You cannot specify wildcard characters.</span></span>

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

### <span data-ttu-id="93ef3-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="93ef3-124">-Confirm</span></span>
<span data-ttu-id="93ef3-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93ef3-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ef3-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ef3-126">-WhatIf</span></span>
<span data-ttu-id="93ef3-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93ef3-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ef3-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="93ef3-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ef3-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ef3-129">-DefaultProfile</span></span>
<span data-ttu-id="93ef3-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93ef3-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93ef3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ef3-131">CommonParameters</span></span>
<span data-ttu-id="93ef3-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93ef3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ef3-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93ef3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ef3-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="93ef3-134">INPUTS</span></span>

### <span data-ttu-id="93ef3-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="93ef3-135">BatchAccountContext</span></span>
<span data-ttu-id="93ef3-136">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="93ef3-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="93ef3-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93ef3-137">OUTPUTS</span></span>

## <span data-ttu-id="93ef3-138">Note</span><span class="sxs-lookup"><span data-stu-id="93ef3-138">NOTES</span></span>

## <span data-ttu-id="93ef3-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93ef3-139">RELATED LINKS</span></span>

[<span data-ttu-id="93ef3-140">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="93ef3-140">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="93ef3-141">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="93ef3-141">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="93ef3-142">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="93ef3-142">New-AzureBatchPool</span></span>](./New-AzureBatchPool.md)

[<span data-ttu-id="93ef3-143">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="93ef3-143">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


