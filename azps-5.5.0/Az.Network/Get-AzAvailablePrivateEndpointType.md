---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azavailableprivateendpointtype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzAvailablePrivateEndpointType.md
ms.openlocfilehash: 1ca9e604a1371d83fdedd2986534fa8926b6286b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100187239"
---
# <span data-ttu-id="aa8ff-101">Get-AzAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="aa8ff-101">Get-AzAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="aa8ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa8ff-102">SYNOPSIS</span></span>
<span data-ttu-id="aa8ff-103">Restituire i tipi di punto finale privati disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-103">Return available private end point types in the location.</span></span>

## <span data-ttu-id="aa8ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa8ff-104">SYNTAX</span></span>

```
Get-AzAvailablePrivateEndpointType -Location <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa8ff-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aa8ff-105">DESCRIPTION</span></span>
<span data-ttu-id="aa8ff-106">Il cmdlet **Get-AzAvailablePrivateEndpointType** restituisce tutti i tipi di punto finale privato disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-106">The **Get-AzAvailablePrivateEndpointType** cmdlet returns all available private end point types in the location.</span></span>

## <span data-ttu-id="aa8ff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa8ff-107">EXAMPLES</span></span>

### <span data-ttu-id="aa8ff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa8ff-108">Example 1</span></span>
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

<span data-ttu-id="aa8ff-109">Questo esempio restituisce tutti i tipi di punto finale privato disponibili nella posizione.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-109">This example returns all available private end point types in the location.</span></span>

## <span data-ttu-id="aa8ff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa8ff-110">PARAMETERS</span></span>

### <span data-ttu-id="aa8ff-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa8ff-111">-DefaultProfile</span></span>
<span data-ttu-id="aa8ff-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa8ff-113">-Location</span><span class="sxs-lookup"><span data-stu-id="aa8ff-113">-Location</span></span>
<span data-ttu-id="aa8ff-114">Posizione.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-114">The location.</span></span>

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

### <span data-ttu-id="aa8ff-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa8ff-115">-ResourceGroupName</span></span>
<span data-ttu-id="aa8ff-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-116">The resource group name.</span></span>

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

### <span data-ttu-id="aa8ff-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa8ff-117">CommonParameters</span></span>
<span data-ttu-id="aa8ff-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa8ff-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="aa8ff-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa8ff-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="aa8ff-120">INPUTS</span></span>

### <span data-ttu-id="aa8ff-121">System.String</span><span class="sxs-lookup"><span data-stu-id="aa8ff-121">System.String</span></span>

## <span data-ttu-id="aa8ff-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa8ff-122">OUTPUTS</span></span>

### <span data-ttu-id="aa8ff-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span><span class="sxs-lookup"><span data-stu-id="aa8ff-123">Microsoft.Azure.Commands.Network.Models.PSAvailablePrivateEndpointType</span></span>

## <span data-ttu-id="aa8ff-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="aa8ff-124">NOTES</span></span>

## <span data-ttu-id="aa8ff-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa8ff-125">RELATED LINKS</span></span>
