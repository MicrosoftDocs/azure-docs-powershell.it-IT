---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5358C08F-A1EB-457E-85B1-7F12396A873A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayipconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Add-AzApplicationGatewayIPConfiguration.md
ms.openlocfilehash: c26fe80110066e1f6305e2d35b952ed8ab45f00d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93861013"
---
# <span data-ttu-id="38499-101">Add-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38499-101">Add-AzApplicationGatewayIPConfiguration</span></span>

## <span data-ttu-id="38499-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38499-102">SYNOPSIS</span></span>
<span data-ttu-id="38499-103">Aggiunge una configurazione IP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38499-103">Adds an IP configuration to an application gateway.</span></span>

## <span data-ttu-id="38499-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38499-104">SYNTAX</span></span>

### <span data-ttu-id="38499-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="38499-105">SetByResourceId</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-SubnetId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38499-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="38499-106">SetByResource</span></span>
```
Add-AzApplicationGatewayIPConfiguration -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-Subnet <PSSubnet>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38499-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38499-107">DESCRIPTION</span></span>
<span data-ttu-id="38499-108">Il cmdlet **Add-AzApplicationGatewayIPConfiguration** aggiunge una configurazione IP a un gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38499-108">The **Add-AzApplicationGatewayIPConfiguration** cmdlet adds an IP configuration to an application gateway.</span></span>
<span data-ttu-id="38499-109">Le configurazioni IP contengono la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38499-109">IP configurations contain the subnet in which the application gateway is deployed.</span></span>

## <span data-ttu-id="38499-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38499-110">EXAMPLES</span></span>

### <span data-ttu-id="38499-111">Esempio 1: aggiungere una configurazione di rete virtuale a un gateway dell'applicazione</span><span class="sxs-lookup"><span data-stu-id="38499-111">Example 1: Add an virtual network configuration to an application gateway</span></span>
```
PS C:\>$Vnet = Get-AzVirtualNetwork -Name "Vnet01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Subnet = Get-AzVirtualNetworkSubnetConfig -Name "Subnet01" -VirtualNetwork $Vnet 
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayIPConfiguration -ApplicationGateway $AppGw -Name "Appgwsubnet01" -Subnet $Subnet
```

<span data-ttu-id="38499-112">Il primo comando crea una rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="38499-112">The first command creates a virtual network.</span></span>
<span data-ttu-id="38499-113">Il secondo comando crea una subnet usando la rete virtuale creata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="38499-113">The second command creates a subnet using the previously created virtual network.</span></span>
<span data-ttu-id="38499-114">Il terzo comando ottiene il gateway dell'applicazione e lo archivia nella variabile $AppGw.</span><span class="sxs-lookup"><span data-stu-id="38499-114">The third command gets the application gateway and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="38499-115">Il comando quarto aggiunge la configurazione IP al gateway dell'applicazione archiviato in $AppGw.</span><span class="sxs-lookup"><span data-stu-id="38499-115">The fouth command adds the IP configuration to the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="38499-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38499-116">PARAMETERS</span></span>

### <span data-ttu-id="38499-117">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38499-117">-ApplicationGateway</span></span>
<span data-ttu-id="38499-118">Specifica il gateway dell'applicazione a cui questo cmdlet aggiunge una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="38499-118">Specifies the application gateway to which this cmdlet adds an IP configuration.</span></span>

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

### <span data-ttu-id="38499-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38499-119">-DefaultProfile</span></span>
<span data-ttu-id="38499-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38499-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38499-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="38499-121">-Name</span></span>
<span data-ttu-id="38499-122">Specifica il nome della configurazione IP da aggiungere.</span><span class="sxs-lookup"><span data-stu-id="38499-122">Specifies the name of the IP configuration to add.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38499-123">-Subnet</span><span class="sxs-lookup"><span data-stu-id="38499-123">-Subnet</span></span>
<span data-ttu-id="38499-124">Specifica una subnet.</span><span class="sxs-lookup"><span data-stu-id="38499-124">Specifies a subnet.</span></span>
<span data-ttu-id="38499-125">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38499-125">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38499-126">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="38499-126">-SubnetId</span></span>
<span data-ttu-id="38499-127">Specifica un ID subnet.</span><span class="sxs-lookup"><span data-stu-id="38499-127">Specifies a subnet ID.</span></span>
<span data-ttu-id="38499-128">Questa è la subnet in cui è distribuito il gateway dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="38499-128">This is the subnet in which the application gateway is deployed.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38499-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38499-129">CommonParameters</span></span>
<span data-ttu-id="38499-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38499-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38499-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38499-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38499-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38499-132">INPUTS</span></span>

### <span data-ttu-id="38499-133">System. String</span><span class="sxs-lookup"><span data-stu-id="38499-133">System.String</span></span>

## <span data-ttu-id="38499-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38499-134">OUTPUTS</span></span>

### <span data-ttu-id="38499-135">Microsoft. Azure. Commands. Network. Models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="38499-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="38499-136">Note</span><span class="sxs-lookup"><span data-stu-id="38499-136">NOTES</span></span>

## <span data-ttu-id="38499-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38499-137">RELATED LINKS</span></span>

[<span data-ttu-id="38499-138">Get-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38499-138">Get-AzApplicationGatewayIPConfiguration</span></span>](./Get-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="38499-139">New-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38499-139">New-AzApplicationGatewayIPConfiguration</span></span>](./New-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="38499-140">Remove-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38499-140">Remove-AzApplicationGatewayIPConfiguration</span></span>](./Remove-AzApplicationGatewayIPConfiguration.md)

[<span data-ttu-id="38499-141">Set-AzApplicationGatewayIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38499-141">Set-AzApplicationGatewayIPConfiguration</span></span>](./Set-AzApplicationGatewayIPConfiguration.md)


