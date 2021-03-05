---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 8ee58ee3f6c7a92fac0cb3c92f0a45966e4e875e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991015"
---
# <span data-ttu-id="bb607-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb607-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="bb607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb607-102">SYNOPSIS</span></span>
<span data-ttu-id="bb607-103">Rimuove una istanza dell'integrità da un gateway applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="bb607-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="bb607-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bb607-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb607-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="bb607-105">DESCRIPTION</span></span>
<span data-ttu-id="bb607-106">Il cmdlet Remove-AzApplicationGatewayProbeConfig rimuove una pagina Remove-AzApplicationGatewayProbeConfig da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="bb607-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="bb607-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bb607-107">EXAMPLES</span></span>

### <span data-ttu-id="bb607-108">Esempio 1: Rimuovere una istanza dell'integrità da un gateway applicazioni esistente</span><span class="sxs-lookup"><span data-stu-id="bb607-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="bb607-109">Questo comando rimuove l'integrità denominata Pool04 dal gateway di applicazione denominato Gateway.</span><span class="sxs-lookup"><span data-stu-id="bb607-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="bb607-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb607-110">PARAMETERS</span></span>

### <span data-ttu-id="bb607-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb607-111">-ApplicationGateway</span></span>
<span data-ttu-id="bb607-112">Specifica il gateway applicazione in cui questo cmdlet rimuove un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb607-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="bb607-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb607-113">-DefaultProfile</span></span>
<span data-ttu-id="bb607-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bb607-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bb607-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bb607-115">-Name</span></span>
<span data-ttu-id="bb607-116">Specifica il nome del cmdlet per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bb607-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="bb607-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb607-117">CommonParameters</span></span>
<span data-ttu-id="bb607-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb607-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb607-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb607-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb607-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="bb607-120">INPUTS</span></span>

### <span data-ttu-id="bb607-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb607-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb607-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bb607-122">OUTPUTS</span></span>

### <span data-ttu-id="bb607-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bb607-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bb607-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="bb607-124">NOTES</span></span>

## <span data-ttu-id="bb607-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bb607-125">RELATED LINKS</span></span>

[<span data-ttu-id="bb607-126">Rimuovere un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="bb607-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="bb607-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb607-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="bb607-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb607-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="bb607-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb607-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="bb607-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bb607-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

