---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: ec20d7caafe110f03e5a0ce3130247ec877d6af9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864791"
---
# <span data-ttu-id="38f7e-101">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="38f7e-101">Get-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="38f7e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38f7e-102">SYNOPSIS</span></span>
<span data-ttu-id="38f7e-103">Ottiene una configurazione esistente di una sonda sanitaria da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38f7e-103">Gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="38f7e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38f7e-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayProbeConfig [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38f7e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38f7e-105">DESCRIPTION</span></span>
<span data-ttu-id="38f7e-106">Il cmdlet Get-AzApplicationGatewayProbeConfig ottiene una configurazione della sonda di integrità esistente da un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38f7e-106">The Get-AzApplicationGatewayProbeConfig cmdlet gets an existing health probe configuration from an Application Gateway.</span></span>

## <span data-ttu-id="38f7e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38f7e-107">EXAMPLES</span></span>

### <span data-ttu-id="38f7e-108">Esempio 1: ottenere una sonda esistente da un gateway applicazione</span><span class="sxs-lookup"><span data-stu-id="38f7e-108">Example 1: Get an existing probe from an application gateway</span></span>
```
PS C:\>Get-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe02"
```

<span data-ttu-id="38f7e-109">Questo comando ottiene la sonda di integrità denominata Probe02 dal gateway dell'applicazione denominata gateway.</span><span class="sxs-lookup"><span data-stu-id="38f7e-109">This command gets the health probe named Probe02 from the application gateway named Gateway.</span></span>

## <span data-ttu-id="38f7e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38f7e-110">PARAMETERS</span></span>

### <span data-ttu-id="38f7e-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38f7e-111">-ApplicationGateway</span></span>
<span data-ttu-id="38f7e-112">Specifica il gateway dell'applicazione a cui questo cmdlet ottiene una configurazione Probe.</span><span class="sxs-lookup"><span data-stu-id="38f7e-112">Specifies the application gateway to which this cmdlet gets a probe configuration.</span></span>

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

### <span data-ttu-id="38f7e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38f7e-113">-DefaultProfile</span></span>
<span data-ttu-id="38f7e-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38f7e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38f7e-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="38f7e-115">-Name</span></span>
<span data-ttu-id="38f7e-116">Specifica il nome del probe.</span><span class="sxs-lookup"><span data-stu-id="38f7e-116">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="38f7e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38f7e-117">CommonParameters</span></span>
<span data-ttu-id="38f7e-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38f7e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38f7e-119">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38f7e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38f7e-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38f7e-120">INPUTS</span></span>

### <span data-ttu-id="38f7e-121">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38f7e-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38f7e-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38f7e-122">OUTPUTS</span></span>

### <span data-ttu-id="38f7e-123">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayProbe</span><span class="sxs-lookup"><span data-stu-id="38f7e-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="38f7e-124">Note</span><span class="sxs-lookup"><span data-stu-id="38f7e-124">NOTES</span></span>

## <span data-ttu-id="38f7e-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38f7e-125">RELATED LINKS</span></span>

[<span data-ttu-id="38f7e-126">Aggiungere una sonda a un gateway applicazione esistente</span><span class="sxs-lookup"><span data-stu-id="38f7e-126">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="38f7e-127">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="38f7e-127">Add-AzApplicationGatewayProbeConfig</span></span>](./Add-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="38f7e-128">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="38f7e-128">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="38f7e-129">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="38f7e-129">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="38f7e-130">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="38f7e-130">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

