---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 30dbe52805017a00f24cc95c832386545ae036e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965038"
---
# <span data-ttu-id="79b25-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="79b25-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="79b25-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79b25-102">SYNOPSIS</span></span>
<span data-ttu-id="79b25-103">Crea una configurazione IP per un'interfaccia di rete di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="79b25-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="79b25-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="79b25-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-PublicIPAddressVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79b25-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="79b25-105">DESCRIPTION</span></span>
<span data-ttu-id="79b25-106">Il cmdlet **New-AzVmssIpConfig crea** un oggetto di configurazione IP per un'interfaccia di rete di un set di scalabilità delle macchine virtuali (VMSS).</span><span class="sxs-lookup"><span data-stu-id="79b25-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="79b25-107">Specificare la configurazione da questo cmdlet come *parametro IPConfiguration* del cmdlet Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="79b25-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="79b25-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="79b25-108">EXAMPLES</span></span>

### <span data-ttu-id="79b25-109">Esempio 1: Creare un oggetto di configurazione IP per un'interfaccia VMSS</span><span class="sxs-lookup"><span data-stu-id="79b25-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="79b25-110">Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="79b25-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="79b25-111">Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="79b25-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="79b25-112">Il comando archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso futuro **con Add-AzVmssNetworkInterfaceConfiguration.**</span><span class="sxs-lookup"><span data-stu-id="79b25-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="79b25-113">Esempio 2: Creare un oggetto di configurazione IP che include le impostazioni del pool NAT</span><span class="sxs-lookup"><span data-stu-id="79b25-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="79b25-114">Questo comando crea un oggetto configurazione IP denominato ContosoVmssInterface03 e quindi lo archivia nella variabile $IPConfiguration per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="79b25-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="79b25-115">Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="79b25-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="79b25-116">Il comando archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso futuro.</span><span class="sxs-lookup"><span data-stu-id="79b25-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="79b25-117">Il comando specifica i valori per *i parametri LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId.*</span><span class="sxs-lookup"><span data-stu-id="79b25-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="79b25-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79b25-118">PARAMETERS</span></span>

