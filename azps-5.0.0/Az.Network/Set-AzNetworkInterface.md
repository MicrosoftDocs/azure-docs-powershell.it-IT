---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94202658"
---
# <span data-ttu-id="6a3f6-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="6a3f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a3f6-102">SYNOPSIS</span></span>
<span data-ttu-id="6a3f6-103">Aggiorna un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-103">Updates a network interface.</span></span>

## <span data-ttu-id="6a3f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a3f6-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a3f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a3f6-105">DESCRIPTION</span></span>
<span data-ttu-id="6a3f6-106">Il **set-AzNetworkInterface** aggiorna un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="6a3f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a3f6-107">EXAMPLES</span></span>

### <span data-ttu-id="6a3f6-108">Esempio 1: configurare un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="6a3f6-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="6a3f6-109">Questo esempio configura un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-109">This example configures a network interface.</span></span>
<span data-ttu-id="6a3f6-110">Il primo comando consente di ottenere un'interfaccia di rete denominata NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="6a3f6-111">Il secondo comando imposta l'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="6a3f6-112">Il terzo comando imposta il metodo di allocazione IP privato su static.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="6a3f6-113">Il quarto comando imposta un contrassegno nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="6a3f6-114">Il quinto comando usa le informazioni archiviate nella variabile $Nic per impostare l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="6a3f6-115">Esempio 2: modificare le impostazioni DNS in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="6a3f6-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="6a3f6-116">Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 che esiste all'interno del gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="6a3f6-117">Il secondo comando aggiunge il server DNS 192.168.1.100 a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="6a3f6-118">Il terzo comando applica queste modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="6a3f6-119">Per rimuovere un server DNS, seguire i comandi elencati sopra, ma sostituisci ". Aggiungi "con". Rimuovi "nel secondo comando.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="6a3f6-120">Esempio 3: abilitare l'inoltro IP in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="6a3f6-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="6a3f6-121">Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="6a3f6-122">Il secondo comando cambia il valore di inoltro IP in vero.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="6a3f6-123">Infine, il terzo comando applica le modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="6a3f6-124">Per disabilitare l'inoltro IP in un'interfaccia di rete, seguire l'esempio di campione, ma assicurarsi di cambiare il secondo comando in "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="6a3f6-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="6a3f6-125">Esempio 4: cambiare la subnet di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="6a3f6-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="6a3f6-126">Il primo comando ottiene l'interfaccia di rete NetworkInterface1 e lo archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="6a3f6-127">Il secondo comando ottiene la rete virtuale associata alla subnet in cui verrà associata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="6a3f6-128">Il secondo comando ottiene la subnet e la archivia nella variabile $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="6a3f6-129">Il terzo comando associa l'indirizzo IP privato principale dell'interfaccia di rete alla nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="6a3f6-130">Infine, l'ultimo comando ha applicato queste modifiche nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="6a3f6-131">Le configurazioni IP devono essere dinamiche prima di poter modificare la subnet.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="6a3f6-132">Se si hanno configurazioni IP statiche, passare alla dinamica prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="6a3f6-133">Se l'interfaccia di rete include più configurazioni IP, il comando Forth deve essere eseguito per tutte queste configurazioni IP prima dell'esecuzione del comando Set-AzNetworkInterface finale.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="6a3f6-134">Questa operazione può essere eseguita come nel comando avanti, ma sostituendo "0" con il numero appropriato.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="6a3f6-135">Se un'interfaccia di rete include configurazioni N IP, è necessario che N-1 di questi comandi sia presente.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="6a3f6-136">Esempio 5: associare/dissociare un gruppo di sicurezza di rete a un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="6a3f6-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="6a3f6-137">Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="6a3f6-138">Il secondo comando ottiene un gruppo di sicurezza di rete esistente denominato MyNSG e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="6a3f6-139">Il terzo comando assegna la $nsg al $nic.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="6a3f6-140">Infine, il comando Forth applica le modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="6a3f6-141">Per dissociare i gruppi di sicurezza di rete da un'interfaccia di rete, è sufficiente sostituire $nsg nel terzo comando con $null.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="6a3f6-142">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a3f6-142">PARAMETERS</span></span>

### <span data-ttu-id="6a3f6-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6a3f6-143">-AsJob</span></span>
<span data-ttu-id="6a3f6-144">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="6a3f6-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6a3f6-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a3f6-145">-DefaultProfile</span></span>
<span data-ttu-id="6a3f6-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a3f6-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-147">-NetworkInterface</span></span>
<span data-ttu-id="6a3f6-148">Specifica un oggetto interfaccia di rete che rappresenta lo stato in cui deve essere impostata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a3f6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a3f6-149">CommonParameters</span></span>
<span data-ttu-id="6a3f6-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a3f6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a3f6-151">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a3f6-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a3f6-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a3f6-152">INPUTS</span></span>

### <span data-ttu-id="6a3f6-153">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6a3f6-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a3f6-154">OUTPUTS</span></span>

### <span data-ttu-id="6a3f6-155">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="6a3f6-156">Note</span><span class="sxs-lookup"><span data-stu-id="6a3f6-156">NOTES</span></span>

## <span data-ttu-id="6a3f6-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a3f6-157">RELATED LINKS</span></span>

[<span data-ttu-id="6a3f6-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="6a3f6-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="6a3f6-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="6a3f6-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="6a3f6-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
