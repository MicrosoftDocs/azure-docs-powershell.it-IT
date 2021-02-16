---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayredirectconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayRedirectConfiguration.md
ms.openlocfilehash: 8a49bdeed095ee277d632559402c55ca3baf784c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192014"
---
# <span data-ttu-id="23a16-101">Get-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23a16-101">Get-AzApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="23a16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23a16-102">SYNOPSIS</span></span>
<span data-ttu-id="23a16-103">Ottiene una configurazione di reindirizzamento esistente da un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="23a16-103">Gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="23a16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23a16-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayRedirectConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23a16-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="23a16-105">DESCRIPTION</span></span>
<span data-ttu-id="23a16-106">Il cmdlet **Get-AzApplicationGatewayRedirectConfiguration** ottiene una configurazione di reindirizzamento esistente da un Gateway di applicazione.</span><span class="sxs-lookup"><span data-stu-id="23a16-106">The **Get-AzApplicationGatewayRedirectConfiguration** cmdlet gets an existing redirect configuration from an Application Gateway.</span></span>

## <span data-ttu-id="23a16-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23a16-107">EXAMPLES</span></span>

### <span data-ttu-id="23a16-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="23a16-108">Example 1</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $RedirectConfig = Get-AzApplicationGatewayRedirectConfiguration -Name "Redirect01" -ApplicationGateway $AppGW
```

<span data-ttu-id="23a16-109">Il primo comando recupera il Gateway applicazione denominato ApplicationGateway01 e archivia il risultato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="23a16-109">The first command gets the Application Gateway named ApplicationGateway01 and stores the result in the variable named $AppGW.</span></span>
<span data-ttu-id="23a16-110">Il secondo comando recupera la configurazione di reindirizzamento denominata Redirect01 dal Gateway applicazione memorizzato nella variabile $AppGW.</span><span class="sxs-lookup"><span data-stu-id="23a16-110">The second command gets the redirect configuration named Redirect01 from the Application Gateway stored in the variable named $AppGW.</span></span>

## <span data-ttu-id="23a16-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23a16-111">PARAMETERS</span></span>

### <span data-ttu-id="23a16-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23a16-112">-ApplicationGateway</span></span>
<span data-ttu-id="23a16-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23a16-113">The applicationGateway</span></span>

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

### <span data-ttu-id="23a16-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23a16-114">-DefaultProfile</span></span>
<span data-ttu-id="23a16-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23a16-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23a16-116">-Name</span><span class="sxs-lookup"><span data-stu-id="23a16-116">-Name</span></span>
<span data-ttu-id="23a16-117">Nome della regola di routing delle richieste</span><span class="sxs-lookup"><span data-stu-id="23a16-117">The name of the request routing rule</span></span>

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

### <span data-ttu-id="23a16-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23a16-118">CommonParameters</span></span>
<span data-ttu-id="23a16-119">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23a16-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23a16-120">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="23a16-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23a16-121">INPUT</span><span class="sxs-lookup"><span data-stu-id="23a16-121">INPUTS</span></span>

### <span data-ttu-id="23a16-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="23a16-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="23a16-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23a16-123">OUTPUTS</span></span>

### <span data-ttu-id="23a16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23a16-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration</span></span>

## <span data-ttu-id="23a16-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="23a16-125">NOTES</span></span>

## <span data-ttu-id="23a16-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23a16-126">RELATED LINKS</span></span>

[<span data-ttu-id="23a16-127">Add-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23a16-127">Add-AzApplicationGatewayRedirectConfiguration</span></span>](./Add-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="23a16-128">New-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23a16-128">New-AzApplicationGatewayRedirectConfiguration</span></span>](./New-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="23a16-129">Remove-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23a16-129">Remove-AzApplicationGatewayRedirectConfiguration</span></span>](./Remove-AzApplicationGatewayRedirectConfiguration.md)

[<span data-ttu-id="23a16-130">Set-AzApplicationGatewayRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="23a16-130">Set-AzApplicationGatewayRedirectConfiguration</span></span>](./Set-AzApplicationGatewayRedirectConfiguration.md)
