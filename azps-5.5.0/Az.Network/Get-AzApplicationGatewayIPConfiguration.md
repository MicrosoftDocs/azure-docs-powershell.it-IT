---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 32d06b6de2cf3fe4fba8c2c10b28c867deed9fe2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184767"
---
# <span data-ttu-id="d3f0f-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f0f-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d3f0f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3f0f-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f0f-103">Ottiene la configurazione IP di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="d3f0f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3f0f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3f0f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d3f0f-105">DESCRIPTION</span></span>
<span data-ttu-id="d3f0f-106">Il cmdlet **Get-AzApplicationGatewayIPConfiguration** ottiene la configurazione IP di un gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="d3f0f-107">La configurazione IP contiene la subnet in cui è distribuito il gateway applicazioni.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="d3f0f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3f0f-108">EXAMPLES</span></span>

### <span data-ttu-id="d3f0f-109">Esempio 1: Ottenere una configurazione IP specifica</span><span class="sxs-lookup"><span data-stu-id="d3f0f-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="d3f0f-110">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile. Il secondo comando ottiene una configurazione IP denominata GateSubnet01 dal gateway archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="d3f0f-111">Esempio 2: Ottenere un elenco delle configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="d3f0f-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="d3f0f-112">Il primo comando ottiene un gateway applicazione e lo archivia nella $AppGw variabile. Il secondo comando ottiene un elenco di tutte le configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="d3f0f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3f0f-113">PARAMETERS</span></span>

### <span data-ttu-id="d3f0f-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f0f-114">-ApplicationGateway</span></span>
<span data-ttu-id="d3f0f-115">Specifica l'oggetto gateway applicazione che contiene la configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="d3f0f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f0f-116">-DefaultProfile</span></span>
<span data-ttu-id="d3f0f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3f0f-118">-Name</span><span class="sxs-lookup"><span data-stu-id="d3f0f-118">-Name</span></span>
<span data-ttu-id="d3f0f-119">Specifica il nome della configurazione IP a cui deve essere eseguito il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="d3f0f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f0f-120">CommonParameters</span></span>
<span data-ttu-id="d3f0f-121">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f0f-122">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d3f0f-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f0f-123">INPUT</span><span class="sxs-lookup"><span data-stu-id="d3f0f-123">INPUTS</span></span>

### <span data-ttu-id="d3f0f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="d3f0f-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="d3f0f-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3f0f-125">OUTPUTS</span></span>

### <span data-ttu-id="d3f0f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f0f-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="d3f0f-127">NOTE</span><span class="sxs-lookup"><span data-stu-id="d3f0f-127">NOTES</span></span>

## <span data-ttu-id="d3f0f-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3f0f-128">RELATED LINKS</span></span>

[<span data-ttu-id="d3f0f-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f0f-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d3f0f-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f0f-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d3f0f-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f0f-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="d3f0f-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="d3f0f-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


