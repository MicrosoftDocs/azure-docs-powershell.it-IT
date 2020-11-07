---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmssipconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVmssIpConfig.md
ms.openlocfilehash: 271d4c9d9fd4a7eb34d4ced4b32dc3929a32b31b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675302"
---
# <span data-ttu-id="38dcb-101">New-AzVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="38dcb-101">New-AzVmssIpConfig</span></span>

## <span data-ttu-id="38dcb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38dcb-102">SYNOPSIS</span></span>
<span data-ttu-id="38dcb-103">Crea una configurazione IP per un'interfaccia di rete di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="38dcb-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

## <span data-ttu-id="38dcb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38dcb-104">SYNTAX</span></span>

```
New-AzVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-Primary] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-IpTag <VirtualMachineScaleSetIpTag[]>] [-PublicIPPrefix <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38dcb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38dcb-105">DESCRIPTION</span></span>
<span data-ttu-id="38dcb-106">Il cmdlet **New-AzVmssIpConfig** crea un oggetto di configurazione IP per un'interfaccia di rete di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="38dcb-106">The **New-AzVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="38dcb-107">Specifica la configurazione di questo cmdlet come parametro *IPConfiguration* del cmdlet Add-AzVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="38dcb-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="38dcb-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38dcb-108">EXAMPLES</span></span>

### <span data-ttu-id="38dcb-109">Esempio 1: creare un oggetto di configurazione IP per un'interfaccia VMSS</span><span class="sxs-lookup"><span data-stu-id="38dcb-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="38dcb-110">Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="38dcb-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="38dcb-111">Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="38dcb-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="38dcb-112">Il comando Archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso successivo con **Add-AzVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="38dcb-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="38dcb-113">Esempio 2: creare un oggetto di configurazione IP che include le impostazioni del pool NAT</span><span class="sxs-lookup"><span data-stu-id="38dcb-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="38dcb-114">Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface03 e lo archivia nella variabile $IPConfiguration per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="38dcb-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="38dcb-115">Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="38dcb-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="38dcb-116">Il comando Archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="38dcb-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="38dcb-117">Il comando specifica i valori per i parametri *LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="38dcb-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="38dcb-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38dcb-118">PARAMETERS</span></span>

### <span data-ttu-id="38dcb-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="38dcb-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="38dcb-120">Specifica una matrice di riferimenti ai pool di indirizzi back-end di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="38dcb-121">Un set di proporzioni può fare riferimento a pool di indirizzi backend di uno pubblico e di un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="38dcb-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="38dcb-122">Più set di scale non possono usare lo stesso bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-122">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="38dcb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38dcb-123">-DefaultProfile</span></span>
<span data-ttu-id="38dcb-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38dcb-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38dcb-125">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="38dcb-125">-DnsSetting</span></span>
<span data-ttu-id="38dcb-126">Impostazioni DNS da applicare agli indirizzi di publicIP.</span><span class="sxs-lookup"><span data-stu-id="38dcb-126">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="38dcb-127">L'etichetta del nome di dominio delle impostazioni DNS da applicare agli indirizzi di publicIP.</span><span class="sxs-lookup"><span data-stu-id="38dcb-127">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="38dcb-128">La concatenazione dell'etichetta del nome di dominio e dell'indice VM saranno le etichette dei nomi di dominio delle risorse degli indirizzi IP pubblici che verranno create.</span><span class="sxs-lookup"><span data-stu-id="38dcb-128">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

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

### <span data-ttu-id="38dcb-129">-ID</span><span class="sxs-lookup"><span data-stu-id="38dcb-129">-Id</span></span>
<span data-ttu-id="38dcb-130">Specifica un ID.</span><span class="sxs-lookup"><span data-stu-id="38dcb-130">Specifies an ID.</span></span>

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

### <span data-ttu-id="38dcb-131">-IpTag</span><span class="sxs-lookup"><span data-stu-id="38dcb-131">-IpTag</span></span>
<span data-ttu-id="38dcb-132">Specifica una matrice di oggetti Tag IP.</span><span class="sxs-lookup"><span data-stu-id="38dcb-132">Specifies an array of Ip Tag objects.</span></span>

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

### <span data-ttu-id="38dcb-133">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="38dcb-133">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="38dcb-134">Specifica una matrice di riferimenti ai pool NAT (Network Address Translation) in ingresso dei gruppi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-134">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="38dcb-135">Un set di proporzioni può fare riferimento a pool NAT in arrivo di uno pubblico e di un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="38dcb-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="38dcb-136">Più set di scale non possono usare lo stesso bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-136">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="38dcb-137">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="38dcb-137">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="38dcb-138">Specifica una matrice di riferimenti ai pool NAT in arrivo dei gruppi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-138">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="38dcb-139">Un set di proporzioni può fare riferimento a pool NAT in arrivo di uno pubblico e di un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="38dcb-139">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="38dcb-140">Più set di scale non possono usare lo stesso bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-140">Multiple scale sets cannot use the same load balancer.</span></span>

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

### <span data-ttu-id="38dcb-141">-Nome</span><span class="sxs-lookup"><span data-stu-id="38dcb-141">-Name</span></span>
<span data-ttu-id="38dcb-142">Specifica il nome della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="38dcb-142">Specifies the name of the IP configuration.</span></span>

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

### <span data-ttu-id="38dcb-143">-Primaria</span><span class="sxs-lookup"><span data-stu-id="38dcb-143">-Primary</span></span>
<span data-ttu-id="38dcb-144">Specifica la configurazione IP primaria nel caso in cui l'interfaccia di rete abbia più di una configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="38dcb-144">Specifies the primary IP Configuration in case the network interface has more than one IP Configuration.</span></span>

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

### <span data-ttu-id="38dcb-145">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="38dcb-145">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="38dcb-146">Specifica la configurazione IP è IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="38dcb-146">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="38dcb-147">Il valore predefinito viene considerato IPv4.</span><span class="sxs-lookup"><span data-stu-id="38dcb-147">Default is taken as IPv4.</span></span>  <span data-ttu-id="38dcb-148">I valori possibili sono: "IPv4" e "IPv6".</span><span class="sxs-lookup"><span data-stu-id="38dcb-148">Possible values are: 'IPv4' and 'IPv6'.</span></span>

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

### <span data-ttu-id="38dcb-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="38dcb-149">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="38dcb-150">Timeout inattivo dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="38dcb-150">The idle timeout of the public IP address.</span></span>

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

### <span data-ttu-id="38dcb-151">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="38dcb-151">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="38dcb-152">Nome della configurazione dell'indirizzo publicIP.</span><span class="sxs-lookup"><span data-stu-id="38dcb-152">The publicIP address configuration name.</span></span>

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

### <span data-ttu-id="38dcb-153">-PublicIPPrefix</span><span class="sxs-lookup"><span data-stu-id="38dcb-153">-PublicIPPrefix</span></span>
<span data-ttu-id="38dcb-154">ID del prefisso IP pubblico</span><span class="sxs-lookup"><span data-stu-id="38dcb-154">The ID of Public IP Prefix</span></span>

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

### <span data-ttu-id="38dcb-155">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="38dcb-155">-SubnetId</span></span>
<span data-ttu-id="38dcb-156">Specifica l'ID subnet in cui la configurazione crea l'interfaccia di rete VMSS.</span><span class="sxs-lookup"><span data-stu-id="38dcb-156">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

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

### <span data-ttu-id="38dcb-157">-Confermare</span><span class="sxs-lookup"><span data-stu-id="38dcb-157">-Confirm</span></span>
<span data-ttu-id="38dcb-158">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38dcb-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38dcb-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38dcb-159">-WhatIf</span></span>
<span data-ttu-id="38dcb-160">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38dcb-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38dcb-161">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="38dcb-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38dcb-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38dcb-162">CommonParameters</span></span>
<span data-ttu-id="38dcb-163">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38dcb-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38dcb-164">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38dcb-164">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38dcb-165">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38dcb-165">INPUTS</span></span>

### <span data-ttu-id="38dcb-166">System. String</span><span class="sxs-lookup"><span data-stu-id="38dcb-166">System.String</span></span>

### <span data-ttu-id="38dcb-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="38dcb-167">System.String[]</span></span>

### <span data-ttu-id="38dcb-168">System. Int32</span><span class="sxs-lookup"><span data-stu-id="38dcb-168">System.Int32</span></span>

### <span data-ttu-id="38dcb-169">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIpTag []</span><span class="sxs-lookup"><span data-stu-id="38dcb-169">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIpTag[]</span></span>

## <span data-ttu-id="38dcb-170">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38dcb-170">OUTPUTS</span></span>

### <span data-ttu-id="38dcb-171">Microsoft. Azure. Management. Compute. Models. VirtualMachineScaleSetIPConfiguration</span><span class="sxs-lookup"><span data-stu-id="38dcb-171">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration</span></span>

## <span data-ttu-id="38dcb-172">Note</span><span class="sxs-lookup"><span data-stu-id="38dcb-172">NOTES</span></span>

## <span data-ttu-id="38dcb-173">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38dcb-173">RELATED LINKS</span></span>

[<span data-ttu-id="38dcb-174">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="38dcb-174">Add-AzVmssNetworkInterfaceConfiguration</span></span>](./Add-AzVmssNetworkInterfaceConfiguration.md)


