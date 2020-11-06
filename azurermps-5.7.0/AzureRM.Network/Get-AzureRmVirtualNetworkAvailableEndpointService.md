---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkavailableendpointservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkAvailableEndpointService.md
ms.openlocfilehash: e82ff9f04782842fc44a8da95b3e2656c2b86024
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511095"
---
# <span data-ttu-id="1a5fb-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span><span class="sxs-lookup"><span data-stu-id="1a5fb-101">Get-AzureRmVirtualNetworkAvailableEndpointService</span></span>

## <span data-ttu-id="1a5fb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a5fb-102">SYNOPSIS</span></span>
<span data-ttu-id="1a5fb-103">Elenca i servizi endpoint disponibili per la posizione.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-103">Lists available endpoint services for location.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1a5fb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a5fb-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkAvailableEndpointService -Location <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a5fb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a5fb-105">DESCRIPTION</span></span>
<span data-ttu-id="1a5fb-106">Get-AzureRmVirtualNetworkAvailableEndpointService elenca i servizi endpoint disponibili nella posizione specificata.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-106">Get-AzureRmVirtualNetworkAvailableEndpointService lists endpoint services available in the specified location.</span></span>

## <span data-ttu-id="1a5fb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a5fb-107">EXAMPLES</span></span>

### <span data-ttu-id="1a5fb-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1a5fb-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkAvailableEndpointService -Location westus

-Name              Id                                                                                             Type
-----              --                                                                                             ----
-Microsoft.Storage /subscriptions/id/providers/Microsoft.Network/virtualNetworkEndpointServices/Microsoft.Storage Microsoft.Network/virtualNetworkEndpointServices
```

<span data-ttu-id="1a5fb-109">Ottiene i servizi endpoint disponibili nell'area di westus.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-109">Gets available endpoint services in westus region.</span></span>

## <span data-ttu-id="1a5fb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a5fb-110">PARAMETERS</span></span>

### <span data-ttu-id="1a5fb-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a5fb-111">-DefaultProfile</span></span>
<span data-ttu-id="1a5fb-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1a5fb-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1a5fb-113">-Location</span></span>
<span data-ttu-id="1a5fb-114">La posizione in cui recuperare i servizi endpoint.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-114">The location to retrieve the endpoint services from.</span></span>

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

### <span data-ttu-id="1a5fb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a5fb-115">CommonParameters</span></span>
<span data-ttu-id="1a5fb-116">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a5fb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a5fb-117">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a5fb-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a5fb-118">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a5fb-118">INPUTS</span></span>

### <span data-ttu-id="1a5fb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="1a5fb-119">System.String</span></span>

## <span data-ttu-id="1a5fb-120">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a5fb-120">OUTPUTS</span></span>

### <span data-ttu-id="1a5fb-121">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Network. Models. PSEndpointServiceResult, Microsoft. Azure. Commands. Network, Version = 4.2.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="1a5fb-121">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSEndpointServiceResult, Microsoft.Azure.Commands.Network, Version=4.2.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="1a5fb-122">Note</span><span class="sxs-lookup"><span data-stu-id="1a5fb-122">NOTES</span></span>

## <span data-ttu-id="1a5fb-123">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a5fb-123">RELATED LINKS</span></span>

