---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179894"
---
# <span data-ttu-id="93e94-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="93e94-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="93e94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e94-102">SYNOPSIS</span></span>
<span data-ttu-id="93e94-103">Recupera una configurazione di integrità integrità esistente da un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="93e94-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="93e94-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93e94-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93e94-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93e94-105">DESCRIPTION</span></span>
<span data-ttu-id="93e94-106">Il cmdlet Get-AzApplicationGatewayProbeConfig recupera una configurazione health pool esistente da un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="93e94-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="93e94-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93e94-107">EXAMPLES</span></span>

### <span data-ttu-id="93e94-108">Esempio 1: Ottenere un database esistente da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="93e94-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="93e94-109">Questo comando recupera l'integrità denominata Pool02 dal gateway applicazione denominato Gateway.</span><span class="sxs-lookup"><span data-stu-id="93e94-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="93e94-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e94-110">PARAMETERS</span></span>

### <span data-ttu-id="93e94-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93e94-111">-ApplicationGateway</span></span>
<span data-ttu-id="93e94-112">Specifica il gateway applicazione a cui questo cmdlet ottiene una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="93e94-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="93e94-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e94-113">-DefaultProfile</span></span>
<span data-ttu-id="93e94-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93e94-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e94-115">-Name</span><span class="sxs-lookup"><span data-stu-id="93e94-115">-Name</span></span>
<span data-ttu-id="93e94-116">Specifica il nome del tono.</span><span class="sxs-lookup"><span data-stu-id="93e94-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="93e94-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e94-117">CommonParameters</span></span>
<span data-ttu-id="93e94-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e94-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e94-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93e94-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e94-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="93e94-120">INPUTS</span></span>

### <span data-ttu-id="93e94-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="93e94-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="93e94-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93e94-122">OUTPUTS</span></span>

### <span data-ttu-id="93e94-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="93e94-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="93e94-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="93e94-124">NOTES</span></span>

## <span data-ttu-id="93e94-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93e94-125">RELATED LINKS</span></span>

[<span data-ttu-id="93e94-126">Aggiungere un modello a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="93e94-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="93e94-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="93e94-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="93e94-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="93e94-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="93e94-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="93e94-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="93e94-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="93e94-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

