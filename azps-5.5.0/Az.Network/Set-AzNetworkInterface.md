---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186854"
---
# <span data-ttu-id="7d9a5-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="7d9a5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d9a5-102">SYNOPSIS</span></span>
<span data-ttu-id="7d9a5-103">Aggiorna un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-103">Updates a network interface.</span></span>

## <span data-ttu-id="7d9a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d9a5-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d9a5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7d9a5-105">DESCRIPTION</span></span>
<span data-ttu-id="7d9a5-106">**Set-AzNetworkInterface** aggiorna un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="7d9a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d9a5-107">EXAMPLES</span></span>

### <span data-ttu-id="7d9a5-108">Esempio 1: Configurare un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="7d9a5-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="7d9a5-109">Questo esempio configura un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-109">This example configures a network interface.</span></span>
<span data-ttu-id="7d9a5-110">Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="7d9a5-111">Il secondo comando imposta l'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="7d9a5-112">Il terzo comando imposta il metodo di allocazione IP privato su Statico.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="7d9a5-113">Il quarto comando imposta un tag nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="7d9a5-114">Il quinto comando usa le informazioni archiviate nella variabile $Nic per impostare l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="7d9a5-115">Esempio 2: Modificare le impostazioni DNS in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="7d9a5-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7d9a5-116">Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 presente nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="7d9a5-117">Il secondo comando aggiunge il server DNS 192.168.1.100 a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="7d9a5-118">Il terzo comando applica queste modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="7d9a5-119">Per rimuovere un server DNS, seguire i comandi elencati sopra, ma sostituire ". Aggiungere" con ". Rimuovi" nel secondo comando.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="7d9a5-120">Esempio 3: Abilitare l'inoltro IP su un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="7d9a5-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7d9a5-121">Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella $nic variabile.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7d9a5-122">Il secondo comando modifica il valore di inoltro IP in true.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="7d9a5-123">Infine, il terzo comando applica le modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="7d9a5-124">Per disabilitare l'inoltro IP in un'interfaccia di rete, seguire l'esempio di esempio, ma assicurarsi di modificare il secondo comando in "$nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="7d9a5-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="7d9a5-125">Esempio 4: Cambiare la subnet di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="7d9a5-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7d9a5-126">Il primo comando ottiene l'interfaccia di rete NetworkInterface1 e la archivia nella $nic variabile.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7d9a5-127">Il secondo comando ottiene la rete virtuale associata alla subnet a cui verrà associata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="7d9a5-128">Il secondo comando recupera la subnet e la archivia nella variabile $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="7d9a5-129">Il terzo comando ha associato l'indirizzo IP privato primario dell'interfaccia di rete alla nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="7d9a5-130">Infine, l'ultimo comando ha applicato queste modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="7d9a5-131">Le configurazioni IP devono essere dinamiche prima di poter cambiare la subnet.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="7d9a5-132">In caso di configurazioni IP statiche, impostare la configurazione dinamica prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="7d9a5-133">Se l'interfaccia di rete ha più configurazioni IP, il quarto comando deve essere eseguito per tutte queste configurazioni IP prima di eseguire il comando Set-AzNetworkInterface di rete finale.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="7d9a5-134">Questa operazione può essere eseguita come specificato nel comando, ma sostituendo "0" con il numero appropriato.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="7d9a5-135">Se un'interfaccia di rete ha configurazioni N IP, è necessario che esistano N-1 di questi comandi.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="7d9a5-136">Esempio 5: Associare/dissociare un gruppo di sicurezza di rete a un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="7d9a5-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="7d9a5-137">Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella $nic variabile.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="7d9a5-138">Il secondo comando ottiene un gruppo di sicurezza di rete esistente denominato MyNSG e lo archivia nella $nsg variabile.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="7d9a5-139">Il terzo comando assegna la $nsg alla $nic.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="7d9a5-140">Infine, il comando applica le modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="7d9a5-141">Per dissociare i gruppi di sicurezza di rete da un'interfaccia di rete, è possibile sostituire $nsg nel terzo comando con $null.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="7d9a5-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7d9a5-142">PARAMETERS</span></span>

### <span data-ttu-id="7d9a5-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7d9a5-143">-AsJob</span></span>
<span data-ttu-id="7d9a5-144">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7d9a5-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7d9a5-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d9a5-145">-DefaultProfile</span></span>
<span data-ttu-id="7d9a5-146">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d9a5-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-147">-NetworkInterface</span></span>
<span data-ttu-id="7d9a5-148">Specifica un oggetto interfaccia di rete che rappresenta lo stato su cui deve essere impostata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="7d9a5-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d9a5-149">CommonParameters</span></span>
<span data-ttu-id="7d9a5-150">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d9a5-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d9a5-151">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d9a5-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d9a5-152">INPUT</span><span class="sxs-lookup"><span data-stu-id="7d9a5-152">INPUTS</span></span>

### <span data-ttu-id="7d9a5-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7d9a5-154">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d9a5-154">OUTPUTS</span></span>

### <span data-ttu-id="7d9a5-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="7d9a5-156">NOTE</span><span class="sxs-lookup"><span data-stu-id="7d9a5-156">NOTES</span></span>

## <span data-ttu-id="7d9a5-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d9a5-157">RELATED LINKS</span></span>

[<span data-ttu-id="7d9a5-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7d9a5-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="7d9a5-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="7d9a5-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="7d9a5-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
