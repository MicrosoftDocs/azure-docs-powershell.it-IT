---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191998"
---
# <span data-ttu-id="2d223-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d223-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="2d223-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d223-102">SYNOPSIS</span></span>
<span data-ttu-id="2d223-103">Ottiene una matrice di mapping del percorso URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="2d223-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2d223-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2d223-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2d223-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="2d223-105">DESCRIPTION</span></span>
<span data-ttu-id="2d223-106">Il cmdlet **Get-AzApplicationGatewayURLPathMapConfig** ottiene una matrice di mapping del percorso URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="2d223-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="2d223-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2d223-107">EXAMPLES</span></span>

### <span data-ttu-id="2d223-108">Esempio 1: Ottenere una configurazione della mappa del percorso URL</span><span class="sxs-lookup"><span data-stu-id="2d223-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="2d223-109">Questo comando recupera le configurazioni della mappa del percorso URL dal server back-end che si trova nel gateway applicazione denominato Gateway.</span><span class="sxs-lookup"><span data-stu-id="2d223-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="2d223-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d223-110">PARAMETERS</span></span>

### <span data-ttu-id="2d223-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d223-111">-ApplicationGateway</span></span>
<span data-ttu-id="2d223-112">Specifica il gateway applicazione a cui questo cmdlet ottiene una configurazione di mappa del percorso URL.</span><span class="sxs-lookup"><span data-stu-id="2d223-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="2d223-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d223-113">-DefaultProfile</span></span>
<span data-ttu-id="2d223-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2d223-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d223-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2d223-115">-Name</span></span>
<span data-ttu-id="2d223-116">Specifica il nome della mappa del percorso URL in cui questo cmdlet ottiene la configurazione della mappa del percorso.</span><span class="sxs-lookup"><span data-stu-id="2d223-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2d223-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d223-117">CommonParameters</span></span>
<span data-ttu-id="2d223-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d223-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d223-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2d223-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d223-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="2d223-120">INPUTS</span></span>

### <span data-ttu-id="2d223-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2d223-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2d223-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2d223-122">OUTPUTS</span></span>

### <span data-ttu-id="2d223-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="2d223-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="2d223-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="2d223-124">NOTES</span></span>

## <span data-ttu-id="2d223-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2d223-125">RELATED LINKS</span></span>

[<span data-ttu-id="2d223-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d223-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2d223-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d223-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2d223-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d223-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="2d223-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="2d223-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


