---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 5C6D3792-AA56-4210-B376-D9E656B04FBD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodeagentsku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeAgentSku.md
ms.openlocfilehash: 8f7228a540456e76e4f7a22d70d00969a9ef568c
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865647"
---
# <span data-ttu-id="a19e5-101">Get-AzBatchNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="a19e5-101">Get-AzBatchNodeAgentSku</span></span>

## <span data-ttu-id="a19e5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a19e5-102">SYNOPSIS</span></span>
<span data-ttu-id="a19e5-103">Ottiene SKU di agente di nodi batch disponibili in un account batch.</span><span class="sxs-lookup"><span data-stu-id="a19e5-103">Gets Batch node agent SKUs available in a Batch account.</span></span>

## <span data-ttu-id="a19e5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a19e5-104">SYNTAX</span></span>

```
Get-AzBatchNodeAgentSku [-Filter <String>] [-MaxCount <Int32>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a19e5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a19e5-105">DESCRIPTION</span></span>
<span data-ttu-id="a19e5-106">Il cmdlet **Get-AzBatchNodeAgentSku** ottiene SKU dell'agente di nodi disponibili in un account batch di Azure.</span><span class="sxs-lookup"><span data-stu-id="a19e5-106">The **Get-AzBatchNodeAgentSku** cmdlet gets node agent SKUs that are available in an Azure Batch account.</span></span>
<span data-ttu-id="a19e5-107">Specificare l'account usando il parametro *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="a19e5-107">Specify the account by using the *BatchContext* parameter.</span></span>
<span data-ttu-id="a19e5-108">È possibile restringere la ricerca agli SKU che corrispondono a un filtro OData (Open Data Protocol).</span><span class="sxs-lookup"><span data-stu-id="a19e5-108">You can narrow your search to SKUs that match an Open Data Protocol (OData) filter.</span></span>

## <span data-ttu-id="a19e5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a19e5-109">EXAMPLES</span></span>

### <span data-ttu-id="a19e5-110">Esempio 1: ottenere tutte le SKU di agente di nodi disponibili</span><span class="sxs-lookup"><span data-stu-id="a19e5-110">Example 1: Get all available node agent SKUs</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKeys -AccountName "ContosoBatchAccount"
PS C:\> Get-AzBatchNodeAgentSku -BatchContext $Context 
batch.node.centos 7 Linux {7.0, 7.1, 7.2, OL70} 
batch.node.debian 8 Linux {15.10, 8} 
batch.node.opensuse 13.2 Linux {13.2} 
batch.node.opensuse 42.1 Linux {42.1, 12, 12-SP1, 12} 
batch.node.ubuntu 14.04 Linux {14.04.0-LTS, 14.04.1-LTS, 14.04.2-LTS, 14.04.3-LTS...} 
batch.node.windows amd64 Windows {2008-R2-SP1, 2012-Datacenter, 2012-R2-Datacenter, Windows-Server-Technical-Preview}
```

<span data-ttu-id="a19e5-111">Il primo comando ottiene un contesto dell'account batch che contiene i tasti di scelta per l'abbonamento utilizzando **Get-AzBatchAccountKeys**.</span><span class="sxs-lookup"><span data-stu-id="a19e5-111">The first command gets a batch account context that contains access keys for your subscription by using **Get-AzBatchAccountKeys**.</span></span>
<span data-ttu-id="a19e5-112">Il comando Archivia il contesto nella variabile $Context da usare nel comando successivo.</span><span class="sxs-lookup"><span data-stu-id="a19e5-112">The command stores the context in the $Context variable to use in the next command.</span></span>
<span data-ttu-id="a19e5-113">Il secondo comando consente di ottenere tutte le SKU di agente di nodi disponibili supportate in batch.</span><span class="sxs-lookup"><span data-stu-id="a19e5-113">The second command gets all available node agent SKUs that Batch supports.</span></span>

## <span data-ttu-id="a19e5-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a19e5-114">PARAMETERS</span></span>

### <span data-ttu-id="a19e5-115">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="a19e5-115">-BatchContext</span></span>
<span data-ttu-id="a19e5-116">Specifica l'istanza di **BatchAccountContext** utilizzata dal cmdlet per interagire con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a19e5-116">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="a19e5-117">Se si usa il cmdlet Get-AzBatchAccount per ottenere il BatchAccountContext, l'autenticazione di Azure Active Directory verrà usata durante l'interazione con il servizio batch.</span><span class="sxs-lookup"><span data-stu-id="a19e5-117">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="a19e5-118">Per usare invece l'autenticazione con chiave condivisa, usa il cmdlet Get-AzBatchAccountKeys per ottenere un oggetto BatchAccountContext con i relativi tasti di scelta popolati.</span><span class="sxs-lookup"><span data-stu-id="a19e5-118">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="a19e5-119">Quando si usa l'autenticazione con chiave condivisa, il tasto di scelta principale viene usato per impostazione predefinita.</span><span class="sxs-lookup"><span data-stu-id="a19e5-119">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="a19e5-120">Per cambiare la chiave da usare, imposta la proprietà BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="a19e5-120">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="a19e5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a19e5-121">-DefaultProfile</span></span>
<span data-ttu-id="a19e5-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a19e5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a19e5-123">-Filtro</span><span class="sxs-lookup"><span data-stu-id="a19e5-123">-Filter</span></span>
<span data-ttu-id="a19e5-124">Specifica una clausola di filtro OData per SKU agente di nodi.</span><span class="sxs-lookup"><span data-stu-id="a19e5-124">Specifies an OData filter clause for node agent SKUs.</span></span>
<span data-ttu-id="a19e5-125">Se non specifichi un filtro, questo cmdlet restituisce tutti gli SKU degli agenti di nodi supportati da batch.</span><span class="sxs-lookup"><span data-stu-id="a19e5-125">If you do not specify a filter, this cmdlet returns all node agent SKUs that Batch supports.</span></span>

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

### <span data-ttu-id="a19e5-126">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a19e5-126">-MaxCount</span></span>
<span data-ttu-id="a19e5-127">Specifica il numero massimo di SKU di agente di nodi da restituire.</span><span class="sxs-lookup"><span data-stu-id="a19e5-127">Specifies the maximum number of node agent SKUs to return.</span></span>

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

### <span data-ttu-id="a19e5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a19e5-128">CommonParameters</span></span>
<span data-ttu-id="a19e5-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a19e5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a19e5-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a19e5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a19e5-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a19e5-131">INPUTS</span></span>

### <span data-ttu-id="a19e5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="a19e5-132">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="a19e5-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a19e5-133">OUTPUTS</span></span>

### <span data-ttu-id="a19e5-134">Microsoft.Azure.Commands.Batch. Models. PSNodeAgentSku</span><span class="sxs-lookup"><span data-stu-id="a19e5-134">Microsoft.Azure.Commands.Batch.Models.PSNodeAgentSku</span></span>

## <span data-ttu-id="a19e5-135">Note</span><span class="sxs-lookup"><span data-stu-id="a19e5-135">NOTES</span></span>

## <span data-ttu-id="a19e5-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a19e5-136">RELATED LINKS</span></span>

[<span data-ttu-id="a19e5-137">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="a19e5-137">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


