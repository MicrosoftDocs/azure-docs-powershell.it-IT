---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: cf10674f3140e618b82b40e6c8288126cb941c3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511900"
---
# <span data-ttu-id="cbdf4-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="cbdf4-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="cbdf4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbdf4-102">SYNOPSIS</span></span>
<span data-ttu-id="cbdf4-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="cbdf4-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cbdf4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbdf4-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cbdf4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbdf4-105">DESCRIPTION</span></span>
<span data-ttu-id="cbdf4-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="cbdf4-106">List all compute resource Skus</span></span>

## <span data-ttu-id="cbdf4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbdf4-107">EXAMPLES</span></span>

### <span data-ttu-id="cbdf4-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cbdf4-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="cbdf4-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="cbdf4-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="cbdf4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbdf4-110">PARAMETERS</span></span>

### <span data-ttu-id="cbdf4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbdf4-111">-DefaultProfile</span></span>
<span data-ttu-id="cbdf4-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbdf4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cbdf4-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbdf4-113">CommonParameters</span></span>
<span data-ttu-id="cbdf4-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbdf4-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbdf4-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbdf4-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbdf4-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbdf4-116">INPUTS</span></span>

### <span data-ttu-id="cbdf4-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cbdf4-117">None</span></span>

## <span data-ttu-id="cbdf4-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbdf4-118">OUTPUTS</span></span>

### <span data-ttu-id="cbdf4-119">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="cbdf4-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="cbdf4-120">Note</span><span class="sxs-lookup"><span data-stu-id="cbdf4-120">NOTES</span></span>

## <span data-ttu-id="cbdf4-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbdf4-121">RELATED LINKS</span></span>