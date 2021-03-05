---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 3d1df3262fa9cee55d5aa49c026b7b1e681b5c00
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996587"
---
# <span data-ttu-id="e1698-101">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e1698-101">Get-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="e1698-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1698-102">SYNOPSIS</span></span>
<span data-ttu-id="e1698-103">Recupera la configurazione di escolo della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="e1698-103">Gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="e1698-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1698-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1698-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1698-105">DESCRIPTION</span></span>
<span data-ttu-id="e1698-106">Il cmdlet **Get-AzApplicationGatewayConnectionDraining ottiene** la configurazione di estraizione della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="e1698-106">The **Get-AzApplicationGatewayConnectionDraining** cmdlet gets the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="e1698-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1698-107">EXAMPLES</span></span>

### <span data-ttu-id="e1698-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e1698-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> $ConnectionDraining = Get-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="e1698-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="e1698-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e1698-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e le archivia nella variabile $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="e1698-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="e1698-111">L'ultimo comando recupera la configurazione di escolo della connessione dal $Settings HTTP back-end e la archivia nella $ConnectionDraining variabile.</span><span class="sxs-lookup"><span data-stu-id="e1698-111">The last command gets the connection draining configuration from the back-end HTTP settings $Settings and stores it in the $ConnectionDraining variable.</span></span>

## <span data-ttu-id="e1698-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1698-112">PARAMETERS</span></span>

### <span data-ttu-id="e1698-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e1698-113">-BackendHttpSettings</span></span>
<span data-ttu-id="e1698-114">Impostazioni http back-end</span><span class="sxs-lookup"><span data-stu-id="e1698-114">The backend http settings</span></span>

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

### <span data-ttu-id="e1698-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1698-115">-DefaultProfile</span></span>
<span data-ttu-id="e1698-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1698-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1698-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1698-117">CommonParameters</span></span>
<span data-ttu-id="e1698-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1698-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1698-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1698-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1698-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1698-120">INPUTS</span></span>

### <span data-ttu-id="e1698-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e1698-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="e1698-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1698-122">OUTPUTS</span></span>

### <span data-ttu-id="e1698-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e1698-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="e1698-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1698-124">NOTES</span></span>

## <span data-ttu-id="e1698-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1698-125">RELATED LINKS</span></span>

[<span data-ttu-id="e1698-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e1698-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="e1698-127">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e1698-127">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e1698-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e1698-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="e1698-129">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e1698-129">Remove-AzApplicationGatewayConnectionDraining</span></span>](./Remove-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="e1698-130">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e1698-130">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)
