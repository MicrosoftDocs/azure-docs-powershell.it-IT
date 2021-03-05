---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayautoscaleconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayAutoscaleConfiguration.md
ms.openlocfilehash: 78a9623e5e65c93d302b356b64b5c30033697fdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102003662"
---
# <span data-ttu-id="97f4f-101">Get-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="97f4f-101">Get-AzApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="97f4f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97f4f-102">SYNOPSIS</span></span>
<span data-ttu-id="97f4f-103">Ottiene la configurazione della scala automatica del Gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="97f4f-103">Gets the Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="97f4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97f4f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="97f4f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="97f4f-105">DESCRIPTION</span></span>
<span data-ttu-id="97f4f-106">Il **cmdlet Get-AzApplicationGatewayAutoscaleConfiguration** ottiene la configurazione di gradazione automatica del Gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="97f4f-106">The **Get-AzApplicationGatewayAutoscaleConfiguration** cmdlet gets Autoscale Configuration of the Application Gateway.</span></span>

## <span data-ttu-id="97f4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97f4f-107">EXAMPLES</span></span>

### <span data-ttu-id="97f4f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="97f4f-108">Example 1</span></span>
```powershell
PS C:\> $gw = Get-AzApplicationGateway -Name $appgwName -ResourceGroupName $resgpName
PS C:\> $autoscaleConfiguration = Get-AzApplicationGatewayAutoscaleConfiguration -ApplicationGateway $gw
PS C:\> $autoscaleConfiguration.MinCapacity
```

<span data-ttu-id="97f4f-109">Il primo comando recupera il gateway applicazione e lo archivia in $gw variabile.</span><span class="sxs-lookup"><span data-stu-id="97f4f-109">The first command gets the application gateway and stores it in $gw variable.</span></span>
<span data-ttu-id="97f4f-110">Il secondo comando estrae la configurazione di gradazioni automatica dal gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="97f4f-110">The second command extracts out the autoscale configuration from the application gateway.</span></span>

## <span data-ttu-id="97f4f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="97f4f-111">PARAMETERS</span></span>

### <span data-ttu-id="97f4f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97f4f-112">-ApplicationGateway</span></span>
<span data-ttu-id="97f4f-113">ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97f4f-113">The applicationGateway</span></span>

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

### <span data-ttu-id="97f4f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97f4f-114">-DefaultProfile</span></span>
<span data-ttu-id="97f4f-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="97f4f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97f4f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97f4f-116">CommonParameters</span></span>
<span data-ttu-id="97f4f-117">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97f4f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97f4f-118">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="97f4f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97f4f-119">INPUT</span><span class="sxs-lookup"><span data-stu-id="97f4f-119">INPUTS</span></span>

### <span data-ttu-id="97f4f-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="97f4f-120">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="97f4f-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97f4f-121">OUTPUTS</span></span>

### <span data-ttu-id="97f4f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="97f4f-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAutoscaleConfiguration</span></span>

## <span data-ttu-id="97f4f-123">NOTE</span><span class="sxs-lookup"><span data-stu-id="97f4f-123">NOTES</span></span>

## <span data-ttu-id="97f4f-124">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97f4f-124">RELATED LINKS</span></span>

[<span data-ttu-id="97f4f-125">New-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="97f4f-125">New-AzApplicationGatewayAutoscaleConfiguration</span></span>](./New-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="97f4f-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="97f4f-126">Remove-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Remove-AzApplicationGatewayAutoscaleConfiguration.md)

[<span data-ttu-id="97f4f-127">Set-AzApplicationGatewayAutoscaleConfiguration</span><span class="sxs-lookup"><span data-stu-id="97f4f-127">Set-AzApplicationGatewayAutoscaleConfiguration</span></span>](./Set-AzApplicationGatewayAutoscaleConfiguration.md)
