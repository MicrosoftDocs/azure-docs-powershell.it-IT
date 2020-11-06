---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmComputeResourceSku.md
ms.openlocfilehash: fd4a06375a4dfab7f8b8cd4b08a2112310e99b73
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521273"
---
# <span data-ttu-id="19dd5-101">Get-AzureRmComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="19dd5-101">Get-AzureRmComputeResourceSku</span></span>

## <span data-ttu-id="19dd5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="19dd5-102">SYNOPSIS</span></span>
<span data-ttu-id="19dd5-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="19dd5-103">List all compute resource Skus</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19dd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="19dd5-104">SYNTAX</span></span>

```
Get-AzureRmComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19dd5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19dd5-105">DESCRIPTION</span></span>
<span data-ttu-id="19dd5-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="19dd5-106">List all compute resource Skus</span></span>

## <span data-ttu-id="19dd5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="19dd5-107">EXAMPLES</span></span>

### <span data-ttu-id="19dd5-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="19dd5-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzureRmComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="19dd5-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="19dd5-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="19dd5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="19dd5-110">PARAMETERS</span></span>

### <span data-ttu-id="19dd5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dd5-111">-DefaultProfile</span></span>
<span data-ttu-id="19dd5-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="19dd5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19dd5-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dd5-113">CommonParameters</span></span>
<span data-ttu-id="19dd5-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19dd5-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dd5-115">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19dd5-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dd5-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="19dd5-116">INPUTS</span></span>

### <span data-ttu-id="19dd5-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="19dd5-117">None</span></span>

## <span data-ttu-id="19dd5-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="19dd5-118">OUTPUTS</span></span>

### <span data-ttu-id="19dd5-119">System. Object</span><span class="sxs-lookup"><span data-stu-id="19dd5-119">System.Object</span></span>

## <span data-ttu-id="19dd5-120">Note</span><span class="sxs-lookup"><span data-stu-id="19dd5-120">NOTES</span></span>

## <span data-ttu-id="19dd5-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="19dd5-121">RELATED LINKS</span></span>

