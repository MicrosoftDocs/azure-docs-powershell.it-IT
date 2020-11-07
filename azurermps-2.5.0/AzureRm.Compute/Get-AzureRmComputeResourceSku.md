---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
ms.openlocfilehash: e7ebc6a8e6b59679757f559ff2d09ebaa8c5475f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867156"
---
# <span data-ttu-id="6a3b8-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="6a3b8-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="6a3b8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a3b8-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3b8-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="6a3b8-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a3b8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a3b8-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3b8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a3b8-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3b8-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="6a3b8-106">List all compute resource Skus</span></span>

## <span data-ttu-id="6a3b8-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a3b8-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3b8-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a3b8-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="6a3b8-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="6a3b8-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="6a3b8-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a3b8-110">PARAMETERS</span></span>

### <span data-ttu-id="6a3b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3b8-111">-DefaultProfile</span></span>
<span data-ttu-id="6a3b8-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3b8-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3b8-113">CommonParameters</span></span>
<span data-ttu-id="6a3b8-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3b8-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3b8-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3b8-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3b8-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a3b8-116">INPUTS</span></span>

### <span data-ttu-id="6a3b8-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a3b8-117">None</span></span>

## <span data-ttu-id="6a3b8-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a3b8-118">OUTPUTS</span></span>

### <span data-ttu-id="6a3b8-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="6a3b8-119">System.Object</span></span>

## <span data-ttu-id="6a3b8-120">Note</span><span class="sxs-lookup"><span data-stu-id="6a3b8-120">NOTES</span></span>

## <span data-ttu-id="6a3b8-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a3b8-121">RELATED LINKS</span></span>

