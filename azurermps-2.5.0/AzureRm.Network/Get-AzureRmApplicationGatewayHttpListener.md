---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 79b61f5d96307afea47851b210fc1a1ee97acf61
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866669"
---
# <span data-ttu-id="b8f73-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b8f73-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b8f73-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b8f73-102">SYNOPSIS</span></span>
<span data-ttu-id="b8f73-103">Ottiene il listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b8f73-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b8f73-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b8f73-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b8f73-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b8f73-105">DESCRIPTION</span></span>
<span data-ttu-id="b8f73-106">Il cmdlet **Get-AzureRmApplicationGatewayHttpListener** ottiene il listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="b8f73-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="b8f73-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b8f73-107">EXAMPLES</span></span>

### <span data-ttu-id="b8f73-108">Esempio 1: ottenere un listener HTTP specifico</span><span class="sxs-lookup"><span data-stu-id="b8f73-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="b8f73-109">Questo comando ottiene un listener HTTP denominato Listener01.</span><span class="sxs-lookup"><span data-stu-id="b8f73-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="b8f73-110">Esempio 2: ottenere un elenco di listener HTTP</span><span class="sxs-lookup"><span data-stu-id="b8f73-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="b8f73-111">Questo comando ottiene un elenco di listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8f73-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="b8f73-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b8f73-112">PARAMETERS</span></span>

### <span data-ttu-id="b8f73-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b8f73-113">-ApplicationGateway</span></span>
<span data-ttu-id="b8f73-114">Specifica l'oggetto gateway dell'applicazione che contiene il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="b8f73-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="b8f73-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8f73-115">-DefaultProfile</span></span>
<span data-ttu-id="b8f73-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b8f73-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8f73-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b8f73-117">-Name</span></span>
<span data-ttu-id="b8f73-118">Specifica il nome del listener HTTP ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8f73-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8f73-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8f73-119">CommonParameters</span></span>
<span data-ttu-id="b8f73-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8f73-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8f73-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b8f73-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8f73-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b8f73-122">INPUTS</span></span>

### <span data-ttu-id="b8f73-123">System. String</span><span class="sxs-lookup"><span data-stu-id="b8f73-123">System.String</span></span>

## <span data-ttu-id="b8f73-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b8f73-124">OUTPUTS</span></span>

### <span data-ttu-id="b8f73-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b8f73-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="b8f73-126">Note</span><span class="sxs-lookup"><span data-stu-id="b8f73-126">NOTES</span></span>

## <span data-ttu-id="b8f73-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b8f73-127">RELATED LINKS</span></span>

[<span data-ttu-id="b8f73-128">Add-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b8f73-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b8f73-129">New-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b8f73-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b8f73-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b8f73-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="b8f73-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="b8f73-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


