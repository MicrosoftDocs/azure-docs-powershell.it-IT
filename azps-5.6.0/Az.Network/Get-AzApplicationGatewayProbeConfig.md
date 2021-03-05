---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 1bdee7a9ffb35085f8194d86dc9a9486f5dd7fb6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994095"
---
# <span data-ttu-id="518dd-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="518dd-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="518dd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="518dd-102">SYNOPSIS</span></span>
<span data-ttu-id="518dd-103">Recupera una configurazione di integrità integrità esistente da un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="518dd-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="518dd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="518dd-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="518dd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="518dd-105">DESCRIPTION</span></span>
<span data-ttu-id="518dd-106">Il cmdlet Get-AzApplicationGatewayProbeConfig recupera una configurazione health pool esistente da un Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="518dd-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="518dd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="518dd-107">EXAMPLES</span></span>

### <span data-ttu-id="518dd-108">Esempio 1: Ottenere un database esistente da un gateway applicazioni</span><span class="sxs-lookup"><span data-stu-id="518dd-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="518dd-109">Questo comando recupera l'integrità denominata Pool02 dal gateway di applicazione denominato Gateway.</span><span class="sxs-lookup"><span data-stu-id="518dd-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="518dd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="518dd-110">PARAMETERS</span></span>

### <span data-ttu-id="518dd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="518dd-111">-ApplicationGateway</span></span>
<span data-ttu-id="518dd-112">Specifica il gateway applicazione a cui questo cmdlet ottiene una configurazione specifica.</span><span class="sxs-lookup"><span data-stu-id="518dd-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="518dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="518dd-113">-DefaultProfile</span></span>
<span data-ttu-id="518dd-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="518dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="518dd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="518dd-115">-Name</span></span>
<span data-ttu-id="518dd-116">Specifica il nome del tono.</span><span class="sxs-lookup"><span data-stu-id="518dd-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="518dd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="518dd-117">CommonParameters</span></span>
<span data-ttu-id="518dd-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="518dd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="518dd-119">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="518dd-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="518dd-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="518dd-120">INPUTS</span></span>

### <span data-ttu-id="518dd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="518dd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="518dd-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="518dd-122">OUTPUTS</span></span>

### <span data-ttu-id="518dd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="518dd-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="518dd-124">NOTE</span><span class="sxs-lookup"><span data-stu-id="518dd-124">NOTES</span></span>

## <span data-ttu-id="518dd-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="518dd-125">RELATED LINKS</span></span>

[<span data-ttu-id="518dd-126">Aggiungere un modello a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="518dd-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="518dd-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="518dd-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="518dd-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="518dd-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="518dd-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="518dd-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="518dd-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="518dd-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

