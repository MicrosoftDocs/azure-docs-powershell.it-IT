---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-aznetworkwatcher
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzNetworkWatcher.md
ms.openlocfilehash: 276cd57a51b6b457f2f4d205932cdbfabd7613b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862953"
---
# <span data-ttu-id="344a9-101">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="344a9-101">Remove-AzNetworkWatcher</span></span>

## <span data-ttu-id="344a9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="344a9-102">SYNOPSIS</span></span>
<span data-ttu-id="344a9-103">Rimuove un Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="344a9-103">Removes a Network Watcher.</span></span>

## <span data-ttu-id="344a9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="344a9-104">SYNTAX</span></span>

```
Remove-AzNetworkWatcher -Name <String> -ResourceGroupName <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="344a9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="344a9-105">DESCRIPTION</span></span>
<span data-ttu-id="344a9-106">Il cmdlet Remove-AzNetworkWatcher consente di rimuovere una risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="344a9-106">The Remove-AzNetworkWatcher cmdlet removes a Network Watcher resource.</span></span>

## <span data-ttu-id="344a9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="344a9-107">EXAMPLES</span></span>

### <span data-ttu-id="344a9-108">--------------------------Esempio 1: creare ed eliminare un Watcher di rete--------------------------</span><span class="sxs-lookup"><span data-stu-id="344a9-108">--------------------------  Example 1: Create and delete a Network Watcher  --------------------------</span></span>
```
New-AzResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG -Location westcentralus
Remove-AzNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG
```

<span data-ttu-id="344a9-109">Questo esempio crea un Watcher di rete in un gruppo di risorse e quindi lo elimina immediatamente.</span><span class="sxs-lookup"><span data-stu-id="344a9-109">This example creates a Network Watcher in a resource group and then immediately deletes it.</span></span> <span data-ttu-id="344a9-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="344a9-110">Note that only one Network Watcher can be created per region per subscription.</span></span>
<span data-ttu-id="344a9-111">Per eliminare la richiesta quando si elimina la rete virtuale, usare il contrassegno-forza.</span><span class="sxs-lookup"><span data-stu-id="344a9-111">To suppress the prompt when deleting the virtual network, use the -Force flag.</span></span>

## <span data-ttu-id="344a9-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="344a9-112">PARAMETERS</span></span>

### <span data-ttu-id="344a9-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="344a9-113">-AsJob</span></span>
<span data-ttu-id="344a9-114">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="344a9-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="344a9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344a9-115">-DefaultProfile</span></span>
<span data-ttu-id="344a9-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="344a9-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="344a9-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="344a9-117">-Name</span></span>
<span data-ttu-id="344a9-118">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="344a9-118">The resource name.</span></span>

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

### <span data-ttu-id="344a9-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="344a9-119">-PassThru</span></span>
<span data-ttu-id="344a9-120">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="344a9-120">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="344a9-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="344a9-121">-ResourceGroupName</span></span>
<span data-ttu-id="344a9-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="344a9-122">The resource group name.</span></span>

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

### <span data-ttu-id="344a9-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="344a9-123">-Confirm</span></span>
<span data-ttu-id="344a9-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="344a9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="344a9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344a9-125">-WhatIf</span></span>
<span data-ttu-id="344a9-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="344a9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344a9-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="344a9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="344a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344a9-128">CommonParameters</span></span>
<span data-ttu-id="344a9-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="344a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344a9-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="344a9-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344a9-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="344a9-131">INPUTS</span></span>

### <span data-ttu-id="344a9-132">System. String</span><span class="sxs-lookup"><span data-stu-id="344a9-132">System.String</span></span>

## <span data-ttu-id="344a9-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="344a9-133">OUTPUTS</span></span>

### <span data-ttu-id="344a9-134">System. Object</span><span class="sxs-lookup"><span data-stu-id="344a9-134">System.Object</span></span>

## <span data-ttu-id="344a9-135">Note</span><span class="sxs-lookup"><span data-stu-id="344a9-135">NOTES</span></span>
<span data-ttu-id="344a9-136">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="344a9-136">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="344a9-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="344a9-137">RELATED LINKS</span></span>

[<span data-ttu-id="344a9-138">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="344a9-138">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="344a9-139">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="344a9-139">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="344a9-140">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="344a9-140">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="344a9-141">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="344a9-141">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="344a9-142">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="344a9-142">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="344a9-143">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="344a9-143">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="344a9-144">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="344a9-144">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="344a9-145">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="344a9-145">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="344a9-146">Get-AzNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="344a9-146">Get-AzNetworkWatcherNextHop</span></span>](./Get-AzNetworkWatcherNextHop.md)

[<span data-ttu-id="344a9-147">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="344a9-147">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="344a9-148">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="344a9-148">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="344a9-149">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="344a9-149">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)
