---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: ab57e922a7ef63d14a36bbd91ed268822e2c61e1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021649"
---
# <span data-ttu-id="364f0-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="364f0-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="364f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="364f0-102">SYNOPSIS</span></span>
<span data-ttu-id="364f0-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="364f0-103">List all compute resource Skus</span></span>

## <span data-ttu-id="364f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="364f0-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="364f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="364f0-105">DESCRIPTION</span></span>
<span data-ttu-id="364f0-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="364f0-106">List all compute resource Skus</span></span>

## <span data-ttu-id="364f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="364f0-107">EXAMPLES</span></span>

### <span data-ttu-id="364f0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="364f0-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="364f0-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="364f0-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="364f0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="364f0-110">PARAMETERS</span></span>

### <span data-ttu-id="364f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="364f0-111">-DefaultProfile</span></span>
<span data-ttu-id="364f0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="364f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="364f0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="364f0-113">CommonParameters</span></span>
<span data-ttu-id="364f0-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="364f0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="364f0-115">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="364f0-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="364f0-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="364f0-116">INPUTS</span></span>

### <span data-ttu-id="364f0-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="364f0-117">None</span></span>

## <span data-ttu-id="364f0-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="364f0-118">OUTPUTS</span></span>

### <span data-ttu-id="364f0-119">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="364f0-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="364f0-120">Note</span><span class="sxs-lookup"><span data-stu-id="364f0-120">NOTES</span></span>

## <span data-ttu-id="364f0-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="364f0-121">RELATED LINKS</span></span>
