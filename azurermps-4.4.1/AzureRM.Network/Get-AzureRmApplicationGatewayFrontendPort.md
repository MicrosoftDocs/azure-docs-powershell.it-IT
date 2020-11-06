---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: f0a897dfcc68d2313326d974d1b5a172bd79db6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510495"
---
# <span data-ttu-id="31daa-101">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="31daa-101">Get-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="31daa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31daa-102">SYNOPSIS</span></span>
<span data-ttu-id="31daa-103">Ottiene la porta front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="31daa-103">Gets the front-end port of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31daa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31daa-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31daa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31daa-105">DESCRIPTION</span></span>
<span data-ttu-id="31daa-106">Il cmdlet **Get-AzureRmApplicationGatewayFrontendPort** ottiene la porta front-end di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="31daa-106">The **Get-AzureRmApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="31daa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31daa-107">EXAMPLES</span></span>

### <span data-ttu-id="31daa-108">Esempio 1: ottenere una porta front-end specificata</span><span class="sxs-lookup"><span data-stu-id="31daa-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzureRmApplicationGatewayFrontendIPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="31daa-109">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="31daa-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31daa-110">Il secondo comando ottiene la porta front-end denominata FrontEndPort01 da $AppGw e la archivia nella variabile $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="31daa-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="31daa-111">Esempio 2: ottenere un elenco di porte front-end</span><span class="sxs-lookup"><span data-stu-id="31daa-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzureRmApplicationGatewayFrontendIPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="31daa-112">Il primo comando ottiene un gateway dell'applicazione denominato ApplicationGateway01 dal gruppo di risorse denominato ResourceGroup01 e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="31daa-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="31daa-113">Il secondo comando ottiene un elenco delle porte front-end da $AppGw e lo archivia nella variabile $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="31daa-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="31daa-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31daa-114">PARAMETERS</span></span>

### <span data-ttu-id="31daa-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="31daa-115">-ApplicationGateway</span></span>
<span data-ttu-id="31daa-116">Specifica l'oggetto gateway dell'applicazione che contiene la porta front-end.</span><span class="sxs-lookup"><span data-stu-id="31daa-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="31daa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="31daa-117">-Name</span></span>
<span data-ttu-id="31daa-118">Specifica il nome della porta front-end da ottenere.</span><span class="sxs-lookup"><span data-stu-id="31daa-118">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31daa-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31daa-119">-DefaultProfile</span></span>
<span data-ttu-id="31daa-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31daa-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31daa-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31daa-121">CommonParameters</span></span>
<span data-ttu-id="31daa-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31daa-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31daa-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31daa-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31daa-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31daa-124">INPUTS</span></span>

### <span data-ttu-id="31daa-125">System. String</span><span class="sxs-lookup"><span data-stu-id="31daa-125">System.String</span></span>

## <span data-ttu-id="31daa-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31daa-126">OUTPUTS</span></span>

### <span data-ttu-id="31daa-127">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="31daa-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="31daa-128">Note</span><span class="sxs-lookup"><span data-stu-id="31daa-128">NOTES</span></span>

## <span data-ttu-id="31daa-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31daa-129">RELATED LINKS</span></span>

[<span data-ttu-id="31daa-130">Add-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="31daa-130">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="31daa-131">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="31daa-131">New-AzureRmApplicationGatewayFrontendPort</span></span>](./New-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="31daa-132">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="31daa-132">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="31daa-133">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="31daa-133">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)

