---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerfrontendipconfig
schema: 2.0.0
ms.openlocfilehash: 3cd241b84f7ac03dc268a8f04df0490f6a9f9665
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866878"
---
# <span data-ttu-id="fc8bc-101">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc8bc-101">New-AzureRmLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="fc8bc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fc8bc-102">SYNOPSIS</span></span>
<span data-ttu-id="fc8bc-103">Crea una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-103">Creates a front-end IP configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc8bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fc8bc-104">SYNTAX</span></span>

### <span data-ttu-id="fc8bc-105">SetByResourceSubnet</span><span class="sxs-lookup"><span data-stu-id="fc8bc-105">SetByResourceSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -Subnet <PSSubnet>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc8bc-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="fc8bc-106">SetByResourceIdSubnet</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>] -SubnetId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc8bc-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc8bc-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddressId <String>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fc8bc-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc8bc-108">SetByResourcePublicIpAddress</span></span>
```
New-AzureRmLoadBalancerFrontendIpConfig -Name <String> -PublicIpAddress <PSPublicIpAddress>
 [-Zone <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fc8bc-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fc8bc-109">DESCRIPTION</span></span>
<span data-ttu-id="fc8bc-110">Il cmdlet **New-AzureRmLoadBalancerFrontendIpConfig** crea una configurazione IP front-end per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-110">The **New-AzureRmLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="fc8bc-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fc8bc-111">EXAMPLES</span></span>

### <span data-ttu-id="fc8bc-112">Esempio 1: creare una configurazione IP front-end per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="fc8bc-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="fc8bc-113">Il primo comando crea un indirizzo IP pubblico dinamico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="fc8bc-114">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="fc8bc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fc8bc-115">PARAMETERS</span></span>

### <span data-ttu-id="fc8bc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc8bc-116">-DefaultProfile</span></span>
<span data-ttu-id="fc8bc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fc8bc-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="fc8bc-118">-Name</span></span>
<span data-ttu-id="fc8bc-119">Specifica la configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="fc8bc-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc8bc-120">-PrivateIpAddress</span></span>
<span data-ttu-id="fc8bc-121">Specifica l'indirizzo IP privato del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="fc8bc-122">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="fc8bc-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8bc-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc8bc-123">-PublicIpAddress</span></span>
<span data-ttu-id="fc8bc-124">Specifica l'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-124">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8bc-125">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="fc8bc-125">-PublicIpAddressId</span></span>
<span data-ttu-id="fc8bc-126">Specifica l'ID dell'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-126">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8bc-127">-Subnet</span><span class="sxs-lookup"><span data-stu-id="fc8bc-127">-Subnet</span></span>
<span data-ttu-id="fc8bc-128">Specifica l'oggetto **subnet** in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-128">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8bc-129">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="fc8bc-129">-SubnetId</span></span>
<span data-ttu-id="fc8bc-130">Specifica l'ID della subnet in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-130">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdSubnet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc8bc-131">-Zona</span><span class="sxs-lookup"><span data-stu-id="fc8bc-131">-Zone</span></span>
<span data-ttu-id="fc8bc-132">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-132">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc8bc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc8bc-133">CommonParameters</span></span>
<span data-ttu-id="fc8bc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc8bc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc8bc-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc8bc-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc8bc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fc8bc-136">INPUTS</span></span>

## <span data-ttu-id="fc8bc-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fc8bc-137">OUTPUTS</span></span>

### <span data-ttu-id="fc8bc-138">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="fc8bc-138">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="fc8bc-139">Note</span><span class="sxs-lookup"><span data-stu-id="fc8bc-139">NOTES</span></span>

## <span data-ttu-id="fc8bc-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fc8bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="fc8bc-141">Add-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc8bc-141">Add-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Add-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fc8bc-142">Get-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc8bc-142">Get-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Get-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fc8bc-143">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="fc8bc-143">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="fc8bc-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc8bc-144">Remove-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Remove-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="fc8bc-145">Set-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="fc8bc-145">Set-AzureRmLoadBalancerFrontendIpConfig</span></span>](./Set-AzureRmLoadBalancerFrontendIpConfig.md)


