---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022090"
---
# <span data-ttu-id="14cf7-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="14cf7-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="14cf7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="14cf7-102">SYNOPSIS</span></span>
<span data-ttu-id="14cf7-103">Ottiene le quote del servizio batch per l'abbonamento nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="14cf7-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="14cf7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="14cf7-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14cf7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="14cf7-105">DESCRIPTION</span></span>
<span data-ttu-id="14cf7-106">Ottiene le quote del servizio batch per l'abbonamento specificato nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="14cf7-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="14cf7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="14cf7-107">EXAMPLES</span></span>

### <span data-ttu-id="14cf7-108">Esempio 1: ottenere le quote del servizio batch per l'abbonamento nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="14cf7-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="14cf7-109">Questo comando consente di ottenere le quote per l'abbonamento corrente nell'area ovest degli Stati Uniti.</span><span class="sxs-lookup"><span data-stu-id="14cf7-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="14cf7-110">Il valore restituito indica che questo abbonamento può creare un solo account batch in quell'area geografica.</span><span class="sxs-lookup"><span data-stu-id="14cf7-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="14cf7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="14cf7-111">PARAMETERS</span></span>

### <span data-ttu-id="14cf7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14cf7-112">-DefaultProfile</span></span>
<span data-ttu-id="14cf7-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="14cf7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14cf7-114">-Posizione</span><span class="sxs-lookup"><span data-stu-id="14cf7-114">-Location</span></span>
<span data-ttu-id="14cf7-115">Specifica l'area geografica per cui questo cmdlet controlla le quote.</span><span class="sxs-lookup"><span data-stu-id="14cf7-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="14cf7-116">Per altre informazioni, vedere aree di Azure ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="14cf7-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="14cf7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14cf7-117">CommonParameters</span></span>
<span data-ttu-id="14cf7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14cf7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14cf7-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="14cf7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14cf7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="14cf7-120">INPUTS</span></span>

### <span data-ttu-id="14cf7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="14cf7-121">System.String</span></span>

## <span data-ttu-id="14cf7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="14cf7-122">OUTPUTS</span></span>

### <span data-ttu-id="14cf7-123">Microsoft.Azure.Commands.Batch. Models. PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="14cf7-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="14cf7-124">Note</span><span class="sxs-lookup"><span data-stu-id="14cf7-124">NOTES</span></span>

## <span data-ttu-id="14cf7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="14cf7-125">RELATED LINKS</span></span>
