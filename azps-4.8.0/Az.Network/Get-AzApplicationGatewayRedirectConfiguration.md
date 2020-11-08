---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190465"
---
# <span data-ttu-id="96722-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96722-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="96722-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="96722-102">SYNOPSIS</span></span>
<span data-ttu-id="96722-103">Ottiene una configurazione di reindirizzamento esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96722-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="96722-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96722-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="96722-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="96722-105">DESCRIPTION</span></span>
<span data-ttu-id="96722-106">Il cmdlet **Get-AzApplicationGatewayRedirectConfiguration** ottiene una configurazione di reindirizzamento esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="96722-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="96722-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96722-107">EXAMPLES</span></span>

### <span data-ttu-id="96722-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="96722-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="96722-109">Il primo comando ottiene il gateway dell'applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="96722-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="96722-110">Il secondo comando consente di ottenere la configurazione di reindirizzamento denominata Redirect01 dal gateway dell'applicazione archiviato nella variabile denominata $AppGW.</span><span class="sxs-lookup"><span data-stu-id="96722-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="96722-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="96722-111">PARAMETERS</span></span>

### <span data-ttu-id="96722-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96722-112">-ApplicationGateway</span></span>
<span data-ttu-id="96722-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96722-113">The applicationGateway</span></span>

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

### <span data-ttu-id="96722-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96722-114">-DefaultProfile</span></span>
<span data-ttu-id="96722-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96722-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="96722-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="96722-116">-Name</span></span>
<span data-ttu-id="96722-117">Nome della regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="96722-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="96722-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96722-118">CommonParameters</span></span>
<span data-ttu-id="96722-119">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96722-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96722-120">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="96722-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96722-121">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="96722-121">INPUTS</span></span>

### <span data-ttu-id="96722-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="96722-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="96722-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96722-123">OUTPUTS</span></span>

### <span data-ttu-id="96722-124">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96722-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="96722-125">Note</span><span class="sxs-lookup"><span data-stu-id="96722-125">NOTES</span></span>

## <span data-ttu-id="96722-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96722-126">RELATED LINKS</span></span>

[<span data-ttu-id="96722-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96722-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="96722-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96722-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="96722-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96722-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="96722-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="96722-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
