---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202638"
---
# <span data-ttu-id="fabf1-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fabf1-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="fabf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fabf1-102">SYNOPSIS</span></span>
<span data-ttu-id="fabf1-103">Rimuove una istanza dell'integrità da un gateway applicazioni esistente.</span><span class="sxs-lookup"><span data-stu-id="fabf1-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="fabf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fabf1-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fabf1-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fabf1-105">DESCRIPTION</span></span>
<span data-ttu-id="fabf1-106">Il cmdlet Remove-AzApplicationGatewayProbeConfig rimuove una pagina Remove-AzApplicationGatewayProbeConfig da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="fabf1-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="fabf1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fabf1-107">EXAMPLES</span></span>

### <span data-ttu-id="fabf1-108">Esempio 1: Rimuovere una istanza dell'integrità da un gateway applicazioni esistente</span><span class="sxs-lookup"><span data-stu-id="fabf1-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="fabf1-109">Questo comando rimuove l'integrità denominata Pool04 dal gateway di applicazione denominato Gateway.</span><span class="sxs-lookup"><span data-stu-id="fabf1-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="fabf1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fabf1-110">PARAMETERS</span></span>

### <span data-ttu-id="fabf1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fabf1-111">-ApplicationGateway</span></span>
<span data-ttu-id="fabf1-112">Specifica il gateway applicazione in cui questo cmdlet rimuove un cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fabf1-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="fabf1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fabf1-113">-DefaultProfile</span></span>
<span data-ttu-id="fabf1-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fabf1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fabf1-115">-Name</span><span class="sxs-lookup"><span data-stu-id="fabf1-115">-Name</span></span>
<span data-ttu-id="fabf1-116">Specifica il nome del cmdlet per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fabf1-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="fabf1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fabf1-117">CommonParameters</span></span>
<span data-ttu-id="fabf1-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fabf1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fabf1-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fabf1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fabf1-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="fabf1-120">INPUTS</span></span>

### <span data-ttu-id="fabf1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fabf1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fabf1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fabf1-122">OUTPUTS</span></span>

### <span data-ttu-id="fabf1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="fabf1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="fabf1-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="fabf1-124">NOTES</span></span>

## <span data-ttu-id="fabf1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fabf1-125">RELATED LINKS</span></span>

[<span data-ttu-id="fabf1-126">Rimuovere un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="fabf1-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="fabf1-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fabf1-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fabf1-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fabf1-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fabf1-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fabf1-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="fabf1-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="fabf1-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

