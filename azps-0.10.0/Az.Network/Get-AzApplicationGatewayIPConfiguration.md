---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 35562212-283C-4BB2-8B12-C3617A6760D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c7912f1a5d0539a0c81aff930cd94cb944e45bb7
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860878"
---
# <span data-ttu-id="55e47-101">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e47-101">Get-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="55e47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="55e47-102">SYNOPSIS</span></span>
<span data-ttu-id="55e47-103">Ottiene la configurazione IP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55e47-103">Gets the IP configuration of an application gateway.</span></span>

## <span data-ttu-id="55e47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="55e47-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayIPConfiguration [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55e47-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="55e47-105">DESCRIPTION</span></span>
<span data-ttu-id="55e47-106">Il cmdlet **Get-AzApplicationGatewayIPConfiguration** ottiene la configurazione IP di un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55e47-106">The **Get-AzApplicationGatewayIPConfiguration** cmdlet gets the IP configuration of an application gateway.</span></span>
<span data-ttu-id="55e47-107">La configurazione IP contiene la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="55e47-107">The IP configuration contains the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="55e47-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="55e47-108">EXAMPLES</span></span>

### <span data-ttu-id="55e47-109">Esempio 1: ottenere una configurazione IP specifica</span><span class="sxs-lookup"><span data-stu-id="55e47-109">Example 1: Get a specific IP configuration</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnet = Get-AzApplicationGatewayIPConfiguration -Name "GatewaySubnet01" -ApplicationGateway $AppGw
```

<span data-ttu-id="55e47-110">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando ottiene una configurazione IP denominata GateSubnet01 dal gateway archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="55e47-110">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets an IP configuration named GateSubnet01 from the gateway stored in $AppGw.</span></span>

### <span data-ttu-id="55e47-111">Esempio 2: ottenere un elenco di configurazioni IP</span><span class="sxs-lookup"><span data-stu-id="55e47-111">Example 2: Get a list of IP configurations</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $GatewaySubnets = Get-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw
```

<span data-ttu-id="55e47-112">Il primo comando ottiene un gateway dell'applicazione e lo archivia nella variabile $AppGw. Il secondo comando ottiene un elenco di tutte le configurazioni IP.</span><span class="sxs-lookup"><span data-stu-id="55e47-112">The first command gets an application gateway and stores it in the $AppGw variable.The second command gets a list of all IP configurations.</span></span>

## <span data-ttu-id="55e47-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="55e47-113">PARAMETERS</span></span>

### <span data-ttu-id="55e47-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="55e47-114">-ApplicationGateway</span></span>
<span data-ttu-id="55e47-115">Specifica l'oggetto gateway dell'applicazione che contiene la configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="55e47-115">Specifies the application gateway object that contains IP configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55e47-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55e47-116">-DefaultProfile</span></span>
<span data-ttu-id="55e47-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="55e47-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e47-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="55e47-118">-Name</span></span>
<span data-ttu-id="55e47-119">Specifica il nome della configurazione IP ottenuta da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="55e47-119">Specifies the name of the IP configuration which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55e47-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55e47-120">CommonParameters</span></span>
<span data-ttu-id="55e47-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55e47-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55e47-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55e47-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55e47-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="55e47-123">INPUTS</span></span>

### <span data-ttu-id="55e47-124">System. String</span><span class="sxs-lookup"><span data-stu-id="55e47-124">System.String</span></span>

## <span data-ttu-id="55e47-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="55e47-125">OUTPUTS</span></span>

### <span data-ttu-id="55e47-126">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e47-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="55e47-127">Note</span><span class="sxs-lookup"><span data-stu-id="55e47-127">NOTES</span></span>

## <span data-ttu-id="55e47-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="55e47-128">RELATED LINKS</span></span>

[<span data-ttu-id="55e47-129">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e47-129">Add-AzApplicationGatewayIPConfiguration</span></span>](./Add-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="55e47-130">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e47-130">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="55e47-131">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e47-131">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="55e47-132">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="55e47-132">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


