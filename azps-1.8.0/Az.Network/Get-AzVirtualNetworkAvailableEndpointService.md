---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: 2de970201456f941d8b35d40c569c41e114468c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678443"
---
# <span data-ttu-id="a3d0a-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="a3d0a-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="a3d0a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3d0a-102">SYNOPSIS</span></span>
<span data-ttu-id="a3d0a-103">Elenca i servizi endpoint disponibili per la posizione.</span><span class="sxs-lookup"><span data-stu-id="a3d0a-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="a3d0a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3d0a-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a3d0a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3d0a-105">DESCRIPTION</span></span>
<span data-ttu-id="a3d0a-106">Get-AzVirtualNetworkAvailableEndpointService elenca i servizi endpoint disponibili nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="a3d0a-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="a3d0a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3d0a-107">EXAMPLES</span></span>

### <span data-ttu-id="a3d0a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a3d0a-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="a3d0a-109">Ottiene i servizi endpoint disponibili nell'area di westus.</span><span class="sxs-lookup"><span data-stu-id="a3d0a-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="a3d0a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3d0a-110">PARAMETERS</span></span>

### <span data-ttu-id="a3d0a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3d0a-111">-DefaultProfile</span></span>
<span data-ttu-id="a3d0a-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3d0a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3d0a-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="a3d0a-113">-Location</span></span>
<span data-ttu-id="a3d0a-114">La posizione in cui recuperare i servizi endpoint.</span><span class="sxs-lookup"><span data-stu-id="a3d0a-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="a3d0a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3d0a-115">CommonParameters</span></span>
<span data-ttu-id="a3d0a-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3d0a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3d0a-117">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3d0a-117">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3d0a-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3d0a-118">INPUTS</span></span>

### <span data-ttu-id="a3d0a-119">System. String</span><span class="sxs-lookup"><span data-stu-id="a3d0a-119">System.String</span></span>

## <span data-ttu-id="a3d0a-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3d0a-120">OUTPUTS</span></span>

### <span data-ttu-id="a3d0a-121">Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult</span><span class="sxs-lookup"><span data-stu-id="a3d0a-121">Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult</span></span>

## <span data-ttu-id="a3d0a-122">Note</span><span class="sxs-lookup"><span data-stu-id="a3d0a-122">NOTES</span></span>

## <span data-ttu-id="a3d0a-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3d0a-123">RELATED LINKS</span></span>
