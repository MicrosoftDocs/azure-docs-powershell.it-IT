---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 751a551f5ed0a0a1968c74e5f94bcabad3b5ff32
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863822"
---
# <span data-ttu-id="a0115-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="a0115-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="a0115-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0115-102">SYNOPSIS</span></span>
<span data-ttu-id="a0115-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="a0115-103">List all compute resource Skus</span></span>

## <span data-ttu-id="a0115-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0115-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0115-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0115-105">DESCRIPTION</span></span>
<span data-ttu-id="a0115-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="a0115-106">List all compute resource Skus</span></span>

## <span data-ttu-id="a0115-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0115-107">EXAMPLES</span></span>

### <span data-ttu-id="a0115-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0115-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="a0115-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="a0115-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="a0115-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0115-110">PARAMETERS</span></span>

### <span data-ttu-id="a0115-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0115-111">-DefaultProfile</span></span>
<span data-ttu-id="a0115-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0115-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0115-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0115-113">CommonParameters</span></span>
<span data-ttu-id="a0115-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0115-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0115-115">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0115-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0115-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0115-116">INPUTS</span></span>

### <span data-ttu-id="a0115-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a0115-117">None</span></span>

## <span data-ttu-id="a0115-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0115-118">OUTPUTS</span></span>

### <span data-ttu-id="a0115-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="a0115-119">System.Object</span></span>

## <span data-ttu-id="a0115-120">Note</span><span class="sxs-lookup"><span data-stu-id="a0115-120">NOTES</span></span>

## <span data-ttu-id="a0115-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0115-121">RELATED LINKS</span></span>

