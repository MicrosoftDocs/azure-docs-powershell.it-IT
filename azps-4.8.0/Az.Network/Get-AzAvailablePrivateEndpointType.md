---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188554"
---
# <span data-ttu-id="6ffa7-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6ffa7-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="6ffa7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6ffa7-102">SYNOPSIS</span></span>
<span data-ttu-id="6ffa7-103">Restituisce i tipi di endpoint privati disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="6ffa7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6ffa7-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ffa7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6ffa7-105">DESCRIPTION</span></span>
<span data-ttu-id="6ffa7-106">Il cmdlet **Get-AzAvailablePrivateEndpointType** restituisce tutti i tipi di endpoint privati disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="6ffa7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6ffa7-107">EXAMPLES</span></span>

### <span data-ttu-id="6ffa7-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6ffa7-108">Example 1</span></span>
```powershell
Get-AzAvailablePrivateEndpointType -Location eastus

[
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename1",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Sql/servers"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename2",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Storage/accounts"
  },
  {
    "id": "subscriptions/00000000-0000-0000-0000-000000000000/providers/Microsoft.Network/locations/availablePrivateEndpointTypes/typename3",
    "type": "Microsoft.Network/availablePrivateEndpointType",
    "resourceName": "Microsoft.Cosmos/cosmosDbAccounts"
  }
]
```

<span data-ttu-id="6ffa7-109">In questo esempio vengono restituiti tutti i tipi di endpoint privati disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="6ffa7-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6ffa7-110">PARAMETERS</span></span>

### <span data-ttu-id="6ffa7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ffa7-111">-DefaultProfile</span></span>
<span data-ttu-id="6ffa7-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ffa7-113">-Posizione</span><span class="sxs-lookup"><span data-stu-id="6ffa7-113">-Location</span></span>
<span data-ttu-id="6ffa7-114">La posizione.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-114">The location.</span></span>

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

### <span data-ttu-id="6ffa7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ffa7-115">-ResourceGroupName</span></span>
<span data-ttu-id="6ffa7-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ffa7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ffa7-117">CommonParameters</span></span>
<span data-ttu-id="6ffa7-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ffa7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ffa7-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6ffa7-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ffa7-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6ffa7-120">INPUTS</span></span>

### <span data-ttu-id="6ffa7-121">System. String</span><span class="sxs-lookup"><span data-stu-id="6ffa7-121">System.String</span></span>

## <span data-ttu-id="6ffa7-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6ffa7-122">OUTPUTS</span></span>

### <span data-ttu-id="6ffa7-123">Microsoft. Azure. Commands. Network. Models. PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="6ffa7-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="6ffa7-124">Note</span><span class="sxs-lookup"><span data-stu-id="6ffa7-124">NOTES</span></span>

## <span data-ttu-id="6ffa7-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6ffa7-125">RELATED LINKS</span></span>
