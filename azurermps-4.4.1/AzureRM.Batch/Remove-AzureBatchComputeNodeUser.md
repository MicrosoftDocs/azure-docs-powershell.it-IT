---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 9E423A10-06AF-42F8-AC90-82DB01012AFA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureBatchComputeNodeUser.md
ms.openlocfilehash: ec050d4410e50e0838512879856e6534196108af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520134"
---
# <span data-ttu-id="0d409-101">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0d409-101">Remove-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="0d409-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d409-102">SYNOPSIS</span></span>
<span data-ttu-id="0d409-103">Elimina un account utente da un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="0d409-103">Deletes a user account from a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0d409-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d409-104">SYNTAX</span></span>

```
Remove-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0d409-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d409-105">DESCRIPTION</span></span>
<span data-ttu-id="0d409-106">Il cmdlet **Remove-AzureBatchComputeNodeUser** Elimina un account utente da un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="0d409-106">The **Remove-AzureBatchComputeNodeUser** cmdlet deletes a user account from an Azure Batch compute node.</span></span>

## <span data-ttu-id="0d409-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d409-107">EXAMPLES</span></span>

### <span data-ttu-id="0d409-108">Esempio 1: eliminare un utente da un nodo Compute senza conferma</span><span class="sxs-lookup"><span data-stu-id="0d409-108">Example 1: Delete a user from a compute node without confirmation</span></span>
```
PS C:\>Remove-AzureBatchComputeNodeUser -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Name "User14" -Force -BatchContext $Context
```

<span data-ttu-id="0d409-109">Questo comando Elimina l'utente denominato User14 dal nodo Compute denominato ComputeNode01.</span><span class="sxs-lookup"><span data-stu-id="0d409-109">This command deletes the user named User14 from compute node named ComputeNode01.</span></span>
<span data-ttu-id="0d409-110">Il nodo Compute si trova nel pool denominato pool01.</span><span class="sxs-lookup"><span data-stu-id="0d409-110">The compute node is in the pool named Pool01.</span></span>
<span data-ttu-id="0d409-111">Questo comando specifica il parametro *Force* .</span><span class="sxs-lookup"><span data-stu-id="0d409-111">This command specifies the *Force* parameter.</span></span>
<span data-ttu-id="0d409-112">Di conseguenza, il comando non chiede conferma.</span><span class="sxs-lookup"><span data-stu-id="0d409-112">Therefore, the command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="0d409-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d409-113">PARAMETERS</span></span>

### <span data-ttu-id="0d409-114">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="0d409-114">-BatchContext</span></span>
<span data-ttu-id="0d409-115">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="0d409-115">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="0d409-116">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="0d409-116">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="0d409-117">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="0d409-117">-ComputeNodeId</span></span>
<span data-ttu-id="0d409-118">Specifica l'ID del nodo COMPUTE in cui questo cmdlet elimina l'account utente.</span><span class="sxs-lookup"><span data-stu-id="0d409-118">Specifies the ID of the compute node on which this cmdlet deletes the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d409-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="0d409-119">-Name</span></span>
<span data-ttu-id="0d409-120">Specifica il nome dell'account utente da eliminare.</span><span class="sxs-lookup"><span data-stu-id="0d409-120">Specifies the name of the user account to delete.</span></span>
<span data-ttu-id="0d409-121">Non è possibile specificare caratteri jolly.</span><span class="sxs-lookup"><span data-stu-id="0d409-121">You cannot specify wildcard characters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d409-122">-PoolId</span><span class="sxs-lookup"><span data-stu-id="0d409-122">-PoolId</span></span>
<span data-ttu-id="0d409-123">Specifica l'ID del pool che contiene il nodo COMPUTE in cui eliminare l'account utente.</span><span class="sxs-lookup"><span data-stu-id="0d409-123">Specifies the ID of the pool that contains the compute node on which to delete the user account.</span></span>

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

### <span data-ttu-id="0d409-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0d409-124">-Confirm</span></span>
<span data-ttu-id="0d409-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0d409-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d409-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d409-126">-WhatIf</span></span>
<span data-ttu-id="0d409-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d409-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d409-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0d409-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d409-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d409-129">-DefaultProfile</span></span>
<span data-ttu-id="0d409-130">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d409-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d409-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d409-131">CommonParameters</span></span>
<span data-ttu-id="0d409-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d409-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d409-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d409-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d409-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d409-134">INPUTS</span></span>

### <span data-ttu-id="0d409-135">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="0d409-135">BatchAccountContext</span></span>
<span data-ttu-id="0d409-136">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0d409-136">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="0d409-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d409-137">OUTPUTS</span></span>

## <span data-ttu-id="0d409-138">Note</span><span class="sxs-lookup"><span data-stu-id="0d409-138">NOTES</span></span>

## <span data-ttu-id="0d409-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d409-139">RELATED LINKS</span></span>

[<span data-ttu-id="0d409-140">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="0d409-140">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="0d409-141">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="0d409-141">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="0d409-142">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="0d409-142">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


