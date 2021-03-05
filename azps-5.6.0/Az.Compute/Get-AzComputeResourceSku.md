---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: e2b3dd89152b376ac12826eeb342c80486c2c39a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983757"
---
# <span data-ttu-id="33774-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="33774-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="33774-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33774-102">SYNOPSIS</span></span>
<span data-ttu-id="33774-103">Elencare tutte le SKU delle risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="33774-103">List all compute resource Skus</span></span>

## <span data-ttu-id="33774-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33774-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33774-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33774-105">DESCRIPTION</span></span>
<span data-ttu-id="33774-106">Elencare tutte le SKU delle risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="33774-106">List all compute resource Skus</span></span>

## <span data-ttu-id="33774-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33774-107">EXAMPLES</span></span>

### <span data-ttu-id="33774-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33774-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="33774-109">Elencare tutte le SKU delle risorse di calcolo nell'area Degli Stati Uniti occidentali</span><span class="sxs-lookup"><span data-stu-id="33774-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="33774-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33774-110">PARAMETERS</span></span>

### <span data-ttu-id="33774-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33774-111">-DefaultProfile</span></span>
<span data-ttu-id="33774-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33774-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33774-113">-Location</span><span class="sxs-lookup"><span data-stu-id="33774-113">-Location</span></span>
<span data-ttu-id="33774-114">Specifica una posizione delle SKU disponibili da elencare.</span><span class="sxs-lookup"><span data-stu-id="33774-114">Specifies a location of the available skus to list.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33774-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33774-115">CommonParameters</span></span>
<span data-ttu-id="33774-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33774-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33774-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="33774-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33774-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="33774-118">INPUTS</span></span>

### <span data-ttu-id="33774-119">System.String</span><span class="sxs-lookup"><span data-stu-id="33774-119">System.String</span></span>

## <span data-ttu-id="33774-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33774-120">OUTPUTS</span></span>

### <span data-ttu-id="33774-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="33774-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="33774-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="33774-122">NOTES</span></span>

## <span data-ttu-id="33774-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33774-123">RELATED LINKS</span></span>
