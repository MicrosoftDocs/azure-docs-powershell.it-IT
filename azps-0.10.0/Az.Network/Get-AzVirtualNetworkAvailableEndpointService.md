---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: bcd4ba14a14fdacdcdaa0ea85ec8059d2639bdc6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860678"
---
# <span data-ttu-id="62c16-101">Get-AzVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="62c16-101">Get-AzVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="62c16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="62c16-102">SYNOPSIS</span></span>
<span data-ttu-id="62c16-103">Elenca i servizi endpoint disponibili per la posizione.</span><span class="sxs-lookup"><span data-stu-id="62c16-103">Lists available endpoint services for location.</span></span>

## <span data-ttu-id="62c16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="62c16-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="62c16-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="62c16-105">DESCRIPTION</span></span>
<span data-ttu-id="62c16-106">Get-AzVirtualNetworkAvailableEndpointService elenca i servizi endpoint disponibili nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="62c16-106">Get-AzVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="62c16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="62c16-107">EXAMPLES</span></span>

### <span data-ttu-id="62c16-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="62c16-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="62c16-109">Ottiene i servizi endpoint disponibili nell'area di westus.</span><span class="sxs-lookup"><span data-stu-id="62c16-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="62c16-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="62c16-110">PARAMETERS</span></span>

### <span data-ttu-id="62c16-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62c16-111">-DefaultProfile</span></span>
<span data-ttu-id="62c16-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="62c16-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62c16-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="62c16-113">-Location</span></span>
<span data-ttu-id="62c16-114">La posizione in cui recuperare i servizi endpoint.</span><span class="sxs-lookup"><span data-stu-id="62c16-114">The location to retrieve the endpoint services from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62c16-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62c16-115">CommonParameters</span></span>
<span data-ttu-id="62c16-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62c16-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62c16-117">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62c16-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62c16-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="62c16-118">INPUTS</span></span>

### <span data-ttu-id="62c16-119">System. String</span><span class="sxs-lookup"><span data-stu-id="62c16-119">System.String</span></span>

## <span data-ttu-id="62c16-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="62c16-120">OUTPUTS</span></span>

### <span data-ttu-id="62c16-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="62c16-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="62c16-122">Note</span><span class="sxs-lookup"><span data-stu-id="62c16-122">NOTES</span></span>

## <span data-ttu-id="62c16-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="62c16-123">RELATED LINKS</span></span>

