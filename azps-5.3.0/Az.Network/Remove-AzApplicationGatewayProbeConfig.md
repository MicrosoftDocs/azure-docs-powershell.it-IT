---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: 20704f404d5fe47267f42398ef885fb2c038f84e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486692"
---
# <span data-ttu-id="4fd44-101">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4fd44-101">Remove-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="4fd44-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4fd44-102">SYNOPSIS</span></span>
<span data-ttu-id="4fd44-103">Rimuove una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="4fd44-103">Removes a health probe from an existing application gateway.</span></span>

## <span data-ttu-id="4fd44-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4fd44-104">SYNTAX</span></span>

```
Remove-AzApplicationGatewayProbeConfig -Name <String> -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fd44-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4fd44-105">DESCRIPTION</span></span>
<span data-ttu-id="4fd44-106">Il cmdlet Remove-AzApplicationGatewayProbeConfig consente di rimuovere una sonda di integrità da un gateway applicazione esistente.</span><span class="sxs-lookup"><span data-stu-id="4fd44-106">The Remove-AzApplicationGatewayProbeConfig cmdlet removes a heath probe from an existing application gateway.</span></span>

## <span data-ttu-id="4fd44-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4fd44-107">EXAMPLES</span></span>

### <span data-ttu-id="4fd44-108">Esempio 1: rimuovere una sonda di integrità da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="4fd44-108">Example 1: Remove a health probe from an existing application gateway</span></span>
```
PS C:\>$Gateway = Remove-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe04"
```

<span data-ttu-id="4fd44-109">Questo comando rimuove la sonda di integrità denominata Probe04 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="4fd44-109">This command removes the health probe named Probe04 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="4fd44-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4fd44-110">PARAMETERS</span></span>

### <span data-ttu-id="4fd44-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fd44-111">-ApplicationGateway</span></span>
<span data-ttu-id="4fd44-112">Specifica il gateway dell'applicazione a cui questo cmdlet rimuove un probe.</span><span class="sxs-lookup"><span data-stu-id="4fd44-112">Specifies the application gateway to which this cmdlet removes a probe.</span></span>

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

### <span data-ttu-id="4fd44-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fd44-113">-DefaultProfile</span></span>
<span data-ttu-id="4fd44-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4fd44-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4fd44-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4fd44-115">-Name</span></span>
<span data-ttu-id="4fd44-116">Specifica il nome del probe per cui viene rimosso questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4fd44-116">Specifies the name of the probe for which this cmdlet removes.</span></span>

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

### <span data-ttu-id="4fd44-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fd44-117">CommonParameters</span></span>
<span data-ttu-id="4fd44-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fd44-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fd44-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fd44-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fd44-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4fd44-120">INPUTS</span></span>

### <span data-ttu-id="4fd44-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fd44-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fd44-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4fd44-122">OUTPUTS</span></span>

### <span data-ttu-id="4fd44-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4fd44-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4fd44-124">Note</span><span class="sxs-lookup"><span data-stu-id="4fd44-124">NOTES</span></span>

## <span data-ttu-id="4fd44-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4fd44-125">RELATED LINKS</span></span>

[<span data-ttu-id="4fd44-126">Rimuovere una sonda da un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="4fd44-126">Remove a probe from an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#remove-a-probe-from-an-existing-application-gateway)

[<span data-ttu-id="4fd44-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4fd44-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="4fd44-128">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4fd44-128">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="4fd44-129">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4fd44-129">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="4fd44-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="4fd44-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

