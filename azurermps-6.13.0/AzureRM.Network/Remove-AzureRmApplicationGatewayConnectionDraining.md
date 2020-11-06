---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayconnectiondraining
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayConnectionDraining.md
ms.openlocfilehash: 92e1f701eb9d0eafdea72ba031a7799c7c0adbce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510880"
---
# <span data-ttu-id="89def-101">Remove-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89def-101">Remove-AzureRmApplicationGatewayConnectionDraining</span></span>

## <span data-ttu-id="89def-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="89def-102">SYNOPSIS</span></span>
<span data-ttu-id="89def-103">Rimuove la configurazione di svuotamento della connessione di un oggetto impostazioni HTTP back-end.</span><span class="sxs-lookup"><span data-stu-id="89def-103">Removes the connection draining configuration of a back-end HTTP settings object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89def-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="89def-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayConnectionDraining
 -BackendHttpSettings <PSApplicationGatewayBackendHttpSettings> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="89def-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="89def-105">DESCRIPTION</span></span>
<span data-ttu-id="89def-106">Il cmdlet **Remove-AzureRmApplicationGatewayConnectionDraining** rimuove la configurazione di svuotamento della connessione di un oggetto impostazioni http back-end.</span><span class="sxs-lookup"><span data-stu-id="89def-106">The **Remove-AzureRmApplicationGatewayConnectionDraining** cmdlet removes the connection draining configuration of a back-end HTTP settings object.</span></span>

## <span data-ttu-id="89def-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="89def-107">EXAMPLES</span></span>

### <span data-ttu-id="89def-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="89def-108">Example 1</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Settings  = Get-AzureRmApplicationGatewayBackendHttpSettings -Name "Settings01" -ApplicationGateway $AppGw
PS C:\> Remove-AzureRmApplicationGatewayConnectionDraining -BackendHttpSettings $Settings
```

<span data-ttu-id="89def-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 nel gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="89def-109">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="89def-110">Il secondo comando recupera le impostazioni HTTP di back-end denominate Settings01 per $AppGw e archivia le impostazioni nella variabile $Settings.</span><span class="sxs-lookup"><span data-stu-id="89def-110">The second command gets the back-end HTTP settings named Settings01 for $AppGw and stores the settings in the $Settings variable.</span></span>
<span data-ttu-id="89def-111">L'ultimo comando rimuove la configurazione di svuotamento della connessione delle impostazioni HTTP back-end archiviate in $Settings.</span><span class="sxs-lookup"><span data-stu-id="89def-111">The last command removes the connection draining configuration of the back-end HTTP settings stored in $Settings.</span></span>

## <span data-ttu-id="89def-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="89def-112">PARAMETERS</span></span>

### <span data-ttu-id="89def-113">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="89def-113">-BackendHttpSettings</span></span>
<span data-ttu-id="89def-114">Impostazioni http di backend</span><span class="sxs-lookup"><span data-stu-id="89def-114">The backend http settings</span></span>

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

### <span data-ttu-id="89def-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89def-115">-DefaultProfile</span></span>
<span data-ttu-id="89def-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="89def-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89def-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89def-117">CommonParameters</span></span>
<span data-ttu-id="89def-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89def-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89def-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89def-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89def-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="89def-120">INPUTS</span></span>

### <span data-ttu-id="89def-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="89def-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>
<span data-ttu-id="89def-122">Parametri: BackendHttpSettings (ByValue)</span><span class="sxs-lookup"><span data-stu-id="89def-122">Parameters: BackendHttpSettings (ByValue)</span></span>

## <span data-ttu-id="89def-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="89def-123">OUTPUTS</span></span>

### <span data-ttu-id="89def-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="89def-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="89def-125">Note</span><span class="sxs-lookup"><span data-stu-id="89def-125">NOTES</span></span>

## <span data-ttu-id="89def-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="89def-126">RELATED LINKS</span></span>

[<span data-ttu-id="89def-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="89def-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="89def-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="89def-128">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>](./Get-AzureRmApplicationGatewayBackendHttpSettings.md)

[<span data-ttu-id="89def-129">Get-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89def-129">Get-AzureRmApplicationGatewayConnectionDraining</span></span>](./Get-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="89def-130">New-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89def-130">New-AzureRmApplicationGatewayConnectionDraining</span></span>](./New-AzureRmApplicationGatewayConnectionDraining.md)

[<span data-ttu-id="89def-131">Set-AzureRmApplicationGatewayConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="89def-131">Set-AzureRmApplicationGatewayConnectionDraining</span></span>](./Set-AzureRmApplicationGatewayConnectionDraining.md)

