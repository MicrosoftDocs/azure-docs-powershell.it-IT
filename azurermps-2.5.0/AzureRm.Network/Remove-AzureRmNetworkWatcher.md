---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermnetworkwatcher
schema: 2.0.0
ms.openlocfilehash: 84b92468f4945cbe25404b81f4c6403254a23ad3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866466"
---
# <span data-ttu-id="b240e-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b240e-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="b240e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b240e-102">SYNOPSIS</span></span>
<span data-ttu-id="b240e-103">Rimuove un Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="b240e-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b240e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b240e-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b240e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b240e-105">DESCRIPTION</span></span>
<span data-ttu-id="b240e-106">Il cmdlet Remove-AzureRmNetworkWatcher consente di rimuovere una risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="b240e-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="b240e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b240e-107">EXAMPLES</span></span>

### <span data-ttu-id="b240e-108">--------------------------Esempio 1: creare ed eliminare un Watcher di rete--------------------------</span><span class="sxs-lookup"><span data-stu-id="b240e-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="b240e-109">Questo esempio crea un Watcher di rete in un gruppo di risorse e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="b240e-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="b240e-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="b240e-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="b240e-111">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="b240e-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="b240e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b240e-112">PARAMETERS</span></span>

### <span data-ttu-id="b240e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b240e-113">-AsJob</span></span>
<span data-ttu-id="b240e-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="b240e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b240e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b240e-115">-DefaultProfile</span></span>
<span data-ttu-id="b240e-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b240e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b240e-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="b240e-117">-Name</span></span>
<span data-ttu-id="b240e-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="b240e-118">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b240e-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b240e-119">-PassThru</span></span>
<span data-ttu-id="b240e-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b240e-120">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b240e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b240e-121">-ResourceGroupName</span></span>
<span data-ttu-id="b240e-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="b240e-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b240e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b240e-123">-Confirm</span></span>
<span data-ttu-id="b240e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b240e-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b240e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b240e-125">-WhatIf</span></span>
<span data-ttu-id="b240e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b240e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b240e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b240e-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b240e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b240e-128">CommonParameters</span></span>
<span data-ttu-id="b240e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b240e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b240e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b240e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b240e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b240e-131">INPUTS</span></span>

### <span data-ttu-id="b240e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b240e-132">System.String</span></span>

## <span data-ttu-id="b240e-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b240e-133">OUTPUTS</span></span>

### <span data-ttu-id="b240e-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="b240e-134">System.Object</span></span>

## <span data-ttu-id="b240e-135">Note</span><span class="sxs-lookup"><span data-stu-id="b240e-135">NOTES</span></span>
<span data-ttu-id="b240e-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="b240e-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="b240e-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b240e-137">RELATED LINKS</span></span>

[<span data-ttu-id="b240e-138">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b240e-138">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b240e-139">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="b240e-139">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="b240e-140">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b240e-140">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b240e-141">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="b240e-141">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="b240e-142">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b240e-142">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b240e-143">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b240e-143">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b240e-144">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="b240e-144">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="b240e-145">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="b240e-145">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="b240e-146">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="b240e-146">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="b240e-147">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="b240e-147">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="b240e-148">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="b240e-148">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="b240e-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="b240e-149">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
