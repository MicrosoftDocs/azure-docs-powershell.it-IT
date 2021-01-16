---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E43C8D2A-A6B5-4259-94B9-353FBC15F5A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: ec2c73be940e887b4cd1ca96da1442f8ae007ab6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358175"
---
# <span data-ttu-id="91648-101">Remove-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91648-101">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="91648-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="91648-102">SYNOPSIS</span></span>
<span data-ttu-id="91648-103">Rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="91648-103">Removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="91648-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="91648-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayUrlPathMapConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="91648-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="91648-105">DESCRIPTION</span></span>
<span data-ttu-id="91648-106">Il cmdlet **Remove-AzApplicationGatewayUrlPathMapConfig** rimuove i mapping del percorso URL in un pool di server back-end.</span><span class="sxs-lookup"><span data-stu-id="91648-106">The **Remove-AzApplicationGatewayUrlPathMapConfig** cmdlet removes URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="91648-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="91648-107">EXAMPLES</span></span>

### <span data-ttu-id="91648-108">Esempio 1: rimuovere il mapping di un percorso URL da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="91648-108">Example 1: Remove an URL path mapping from an application gateway</span></span>
```
PS C:\> $appgw = Get-AzApplicationGateway -ResourceGroupName "rg" -Name "appGwName"
PS C:\> $appgw = Remove-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway $appgw -Name "map01"
PS C:\> $appgw = Set-AzApplicationGateway -ApplicationGateway $appgw
```

<span data-ttu-id="91648-109">Il primo comando ottiene il gateway dell'applicazione denominato appGwName e archivia il risultato nella variabile $appgw.</span><span class="sxs-lookup"><span data-stu-id="91648-109">The first command gets the application gateway named appGwName and stores the result in the $appgw variable.</span></span>
<span data-ttu-id="91648-110">Il secondo comando rimuove il mapping del percorso URL denominato map01 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91648-110">The second command removes the URL path mapping named map01 from the application gateway.</span></span>
<span data-ttu-id="91648-111">Il terzo comando Aggiorna il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="91648-111">The third command updates the application gateway.</span></span>

## <span data-ttu-id="91648-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="91648-112">PARAMETERS</span></span>

### <span data-ttu-id="91648-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91648-113">-ApplicationGateway</span></span>
<span data-ttu-id="91648-114">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove la configurazione della mappa percorso URL.</span><span class="sxs-lookup"><span data-stu-id="91648-114">Specifies the application gateway to which this cmdlet removes URL path map configuration.</span></span>

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

### <span data-ttu-id="91648-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91648-115">-DefaultProfile</span></span>
<span data-ttu-id="91648-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="91648-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="91648-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="91648-117">-Name</span></span>
<span data-ttu-id="91648-118">Specifica il nome della mappa percorso URL che questo cmdlet rimuove dal server back-end.</span><span class="sxs-lookup"><span data-stu-id="91648-118">Specifies the URL path map name that this cmdlet removes from the backend server.</span></span>

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

### <span data-ttu-id="91648-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91648-119">CommonParameters</span></span>
<span data-ttu-id="91648-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91648-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91648-121">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91648-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91648-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="91648-122">INPUTS</span></span>

### <span data-ttu-id="91648-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91648-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91648-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="91648-124">OUTPUTS</span></span>

### <span data-ttu-id="91648-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="91648-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="91648-126">Note</span><span class="sxs-lookup"><span data-stu-id="91648-126">NOTES</span></span>

## <span data-ttu-id="91648-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="91648-127">RELATED LINKS</span></span>

[<span data-ttu-id="91648-128">Add-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91648-128">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="91648-129">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91648-129">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="91648-130">New-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91648-130">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="91648-131">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="91648-131">Set-AzApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzApplicationGatewayUrlPathMapConfig.md)


