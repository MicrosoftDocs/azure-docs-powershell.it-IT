---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azcomputeresourcesku
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzComputeResourceSku.md
ms.openlocfilehash: 970cbb3e03a4934f648df2f6f8c06275a30740de
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477851"
---
# <span data-ttu-id="dc0b3-101">Get-AzComputeResourceSku</span><span class="sxs-lookup"><span data-stu-id="dc0b3-101">Get-AzComputeResourceSku</span></span>

## <span data-ttu-id="dc0b3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dc0b3-102">SYNOPSIS</span></span>
<span data-ttu-id="dc0b3-103">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="dc0b3-103">List all compute resource Skus</span></span>

## <span data-ttu-id="dc0b3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dc0b3-104">SYNTAX</span></span>

```
Get-AzComputeResourceSku [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc0b3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc0b3-105">DESCRIPTION</span></span>
<span data-ttu-id="dc0b3-106">Elenca tutte le SKU di risorse COMPUTE</span><span class="sxs-lookup"><span data-stu-id="dc0b3-106">List all compute resource Skus</span></span>

## <span data-ttu-id="dc0b3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dc0b3-107">EXAMPLES</span></span>

### <span data-ttu-id="dc0b3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dc0b3-108">Example 1</span></span>
```
PS C:\> Get-AzComputeResourceSku "westus";
```

<span data-ttu-id="dc0b3-109">Elenca tutti gli SKU delle risorse di calcolo nell'area ovest degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="dc0b3-109">List all compute resource skus in West US region</span></span>

## <span data-ttu-id="dc0b3-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dc0b3-110">PARAMETERS</span></span>

### <span data-ttu-id="dc0b3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc0b3-111">-DefaultProfile</span></span>
<span data-ttu-id="dc0b3-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dc0b3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dc0b3-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="dc0b3-113">-Location</span></span>
<span data-ttu-id="dc0b3-114">Specifica una posizione dell'elenco SKU disponibili.</span><span class="sxs-lookup"><span data-stu-id="dc0b3-114">Specifies a location of the available skus to list.</span></span>

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

### <span data-ttu-id="dc0b3-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc0b3-115">CommonParameters</span></span>
<span data-ttu-id="dc0b3-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc0b3-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc0b3-117">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dc0b3-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc0b3-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dc0b3-118">INPUTS</span></span>

### <span data-ttu-id="dc0b3-119">System. String</span><span class="sxs-lookup"><span data-stu-id="dc0b3-119">System.String</span></span>

## <span data-ttu-id="dc0b3-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dc0b3-120">OUTPUTS</span></span>

### <span data-ttu-id="dc0b3-121">Microsoft. Azure. Commands. Compute. Automation. Models. PSResourceSku</span><span class="sxs-lookup"><span data-stu-id="dc0b3-121">Microsoft.Azure.Commands.Compute.Automation.Models.PSResourceSku</span></span>

## <span data-ttu-id="dc0b3-122">Note</span><span class="sxs-lookup"><span data-stu-id="dc0b3-122">NOTES</span></span>

## <span data-ttu-id="dc0b3-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dc0b3-123">RELATED LINKS</span></span>
