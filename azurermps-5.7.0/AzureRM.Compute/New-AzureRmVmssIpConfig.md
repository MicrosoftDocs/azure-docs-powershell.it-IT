---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 92F192A5-F75E-4EFE-B2D2-B0DF0B78D3B5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVmssIpConfig.md
ms.openlocfilehash: 448f6236f5c9545ff1a1194c8103463f78a8fefd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514487"
---
# <span data-ttu-id="1dd4d-101">New-AzureRmVmssIpConfig</span><span class="sxs-lookup"><span data-stu-id="1dd4d-101">New-AzureRmVmssIpConfig</span></span>

## <span data-ttu-id="1dd4d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="1dd4d-103">Crea una configurazione IP per un'interfaccia di rete di un VMSS.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-103">Creates an IP configuration for a network interface of a VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1dd4d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dd4d-104">SYNTAX</span></span>

```
New-AzureRmVmssIpConfig [[-Name] <String>] [[-Id] <String>] [[-SubnetId] <String>]
 [[-ApplicationGatewayBackendAddressPoolsId] <String[]>] [[-LoadBalancerBackendAddressPoolsId] <String[]>]
 [[-LoadBalancerInboundNatPoolsId] <String[]>] [-PrivateIPAddressVersion <String>]
 [-PublicIPAddressConfigurationName <String>] [-PublicIPAddressConfigurationIdleTimeoutInMinutes <Int32>]
 [-DnsSetting <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dd4d-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dd4d-105">DESCRIPTION</span></span>
<span data-ttu-id="1dd4d-106">Il cmdlet **New-AzureRmVmssIpConfig** crea un oggetto di configurazione IP per un'interfaccia di rete di un set di scale della macchina virtuale (VMSS).</span><span class="sxs-lookup"><span data-stu-id="1dd4d-106">The **New-AzureRmVmssIpConfig** cmdlet creates an IP configuration object for a network interface of a Virtual Machine Scale Set (VMSS).</span></span>
<span data-ttu-id="1dd4d-107">Specifica la configurazione di questo cmdlet come parametro *IPConfiguration* del cmdlet Add-AzureRmVmssNetworkInterfaceConfiguration.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-107">Specify the configuration from this cmdlet as the *IPConfiguration* parameter of the Add-AzureRmVmssNetworkInterfaceConfiguration cmdlet.</span></span>

## <span data-ttu-id="1dd4d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dd4d-108">EXAMPLES</span></span>

### <span data-ttu-id="1dd4d-109">Esempio 1: creare un oggetto di configurazione IP per un'interfaccia VMSS</span><span class="sxs-lookup"><span data-stu-id="1dd4d-109">Example 1: Create an IP configuration object for a VMSS interface</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface02" -SubnetId $SubnetId
```

<span data-ttu-id="1dd4d-110">Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface02.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-110">This command creates an IP configuration object named ContosoVmssInterface02.</span></span>
<span data-ttu-id="1dd4d-111">Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-111">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="1dd4d-112">Il comando Archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso successivo con **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-112">The command stores the configuration settings in the $IPConfiguration variable for later use with **Add-AzureRmVmssNetworkInterfaceConfiguration**.</span></span>

### <span data-ttu-id="1dd4d-113">Esempio 2: creare un oggetto di configurazione IP che include le impostazioni del pool NAT</span><span class="sxs-lookup"><span data-stu-id="1dd4d-113">Example 2: Create an IP configuration object that includes NAT pool settings</span></span>
```
PS C:\> $IPConfiguration = New-AzureRmVmssIPConfig -Name "ContosoVmssInterface03" -LoadBalancerInboundNatPoolsId $expectedLb.InboundNatPools[0].Id -LoadBalancerBackendAddressPoolsId $expectedLb.BackendAddressPools[0].Id -SubnetId $SubnetId
```

<span data-ttu-id="1dd4d-114">Questo comando crea un oggetto di configurazione IP denominato ContosoVmssInterface03 e lo archivia nella variabile $IPConfiguration per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-114">This command creates an IP configuration object named ContosoVmssInterface03, and then stores it in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="1dd4d-115">Il comando usa un ID subnet definito in precedenza archiviato in $SubnetId.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-115">The command uses a previously defined subnet ID stored in $SubnetId.</span></span>
<span data-ttu-id="1dd4d-116">Il comando Archivia le impostazioni di configurazione nella variabile $IPConfiguration per un uso successivo.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-116">The command stores the configuration settings in the $IPConfiguration variable for later use.</span></span>
<span data-ttu-id="1dd4d-117">Il comando specifica i valori per i parametri *LoadBalancerInboundNatPoolsId* e *LoadBalancerBackendAddressPoolsId* .</span><span class="sxs-lookup"><span data-stu-id="1dd4d-117">The command specifies values for the *LoadBalancerInboundNatPoolsId* and *LoadBalancerBackendAddressPoolsId* parameters.</span></span>

## <span data-ttu-id="1dd4d-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dd4d-118">PARAMETERS</span></span>

