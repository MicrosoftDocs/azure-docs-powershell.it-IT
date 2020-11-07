---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6C90AF6C-3193-4D75-A78F-3EC315C6D7DF
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: beceb6788fd2d7498fc886cfbc22aec5ad3a9e23
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93852821"
---
# <span data-ttu-id="3b257-101">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3b257-101">Remove-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3b257-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b257-102">SYNOPSIS</span></span>
<span data-ttu-id="3b257-103">Rimuove un listener HTTP da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="3b257-103">Removes an HTTP listener from an application gateway.</span></span>

## <span data-ttu-id="3b257-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b257-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayHttpListener -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b257-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b257-105">DESCRIPTION</span></span>
<span data-ttu-id="3b257-106">Il cmdlet **Remove-AzApplicationGatewayHttpListener** rimuove un listener HTTP da un gateway dell'applicazione Azure.</span><span class="sxs-lookup"><span data-stu-id="3b257-106">The **Remove-AzApplicationGatewayHttpListener** cmdlet removes an HTTP listener from an Azure application gateway.</span></span>

## <span data-ttu-id="3b257-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b257-107">EXAMPLES</span></span>

### <span data-ttu-id="3b257-108">Esempio 1: rimuovere un listener HTTP gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="3b257-108">Example 1: Remove an application gateway HTTP listener</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> Remove-AzApplicationGatewayHttpListener -ApplicationGateway $AppGw -Name "Listener02"
```

<span data-ttu-id="3b257-109">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3b257-109">The first command gets an application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="3b257-110">Il secondo comando rimuove il listener HTTP denominato Listener02 dal gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3b257-110">The second command removes the HTTP listener named Listener02 from the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="3b257-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b257-111">PARAMETERS</span></span>

### <span data-ttu-id="3b257-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b257-112">-ApplicationGateway</span></span>
<span data-ttu-id="3b257-113">Specifica il gateway dell'applicazione da cui rimuovere un listener HTTP.</span><span class="sxs-lookup"><span data-stu-id="3b257-113">Specifies the application gateway from which to remove an HTTP listener.</span></span>

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

### <span data-ttu-id="3b257-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b257-114">-DefaultProfile</span></span>
<span data-ttu-id="3b257-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b257-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b257-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="3b257-116">-Name</span></span>
<span data-ttu-id="3b257-117">Specifica il nome del listener HTTP rimosso da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3b257-117">Specifies the name of the HTTP listener that this cmdlet removes.</span></span>

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

### <span data-ttu-id="3b257-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b257-118">CommonParameters</span></span>
<span data-ttu-id="3b257-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b257-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b257-120">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b257-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b257-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b257-121">INPUTS</span></span>

### <span data-ttu-id="3b257-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3b257-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3b257-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b257-123">OUTPUTS</span></span>

### <span data-ttu-id="3b257-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3b257-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="3b257-125">Note</span><span class="sxs-lookup"><span data-stu-id="3b257-125">NOTES</span></span>

## <span data-ttu-id="3b257-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b257-126">RELATED LINKS</span></span>

[<span data-ttu-id="3b257-127">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3b257-127">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3b257-128">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3b257-128">Get-AzApplicationGatewayHttpListener</span></span>](./Get-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3b257-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3b257-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="3b257-130">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="3b257-130">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


