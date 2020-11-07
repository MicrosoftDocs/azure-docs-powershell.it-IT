---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 4079d8b6859a2860116520c52928d13c7e3fa29e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688386"
---
# <span data-ttu-id="7300c-101">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7300c-101">Remove-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7300c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7300c-102">SYNOPSIS</span></span>
<span data-ttu-id="7300c-103">Rimuove un listener HTTP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7300c-103">Removes an HTTP listener from an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7300c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7300c-104">SYNTAX</span></span>

```
Remove-AzureRmApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7300c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7300c-105">DESCRIPTION</span></span>
<span data-ttu-id="7300c-106">Il cmdlet **Remove-AzureRmApplicationGatewayHttpListener** rimuove un listener HTTP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="7300c-106">The **Remove-AzureRmApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="7300c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7300c-107">EXAMPLES</span></span>

### <span data-ttu-id="7300c-108">Esempio 1: rimuovere un listener HTTP gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="7300c-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzureRmApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="7300c-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7300c-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="7300c-110">Il secondo comando rimuove il listener HTTP denominato Listener02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="7300c-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="7300c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7300c-111">PARAMETERS</span></span>

### <span data-ttu-id="7300c-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7300c-112">-ApplicationGateway</span></span>
<span data-ttu-id="7300c-113">Specifica il gateway dell'applicazione da cui rimuovere un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="7300c-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="7300c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7300c-114">-DefaultProfile</span></span>
<span data-ttu-id="7300c-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7300c-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7300c-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="7300c-116">-Name</span></span>
<span data-ttu-id="7300c-117">Specifica il nome del listener HTTP rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7300c-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7300c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7300c-118">CommonParameters</span></span>
<span data-ttu-id="7300c-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7300c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7300c-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7300c-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7300c-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7300c-121">INPUTS</span></span>

### <span data-ttu-id="7300c-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7300c-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="7300c-123">Parametri: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7300c-123">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="7300c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7300c-124">OUTPUTS</span></span>

### <span data-ttu-id="7300c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7300c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="7300c-126">Note</span><span class="sxs-lookup"><span data-stu-id="7300c-126">NOTES</span></span>

## <span data-ttu-id="7300c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7300c-127">RELATED LINKS</span></span>

[<span data-ttu-id="7300c-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7300c-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7300c-129">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7300c-129">Get-AzureRmApplicationGatewayHttpListener</span></span>](./Get-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7300c-130">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7300c-130">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="7300c-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="7300c-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


