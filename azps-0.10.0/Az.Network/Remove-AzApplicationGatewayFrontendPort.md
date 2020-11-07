---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: A698954A-994E-45AD-BA36-1E03196CFCB0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 39a2bd8ad1951cba41ff8fffb124c7486680b352
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860358"
---
# <span data-ttu-id="e9924-101">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e9924-101">Remove-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="e9924-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e9924-102">SYNOPSIS</span></span>
<span data-ttu-id="e9924-103">Rimuove una porta front-end da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9924-103">Removes a front-end port from an application gateway.</span></span>

## <span data-ttu-id="e9924-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e9924-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayFrontendPort -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e9924-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e9924-105">DESCRIPTION</span></span>
<span data-ttu-id="e9924-106">Il cmdlet **Remove-AzApplicationGatewayFrontendPort** rimuove una porta front-end da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="e9924-106">The **Remove-AzApplicationGatewayFrontendPort** cmdlet removes a front-end port from an Azure application gateway.</span></span>

## <span data-ttu-id="e9924-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e9924-107">EXAMPLES</span></span>

### <span data-ttu-id="e9924-108">Esempio: rimuovere una porta front-end da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="e9924-108">Example: Remove a front-end port from an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort02"
```

<span data-ttu-id="e9924-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 che appartiene al gruppo di risorse denominato ResourceGroup01 e archivia il gateway in $AppGw variabile.</span><span class="sxs-lookup"><span data-stu-id="e9924-109">The first command gets an application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores the gateway in $AppGw variable.</span></span>

<span data-ttu-id="e9924-110">Il secondo comando rimuove la porta denominata FrontEndPort02 dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="e9924-110">The second command removes the port named FrontEndPort02 from the application gateway.</span></span>

## <span data-ttu-id="e9924-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e9924-111">PARAMETERS</span></span>

### <span data-ttu-id="e9924-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9924-112">-ApplicationGateway</span></span>
<span data-ttu-id="e9924-113">Specifica il gateway dell'applicazione da cui rimuovere una porta front-end.</span><span class="sxs-lookup"><span data-stu-id="e9924-113">Specifies the application gateway from which to remove a front-end port.</span></span>

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

### <span data-ttu-id="e9924-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9924-114">-DefaultProfile</span></span>
<span data-ttu-id="e9924-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e9924-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9924-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="e9924-116">-Name</span></span>
<span data-ttu-id="e9924-117">Specifica il nome della porta frontend da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="e9924-117">Specifies name of the frontend port to remove.</span></span>

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

### <span data-ttu-id="e9924-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9924-118">CommonParameters</span></span>
<span data-ttu-id="e9924-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9924-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9924-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9924-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9924-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e9924-121">INPUTS</span></span>

### <span data-ttu-id="e9924-122">System. String</span><span class="sxs-lookup"><span data-stu-id="e9924-122">System.String</span></span>

## <span data-ttu-id="e9924-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e9924-123">OUTPUTS</span></span>

### <span data-ttu-id="e9924-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e9924-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e9924-125">Note</span><span class="sxs-lookup"><span data-stu-id="e9924-125">NOTES</span></span>

## <span data-ttu-id="e9924-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e9924-126">RELATED LINKS</span></span>

[<span data-ttu-id="e9924-127">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e9924-127">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e9924-128">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e9924-128">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e9924-129">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e9924-129">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="e9924-130">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="e9924-130">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


