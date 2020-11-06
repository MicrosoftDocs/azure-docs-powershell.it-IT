---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmNetworkWatcher.md
ms.openlocfilehash: 10cc869bf6e0ac194ce5e2e77c69885a8e0a0d25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513283"
---
# <span data-ttu-id="0ee12-101">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ee12-101">New-AzureRmNetworkWatcher</span></span>

## <span data-ttu-id="0ee12-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ee12-102">SYNOPSIS</span></span>
<span data-ttu-id="0ee12-103">Crea una nuova risorsa di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="0ee12-103">Creates a new Network Watcher resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ee12-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ee12-104">SYNTAX</span></span>

```
New-AzureRmNetworkWatcher -Name <String> -ResourceGroupName <String> -Location <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ee12-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ee12-105">DESCRIPTION</span></span>
<span data-ttu-id="0ee12-106">Il cmdlet New-AzureRmNetworkWatcher crea una nuova risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="0ee12-106">The New-AzureRmNetworkWatcher cmdlet creates a new Network Watcher resource.</span></span>

## <span data-ttu-id="0ee12-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ee12-107">EXAMPLES</span></span>

### <span data-ttu-id="0ee12-108">Esempio 1: creare un Watcher di rete</span><span class="sxs-lookup"><span data-stu-id="0ee12-108">Example 1: Create a Network Watcher</span></span>
```
New-AzureRmResourceGroup -Name NetworkWatcherRG -Location westcentralus
New-AzureRmNetworkWatcher -Name NetworkWatcher_westcentralus -ResourceGroup NetworkWatcherRG

Name              : NetworkWatcher_westcentralus
Id                : /subscriptions/bbbbbbbb-bbbb-bbbb-bbbb-bbbbbbbbbbbb/resourceGroups/NetworkWatcherRG/providers/Microsoft.Network/networkWatchers/NetworkWatcher_westcentralus
Etag              : W/"7cf1f2fe-8445-4aa7-9bf5-c15347282c39"
Location          : westcentralus
Tags              :
ProvisioningState : Succeeded
```

<span data-ttu-id="0ee12-109">Questo esempio crea un nuovo Watcher di rete all'interno di un gruppo di risorse appena creato.</span><span class="sxs-lookup"><span data-stu-id="0ee12-109">This example creates a new Network Watcher inside a newly created Resource Group.</span></span> <span data-ttu-id="0ee12-110">Tieni presente che è possibile creare un solo Watcher di rete per ogni area di abbonamento.</span><span class="sxs-lookup"><span data-stu-id="0ee12-110">Note that only one Network Watcher can be created per region per subscription.</span></span>

## <span data-ttu-id="0ee12-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ee12-111">PARAMETERS</span></span>

### <span data-ttu-id="0ee12-112">-Posizione</span><span class="sxs-lookup"><span data-stu-id="0ee12-112">-Location</span></span>
<span data-ttu-id="0ee12-113">Posizione.</span><span class="sxs-lookup"><span data-stu-id="0ee12-113">Location.</span></span>

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

### <span data-ttu-id="0ee12-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ee12-114">-Name</span></span>
<span data-ttu-id="0ee12-115">Nome del Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="0ee12-115">The network watcher name.</span></span>

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

### <span data-ttu-id="0ee12-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ee12-116">-ResourceGroupName</span></span>
<span data-ttu-id="0ee12-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0ee12-117">The resource group name.</span></span>

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

### <span data-ttu-id="0ee12-118">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ee12-118">-Tag</span></span>
<span data-ttu-id="0ee12-119">Coppie chiave-valore in forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="0ee12-119">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="0ee12-120">Per esempio:</span><span class="sxs-lookup"><span data-stu-id="0ee12-120">For example:</span></span>

<span data-ttu-id="0ee12-121">@ {Key0 = "value0"; Key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="0ee12-121">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ee12-122">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0ee12-122">-Confirm</span></span>
<span data-ttu-id="0ee12-123">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ee12-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ee12-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ee12-124">-WhatIf</span></span>
<span data-ttu-id="0ee12-125">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ee12-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ee12-126">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0ee12-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ee12-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ee12-127">-DefaultProfile</span></span>
<span data-ttu-id="0ee12-128">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ee12-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ee12-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ee12-129">CommonParameters</span></span>
<span data-ttu-id="0ee12-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ee12-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ee12-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ee12-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ee12-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ee12-132">INPUTS</span></span>

### <span data-ttu-id="0ee12-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ee12-133">System.String</span></span>
<span data-ttu-id="0ee12-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ee12-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ee12-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ee12-135">OUTPUTS</span></span>

### <span data-ttu-id="0ee12-136">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ee12-136">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>

## <span data-ttu-id="0ee12-137">Note</span><span class="sxs-lookup"><span data-stu-id="0ee12-137">NOTES</span></span>
<span data-ttu-id="0ee12-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher</span><span class="sxs-lookup"><span data-stu-id="0ee12-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher</span></span>

## <span data-ttu-id="0ee12-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ee12-139">RELATED LINKS</span></span>

[<span data-ttu-id="0ee12-140">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ee12-140">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0ee12-141">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="0ee12-141">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="0ee12-142">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ee12-142">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ee12-143">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="0ee12-143">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="0ee12-144">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ee12-144">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ee12-145">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ee12-145">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ee12-146">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="0ee12-146">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="0ee12-147">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="0ee12-147">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="0ee12-148">Get-AzureRmNetworkWatcherNextHop</span><span class="sxs-lookup"><span data-stu-id="0ee12-148">Get-AzureRmNetworkWatcherNextHop</span></span>](./Get-AzureRmNetworkWatcherNextHop.md)

[<span data-ttu-id="0ee12-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="0ee12-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="0ee12-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="0ee12-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="0ee12-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="0ee12-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)