### <span data-ttu-id="79b25-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="79b25-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="79b25-120">Specifica una matrice di riferimenti a pool di indirizzi back-end di servizi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="79b25-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="79b25-121">Un set di scale può fare riferimento a pool di indirizzi back-end di una bilanciamento del carico pubblico e uno interno.</span><span class="sxs-lookup"><span data-stu-id="79b25-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="79b25-122">Più set di scala non possono usare la stessa bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="79b25-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79b25-123">-DefaultProfile</span></span>
<span data-ttu-id="79b25-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="79b25-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79b25-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="79b25-125">-DnsSetting</span></span>
<span data-ttu-id="79b25-126">Impostazioni dns da applicare agli indirizzi publicIP.</span><span class="sxs-lookup"><span data-stu-id="79b25-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="79b25-127">Etichetta del nome di dominio delle impostazioni Dns da applicare agli indirizzi PublicIP.</span><span class="sxs-lookup"><span data-stu-id="79b25-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="79b25-128">La concatenazione dell'etichetta del nome di dominio e dell'indice della macchina virtuale sarà l'etichetta dei nomi di dominio delle risorse Indirizzo IP pubblico che verranno create.</span><span class="sxs-lookup"><span data-stu-id="79b25-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressDomainNameLabel

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-129">-Id</span><span class="sxs-lookup"><span data-stu-id="79b25-129">-Id</span></span>
<span data-ttu-id="79b25-130">Specifica un ID.</span><span class="sxs-lookup"><span data-stu-id="79b25-130">Specifies an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="79b25-131">-IpTag</span></span>
<span data-ttu-id="79b25-132">Specifica una matrice di oggetti Tag IP.</span><span class="sxs-lookup"><span data-stu-id="79b25-132">Specifies an array of Ip Tag objects.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="79b25-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="79b25-134">Specifica una matrice di riferimenti a pool NAT (Network Address Translation) in ingresso delle servizi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="79b25-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="79b25-135">Un set di scala può fare riferimento a pool di NAT in ingresso di una bilanciamento del carico pubblico e uno interno.</span><span class="sxs-lookup"><span data-stu-id="79b25-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="79b25-136">Più set di scala non possono usare la stessa bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="79b25-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="79b25-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="79b25-138">Specifica una matrice di riferimenti a pool NAT in ingresso delle servizi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="79b25-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="79b25-139">Un set di scala può fare riferimento a pool di NAT in ingresso di una bilanciamento del carico pubblico e uno interno.</span><span class="sxs-lookup"><span data-stu-id="79b25-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="79b25-140">Più set di scala non possono usare la stessa bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="79b25-140">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-141">-Name</span><span class="sxs-lookup"><span data-stu-id="79b25-141">-Name</span></span>
<span data-ttu-id="79b25-142">Specifica il nome della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="79b25-142">Specifies the name of the IP configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-143">-Principale</span><span class="sxs-lookup"><span data-stu-id="79b25-143">-Primary</span></span>
<span data-ttu-id="79b25-144">Specifica la configurazione IP principale nel caso in cui l'interfaccia di rete abbia più di una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="79b25-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="79b25-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="79b25-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="79b25-146">Specificare la configurazione IP per l'indirizzo IP privato.</span><span class="sxs-lookup"><span data-stu-id="79b25-146">Specify the IP configuration for private IP address.</span></span>  <span data-ttu-id="79b25-147">Il valore predefinito è IPv4.</span><span class="sxs-lookup"><span data-stu-id="79b25-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="79b25-148">I valori possibili sono "IPv4" e "IPv6".</span><span class="sxs-lookup"><span data-stu-id="79b25-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="79b25-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="79b25-150">Timeout di inattività dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="79b25-150">The idle timeout of the public IP address.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: PublicIPAddressIdleTimeoutInMinutes

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="79b25-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="79b25-152">Nome di configurazione dell'indirizzo publicIP.</span><span class="sxs-lookup"><span data-stu-id="79b25-152">The publicIP address configuration name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: PublicIPAddressName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-153">-PublicIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="79b25-153">-PublicIPAddressVersion</span></span>
<span data-ttu-id="79b25-154">Specificare la configurazione IP per l'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="79b25-154">Specify the IP configuration for public IP address.</span></span>  <span data-ttu-id="79b25-155">Il valore predefinito è IPv4.</span><span class="sxs-lookup"><span data-stu-id="79b25-155">Default is taken as IPv4.</span></span>  <span data-ttu-id="79b25-156">I valori possibili sono "IPv4" e "IPv6".</span><span class="sxs-lookup"><span data-stu-id="79b25-156">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-157">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="79b25-157">-PublicIPPrefix</span></span>
<span data-ttu-id="79b25-158">ID del prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="79b25-158">The ID of Public IP Prefix</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-159">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="79b25-159">-SubnetId</span></span>
<span data-ttu-id="79b25-160">Specifica l'ID subnet in cui la configurazione crea l'interfaccia di rete VMSS.</span><span class="sxs-lookup"><span data-stu-id="79b25-160">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79b25-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="79b25-161">-Confirm</span></span>
<span data-ttu-id="79b25-162">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79b25-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79b25-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79b25-163">-WhatIf</span></span>
<span data-ttu-id="79b25-164">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79b25-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79b25-165">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="79b25-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79b25-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79b25-166">CommonParameters</span></span>
<span data-ttu-id="79b25-167">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79b25-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79b25-168">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="79b25-168">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79b25-169">INPUT</span><span class="sxs-lookup"><span data-stu-id="79b25-169">INPUTS</span></span>

### <span data-ttu-id="79b25-170">System.String</span><span class="sxs-lookup"><span data-stu-id="79b25-170">System.String</span></span>

### <span data-ttu-id="79b25-171">System.String[]</span><span class="sxs-lookup"><span data-stu-id="79b25-171">System.String[]</span></span>

### <span data-ttu-id="79b25-172">System.Int32</span><span class="sxs-lookup"><span data-stu-id="79b25-172">System.Int32</span></span>

### <span data-ttu-id="79b25-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span><span class="sxs-lookup"><span data-stu-id="79b25-173">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="79b25-174">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="79b25-174">OUTPUTS</span></span>

### <span data-ttu-id="79b25-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b25-175">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="79b25-176">NOTE</span><span class="sxs-lookup"><span data-stu-id="79b25-176">NOTES</span></span>

## <span data-ttu-id="79b25-177">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="79b25-177">RELATED LINKS</span></span>

[<span data-ttu-id="79b25-178">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="79b25-178">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


