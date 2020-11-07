---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 289B761C-1A1D-46D2-8755-B6B6A4758EFC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayFrontendIPConfig.md
ms.openlocfilehash: 2d1ac2c3e5705a4214e211bf7db9af89d432a393
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688443"
---
# <span data-ttu-id="2cda0-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cda0-101">Remove-AzureRmApplicationGatewayFrontendIPConfig</span></span>

## <span data-ttu-id="2cda0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2cda0-102">SYNOPSIS</span></span>
<span data-ttu-id="2cda0-103">Rimuove una configurazione IP front-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2cda0-103">Removes a front-end IP configuration from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2cda0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2cda0-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayFrontendIPConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2cda0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2cda0-105">DESCRIPTION</span></span>
<span data-ttu-id="2cda0-106">Il cmdlet **Remove-AzureRmApplicationGatewayFrontendIPConfig** rimuove l'IP frontend da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="2cda0-106">The **Remove-AzureRmApplicationGatewayFrontendIPConfig** cmdlet removes frontend IP from an Azure application gateway.</span></span>

## <span data-ttu-id="2cda0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2cda0-107">EXAMPLES</span></span>

### <span data-ttu-id="2cda0-108">Esempio 1: rimuovere una configurazione IP front-end</span><span class="sxs-lookup"><span data-stu-id="2cda0-108">Example 1: Remove a front-end IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayFrontendIPConfig -ApplicationGateway $AppGw -Name "FrontEndIP02"
```

<span data-ttu-id="2cda0-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2cda0-109">The first command gets an application gateway named ApplicationGateway01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="2cda0-110">Il secondo comando rimuove la configurazione IP front-end denominata FrontEndIP02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2cda0-110">The second command removes the front-end IP configuration named FrontEndIP02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="2cda0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2cda0-111">PARAMETERS</span></span>

### <span data-ttu-id="2cda0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cda0-112">-ApplicationGateway</span></span>
<span data-ttu-id="2cda0-113">Specifica un gateway dell'applicazione da cui rimuovere una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="2cda0-113">Specifies an application gateway from which to remove a front-end IP configuration.</span></span>

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

### <span data-ttu-id="2cda0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cda0-114">-DefaultProfile</span></span>
<span data-ttu-id="2cda0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2cda0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2cda0-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="2cda0-116">-Name</span></span>
<span data-ttu-id="2cda0-117">Specifica il nome di una configurazione IP front-end da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2cda0-117">Specifies the name of a front-end IP configuration to remove.</span></span>

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

### <span data-ttu-id="2cda0-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cda0-118">CommonParameters</span></span>
<span data-ttu-id="2cda0-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2cda0-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cda0-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2cda0-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cda0-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2cda0-121">INPUTS</span></span>

### <span data-ttu-id="2cda0-122">System. String</span><span class="sxs-lookup"><span data-stu-id="2cda0-122">System.String</span></span>

## <span data-ttu-id="2cda0-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2cda0-123">OUTPUTS</span></span>

### <span data-ttu-id="2cda0-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2cda0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2cda0-125">Note</span><span class="sxs-lookup"><span data-stu-id="2cda0-125">NOTES</span></span>

## <span data-ttu-id="2cda0-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2cda0-126">RELATED LINKS</span></span>

[<span data-ttu-id="2cda0-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cda0-127">Add-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Add-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2cda0-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cda0-128">Get-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Get-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2cda0-129">New-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cda0-129">New-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./New-AzureRmApplicationGatewayFrontendIPConfig.md)

[<span data-ttu-id="2cda0-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span><span class="sxs-lookup"><span data-stu-id="2cda0-130">Set-AzureRmApplicationGatewayFrontendIPConfig</span></span>](./Set-AzureRmApplicationGatewayFrontendIPConfig.md)


