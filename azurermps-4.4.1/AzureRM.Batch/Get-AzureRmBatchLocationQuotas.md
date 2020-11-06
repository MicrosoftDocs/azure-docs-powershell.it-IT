---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchLocationQuotas.md
ms.openlocfilehash: 208ba1055523a1dc76de88d665a7b1dbd097144e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516280"
---
# <span data-ttu-id="620dc-101">Get-AzureRmBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="620dc-101">Get-AzureRmBatchLocationQuotas</span></span>

## <span data-ttu-id="620dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="620dc-102">SYNOPSIS</span></span>
<span data-ttu-id="620dc-103">Ottiene le quote del servizio batch per l'abbonamento nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="620dc-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="620dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="620dc-104">SYNTAX</span></span>

```
Get-AzureRmBatchLocationQuotas [-Location] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="620dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="620dc-105">DESCRIPTION</span></span>
<span data-ttu-id="620dc-106">Ottiene le quote del servizio batch per l'abbonamento specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="620dc-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="620dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="620dc-107">EXAMPLES</span></span>

### <span data-ttu-id="620dc-108">Esempio 1: ottenere le quote del servizio batch per l'abbonamento nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="620dc-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzureRmBatchLocationQuotas -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="620dc-109">Questo comando consente di ottenere le quote per l'abbonamento corrente nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="620dc-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="620dc-110">Il valore restituito indica che questo abbonamento può creare un solo account batch in quell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="620dc-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="620dc-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="620dc-111">PARAMETERS</span></span>

### <span data-ttu-id="620dc-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="620dc-112">-Location</span></span>
<span data-ttu-id="620dc-113">Specifica l'area geografica per cui questo cmdlet controlla le quote.</span><span class="sxs-lookup"><span data-stu-id="620dc-113">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="620dc-114">Per altre informazioni, vedere aree di Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="620dc-114">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="620dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="620dc-115">-DefaultProfile</span></span>
<span data-ttu-id="620dc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="620dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="620dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="620dc-117">CommonParameters</span></span>
<span data-ttu-id="620dc-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="620dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="620dc-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="620dc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="620dc-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="620dc-120">INPUTS</span></span>

## <span data-ttu-id="620dc-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="620dc-121">OUTPUTS</span></span>

### <span data-ttu-id="620dc-122">Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="620dc-122">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="620dc-123">Note</span><span class="sxs-lookup"><span data-stu-id="620dc-123">NOTES</span></span>

## <span data-ttu-id="620dc-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="620dc-124">RELATED LINKS</span></span>

