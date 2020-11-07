---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermpacketcapturefilterconfig
schema: 2.0.0
ms.openlocfilehash: 1d6054307ad1e499fbb36342f6c81e7e32227f37
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866250"
---
# <span data-ttu-id="c26e1-101">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="c26e1-101">New-AzureRmPacketCaptureFilterConfig</span></span>

## <span data-ttu-id="c26e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c26e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c26e1-103">Crea un nuovo oggetto filtro di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="c26e1-103">Creates a new packet capture filter object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c26e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c26e1-104">SYNTAX</span></span>

```
New-AzureRmPacketCaptureFilterConfig [-Protocol <String>] [-RemoteIPAddress <String>]
 [-LocalIPAddress <String>] [-LocalPort <String>] [-RemotePort <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c26e1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c26e1-105">DESCRIPTION</span></span>
<span data-ttu-id="c26e1-106">Il cmdlet New-AzureRmPacketCaptureFilterConfig crea un nuovo oggetto filtro di acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="c26e1-106">The New-AzureRmPacketCaptureFilterConfig cmdlet creates a new packet capture filter object.</span></span> <span data-ttu-id="c26e1-107">Questo oggetto viene usato per limitare il tipo di pacchetti acquisiti durante una sessione di acquisizione di pacchetti usando i criteri specificati.</span><span class="sxs-lookup"><span data-stu-id="c26e1-107">This object is used to restrict the type of packets that are captured during a packet capture session using the specified criteria.</span></span> <span data-ttu-id="c26e1-108">Il cmdlet New-AzureRmNetworkWatcherPacketCapture può accettare più oggetti Filter per abilitare sessioni di acquisizione componibili.</span><span class="sxs-lookup"><span data-stu-id="c26e1-108">The New-AzureRmNetworkWatcherPacketCapture cmdlet can accept multiple filter objects to enable composable capture sessions.</span></span>

## <span data-ttu-id="c26e1-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c26e1-109">EXAMPLES</span></span>

### <span data-ttu-id="c26e1-110">---Esempio 1: creare un'acquisizione di pacchetti con più filtri---</span><span class="sxs-lookup"><span data-stu-id="c26e1-110">--- Example 1: Create a Packet Capture with multiple filters ---</span></span>
```
$nw = Get-AzurermResource | Where {$_.ResourceType -eq "Microsoft.Network/networkWatchers" -and $_.Location -eq "WestCentralUS" } 
$networkWatcher = Get-AzureRmNetworkWatcher -Name $nw.Name -ResourceGroupName $nw.ResourceGroupName 

$storageAccount = Get-AzureRmStorageAccount -ResourceGroupName contosoResourceGroup -Name contosostorage123

