---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: fa520056b9e1d098271cd726575e8d521d7c27f6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201780"
---
# <span data-ttu-id="be92c-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="be92c-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="be92c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be92c-102">SYNOPSIS</span></span>
<span data-ttu-id="be92c-103">Crea una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="be92c-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="be92c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be92c-104">SYNTAX</span></span>

### <span data-ttu-id="be92c-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be92c-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be92c-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="be92c-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be92c-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="be92c-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="be92c-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="be92c-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="be92c-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be92c-109">DESCRIPTION</span></span>
<span data-ttu-id="be92c-110">Il cmdlet **New-AzLoadBalancerFrontendIpConfig** crea una configurazione IP front-end per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="be92c-110">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="be92c-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be92c-111">EXAMPLES</span></span>

### <span data-ttu-id="be92c-112">Esempio 1: creare una configurazione IP front-end per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="be92c-112">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="be92c-113">Il primo comando crea un indirizzo IP pubblico dinamico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="be92c-113">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="be92c-114">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip.</span><span class="sxs-lookup"><span data-stu-id="be92c-114">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

## <span data-ttu-id="be92c-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be92c-115">PARAMETERS</span></span>

### <span data-ttu-id="be92c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be92c-116">-DefaultProfile</span></span>
<span data-ttu-id="be92c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be92c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="be92c-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="be92c-118">-Name</span></span>
<span data-ttu-id="be92c-119">Specifica la configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be92c-119">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="be92c-120">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="be92c-120">-PrivateIpAddress</span></span>
<span data-ttu-id="be92c-121">Specifica l'indirizzo IP privato del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="be92c-121">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="be92c-122">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="be92c-122">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-123">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="be92c-123">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="be92c-124">La versione dell'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="be92c-124">The private IP address version of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceSubnet, SetByResourceIdSubnet
Aliases:
Accepted values: IPv4, IPv6

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-125">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="be92c-125">-PublicIpAddress</span></span>
<span data-ttu-id="be92c-126">Specifica l'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="be92c-126">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: SetByResourcePublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-127">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="be92c-127">-PublicIpAddressId</span></span>
<span data-ttu-id="be92c-128">Specifica l'ID dell'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="be92c-128">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="be92c-129">-Subnet</span></span>
<span data-ttu-id="be92c-130">Specifica l'oggetto **subnet** in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="be92c-130">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: SetByResourceSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-131">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="be92c-131">-SubnetId</span></span>
<span data-ttu-id="be92c-132">Specifica l'ID della subnet in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="be92c-132">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdSubnet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-133">-Zona</span><span class="sxs-lookup"><span data-stu-id="be92c-133">-Zone</span></span>
<span data-ttu-id="be92c-134">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="be92c-134">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be92c-135">-Confirm</span></span>
<span data-ttu-id="be92c-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be92c-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be92c-137">-WhatIf</span></span>
<span data-ttu-id="be92c-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be92c-138">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="be92c-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be92c-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be92c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be92c-140">CommonParameters</span></span>
<span data-ttu-id="be92c-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be92c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be92c-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be92c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be92c-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be92c-143">INPUTS</span></span>

### <span data-ttu-id="be92c-144">System. String</span><span class="sxs-lookup"><span data-stu-id="be92c-144">System.String</span></span>

### <span data-ttu-id="be92c-145">System. String []</span><span class="sxs-lookup"><span data-stu-id="be92c-145">System.String[]</span></span>

### <span data-ttu-id="be92c-146">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="be92c-146">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="be92c-147">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="be92c-147">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="be92c-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be92c-148">OUTPUTS</span></span>

### <span data-ttu-id="be92c-149">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="be92c-149">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="be92c-150">Note</span><span class="sxs-lookup"><span data-stu-id="be92c-150">NOTES</span></span>

## <span data-ttu-id="be92c-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be92c-151">RELATED LINKS</span></span>

[<span data-ttu-id="be92c-152">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="be92c-152">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="be92c-153">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="be92c-153">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="be92c-154">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="be92c-154">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="be92c-155">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="be92c-155">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="be92c-156">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="be92c-156">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


