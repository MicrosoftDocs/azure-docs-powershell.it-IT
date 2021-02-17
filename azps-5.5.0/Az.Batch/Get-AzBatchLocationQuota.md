---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 5c20529e174e37bd4d9d5d3f60b56c448206d09e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100205283"
---
# <span data-ttu-id="49b07-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="49b07-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="49b07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b07-102">SYNOPSIS</span></span>
<span data-ttu-id="49b07-103">Ottiene le quote del servizio batch per la sottoscrizione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="49b07-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="49b07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="49b07-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49b07-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="49b07-105">DESCRIPTION</span></span>
<span data-ttu-id="49b07-106">Ottiene le quote del servizio batch per la sottoscrizione specificata nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="49b07-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="49b07-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="49b07-107">EXAMPLES</span></span>

### <span data-ttu-id="49b07-108">Esempio 1: Ottenere le quote del servizio batch per la sottoscrizione nell'area Degli Stati Uniti occidentali</span><span class="sxs-lookup"><span data-stu-id="49b07-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="49b07-109">Questo comando ottiene le quote per la sottoscrizione corrente nell'area degli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="49b07-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="49b07-110">Il valore restituito indica che questa sottoscrizione può creare un solo account batch in tale area geografica.</span><span class="sxs-lookup"><span data-stu-id="49b07-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="49b07-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b07-111">PARAMETERS</span></span>

### <span data-ttu-id="49b07-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b07-112">-DefaultProfile</span></span>
<span data-ttu-id="49b07-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="49b07-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b07-114">-Location</span><span class="sxs-lookup"><span data-stu-id="49b07-114">-Location</span></span>
<span data-ttu-id="49b07-115">Specifica l'area geografica per cui questo cmdlet controlla le quote.</span><span class="sxs-lookup"><span data-stu-id="49b07-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="49b07-116">Per altre informazioni, vedere Azure Regions ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="49b07-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="49b07-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b07-117">CommonParameters</span></span>
<span data-ttu-id="49b07-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49b07-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b07-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49b07-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b07-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="49b07-120">INPUTS</span></span>

### <span data-ttu-id="49b07-121">System.String</span><span class="sxs-lookup"><span data-stu-id="49b07-121">System.String</span></span>

## <span data-ttu-id="49b07-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="49b07-122">OUTPUTS</span></span>

### <span data-ttu-id="49b07-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="49b07-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="49b07-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="49b07-124">NOTES</span></span>

## <span data-ttu-id="49b07-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="49b07-125">RELATED LINKS</span></span>
