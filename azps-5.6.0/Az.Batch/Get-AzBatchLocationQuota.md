---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: A39A415A-B403-48D3-AF80-CF7CFE382577
online version: https://docs.microsoft.com/powershell/module/az.batch/get-azbatchlocationquota
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchLocationQuota.md
ms.openlocfilehash: 297b862cb9491c0659d5fd2ec5ab0da4fc071e4b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959006"
---
# <span data-ttu-id="953b7-101">Get-AzBatchLocationQuota</span><span class="sxs-lookup"><span data-stu-id="953b7-101">Get-AzBatchLocationQuota</span></span>

## <span data-ttu-id="953b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="953b7-102">SYNOPSIS</span></span>
<span data-ttu-id="953b7-103">Ottiene le quote del servizio batch per la sottoscrizione nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="953b7-103">Gets the Batch service quotas for your subscription at the given location.</span></span>

## <span data-ttu-id="953b7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="953b7-104">SYNTAX</span></span>

```
Get-AzBatchLocationQuota [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="953b7-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="953b7-105">DESCRIPTION</span></span>
<span data-ttu-id="953b7-106">Ottiene le quote del servizio batch per la sottoscrizione specificata nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="953b7-106">Gets the Batch service quotas for the specified subscription at the given location.</span></span>

## <span data-ttu-id="953b7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="953b7-107">EXAMPLES</span></span>

### <span data-ttu-id="953b7-108">Esempio 1: Ottenere le quote del servizio batch per la sottoscrizione nell'area Degli Stati Uniti occidentali</span><span class="sxs-lookup"><span data-stu-id="953b7-108">Example 1: Get the Batch service quotas for the subscription in the West US region</span></span>
```
PS C:\>Get-AzBatchLocationQuota -Location "westus"
          AccountQuota Location
          ------------ --------
          1            westus
```

<span data-ttu-id="953b7-109">Questo comando ottiene le quote per la sottoscrizione corrente nell'area degli Stati Uniti occidentali.</span><span class="sxs-lookup"><span data-stu-id="953b7-109">This command gets the quotas for the current subscription in the West US region.</span></span>
<span data-ttu-id="953b7-110">Il valore restituito indica che questa sottoscrizione può creare un solo account batch in tale area geografica.</span><span class="sxs-lookup"><span data-stu-id="953b7-110">The return value indicates that this subscription can create only one Batch account in that region.</span></span>

## <span data-ttu-id="953b7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="953b7-111">PARAMETERS</span></span>

### <span data-ttu-id="953b7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="953b7-112">-DefaultProfile</span></span>
<span data-ttu-id="953b7-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="953b7-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="953b7-114">-Location</span><span class="sxs-lookup"><span data-stu-id="953b7-114">-Location</span></span>
<span data-ttu-id="953b7-115">Specifica l'area geografica per cui questo cmdlet controlla le quote.</span><span class="sxs-lookup"><span data-stu-id="953b7-115">Specifies the region for which this cmdlet checks the quotas.</span></span>
<span data-ttu-id="953b7-116">Per altre informazioni, vedere Azure Regions ( https://azure.microsoft.com/regions) .</span><span class="sxs-lookup"><span data-stu-id="953b7-116">For more information, see Azure Regions (https://azure.microsoft.com/regions).</span></span>

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

### <span data-ttu-id="953b7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="953b7-117">CommonParameters</span></span>
<span data-ttu-id="953b7-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="953b7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="953b7-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="953b7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="953b7-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="953b7-120">INPUTS</span></span>

### <span data-ttu-id="953b7-121">System.String</span><span class="sxs-lookup"><span data-stu-id="953b7-121">System.String</span></span>

## <span data-ttu-id="953b7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="953b7-122">OUTPUTS</span></span>

### <span data-ttu-id="953b7-123">Microsoft.Azure.Commands.Batch. Models.PSBatchLocationQuotas</span><span class="sxs-lookup"><span data-stu-id="953b7-123">Microsoft.Azure.Commands.Batch.Models.PSBatchLocationQuotas</span></span>

## <span data-ttu-id="953b7-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="953b7-124">NOTES</span></span>

## <span data-ttu-id="953b7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="953b7-125">RELATED LINKS</span></span>
