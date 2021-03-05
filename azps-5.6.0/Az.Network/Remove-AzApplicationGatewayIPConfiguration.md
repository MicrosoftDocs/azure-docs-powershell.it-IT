---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 610fe3f2ba4867dc1145488dfe789dba051b23bb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987753"
---
# <span data-ttu-id="a42b5-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a42b5-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="a42b5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a42b5-102">SYNOPSIS</span></span>
<span data-ttu-id="a42b5-103">Rimuove una configurazione IP da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="a42b5-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="a42b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a42b5-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a42b5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a42b5-105">DESCRIPTION</span></span>
<span data-ttu-id="a42b5-106">Il cmdlet **Remove-AzApplicationGatewayIPConfiguration** rimuove una configurazione IP da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a42b5-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="a42b5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a42b5-107">EXAMPLES</span></span>

### <span data-ttu-id="a42b5-108">Esempio 1: Rimuovere una configurazione IP da un gateway applicazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a42b5-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="a42b5-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="a42b5-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="a42b5-110">Il secondo comando rimuove la configurazione IP denominata Subnet02 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="a42b5-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="a42b5-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a42b5-111">PARAMETERS</span></span>

### <span data-ttu-id="a42b5-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a42b5-112">-ApplicationGateway</span></span>
<span data-ttu-id="a42b5-113">Specifica il gateway applicazione da cui rimuovere una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="a42b5-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="a42b5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a42b5-114">-DefaultProfile</span></span>
<span data-ttu-id="a42b5-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a42b5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a42b5-116">-Name</span><span class="sxs-lookup"><span data-stu-id="a42b5-116">-Name</span></span>
<span data-ttu-id="a42b5-117">Specifica il nome della configurazione IP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="a42b5-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="a42b5-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a42b5-118">CommonParameters</span></span>
<span data-ttu-id="a42b5-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a42b5-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a42b5-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a42b5-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a42b5-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="a42b5-121">INPUTS</span></span>

### <span data-ttu-id="a42b5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a42b5-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a42b5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a42b5-123">OUTPUTS</span></span>

### <span data-ttu-id="a42b5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="a42b5-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="a42b5-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="a42b5-125">NOTES</span></span>

## <span data-ttu-id="a42b5-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a42b5-126">RELATED LINKS</span></span>

[<span data-ttu-id="a42b5-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a42b5-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a42b5-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a42b5-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a42b5-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a42b5-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="a42b5-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="a42b5-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


