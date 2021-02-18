---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 4b0eb6188f75b71e3e56107138b6d5e2f9fc7b93
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100406075"
---
# <span data-ttu-id="7c8bf-101">Remove-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7c8bf-101">Remove-AzApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="7c8bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="7c8bf-103">Rimuove la configurazione di escolo della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="7c8bf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c8bf-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7c8bf-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7c8bf-105">DESCRIPTION</span></span>
<span data-ttu-id="7c8bf-106">Il cmdlet **Remove-AzApplicationGatewayConnectionDraining** rimuove la configurazione di estraizione della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-106">The **Remove-AzApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="7c8bf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c8bf-107">EXAMPLES</span></span>

### <span data-ttu-id="7c8bf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c8bf-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="7c8bf-109">Il primo comando recupera il gateway applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw risorsa.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7c8bf-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings back-end.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="7c8bf-111">L'ultimo comando rimuove la configurazione di escolo della connessione delle impostazioni HTTP back-end archiviate in $Settings.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="7c8bf-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c8bf-112">PARAMETERS</span></span>

### <span data-ttu-id="7c8bf-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c8bf-113">-BackendHttpSettings</span></span>
<span data-ttu-id="7c8bf-114">Impostazioni http back-end</span><span class="sxs-lookup"><span data-stu-id="7c8bf-114">The backend http settings</span></span>

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

### <span data-ttu-id="7c8bf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c8bf-115">-DefaultProfile</span></span>
<span data-ttu-id="7c8bf-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c8bf-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c8bf-117">CommonParameters</span></span>
<span data-ttu-id="7c8bf-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c8bf-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c8bf-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c8bf-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c8bf-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="7c8bf-120">INPUTS</span></span>

### <span data-ttu-id="7c8bf-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c8bf-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7c8bf-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c8bf-122">OUTPUTS</span></span>

### <span data-ttu-id="7c8bf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7c8bf-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="7c8bf-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="7c8bf-124">NOTES</span></span>

## <span data-ttu-id="7c8bf-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c8bf-125">RELATED LINKS</span></span>

[<span data-ttu-id="7c8bf-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7c8bf-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)


[<span data-ttu-id="7c8bf-127">Get-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7c8bf-127">Get-AzApplicationGatewayConnectionDraining</span></span>](./Get-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7c8bf-128">New-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7c8bf-128">New-AzApplicationGatewayConnectionDraining</span></span>](./New-AzApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="7c8bf-129">Set-AzApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="7c8bf-129">Set-AzApplicationGatewayConnectionDraining</span></span>](./Set-AzApplicationGatewayConnectionDraining.md)

