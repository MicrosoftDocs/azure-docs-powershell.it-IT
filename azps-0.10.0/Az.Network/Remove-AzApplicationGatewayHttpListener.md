---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: c3bc83f3f38c8a9b3c34e990e5729648a3677dd8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860357"
---
# <span data-ttu-id="06079-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06079-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="06079-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="06079-102">SYNOPSIS</span></span>
<span data-ttu-id="06079-103">Rimuove un listener HTTP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="06079-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="06079-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="06079-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06079-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="06079-105">DESCRIPTION</span></span>
<span data-ttu-id="06079-106">Il cmdlet **Remove-AzApplicationGatewayHttpListener** rimuove un listener HTTP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="06079-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="06079-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="06079-107">EXAMPLES</span></span>

### <span data-ttu-id="06079-108">Esempio 1: rimuovere un listener HTTP gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="06079-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="06079-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="06079-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="06079-110">Il secondo comando rimuove il listener HTTP denominato Listener02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="06079-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="06079-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="06079-111">PARAMETERS</span></span>

### <span data-ttu-id="06079-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="06079-112">-ApplicationGateway</span></span>
<span data-ttu-id="06079-113">Specifica il gateway dell'applicazione da cui rimuovere un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="06079-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="06079-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06079-114">-DefaultProfile</span></span>
<span data-ttu-id="06079-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="06079-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06079-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="06079-116">-Name</span></span>
<span data-ttu-id="06079-117">Specifica il nome del listener HTTP rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06079-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="06079-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06079-118">CommonParameters</span></span>
<span data-ttu-id="06079-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06079-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06079-120">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06079-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06079-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="06079-121">INPUTS</span></span>

### <span data-ttu-id="06079-122">System. String</span><span class="sxs-lookup"><span data-stu-id="06079-122">System.String</span></span>

## <span data-ttu-id="06079-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="06079-123">OUTPUTS</span></span>

### <span data-ttu-id="06079-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06079-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="06079-125">Note</span><span class="sxs-lookup"><span data-stu-id="06079-125">NOTES</span></span>

## <span data-ttu-id="06079-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="06079-126">RELATED LINKS</span></span>

[<span data-ttu-id="06079-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06079-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06079-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06079-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06079-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06079-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="06079-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="06079-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


