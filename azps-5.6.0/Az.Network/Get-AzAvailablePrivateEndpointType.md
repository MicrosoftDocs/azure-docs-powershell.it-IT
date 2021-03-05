---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: ae7c7bdd41f21c3f9263a8ea65aab722512543f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993900"
---
# <span data-ttu-id="8cf90-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8cf90-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="8cf90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf90-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf90-103">Restituire i tipi di punto finale privati disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="8cf90-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="8cf90-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cf90-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cf90-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8cf90-105">DESCRIPTION</span></span>
<span data-ttu-id="8cf90-106">Il cmdlet **Get-AzAvailablePrivateEndpointType** restituisce tutti i tipi di punto finale privato disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="8cf90-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="8cf90-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cf90-107">EXAMPLES</span></span>

### <span data-ttu-id="8cf90-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cf90-108">Example 1</span></span>
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

<span data-ttu-id="8cf90-109">Questo esempio restituisce tutti i tipi di punto finale privato disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="8cf90-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="8cf90-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8cf90-110">PARAMETERS</span></span>

### <span data-ttu-id="8cf90-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf90-111">-DefaultProfile</span></span>
<span data-ttu-id="8cf90-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf90-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf90-113">-Location</span><span class="sxs-lookup"><span data-stu-id="8cf90-113">-Location</span></span>
<span data-ttu-id="8cf90-114">Posizione.</span><span class="sxs-lookup"><span data-stu-id="8cf90-114">The location.</span></span>

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

### <span data-ttu-id="8cf90-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf90-115">-ResourceGroupName</span></span>
<span data-ttu-id="8cf90-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cf90-116">The resource group name.</span></span>

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

### <span data-ttu-id="8cf90-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf90-117">CommonParameters</span></span>
<span data-ttu-id="8cf90-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf90-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf90-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="8cf90-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf90-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="8cf90-120">INPUTS</span></span>

### <span data-ttu-id="8cf90-121">System.String</span><span class="sxs-lookup"><span data-stu-id="8cf90-121">System.String</span></span>

## <span data-ttu-id="8cf90-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cf90-122">OUTPUTS</span></span>

### <span data-ttu-id="8cf90-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="8cf90-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="8cf90-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="8cf90-124">NOTES</span></span>

## <span data-ttu-id="8cf90-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cf90-125">RELATED LINKS</span></span>
