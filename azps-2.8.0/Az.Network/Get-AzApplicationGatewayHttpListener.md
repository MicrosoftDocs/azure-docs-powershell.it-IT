---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91b2791b7f61c7586c1fbd4bca954e374ccbb43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93853825"
---
# <span data-ttu-id="c7b3c-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7b3c-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c7b3c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c7b3c-102">SYNOPSIS</span></span>
<span data-ttu-id="c7b3c-103">Ottiene il listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="c7b3c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c7b3c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7b3c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c7b3c-105">DESCRIPTION</span></span>
<span data-ttu-id="c7b3c-106">Il cmdlet **Get-AzApplicationGatewayHttpListener** ottiene il listener HTTP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="c7b3c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c7b3c-107">EXAMPLES</span></span>

### <span data-ttu-id="c7b3c-108">Esempio 1: ottenere un listener HTTP specifico</span><span class="sxs-lookup"><span data-stu-id="c7b3c-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="c7b3c-109">Questo comando ottiene un listener HTTP denominato Listener01.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="c7b3c-110">Esempio 2: ottenere un elenco di listener HTTP</span><span class="sxs-lookup"><span data-stu-id="c7b3c-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="c7b3c-111">Questo comando ottiene un elenco di listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="c7b3c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c7b3c-112">PARAMETERS</span></span>

### <span data-ttu-id="c7b3c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7b3c-113">-ApplicationGateway</span></span>
<span data-ttu-id="c7b3c-114">Specifica l'oggetto gateway dell'applicazione che contiene il listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="c7b3c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7b3c-115">-DefaultProfile</span></span>
<span data-ttu-id="c7b3c-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7b3c-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7b3c-117">-Name</span></span>
<span data-ttu-id="c7b3c-118">Specifica il nome del listener HTTP ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="c7b3c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7b3c-119">CommonParameters</span></span>
<span data-ttu-id="c7b3c-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7b3c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7b3c-121">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c7b3c-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7b3c-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c7b3c-122">INPUTS</span></span>

### <span data-ttu-id="c7b3c-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c7b3c-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c7b3c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c7b3c-124">OUTPUTS</span></span>

### <span data-ttu-id="c7b3c-125">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7b3c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="c7b3c-126">Note</span><span class="sxs-lookup"><span data-stu-id="c7b3c-126">NOTES</span></span>

## <span data-ttu-id="c7b3c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c7b3c-127">RELATED LINKS</span></span>

[<span data-ttu-id="c7b3c-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7b3c-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7b3c-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7b3c-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7b3c-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7b3c-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="c7b3c-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="c7b3c-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


