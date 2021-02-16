---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195055"
---
# <span data-ttu-id="8e4d1-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="8e4d1-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="8e4d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e4d1-102">SYNOPSIS</span></span>
<span data-ttu-id="8e4d1-103">Elencare tutte le SKU delle risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="8e4d1-103">List all compute resource Skus</span></span>

## <span data-ttu-id="8e4d1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8e4d1-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8e4d1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8e4d1-105">DESCRIPTION</span></span>
<span data-ttu-id="8e4d1-106">Elencare tutte le SKU delle risorse di calcolo</span><span class="sxs-lookup"><span data-stu-id="8e4d1-106">List all compute resource Skus</span></span>

## <span data-ttu-id="8e4d1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8e4d1-107">EXAMPLES</span></span>

### <span data-ttu-id="8e4d1-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8e4d1-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="8e4d1-109">Elencare tutte le SKU delle risorse di calcolo nell'area Degli Stati Uniti occidentali</span><span class="sxs-lookup"><span data-stu-id="8e4d1-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="8e4d1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e4d1-110">PARAMETERS</span></span>

### <span data-ttu-id="8e4d1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e4d1-111">-DefaultProfile</span></span>
<span data-ttu-id="8e4d1-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8e4d1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8e4d1-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8e4d1-113">-Location</span></span>
<span data-ttu-id="8e4d1-114">Specifica una posizione delle SKU disponibili da elencare.</span><span class="sxs-lookup"><span data-stu-id="8e4d1-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="8e4d1-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e4d1-115">CommonParameters</span></span>
<span data-ttu-id="8e4d1-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e4d1-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e4d1-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8e4d1-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e4d1-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="8e4d1-118">INPUTS</span></span>

### <span data-ttu-id="8e4d1-119">System.String</span><span class="sxs-lookup"><span data-stu-id="8e4d1-119">System.String</span></span>

## <span data-ttu-id="8e4d1-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8e4d1-120">OUTPUTS</span></span>

### <span data-ttu-id="8e4d1-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="8e4d1-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="8e4d1-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="8e4d1-122">NOTES</span></span>

## <span data-ttu-id="8e4d1-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8e4d1-123">RELATED LINKS</span></span>
