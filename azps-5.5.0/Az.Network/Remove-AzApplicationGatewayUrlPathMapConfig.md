---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191782"
---
# <span data-ttu-id="fbdac-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fbdac-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="fbdac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbdac-102">SYNOPSIS</span></span>
<span data-ttu-id="fbdac-103">Rimuove i mapping del percorso URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="fbdac-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="fbdac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fbdac-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbdac-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fbdac-105">DESCRIPTION</span></span>
<span data-ttu-id="fbdac-106">Il cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** rimuove i mapping del percorso dell'URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="fbdac-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="fbdac-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fbdac-107">EXAMPLES</span></span>

### <span data-ttu-id="fbdac-108">Esempio 1: Rimuovere il mapping di un percorso URL da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="fbdac-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="fbdac-109">Il primo comando recupera il gateway applicazione denominato appGwName e archivia il risultato nella $appgw variabile.</span><span class="sxs-lookup"><span data-stu-id="fbdac-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="fbdac-110">Il secondo comando rimuove il mapping del percorso URL denominato map01 dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbdac-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="fbdac-111">Il terzo comando aggiorna il gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="fbdac-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="fbdac-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbdac-112">PARAMETERS</span></span>

### <span data-ttu-id="fbdac-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbdac-113">-ApplicationGateway</span></span>
<span data-ttu-id="fbdac-114">Specifica il gateway applicazione a cui questo cmdlet rimuove la configurazione della mappa del percorso URL.</span><span class="sxs-lookup"><span data-stu-id="fbdac-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbdac-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbdac-115">-DefaultProfile</span></span>
<span data-ttu-id="fbdac-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fbdac-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fbdac-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fbdac-117">-Name</span></span>
<span data-ttu-id="fbdac-118">Specifica il nome della mappa del percorso URL che questo cmdlet rimuove dal server back-end.</span><span class="sxs-lookup"><span data-stu-id="fbdac-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fbdac-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbdac-119">CommonParameters</span></span>
<span data-ttu-id="fbdac-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbdac-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbdac-121">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fbdac-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbdac-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="fbdac-122">INPUTS</span></span>

### <span data-ttu-id="fbdac-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbdac-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fbdac-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fbdac-124">OUTPUTS</span></span>

### <span data-ttu-id="fbdac-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fbdac-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fbdac-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="fbdac-126">NOTES</span></span>

## <span data-ttu-id="fbdac-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fbdac-127">RELATED LINKS</span></span>

[<span data-ttu-id="fbdac-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fbdac-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fbdac-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fbdac-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fbdac-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fbdac-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="fbdac-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="fbdac-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