$filter1 = New-AzureRmPacketCaptureFilterConfig -Protocol TCP -RemoteIPAddress "1.1.1.1-255.255.255" -LocalIPAddress "10.0.0.3" -LocalPort "1-65535" -RemotePort "20;80;443"
$filter2 = New-AzureRmPacketCaptureFilterConfig -Protocol UDP 
New-AzureRmNetworkWatcherPacketCapture -NetworkWatcher $networkWatcher -TargetVirtualMachineId $vm.Id -PacketCaptureName "PacketCaptureTest" -StorageAccountId $storageAccount.id -TimeLimitInSeconds 60 -Filters $filter1, $filter2
```

<span data-ttu-id="c26e1-111">In questo esempio creiamo un'acquisizione di pacchetti denominata "PacketCaptureTest" con più filtri e un limite di tempo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-111">In this example we create a packet capture named "PacketCaptureTest" with multiple filters and a time limit.</span></span> <span data-ttu-id="c26e1-112">Una volta completata la sessione, verrà salvata nell'account di archiviazione specificato.</span><span class="sxs-lookup"><span data-stu-id="c26e1-112">Once the session is complete, it will be saved to the specified storage account.</span></span> 

<span data-ttu-id="c26e1-113">Nota: l'estensione Azure Network Watcher deve essere installata nella macchina virtuale di destinazione per creare acquisizioni di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="c26e1-113">Note: The Azure Network Watcher extension must be installed on the target virtual machine to create packet captures.</span></span>

## <span data-ttu-id="c26e1-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c26e1-114">PARAMETERS</span></span>

### <span data-ttu-id="c26e1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c26e1-115">-DefaultProfile</span></span>
<span data-ttu-id="c26e1-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c26e1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c26e1-117">-IndirizzoIPLocale</span><span class="sxs-lookup"><span data-stu-id="c26e1-117">-LocalIPAddress</span></span>
<span data-ttu-id="c26e1-118">Specifica l'indirizzo IP locale a cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="c26e1-118">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="c26e1-119">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-119">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="c26e1-120">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-120">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="c26e1-121">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="c26e1-121">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="c26e1-122">-LocalPort</span><span class="sxs-lookup"><span data-stu-id="c26e1-122">-LocalPort</span></span>
<span data-ttu-id="c26e1-123">Specifica l'indirizzo IP locale a cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="c26e1-123">Specifies the Local IP Address to filter on.</span></span>
<span data-ttu-id="c26e1-124">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-124">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="c26e1-125">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-125">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="c26e1-126">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="c26e1-126">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="c26e1-127">-Protocollo</span><span class="sxs-lookup"><span data-stu-id="c26e1-127">-Protocol</span></span>
<span data-ttu-id="c26e1-128">Specifica il procotol in cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="c26e1-128">Specifies the Procotol to filter on.</span></span> <span data-ttu-id="c26e1-129">Valori accettabili "TCP", "UDP", "any"</span><span class="sxs-lookup"><span data-stu-id="c26e1-129">Acceptable values "TCP","UDP","Any"</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c26e1-130">-IndirizzoIPRemoto</span><span class="sxs-lookup"><span data-stu-id="c26e1-130">-RemoteIPAddress</span></span>
<span data-ttu-id="c26e1-131">Specifica l'indirizzo IP remoto su cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="c26e1-131">Specifies the remote IP address to filter on.</span></span>
<span data-ttu-id="c26e1-132">Input di esempio: "127.0.0.1" per l'immissione di un singolo indirizzo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-132">Example inputs: "127.0.0.1" for single address entry.</span></span>
<span data-ttu-id="c26e1-133">"127.0.0.1-127.0.0.255" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-133">"127.0.0.1-127.0.0.255" for range.</span></span>
<span data-ttu-id="c26e1-134">"127.0.0.1; 127.0.0.5;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="c26e1-134">"127.0.0.1;127.0.0.5;" for multiple entries.</span></span>

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

### <span data-ttu-id="c26e1-135">-RemotePort</span><span class="sxs-lookup"><span data-stu-id="c26e1-135">-RemotePort</span></span>
<span data-ttu-id="c26e1-136">Specifica la porta remota in cui applicare il filtro.</span><span class="sxs-lookup"><span data-stu-id="c26e1-136">Specifies the Remote Port to filter on.</span></span>
<span data-ttu-id="c26e1-137">Input di esempio di porta remota: "80" per l'immissione di una sola porta.</span><span class="sxs-lookup"><span data-stu-id="c26e1-137">Remote port Example inputs: "80" for single port entry.</span></span>
<span data-ttu-id="c26e1-138">"80-85" per l'intervallo.</span><span class="sxs-lookup"><span data-stu-id="c26e1-138">"80-85" for range.</span></span>
<span data-ttu-id="c26e1-139">"80; 443;" per più voci.</span><span class="sxs-lookup"><span data-stu-id="c26e1-139">"80;443;" for multiple entries.</span></span>

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

### <span data-ttu-id="c26e1-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c26e1-140">CommonParameters</span></span>
<span data-ttu-id="c26e1-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c26e1-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c26e1-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c26e1-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c26e1-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c26e1-143">INPUTS</span></span>

### <span data-ttu-id="c26e1-144">System. String</span><span class="sxs-lookup"><span data-stu-id="c26e1-144">System.String</span></span>

## <span data-ttu-id="c26e1-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c26e1-145">OUTPUTS</span></span>

### <span data-ttu-id="c26e1-146">Microsoft. Azure. Commands. Network. Models. PSPacketCaptureFilter</span><span class="sxs-lookup"><span data-stu-id="c26e1-146">Microsoft.Azure.Commands.Network.Models.PSPacketCaptureFilter</span></span>

## <span data-ttu-id="c26e1-147">Note</span><span class="sxs-lookup"><span data-stu-id="c26e1-147">NOTES</span></span>
<span data-ttu-id="c26e1-148">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Watcher, Packet, Capture, Traffic, Filter</span><span class="sxs-lookup"><span data-stu-id="c26e1-148">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, watcher, packet, capture, traffic, filter</span></span> 

## <span data-ttu-id="c26e1-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c26e1-149">RELATED LINKS</span></span>

[<span data-ttu-id="c26e1-150">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c26e1-150">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c26e1-151">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c26e1-151">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c26e1-152">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c26e1-152">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c26e1-153">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="c26e1-153">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="c26e1-154">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c26e1-154">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c26e1-155">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c26e1-155">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c26e1-156">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="c26e1-156">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="c26e1-157">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="c26e1-157">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="c26e1-158">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="c26e1-158">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="c26e1-159">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="c26e1-159">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="c26e1-160">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="c26e1-160">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="c26e1-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="c26e1-161">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
