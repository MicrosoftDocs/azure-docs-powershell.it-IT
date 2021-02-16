---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 1630b0177efbccbf4d1cba674f0cf11ab457307e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402117"
---
# <span data-ttu-id="cde1c-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cde1c-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="cde1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cde1c-102">SYNOPSIS</span></span>
<span data-ttu-id="cde1c-103">Recupera la configurazione di escolo della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="cde1c-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="cde1c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cde1c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cde1c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cde1c-105">DESCRIPTION</span></span>
<span data-ttu-id="cde1c-106">Il cmdlet **Get-AzApplicationGatewayConnectionDraining ottiene** la configurazione di estraizione della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="cde1c-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="cde1c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cde1c-107">EXAMPLES</span></span>

### <span data-ttu-id="cde1c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cde1c-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="cde1c-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="cde1c-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="cde1c-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="cde1c-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="cde1c-111">L'ultimo comando recupera la configurazione di escolo della connessione dal $Settings HTTP back-end e la archivia nella $ConnectionDraining variabile.</span><span class="sxs-lookup"><span data-stu-id="cde1c-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="cde1c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cde1c-112">PARAMETERS</span></span>

### <span data-ttu-id="cde1c-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cde1c-113">-BackendHttpSettings</span></span>
<span data-ttu-id="cde1c-114">Impostazioni http back-end</span><span class="sxs-lookup"><span data-stu-id="cde1c-114">The backend http settings</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cde1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cde1c-115">-DefaultProfile</span></span>
<span data-ttu-id="cde1c-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cde1c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cde1c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cde1c-117">CommonParameters</span></span>
<span data-ttu-id="cde1c-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cde1c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cde1c-119">Per altre informazioni, [vedere](https://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cde1c-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cde1c-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="cde1c-120">INPUTS</span></span>

### <span data-ttu-id="cde1c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="cde1c-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="cde1c-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cde1c-122">OUTPUTS</span></span>

### <span data-ttu-id="cde1c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cde1c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="cde1c-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="cde1c-124">NOTES</span></span>

## <span data-ttu-id="cde1c-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cde1c-125">RELATED LINKS</span></span>

[<span data-ttu-id="cde1c-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="cde1c-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="cde1c-127">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cde1c-127">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="cde1c-128">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cde1c-128">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="cde1c-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="cde1c-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
