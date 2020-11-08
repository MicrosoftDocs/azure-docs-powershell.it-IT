---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: b4238f5b1492afad7d09ee9c338a346d5f54a5e0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201827"
---
# <span data-ttu-id="2bf22-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf22-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="2bf22-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2bf22-102">SYNOPSIS</span></span>
<span data-ttu-id="2bf22-103">Ottiene la configurazione di scala automatica del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2bf22-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="2bf22-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2bf22-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2bf22-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2bf22-105">DESCRIPTION</span></span>
<span data-ttu-id="2bf22-106">Il cmdlet **Get-AzApplicationGatewayAutoscaleConfiguration** ottiene la configurazione di scala automatica del gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2bf22-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="2bf22-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2bf22-107">EXAMPLES</span></span>

### <span data-ttu-id="2bf22-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2bf22-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="2bf22-109">Il primo comando ottiene il gateway dell'applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="2bf22-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="2bf22-110">Il secondo comando estrae la configurazione di scala automatica dal gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="2bf22-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="2bf22-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2bf22-111">PARAMETERS</span></span>

### <span data-ttu-id="2bf22-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bf22-112">-ApplicationGateway</span></span>
<span data-ttu-id="2bf22-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bf22-113">The applicationGateway</span></span>

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

### <span data-ttu-id="2bf22-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bf22-114">-DefaultProfile</span></span>
<span data-ttu-id="2bf22-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2bf22-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2bf22-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bf22-116">CommonParameters</span></span>
<span data-ttu-id="2bf22-117">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bf22-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bf22-118">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2bf22-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bf22-119">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2bf22-119">INPUTS</span></span>

### <span data-ttu-id="2bf22-120">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2bf22-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2bf22-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2bf22-121">OUTPUTS</span></span>

### <span data-ttu-id="2bf22-122">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf22-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="2bf22-123">Note</span><span class="sxs-lookup"><span data-stu-id="2bf22-123">NOTES</span></span>

## <span data-ttu-id="2bf22-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2bf22-124">RELATED LINKS</span></span>

[<span data-ttu-id="2bf22-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf22-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="2bf22-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf22-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="2bf22-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="2bf22-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
