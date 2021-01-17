---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D639E4F5-5AAD-4F13-9B48-70E90D2DFFCA
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerfrontendipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzLoadBalancerFrontendIpConfig.md
ms.openlocfilehash: 5b5ca651442a0150461da64bb5e33a37167fec3b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332119"
---
# <span data-ttu-id="80d07-101">New-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d07-101">New-AzLoadBalancerFrontendIpConfig</span></span>

## <span data-ttu-id="80d07-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="80d07-102">SYNOPSIS</span></span>
<span data-ttu-id="80d07-103">Crea una configurazione IP front-end per un bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="80d07-103">Creates a front-end IP configuration for a load balancer.</span></span>

## <span data-ttu-id="80d07-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="80d07-104">SYNTAX</span></span>

### <span data-ttu-id="80d07-105">SetByResourceSubnet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="80d07-105">SetByResourceSubnet (Default)</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -Subnet <PSSubnet>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d07-106">SetByResourceIdSubnet</span><span class="sxs-lookup"><span data-stu-id="80d07-106">SetByResourceIdSubnet</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-PrivateIpAddress <String>]
 [-PrivateIpAddressVersion <String>] [-Zone <String[]>] -SubnetId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d07-107">SetByResourceIdPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80d07-107">SetByResourceIdPublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d07-108">SetByResourcePublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80d07-108">SetByResourcePublicIpAddress</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddress <PSPublicIpAddress>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d07-109">SetByResourceIdPublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="80d07-109">SetByResourceIdPublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefixId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80d07-110">SetByResourcePublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="80d07-110">SetByResourcePublicIpAddressPrefix</span></span>