### <span data-ttu-id="1dd4d-119">-ApplicationGatewayBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="1dd4d-119">-ApplicationGatewayBackendAddressPoolsId</span></span>
<span data-ttu-id="1dd4d-120">Specifica una matrice di riferimenti ai pool di indirizzi back-end di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-120">Specifies an array of references to backend address pools of load balancers.</span></span>
<span data-ttu-id="1dd4d-121">Un set di proporzioni può fare riferimento a pool di indirizzi backend di uno pubblico e di un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-121">A scale set can reference backend address pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="1dd4d-122">Più set di scale non possono usare lo stesso bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-122">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-123">-DnsSetting</span><span class="sxs-lookup"><span data-stu-id="1dd4d-123">-DnsSetting</span></span>
<span data-ttu-id="1dd4d-124">Impostazioni DNS da applicare agli indirizzi di publicIP.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-124">The dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="1dd4d-125">L'etichetta del nome di dominio delle impostazioni DNS da applicare agli indirizzi di publicIP.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-125">The domain name label of the Dns settings to be applied on the publicIP addresses.</span></span>
<span data-ttu-id="1dd4d-126">La concatenazione dell'etichetta del nome di dominio e dell'indice VM saranno le etichette dei nomi di dominio delle risorse degli indirizzi IP pubblici che verranno create.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-126">The concatenation of the domain name label and vm index will be the domain name labels of the Public IP Address resources that will be created.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-127">-ID</span><span class="sxs-lookup"><span data-stu-id="1dd4d-127">-Id</span></span>
<span data-ttu-id="1dd4d-128">Specifica un ID.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-128">Specifies an ID.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-129">-LoadBalancerBackendAddressPoolsId</span><span class="sxs-lookup"><span data-stu-id="1dd4d-129">-LoadBalancerBackendAddressPoolsId</span></span>
<span data-ttu-id="1dd4d-130">Specifica una matrice di riferimenti ai pool NAT (Network Address Translation) in ingresso dei gruppi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-130">Specifies an array of references to incoming network address translation (NAT) pools of the load balancers.</span></span>
<span data-ttu-id="1dd4d-131">Un set di proporzioni può fare riferimento a pool NAT in arrivo di uno pubblico e di un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-131">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="1dd4d-132">Più set di scale non possono usare lo stesso bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-132">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-133">-LoadBalancerInboundNatPoolsId</span><span class="sxs-lookup"><span data-stu-id="1dd4d-133">-LoadBalancerInboundNatPoolsId</span></span>
<span data-ttu-id="1dd4d-134">Specifica una matrice di riferimenti ai pool NAT in arrivo dei gruppi di bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-134">Specifies an array of references to incoming NAT pools of the load balancers.</span></span>
<span data-ttu-id="1dd4d-135">Un set di proporzioni può fare riferimento a pool NAT in arrivo di uno pubblico e di un bilanciamento del carico interno.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-135">A scale set can reference incoming NAT pools of one public and one internal load balancer.</span></span>
<span data-ttu-id="1dd4d-136">Più set di scale non possono usare lo stesso bilanciamento del carico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-136">Multiple scale sets cannot use the same load balancer.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dd4d-137">-Name</span></span>
<span data-ttu-id="1dd4d-138">Specifica il nome della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-138">Specifies the name of the IP configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-139">-PrivateIPAddressVersion</span><span class="sxs-lookup"><span data-stu-id="1dd4d-139">-PrivateIPAddressVersion</span></span>
<span data-ttu-id="1dd4d-140">Specifica la configurazione IP è IPv4 o IPv6.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-140">Specify the ip configuration is either IPv4 or IPv6.</span></span> <span data-ttu-id="1dd4d-141">Il valore predefinito viene considerato IPv4.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-141">Default is taken as IPv4.</span></span>  <span data-ttu-id="1dd4d-142">I valori possibili sono: "IPv4" e "IPv6".</span><span class="sxs-lookup"><span data-stu-id="1dd4d-142">Possible values are: 'IPv4' and 'IPv6'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="1dd4d-143">-PublicIPAddressConfigurationIdleTimeoutInMinutes</span></span>
<span data-ttu-id="1dd4d-144">Timeout inattivo dell'indirizzo IP pubblico.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-144">The idle timeout of the public IP address.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-145">-PublicIPAddressConfigurationName</span><span class="sxs-lookup"><span data-stu-id="1dd4d-145">-PublicIPAddressConfigurationName</span></span>
<span data-ttu-id="1dd4d-146">Nome della configurazione dell'indirizzo publicIP.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-146">The publicIP address configuration name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-147">-SubnetId</span><span class="sxs-lookup"><span data-stu-id="1dd4d-147">-SubnetId</span></span>
<span data-ttu-id="1dd4d-148">Specifica l'ID subnet in cui la configurazione crea l'interfaccia di rete VMSS.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-148">Specifies the subnet ID in which the configuration creates  the VMSS network interface.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dd4d-149">-Confirm</span></span>
<span data-ttu-id="1dd4d-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dd4d-151">-WhatIf</span></span>
<span data-ttu-id="1dd4d-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1dd4d-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-153">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1dd4d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dd4d-154">CommonParameters</span></span>
<span data-ttu-id="1dd4d-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dd4d-156">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dd4d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dd4d-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dd4d-157">INPUTS</span></span>

### <span data-ttu-id="1dd4d-158">Nessuno</span><span class="sxs-lookup"><span data-stu-id="1dd4d-158">None</span></span>
<span data-ttu-id="1dd4d-159">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="1dd4d-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="1dd4d-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dd4d-160">OUTPUTS</span></span>

## <span data-ttu-id="1dd4d-161">Note</span><span class="sxs-lookup"><span data-stu-id="1dd4d-161">NOTES</span></span>

## <span data-ttu-id="1dd4d-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dd4d-162">RELATED LINKS</span></span>

[<span data-ttu-id="1dd4d-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="1dd4d-163">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>](./Add-AzureRmVmssNetworkInterfaceConfiguration.md)


