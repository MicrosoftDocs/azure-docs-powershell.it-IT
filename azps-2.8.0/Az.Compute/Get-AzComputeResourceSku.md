---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e3c33fb3d61479531303389defb0d7ebdbb3fb64
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675440"
---
# <span data-ttu-id="d4c56-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="d4c56-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="d4c56-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d4c56-102">SYNOPSIS</span></span>
<span data-ttu-id="d4c56-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="d4c56-103">List all compute resource Skus</span></span>

## <span data-ttu-id="d4c56-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d4c56-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4c56-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d4c56-105">DESCRIPTION</span></span>
<span data-ttu-id="d4c56-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="d4c56-106">List all compute resource Skus</span></span>

## <span data-ttu-id="d4c56-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d4c56-107">EXAMPLES</span></span>

### <span data-ttu-id="d4c56-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d4c56-108">Example 1</span></span>
```
PS C:\> PS C:\> Get-AzComputeResourceSku | where {$_.Locations.Contains("westus")};
```

<span data-ttu-id="d4c56-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="d4c56-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="d4c56-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d4c56-110">PARAMETERS</span></span>

### <span data-ttu-id="d4c56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4c56-111">-DefaultProfile</span></span>
<span data-ttu-id="d4c56-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d4c56-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4c56-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4c56-113">CommonParameters</span></span>
<span data-ttu-id="d4c56-114">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4c56-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4c56-115">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d4c56-115">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4c56-116">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d4c56-116">INPUTS</span></span>

### <span data-ttu-id="d4c56-117">Nessuno</span><span class="sxs-lookup"><span data-stu-id="d4c56-117">None</span></span>

## <span data-ttu-id="d4c56-118">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d4c56-118">OUTPUTS</span></span>

### <span data-ttu-id="d4c56-119">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="d4c56-119">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="d4c56-120">Note</span><span class="sxs-lookup"><span data-stu-id="d4c56-120">NOTES</span></span>

## <span data-ttu-id="d4c56-121">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d4c56-121">RELATED LINKS</span></span>
