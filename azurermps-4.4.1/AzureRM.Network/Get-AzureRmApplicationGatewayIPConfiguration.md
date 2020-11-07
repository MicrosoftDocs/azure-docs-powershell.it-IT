---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayIPConfiguration.md
ms.openlocfilehash: 6959f75822143688249b97ee3beaa038ed33a2ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685671"
---
# <span data-ttu-id="314e8-101">Get-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="314e8-101">Get-AzureRmApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="314e8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="314e8-102">SYNOPSIS</span></span>
<span data-ttu-id="314e8-103">Ottiene la configurazione IP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="314e8-103">Gets the IP configuration of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="314e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="314e8-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="314e8-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="314e8-105">DESCRIPTION</span></span>
<span data-ttu-id="314e8-106">Il cmdlet **Get-AzureRmApplicationGatewayIPConfiguration** ottiene la configurazione IP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="314e8-106">The **Get-AzureRmApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="314e8-107">La configurazione IP contiene la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="314e8-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="314e8-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="314e8-108">EXAMPLES</span></span>

### <span data-ttu-id="314e8-109">Esempio 1: ottenere una configurazione IP specifica</span><span class="sxs-lookup"><span data-stu-id="314e8-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzureRmApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="314e8-110">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando ottiene una configurazione IP denominata GateSubnet01 dal gateway archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="314e8-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="314e8-111">Esempio 2: ottenere un elenco di configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="314e8-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzureRmApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="314e8-112">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando ottiene un elenco di tutte le configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="314e8-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="314e8-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="314e8-113">PARAMETERS</span></span>

### <span data-ttu-id="314e8-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="314e8-114">-ApplicationGateway</span></span>
<span data-ttu-id="314e8-115">Specifica l'oggetto gateway dell'applicazione che contiene la configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="314e8-115">Specifies the application gateway object that contains IP configuration.</span></span>

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

### <span data-ttu-id="314e8-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="314e8-116">-Name</span></span>
<span data-ttu-id="314e8-117">Specifica il nome della configurazione IP ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="314e8-117">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

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

### <span data-ttu-id="314e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="314e8-118">-DefaultProfile</span></span>
<span data-ttu-id="314e8-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="314e8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="314e8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="314e8-120">CommonParameters</span></span>
<span data-ttu-id="314e8-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="314e8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="314e8-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="314e8-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="314e8-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="314e8-123">INPUTS</span></span>

### <span data-ttu-id="314e8-124">System. String</span><span class="sxs-lookup"><span data-stu-id="314e8-124">System.String</span></span>

## <span data-ttu-id="314e8-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="314e8-125">OUTPUTS</span></span>

### <span data-ttu-id="314e8-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="314e8-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="314e8-127">Note</span><span class="sxs-lookup"><span data-stu-id="314e8-127">NOTES</span></span>

## <span data-ttu-id="314e8-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="314e8-128">RELATED LINKS</span></span>

[<span data-ttu-id="314e8-129">Add-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="314e8-129">Add-AzureRmApplicationGatewayIPConfiguration</span></span>](./Add-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="314e8-130">New-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="314e8-130">New-AzureRmApplicationGatewayIPConfiguration</span></span>](./New-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="314e8-131">Remove-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="314e8-131">Remove-AzureRmApplicationGatewayIPConfiguration</span></span>](./Remove-AzureRmApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="314e8-132">Set-AzureRmApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="314e8-132">Set-AzureRmApplicationGatewayIPConfiguration</span></span>](./Set-AzureRmApplicationGatewayIPConfiguration.md)


