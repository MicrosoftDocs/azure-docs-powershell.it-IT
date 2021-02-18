---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6943BB5C-D709-4A80-AF5E-DC9501C20680
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 87f6f441220f1f8ab47fee5356bddca8d02b96c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206627"
---
# <span data-ttu-id="d3287-101">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3287-101">Remove-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d3287-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3287-102">SYNOPSIS</span></span>
<span data-ttu-id="d3287-103">Rimuove una configurazione IP da un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d3287-103">Removes an IP configuration from an application gateway.</span></span>

## <span data-ttu-id="d3287-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3287-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayIPConfiguration -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3287-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3287-105">DESCRIPTION</span></span>
<span data-ttu-id="d3287-106">Il cmdlet **Remove-AzApplicationGatewayIPConfiguration** rimuove una configurazione IP da un gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="d3287-106">The **Remove-AzApplicationGatewayIPConfiguration** cmdlet removes an IP configuration from an Azure application gateway.</span></span>

## <span data-ttu-id="d3287-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3287-107">EXAMPLES</span></span>

### <span data-ttu-id="d3287-108">Esempio 1: Rimuovere una configurazione IP da un gateway applicazione di Azure</span><span class="sxs-lookup"><span data-stu-id="d3287-108">Example 1: Remove an IP configuration from an Azure application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Subnet02"
```

<span data-ttu-id="d3287-109">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="d3287-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="d3287-110">Il secondo comando rimuove la configurazione IP denominata Subnet02 dal gateway applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d3287-110">The second command removes the IP configuration named Subnet02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="d3287-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3287-111">PARAMETERS</span></span>

### <span data-ttu-id="d3287-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3287-112">-ApplicationGateway</span></span>
<span data-ttu-id="d3287-113">Specifica il gateway applicazione da cui rimuovere una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="d3287-113">Specifies the application gateway from which to remove an IP configuration.</span></span>

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

### <span data-ttu-id="d3287-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3287-114">-DefaultProfile</span></span>
<span data-ttu-id="d3287-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3287-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3287-116">-Name</span><span class="sxs-lookup"><span data-stu-id="d3287-116">-Name</span></span>
<span data-ttu-id="d3287-117">Specifica il nome della configurazione IP da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="d3287-117">Specifies the name of the IP configuration to remove.</span></span>

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

### <span data-ttu-id="d3287-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3287-118">CommonParameters</span></span>
<span data-ttu-id="d3287-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3287-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3287-120">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3287-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3287-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3287-121">INPUTS</span></span>

### <span data-ttu-id="d3287-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3287-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3287-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3287-123">OUTPUTS</span></span>

### <span data-ttu-id="d3287-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3287-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3287-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3287-125">NOTES</span></span>

## <span data-ttu-id="d3287-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3287-126">RELATED LINKS</span></span>

[<span data-ttu-id="d3287-127">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3287-127">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d3287-128">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3287-128">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d3287-129">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3287-129">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d3287-130">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3287-130">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