```
New-AzLoadBalancerFrontendIpConfig -Name <String> [-Zone <String[]>] -PublicIpAddressPrefix <PSPublicIpPrefix>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80d07-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="80d07-111">DESCRIPTION</span></span>
<span data-ttu-id="80d07-112">Il cmdlet **New-AzLoadBalancerFrontendIpConfig** crea una configurazione IP front-end per un bilanciamento del carico di Azure.</span><span class="sxs-lookup"><span data-stu-id="80d07-112">The **New-AzLoadBalancerFrontendIpConfig** cmdlet creates a front-end IP configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="80d07-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="80d07-113">EXAMPLES</span></span>

### <span data-ttu-id="80d07-114">Esempio 1: creare una configurazione IP front-end per un bilanciamento del carico</span><span class="sxs-lookup"><span data-stu-id="80d07-114">Example 1: Create a front-end IP configuration for a load balancer</span></span>
```
PS C:\> $publicip = New-AzPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
```

<span data-ttu-id="80d07-115">Il primo comando crea un indirizzo IP pubblico dinamico denominato MyPublicIP nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicip.</span><span class="sxs-lookup"><span data-stu-id="80d07-115">The first command creates a dynamic public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>
<span data-ttu-id="80d07-116">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando l'indirizzo IP pubblico in $publicip.</span><span class="sxs-lookup"><span data-stu-id="80d07-116">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip.</span></span>

### <span data-ttu-id="80d07-117">Esempio 2: creare una configurazione IP front-end per un bilanciamento del carico tramite il prefisso IP</span><span class="sxs-lookup"><span data-stu-id="80d07-117">Example 2: Create a front-end IP configuration for a load balancer using ip prefix</span></span>
```
PS C:\> $publicipprefix = New-AzPublicIpPrefix -ResourceGroupName "MyResourceGroup" -name "MyPublicIPPrefix" -location "West US" -Sku Standard -PrefixLength 28
PS C:\> $frontend = New-AzLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddressPrefix $publicipprefix
```

<span data-ttu-id="80d07-118">Il primo comando crea un prefisso IP pubblico denominato MyPublicIP di lunghezza 28 nel gruppo di risorse denominato MyResourceGroup e lo archivia nella variabile $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="80d07-118">The first command creates a public ip prefix named MyPublicIP of length 28 in the resource group named MyResourceGroup, and then stores it in the $publicipprefix variable.</span></span>
<span data-ttu-id="80d07-119">Il secondo comando crea una configurazione IP front-end denominata FrontendIpConfig01 usando il prefisso IP pubblico in $publicipprefix.</span><span class="sxs-lookup"><span data-stu-id="80d07-119">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP prefix in $publicipprefix.</span></span>

## <span data-ttu-id="80d07-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="80d07-120">PARAMETERS</span></span>

### <span data-ttu-id="80d07-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80d07-121">-DefaultProfile</span></span>
<span data-ttu-id="80d07-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="80d07-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="80d07-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="80d07-123">-Name</span></span>
<span data-ttu-id="80d07-124">Specifica la configurazione IP front-end creata da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d07-124">Specifies the front-end IP configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="80d07-125">-PrivateIpAddress</span><span class="sxs-lookup"><span data-stu-id="80d07-125">-PrivateIpAddress</span></span>
<span data-ttu-id="80d07-126">Specifica l'indirizzo IP privato del bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="80d07-126">Specifies the private IP address of the load balancer.</span></span>
<span data-ttu-id="80d07-127">Specificare questo parametro solo se si specifica anche il parametro *subnet* .</span><span class="sxs-lookup"><span data-stu-id="80d07-127">Specify this parameter only if you also specify the *Subnet* parameter.</span></span>

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

### <span data-ttu-id="80d07-128">-PrivateIpAddressVersion</span><span class="sxs-lookup"><span data-stu-id="80d07-128">-PrivateIpAddressVersion</span></span>
<span data-ttu-id="80d07-129">La versione dell'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="80d07-129">The private IP address version of the IP configuration.</span></span>

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

### <span data-ttu-id="80d07-130">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80d07-130">-PublicIpAddress</span></span>
<span data-ttu-id="80d07-131">Specifica l'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="80d07-131">Specifies the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="80d07-132">-PublicIpAddressId</span><span class="sxs-lookup"><span data-stu-id="80d07-132">-PublicIpAddressId</span></span>
<span data-ttu-id="80d07-133">Specifica l'ID dell'oggetto **PublicIpAddress** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="80d07-133">Specifies the ID of the **PublicIpAddress** object to associate with a front-end IP configuration.</span></span>

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

### <span data-ttu-id="80d07-134">-PublicIpAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="80d07-134">-PublicIpAddressPrefix</span></span>
<span data-ttu-id="80d07-135">Specifica l'oggetto **PublicIpAddressPrefix** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="80d07-135">Specifies the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpPrefix
Parameter Sets: SetByResourcePublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d07-136">-PublicIpAddressPrefixId</span><span class="sxs-lookup"><span data-stu-id="80d07-136">-PublicIpAddressPrefixId</span></span>
<span data-ttu-id="80d07-137">Specifica l'ID dell'oggetto **PublicIpAddressPrefix** da associare a una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="80d07-137">Specifies the ID of the **PublicIpAddressPrefix** object to associate with a front-end IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceIdPublicIpAddressPrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80d07-138">-Subnet</span><span class="sxs-lookup"><span data-stu-id="80d07-138">-Subnet</span></span>
<span data-ttu-id="80d07-139">Specifica l'oggetto **subnet** in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="80d07-139">Specifies the **Subnet** object in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="80d07-140">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="80d07-140">-SubnetId</span></span>
<span data-ttu-id="80d07-141">Specifica l'ID della subnet in cui creare una configurazione IP front-end.</span><span class="sxs-lookup"><span data-stu-id="80d07-141">Specifies the ID of the subnet in which to create a front-end IP configuration.</span></span>

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

### <span data-ttu-id="80d07-142">-Zona</span><span class="sxs-lookup"><span data-stu-id="80d07-142">-Zone</span></span>
<span data-ttu-id="80d07-143">Elenco delle aree di disponibilità che indicano che l'IP allocato per la risorsa deve provenire.</span><span class="sxs-lookup"><span data-stu-id="80d07-143">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

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

### <span data-ttu-id="80d07-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="80d07-144">-Confirm</span></span>
<span data-ttu-id="80d07-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="80d07-145">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80d07-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80d07-146">-WhatIf</span></span>
<span data-ttu-id="80d07-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80d07-147">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="80d07-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="80d07-148">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80d07-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80d07-149">CommonParameters</span></span>
<span data-ttu-id="80d07-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="80d07-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80d07-151">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="80d07-151">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80d07-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="80d07-152">INPUTS</span></span>

### <span data-ttu-id="80d07-153">System. String</span><span class="sxs-lookup"><span data-stu-id="80d07-153">System.String</span></span>

### <span data-ttu-id="80d07-154">System. String []</span><span class="sxs-lookup"><span data-stu-id="80d07-154">System.String[]</span></span>

### <span data-ttu-id="80d07-155">Microsoft. Azure. Commands. Network. Models. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="80d07-155">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="80d07-156">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80d07-156">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="80d07-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="80d07-157">OUTPUTS</span></span>

### <span data-ttu-id="80d07-158">Microsoft. Azure. Commands. Network. Models. PSFrontendIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="80d07-158">Microsoft.Azure.Commands.Network.Models.PSFrontendIPConfiguration</span></span>

## <span data-ttu-id="80d07-159">Note</span><span class="sxs-lookup"><span data-stu-id="80d07-159">NOTES</span></span>

## <span data-ttu-id="80d07-160">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="80d07-160">RELATED LINKS</span></span>

[<span data-ttu-id="80d07-161">Add-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d07-161">Add-AzLoadBalancerFrontendIpConfig</span></span>](./Add-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="80d07-162">Get-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d07-162">Get-AzLoadBalancerFrontendIpConfig</span></span>](./Get-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="80d07-163">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="80d07-163">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="80d07-164">Remove-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d07-164">Remove-AzLoadBalancerFrontendIpConfig</span></span>](./Remove-AzLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="80d07-165">Set-AzLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="80d07-165">Set-AzLoadBalancerFrontendIpConfig</span></span>](./Set-AzLoadBalancerFrontendIpConfig.md)


