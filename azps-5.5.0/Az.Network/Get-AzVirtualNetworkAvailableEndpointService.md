---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 79517dc748a0599fca588e18d18a9d1e41f5e7fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179855"
---
# <span data-ttu-id="a2d39-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="a2d39-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="a2d39-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2d39-102">SYNOPSIS</span></span>
<span data-ttu-id="a2d39-103">Elenca i servizi endpoint disponibili per la posizione.</span><span class="sxs-lookup"><span data-stu-id="a2d39-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="a2d39-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2d39-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2d39-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a2d39-105">DESCRIPTION</span></span>
<span data-ttu-id="a2d39-106">Get-AzVirtualNetworkAvailableEndpointService elenca i servizi endpoint disponibili nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a2d39-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="a2d39-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2d39-107">EXAMPLES</span></span>

### <span data-ttu-id="a2d39-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2d39-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="a2d39-109">Ottiene i servizi endpoint disponibili nell'area ovest.</span><span class="sxs-lookup"><span data-stu-id="a2d39-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="a2d39-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2d39-110">PARAMETERS</span></span>

### <span data-ttu-id="a2d39-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2d39-111">-DefaultProfile</span></span>
<span data-ttu-id="a2d39-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2d39-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2d39-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a2d39-113">-Location</span></span>
<span data-ttu-id="a2d39-114">Posizione da cui recuperare i servizi endpoint.</span><span class="sxs-lookup"><span data-stu-id="a2d39-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a2d39-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2d39-115">CommonParameters</span></span>
<span data-ttu-id="a2d39-116">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2d39-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2d39-117">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a2d39-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2d39-118">INPUT</span><span class="sxs-lookup"><span data-stu-id="a2d39-118">INPUTS</span></span>

### <span data-ttu-id="a2d39-119">System.String</span><span class="sxs-lookup"><span data-stu-id="a2d39-119">System.String</span></span>

## <span data-ttu-id="a2d39-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2d39-120">OUTPUTS</span></span>

### <span data-ttu-id="a2d39-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="a2d39-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="a2d39-122">NOTE</span><span class="sxs-lookup"><span data-stu-id="a2d39-122">NOTES</span></span>

## <span data-ttu-id="a2d39-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2d39-123">RELATED LINKS</span></span>
