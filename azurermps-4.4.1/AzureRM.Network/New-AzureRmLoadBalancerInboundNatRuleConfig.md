---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerInboundNatRuleConfig.md
ms.openlocfilehash: 15775f23a205257505d812c5f0493f9f7c124c2b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519104"
---
# <span data-ttu-id="10b42-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10b42-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="10b42-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="10b42-102">SYNOPSIS</span></span>
<span data-ttu-id="10b42-103">Crea una configurazione della regola NAT in ingresso per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="10b42-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="10b42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="10b42-104">SYNTAX</span></span>

### <span data-ttu-id="10b42-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="10b42-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10b42-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="10b42-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="10b42-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="10b42-107">DESCRIPTION</span></span>
<span data-ttu-id="10b42-108">Il cmdlet **New-AzureRmLoadBalancerInboundNatRuleConfig** crea una configurazione della regola NAT (Network Address Translation) in ingresso per un sistema di bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="10b42-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="10b42-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="10b42-109">EXAMPLES</span></span>

### <span data-ttu-id="10b42-110">Esempio 1: creare una configurazione della regola NAT in ingresso per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="10b42-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="10b42-111">Il primo comando crea un indirizzo IP pubblico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="10b42-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="10b42-112">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip e lo archivia nella variabile $frontend.</span><span class="sxs-lookup"><span data-stu-id="10b42-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="10b42-113">Il terzo comando crea una configurazione di regola NAT in ingresso denominata MyInboundNatRule con l'oggetto front-end in $frontend.</span><span class="sxs-lookup"><span data-stu-id="10b42-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="10b42-114">Il protocollo TCP viene specificato e la porta front-end è 3389, uguale alla porta backend in questo caso.</span><span class="sxs-lookup"><span data-stu-id="10b42-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="10b42-115">I parametri *FrontendIpConfiguration* , *procotol* , *FrontendPort* e *BackendPort* sono tutti necessari per creare una configurazione della regola NAT in ingresso.</span><span class="sxs-lookup"><span data-stu-id="10b42-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="10b42-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="10b42-116">PARAMETERS</span></span>

### <span data-ttu-id="10b42-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="10b42-117">-BackendPort</span></span>
<span data-ttu-id="10b42-118">Specifica la porta di backend per il traffico che corrisponde alla configurazione della regola.</span><span class="sxs-lookup"><span data-stu-id="10b42-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-119">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="10b42-119">-EnableFloatingIP</span></span>
<span data-ttu-id="10b42-120">Indica che questo cmdlet Abilita un indirizzo IP mobile per una configurazione di regola.</span><span class="sxs-lookup"><span data-stu-id="10b42-120">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-121">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="10b42-121">-FrontendIpConfiguration</span></span>
<span data-ttu-id="10b42-122">Specifica un elenco di indirizzi IP front-end da associare a una configurazione della regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="10b42-122">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-123">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="10b42-123">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="10b42-124">Specifica l'ID per una configurazione di indirizzi IP front-end.</span><span class="sxs-lookup"><span data-stu-id="10b42-124">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-125">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="10b42-125">-FrontendPort</span></span>
<span data-ttu-id="10b42-126">Specifica la porta front-end corrispondente alla configurazione di una regola di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="10b42-126">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-127">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="10b42-127">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="10b42-128">Specifica il periodo di tempo, in minuti, per il quale lo stato delle conversazioni viene mantenuto in un punto di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="10b42-128">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="10b42-129">-Name</span></span>
<span data-ttu-id="10b42-130">Specifica il nome della configurazione della regola creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="10b42-130">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="10b42-131">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="10b42-131">-Protocol</span></span>
<span data-ttu-id="10b42-132">Specifica un protocollo.</span><span class="sxs-lookup"><span data-stu-id="10b42-132">Specifies a protocol.</span></span>
<span data-ttu-id="10b42-133">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="10b42-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="10b42-134">TCP</span><span class="sxs-lookup"><span data-stu-id="10b42-134">Tcp</span></span>
- <span data-ttu-id="10b42-135">UDP</span><span class="sxs-lookup"><span data-stu-id="10b42-135">Udp</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="10b42-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10b42-136">-DefaultProfile</span></span>
<span data-ttu-id="10b42-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="10b42-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="10b42-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10b42-138">CommonParameters</span></span>
<span data-ttu-id="10b42-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10b42-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10b42-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10b42-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10b42-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="10b42-141">INPUTS</span></span>

## <span data-ttu-id="10b42-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="10b42-142">OUTPUTS</span></span>

### <span data-ttu-id="10b42-143">Microsoft. Azure. Commands. Network. Models. PSInboundNatRule</span><span class="sxs-lookup"><span data-stu-id="10b42-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="10b42-144">Note</span><span class="sxs-lookup"><span data-stu-id="10b42-144">NOTES</span></span>

## <span data-ttu-id="10b42-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="10b42-145">RELATED LINKS</span></span>

[<span data-ttu-id="10b42-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10b42-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="10b42-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10b42-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="10b42-148">New-AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="10b42-148">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="10b42-149">New-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="10b42-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="10b42-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10b42-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="10b42-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="10b42-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


