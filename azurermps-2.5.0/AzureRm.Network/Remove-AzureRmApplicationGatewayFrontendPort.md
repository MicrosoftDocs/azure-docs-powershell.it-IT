---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: ecee205ee831c5ba7a2fa78c00f005af3303a13a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866065"
---
# <span data-ttu-id="5d587-101">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d587-101">Remove-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5d587-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5d587-102">SYNOPSIS</span></span>
<span data-ttu-id="5d587-103">Rimuove una porta front-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5d587-103">Removes a front-end port from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d587-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5d587-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5d587-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5d587-105">DESCRIPTION</span></span>
<span data-ttu-id="5d587-106">Il cmdlet **Remove-AzureRmApplicationGatewayFrontendPort** rimuove una porta front-end da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="5d587-106">The **Remove-AzureRmApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="5d587-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5d587-107">EXAMPLES</span></span>

### <span data-ttu-id="5d587-108">Esempio: rimuovere una porta front-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="5d587-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="5d587-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e archivia il gateway in $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="5d587-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="5d587-110">Il secondo comando rimuove la porta denominata FrontEndPort02 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="5d587-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="5d587-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5d587-111">PARAMETERS</span></span>

### <span data-ttu-id="5d587-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d587-112">-ApplicationGateway</span></span>
<span data-ttu-id="5d587-113">Specifica il gateway dell'applicazione da cui rimuovere una porta front-end.</span><span class="sxs-lookup"><span data-stu-id="5d587-113">Specifies the application gateway from which to remove a front-end port.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5d587-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d587-114">-DefaultProfile</span></span>
<span data-ttu-id="5d587-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5d587-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d587-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="5d587-116">-Name</span></span>
<span data-ttu-id="5d587-117">Specifica il nome della porta frontend da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="5d587-117">Specifies name of the frontend port to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d587-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d587-118">CommonParameters</span></span>
<span data-ttu-id="5d587-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d587-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d587-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d587-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d587-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5d587-121">INPUTS</span></span>

### <span data-ttu-id="5d587-122">System. String</span><span class="sxs-lookup"><span data-stu-id="5d587-122">System.String</span></span>

## <span data-ttu-id="5d587-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5d587-123">OUTPUTS</span></span>

### <span data-ttu-id="5d587-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5d587-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5d587-125">Note</span><span class="sxs-lookup"><span data-stu-id="5d587-125">NOTES</span></span>

## <span data-ttu-id="5d587-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5d587-126">RELATED LINKS</span></span>

[<span data-ttu-id="5d587-127">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d587-127">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5d587-128">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d587-128">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5d587-129">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d587-129">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5d587-130">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5d587-130">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


