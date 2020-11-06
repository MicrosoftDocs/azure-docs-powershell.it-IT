---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: b9e1c42ca3a67a80a939a4e79626253b903764f4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510028"
---
# <span data-ttu-id="f8f02-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="f8f02-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="f8f02-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8f02-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f02-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="f8f02-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8f02-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8f02-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [<CommonParameters>]
```

## <span data-ttu-id="f8f02-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8f02-105">DESCRIPTION</span></span>
<span data-ttu-id="f8f02-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="f8f02-106">List all compute resource Skus</span></span>

## <span data-ttu-id="f8f02-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8f02-107">EXAMPLES</span></span>

### <span data-ttu-id="f8f02-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f8f02-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="f8f02-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="f8f02-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="f8f02-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8f02-110">PARAMETERS</span></span>

### <span data-ttu-id="f8f02-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f02-111">CommonParameters</span></span>
<span data-ttu-id="f8f02-112">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f02-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f02-113">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f02-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f02-114">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8f02-114">INPUTS</span></span>

### <span data-ttu-id="f8f02-115">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f8f02-115">None</span></span>


## <span data-ttu-id="f8f02-116">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8f02-116">OUTPUTS</span></span>

### <span data-ttu-id="f8f02-117">System. Object</span><span class="sxs-lookup"><span data-stu-id="f8f02-117">System.Object</span></span>

## <span data-ttu-id="f8f02-118">Note</span><span class="sxs-lookup"><span data-stu-id="f8f02-118">NOTES</span></span>

## <span data-ttu-id="f8f02-119">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8f02-119">RELATED LINKS</span></span>

