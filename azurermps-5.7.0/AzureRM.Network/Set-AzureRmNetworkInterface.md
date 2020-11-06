---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermnetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: d4f792aecabcbeaa3608f335e3a2d13813d11187
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514251"
---
# <span data-ttu-id="30e32-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="30e32-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30e32-102">SYNOPSIS</span></span>
<span data-ttu-id="30e32-103">Imposta lo stato obiettivo per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30e32-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30e32-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="30e32-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30e32-105">DESCRIPTION</span></span>
<span data-ttu-id="30e32-106">**Set-AzureRmNetworkInterface** imposta lo stato dell'obiettivo per un'interfaccia di rete Azure.</span><span class="sxs-lookup"><span data-stu-id="30e32-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="30e32-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30e32-107">EXAMPLES</span></span>

### <span data-ttu-id="30e32-108">Esempio 1: configurare un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="30e32-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="30e32-109">Questo esempio configura un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-109">This example configures a network interface.</span></span>
<span data-ttu-id="30e32-110">Il primo comando consente di ottenere un'interfaccia di rete denominata NetworkInterface1 nel gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="30e32-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="30e32-111">Il secondo comando imposta l'indirizzo IP privato della configurazione IP.</span><span class="sxs-lookup"><span data-stu-id="30e32-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="30e32-112">Il terzo comando imposta il metodo di allocazione IP privato su static.</span><span class="sxs-lookup"><span data-stu-id="30e32-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="30e32-113">Il quarto comando imposta un contrassegno nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="30e32-114">Il quinto comando usa le informazioni archiviate nella variabile $Nic per impostare l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="30e32-115">Esempio 2: modificare le impostazioni DNS in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="30e32-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="30e32-116">Il primo comando ottiene un'interfaccia di rete denominata NetworkInterface1 che esiste all'interno del gruppo di risorse ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="30e32-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="30e32-117">Il secondo comando aggiunge il server DNS 192.168.1.100 a questa interfaccia.</span><span class="sxs-lookup"><span data-stu-id="30e32-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="30e32-118">Il terzo comando applica queste modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="30e32-119">Per rimuovere un server DNS, seguire i comandi elencati sopra, ma sostituisci ". Aggiungi "con". Rimuovi "nel secondo comando.</span><span class="sxs-lookup"><span data-stu-id="30e32-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="30e32-120">Esempio 3: abilitare l'forwading IP in un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="30e32-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="30e32-121">Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="30e32-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="30e32-122">Il secondo comando cambia il valore di inoltro IP in vero.</span><span class="sxs-lookup"><span data-stu-id="30e32-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="30e32-123">Infine, il terzo comando applica le modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="30e32-124">Per disabilitare l'inoltro IP in un'interfaccia di rete, seguire l'esempio di campione, ma assicurarsi di cambiare il secondo comando in "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="30e32-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="30e32-125">Esempio 4: cambiare la subnet di un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="30e32-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="30e32-126">Il primo comando ottiene l'interfaccia di rete NetworkInterface1 e lo archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="30e32-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="30e32-127">Il secondo comando ottiene la rete virtuale associata alla subnet in cui verrà associata l'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="30e32-128">Il secondo comando ottiene la subnet e la archivia nella variabile $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="30e32-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="30e32-129">Il terzo comando associa l'indirizzo IP privato principale dell'interfaccia di rete alla nuova subnet.</span><span class="sxs-lookup"><span data-stu-id="30e32-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="30e32-130">Infine, l'ultimo comando ha applicato queste modifiche nell'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="30e32-131">Le configurazioni IP devono essere dinamiche prima di poter modificare la subnet.</span><span class="sxs-lookup"><span data-stu-id="30e32-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="30e32-132">Se si hanno configurazioni IP statiche, passare alla dinamica prima di procedere.</span><span class="sxs-lookup"><span data-stu-id="30e32-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="30e32-133">Se l'interfaccia di rete include più configurazioni IP, il comando Forth deve essere eseguito per tutte queste configurazioni IP prima dell'esecuzione del comando Set-AzureRmNetworkInterface finale.</span><span class="sxs-lookup"><span data-stu-id="30e32-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="30e32-134">Questa operazione può essere eseguita come nel comando avanti, ma sostituendo "0" con il numero appropriato.</span><span class="sxs-lookup"><span data-stu-id="30e32-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="30e32-135">Se un'interfaccia di rete include configurazioni N IP, è necessario che N-1 di questi comandi sia presente.</span><span class="sxs-lookup"><span data-stu-id="30e32-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="30e32-136">Esempio 5: associare/dissociare un gruppo di sicurezza di rete a un'interfaccia di rete</span><span class="sxs-lookup"><span data-stu-id="30e32-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="30e32-137">Il primo comando ottiene un'interfaccia di rete esistente denominata NetworkInterface1 e la archivia nella variabile $nic.</span><span class="sxs-lookup"><span data-stu-id="30e32-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="30e32-138">Il secondo comando ottiene un gruppo di sicurezza di rete esistente denominato MyNSG e lo archivia nella variabile $nsg.</span><span class="sxs-lookup"><span data-stu-id="30e32-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="30e32-139">Il comando avanti assegna l'$nsg al $nic.</span><span class="sxs-lookup"><span data-stu-id="30e32-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="30e32-140">Infine, il quinto comando applica le modifiche all'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="30e32-141">Per dissociare i gruppi di sicurezza di rete da un'interfaccia di rete, è sufficiente sostituire $nsg nel comando avanti con $null.</span><span class="sxs-lookup"><span data-stu-id="30e32-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="30e32-142">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30e32-142">PARAMETERS</span></span>

### <span data-ttu-id="30e32-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="30e32-143">-AsJob</span></span>
<span data-ttu-id="30e32-144">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="30e32-144">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30e32-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30e32-145">-DefaultProfile</span></span>
<span data-ttu-id="30e32-146">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="30e32-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="30e32-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-147">-NetworkInterface</span></span>
<span data-ttu-id="30e32-148">Specifica un oggetto **NetworkInterface** che rappresenta lo stato dell'obiettivo per un'interfaccia di rete.</span><span class="sxs-lookup"><span data-stu-id="30e32-148">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

```yaml
Type: PSNetworkInterface
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="30e32-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30e32-149">CommonParameters</span></span>
<span data-ttu-id="30e32-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30e32-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30e32-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30e32-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30e32-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30e32-152">INPUTS</span></span>

### <span data-ttu-id="30e32-153">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-153">PSNetworkInterface</span></span>
<span data-ttu-id="30e32-154">Il parametro ' NetworkInterface ' accetta il valore di tipo ' PSNetworkInterface ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="30e32-154">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="30e32-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30e32-155">OUTPUTS</span></span>

### <span data-ttu-id="30e32-156">Microsoft. Azure. Commands. Network. Models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-156">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="30e32-157">Note</span><span class="sxs-lookup"><span data-stu-id="30e32-157">NOTES</span></span>

## <span data-ttu-id="30e32-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30e32-158">RELATED LINKS</span></span>

[<span data-ttu-id="30e32-159">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-159">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="30e32-160">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-160">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="30e32-161">New-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-161">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="30e32-162">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="30e32-162">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)