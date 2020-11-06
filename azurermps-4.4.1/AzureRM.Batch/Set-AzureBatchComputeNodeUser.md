---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A0D620DA-B5A3-4F8F-BD43-A58630C95432
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchComputeNodeUser.md
ms.openlocfilehash: a5e8fd6e6cfba8832365f385cc90357bac59efb0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517027"
---
# <span data-ttu-id="78a04-101">Set-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="78a04-101">Set-AzureBatchComputeNodeUser</span></span>

## <span data-ttu-id="78a04-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78a04-102">SYNOPSIS</span></span>
<span data-ttu-id="78a04-103">Modifica le proprietà di un account in un nodo di calcolo batch.</span><span class="sxs-lookup"><span data-stu-id="78a04-103">Modifies properties of an account on a Batch compute node.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78a04-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78a04-104">SYNTAX</span></span>

```
Set-AzureBatchComputeNodeUser [-PoolId] <String> [-ComputeNodeId] <String> [-Name] <String>
 [-Password] <String> [-ExpiryTime <DateTime>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78a04-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78a04-105">DESCRIPTION</span></span>
<span data-ttu-id="78a04-106">Il cmdlet **set-AzureBatchComputeNodeUser** modifica le proprietà di un account utente in un nodo di calcolo batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="78a04-106">The **Set-AzureBatchComputeNodeUser** cmdlet modifies properties of a user account on an Azure Batch compute node.</span></span>

## <span data-ttu-id="78a04-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78a04-107">EXAMPLES</span></span>

### <span data-ttu-id="78a04-108">Esempio 1: aggiornare un account utente</span><span class="sxs-lookup"><span data-stu-id="78a04-108">Example 1: Update a user account</span></span>
```
PS C:\>Set-AzureBatchComputeNodeUser -PoolId "ContosoPool" -ComputeNodeId "tvm-3257026573_1-20150904t230807z" -Name "PFuller" -BatchContext $Context -Password "Password" -ExpiryTime ([DateTime]::Now.AddDays(14))
```

<span data-ttu-id="78a04-109">Questo comando modifica l'account utente denominato PFuller nel nodo Compute che contiene l'ID specificato nel pool denominato ContosoPool.</span><span class="sxs-lookup"><span data-stu-id="78a04-109">This command modifies user account named PFuller on the compute node that has the specified ID in the pool named ContosoPool.</span></span>
<span data-ttu-id="78a04-110">Il comando cambia la password dell'account e il tempo di scadenza.</span><span class="sxs-lookup"><span data-stu-id="78a04-110">The command changes the account password and expiry time.</span></span>

## <span data-ttu-id="78a04-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78a04-111">PARAMETERS</span></span>

### <span data-ttu-id="78a04-112">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="78a04-112">-BatchContext</span></span>
<span data-ttu-id="78a04-113">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="78a04-113">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="78a04-114">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="78a04-114">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="78a04-115">-ComputeNodeId</span><span class="sxs-lookup"><span data-stu-id="78a04-115">-ComputeNodeId</span></span>
<span data-ttu-id="78a04-116">Specifica l'ID del nodo COMPUTE in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a04-116">Specifies the ID of the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a04-117">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="78a04-117">-ExpiryTime</span></span>
<span data-ttu-id="78a04-118">Specifica il tempo di scadenza per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="78a04-118">Specifies the expiry time for the user account.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a04-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="78a04-119">-Name</span></span>
<span data-ttu-id="78a04-120">Specifica il nome dell'account utente che questo cmdlet modifica.</span><span class="sxs-lookup"><span data-stu-id="78a04-120">Specifies the name of the user account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a04-121">-Password</span><span class="sxs-lookup"><span data-stu-id="78a04-121">-Password</span></span>
<span data-ttu-id="78a04-122">Specifica la password per l'account utente.</span><span class="sxs-lookup"><span data-stu-id="78a04-122">Specifies the password for the user account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a04-123">-PoolId</span><span class="sxs-lookup"><span data-stu-id="78a04-123">-PoolId</span></span>
<span data-ttu-id="78a04-124">Specifica l'ID del pool che contiene il nodo COMPUTE in cui opera questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="78a04-124">Specifies the ID of the pool that contains the compute node on which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="78a04-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78a04-125">-DefaultProfile</span></span>
<span data-ttu-id="78a04-126">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78a04-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78a04-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78a04-127">CommonParameters</span></span>
<span data-ttu-id="78a04-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78a04-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78a04-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78a04-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78a04-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78a04-130">INPUTS</span></span>

### <span data-ttu-id="78a04-131">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="78a04-131">BatchAccountContext</span></span>
<span data-ttu-id="78a04-132">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="78a04-132">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="78a04-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78a04-133">OUTPUTS</span></span>

## <span data-ttu-id="78a04-134">Note</span><span class="sxs-lookup"><span data-stu-id="78a04-134">NOTES</span></span>

## <span data-ttu-id="78a04-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78a04-135">RELATED LINKS</span></span>

[<span data-ttu-id="78a04-136">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="78a04-136">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="78a04-137">New-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="78a04-137">New-AzureBatchComputeNodeUser</span></span>](./New-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="78a04-138">Remove-AzureBatchComputeNodeUser</span><span class="sxs-lookup"><span data-stu-id="78a04-138">Remove-AzureBatchComputeNodeUser</span></span>](./Remove-AzureBatchComputeNodeUser.md)

[<span data-ttu-id="78a04-139">Cmdlet batch di Azure</span><span class="sxs-lookup"><span data-stu-id="78a04-139">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


