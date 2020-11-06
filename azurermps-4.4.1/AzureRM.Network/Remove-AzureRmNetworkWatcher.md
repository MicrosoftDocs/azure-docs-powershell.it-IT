---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmNetworkWatcher.md
ms.openlocfilehash: ee92fd78d3a69b38620b2af543e01db7569d3b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508519"
---
# <span data-ttu-id="bcb27-101">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcb27-101">Remove-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="bcb27-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bcb27-102">SYNOPSIS</span></span>
<span data-ttu-id="bcb27-103">Rimuove un Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="bcb27-103">Removes a Network Watcher.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bcb27-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bcb27-104">SYNTAX</span></span>

```
Remove-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bcb27-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bcb27-105">DESCRIPTION</span></span>
<span data-ttu-id="bcb27-106">Il cmdlet Remove-AzureRmNetworkWatcher consente di rimuovere una risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="bcb27-106">The Remove-AzureRmNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="bcb27-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bcb27-107">EXAMPLES</span></span>

### <span data-ttu-id="bcb27-108">--------------------------Esempio 1: creare ed eliminare un Watcher di rete--------------------------</span><span class="sxs-lookup"><span data-stu-id="bcb27-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="bcb27-109">Questo esempio crea un Watcher di rete in un gruppo di risorse e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="bcb27-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="bcb27-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="bcb27-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="bcb27-111">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="bcb27-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="bcb27-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bcb27-112">PARAMETERS</span></span>

### <span data-ttu-id="bcb27-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcb27-113">-Name</span></span>
<span data-ttu-id="bcb27-114">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="bcb27-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb27-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bcb27-115">-PassThru</span></span>
<span data-ttu-id="bcb27-116">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bcb27-116">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb27-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcb27-117">-ResourceGroupName</span></span>
<span data-ttu-id="bcb27-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bcb27-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bcb27-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bcb27-119">-Confirm</span></span>
<span data-ttu-id="bcb27-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bcb27-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb27-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bcb27-121">-WhatIf</span></span>
<span data-ttu-id="bcb27-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcb27-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bcb27-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bcb27-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb27-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcb27-124">-DefaultProfile</span></span>
<span data-ttu-id="bcb27-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bcb27-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bcb27-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcb27-126">CommonParameters</span></span>
<span data-ttu-id="bcb27-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcb27-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bcb27-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcb27-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcb27-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bcb27-129">INPUTS</span></span>

### <span data-ttu-id="bcb27-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bcb27-130">System.String</span></span>

## <span data-ttu-id="bcb27-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bcb27-131">OUTPUTS</span></span>

### <span data-ttu-id="bcb27-132">System. Object</span><span class="sxs-lookup"><span data-stu-id="bcb27-132">System.Object</span></span>

## <span data-ttu-id="bcb27-133">Note</span><span class="sxs-lookup"><span data-stu-id="bcb27-133">NOTES</span></span>
<span data-ttu-id="bcb27-134">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="bcb27-134">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="bcb27-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bcb27-135">RELATED LINKS</span></span>

[<span data-ttu-id="bcb27-136">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcb27-136">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bcb27-137">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="bcb27-137">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="bcb27-138">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcb27-138">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcb27-139">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="bcb27-139">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="bcb27-140">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcb27-140">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcb27-141">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcb27-141">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcb27-142">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="bcb27-142">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="bcb27-143">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="bcb27-143">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="bcb27-144">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="bcb27-144">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="bcb27-145">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="bcb27-145">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="bcb27-146">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="bcb27-146">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="bcb27-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="bcb27-147">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
