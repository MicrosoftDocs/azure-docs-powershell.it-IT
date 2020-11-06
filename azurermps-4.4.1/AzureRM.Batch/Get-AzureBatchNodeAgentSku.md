---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureBatchNodeAgentSku.md
ms.openlocfilehash: e29b5df4a72ff21dbacb0928b298306eb585b493
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520555"
---
# <span data-ttu-id="bf1db-101">Get-AzureBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="bf1db-101">Get-AzureBatchNodeAgentSku</span></span>

## <span data-ttu-id="bf1db-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf1db-102">SYNOPSIS</span></span>
<span data-ttu-id="bf1db-103">Ottiene SKU di agente di nodi batch disponibili in un account batch.</span><span class="sxs-lookup"><span data-stu-id="bf1db-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf1db-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf1db-104">SYNTAX</span></span>

```
Get-AzureBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf1db-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf1db-105">DESCRIPTION</span></span>
<span data-ttu-id="bf1db-106">Il cmdlet **Get-AzureBatchNodeAgentSku** ottiene SKU dell'agente di nodi disponibili in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1db-106">The **Get-AzureBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="bf1db-107">Specificare l'account usando il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="bf1db-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="bf1db-108">È possibile restringere la ricerca agli SKU che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="bf1db-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="bf1db-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf1db-109">EXAMPLES</span></span>

### <span data-ttu-id="bf1db-110">Esempio 1: ottenere tutte le SKU di agente di nodi disponibili</span><span class="sxs-lookup"><span data-stu-id="bf1db-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzureRmBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzureBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="bf1db-111">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento utilizzando **Get-AzureRmBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="bf1db-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzureRmBatchAccountKeys**.</span></span>
<span data-ttu-id="bf1db-112">Il comando Archivia il contesto nella variabile $Context da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="bf1db-112">The command stores the context in the $Context variable to use in the next command.</span></span>

<span data-ttu-id="bf1db-113">Il secondo comando consente di ottenere tutte le SKU di agente di nodi disponibili supportate in batch.</span><span class="sxs-lookup"><span data-stu-id="bf1db-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="bf1db-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf1db-114">PARAMETERS</span></span>

### <span data-ttu-id="bf1db-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="bf1db-115">-BatchContext</span></span>
<span data-ttu-id="bf1db-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="bf1db-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="bf1db-117">Per ottenere un oggetto **BatchAccountContext** che contiene i tasti di scelta per l'abbonamento, usare il cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="bf1db-117">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="bf1db-118">-Filtro</span><span class="sxs-lookup"><span data-stu-id="bf1db-118">-Filter</span></span>
<span data-ttu-id="bf1db-119">Specifica una clausola di filtro OData per SKU agente di nodi.</span><span class="sxs-lookup"><span data-stu-id="bf1db-119">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="bf1db-120">Se non specifichi un filtro, questo cmdlet restituisce tutti gli SKU degli agenti di nodi supportati da batch.</span><span class="sxs-lookup"><span data-stu-id="bf1db-120">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1db-121">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="bf1db-121">-MaxCount</span></span>
<span data-ttu-id="bf1db-122">Specifica il numero massimo di SKU di agente di nodi da restituire.</span><span class="sxs-lookup"><span data-stu-id="bf1db-122">Specifies the maximum number of node agent SKUs to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf1db-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf1db-123">-DefaultProfile</span></span>
<span data-ttu-id="bf1db-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bf1db-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf1db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf1db-125">CommonParameters</span></span>
<span data-ttu-id="bf1db-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf1db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf1db-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf1db-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf1db-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf1db-128">INPUTS</span></span>

### <span data-ttu-id="bf1db-129">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="bf1db-129">BatchAccountContext</span></span>
<span data-ttu-id="bf1db-130">Il parametro ' BatchContext ' accetta il valore di tipo ' BatchAccountContext ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bf1db-130">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="bf1db-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf1db-131">OUTPUTS</span></span>

### <span data-ttu-id="bf1db-132">Microsoft.Azure.Commands.Batch. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="bf1db-132">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="bf1db-133">Note</span><span class="sxs-lookup"><span data-stu-id="bf1db-133">NOTES</span></span>

## <span data-ttu-id="bf1db-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf1db-134">RELATED LINKS</span></span>

[<span data-ttu-id="bf1db-135">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="bf1db-135">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


