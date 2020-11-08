---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 000B32E9-FFFB-4165-87ED-F19A6E6CEE54
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 50f80f8c7a191c43bb9e8b6b4aed5f44d1ecb85a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94203437"
---
# <span data-ttu-id="dde6a-101">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dde6a-101">Get-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="dde6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="dde6a-102">SYNOPSIS</span></span>
<span data-ttu-id="dde6a-103">Ottiene una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="dde6a-103">Gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="dde6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dde6a-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayUrlPathMapConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dde6a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dde6a-105">DESCRIPTION</span></span>
<span data-ttu-id="dde6a-106">Il cmdlet **Get-AzApplicationGatewayURLPathMapConfig** ottiene una matrice di mapping dei percorsi URL a un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="dde6a-106">The **Get-AzApplicationGatewayURLPathMapConfig** cmdlet gets an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="dde6a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dde6a-107">EXAMPLES</span></span>

### <span data-ttu-id="dde6a-108">Esempio 1: ottenere una configurazione della mappa percorso URL</span><span class="sxs-lookup"><span data-stu-id="dde6a-108">Example 1: Get a URL path map configuration</span></span>
```
PS C:\>Get-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway Gateway
```

<span data-ttu-id="dde6a-109">Questo comando consente di ottenere le configurazioni della mappa percorso URL dal server back-end situato nel gateway dell'applicazione denominato gateway.</span><span class="sxs-lookup"><span data-stu-id="dde6a-109">This command gets the URL path map configurations from the backend server located on the application gateway named Gateway.</span></span>

## <span data-ttu-id="dde6a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="dde6a-110">PARAMETERS</span></span>

### <span data-ttu-id="dde6a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dde6a-111">-ApplicationGateway</span></span>
<span data-ttu-id="dde6a-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="dde6a-112">Specifies the application gateway to which this cmdlet gets a URL path map configuration.</span></span>

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

### <span data-ttu-id="dde6a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde6a-113">-DefaultProfile</span></span>
<span data-ttu-id="dde6a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dde6a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dde6a-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="dde6a-115">-Name</span></span>
<span data-ttu-id="dde6a-116">Specifica il nome della mappa percorso URL in cui questo cmdlet ottiene la configurazione della mappa di percorso.</span><span class="sxs-lookup"><span data-stu-id="dde6a-116">Specifies the URL path map name in which this cmdlet get the path map configuration.</span></span>

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

### <span data-ttu-id="dde6a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde6a-117">CommonParameters</span></span>
<span data-ttu-id="dde6a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde6a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde6a-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dde6a-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde6a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="dde6a-120">INPUTS</span></span>

### <span data-ttu-id="dde6a-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dde6a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dde6a-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dde6a-122">OUTPUTS</span></span>

### <span data-ttu-id="dde6a-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayUrlPathMap</span><span class="sxs-lookup"><span data-stu-id="dde6a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap</span></span>

## <span data-ttu-id="dde6a-124">Note</span><span class="sxs-lookup"><span data-stu-id="dde6a-124">NOTES</span></span>

## <span data-ttu-id="dde6a-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dde6a-125">RELATED LINKS</span></span>

[<span data-ttu-id="dde6a-126">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dde6a-126">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dde6a-127">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dde6a-127">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dde6a-128">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dde6a-128">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="dde6a-129">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="dde6a-129">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


