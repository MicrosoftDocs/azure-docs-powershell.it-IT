---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 805c8d31b075a39fa8ccc407024aa5a32a91fdb6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860718"
---
# <span data-ttu-id="d592f-101">Get-AzNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="d592f-101">Get-AzNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="d592f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d592f-102">SYNOPSIS</span></span>
<span data-ttu-id="d592f-103">Elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="d592f-103">Lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d592f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d592f-104">SYNTAX</span></span>

### <span data-ttu-id="d592f-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d592f-105">SetByName (Default)</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d592f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="d592f-106">SetByResource</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d592f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="d592f-107">SetByResourceId</span></span>
```
Get-AzNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d592f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d592f-108">DESCRIPTION</span></span>
<span data-ttu-id="d592f-109">La Get-AzNetworkWatcherReachabilityProvidersList elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="d592f-109">The Get-AzNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="d592f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d592f-110">EXAMPLES</span></span>

### <span data-ttu-id="d592f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d592f-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

"countries" : [
    {
        "countryName" : "United States",
        "states" : [
            {
                "stateName" : "washington",
                "cities" : [
                    {
                        "cityName" : "seattle",
                        "providers" : [
                            "Comcast Cable Communications, Inc. - ASN 7922",
                            "Comcast Cable Communications, LLC - ASN 7922",
                            "Level 3 Communications, Inc. (GBLX) - ASN 3549",
                            "Qwest Communications Company, LLC - ASN 209"
                        ]
                    }
                ]
            }
        ]
    }
]
```

<span data-ttu-id="d592f-112">Elenca tutti i provider disponibili in Seattle, WA per Azure Data Center in West US.</span><span class="sxs-lookup"><span data-stu-id="d592f-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="d592f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d592f-113">PARAMETERS</span></span>

### <span data-ttu-id="d592f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d592f-114">-AsJob</span></span>
<span data-ttu-id="d592f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d592f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d592f-116">-Città</span><span class="sxs-lookup"><span data-stu-id="d592f-116">-City</span></span>
<span data-ttu-id="d592f-117">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="d592f-117">The name of the city.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-118">-Paese</span><span class="sxs-lookup"><span data-stu-id="d592f-118">-Country</span></span>
<span data-ttu-id="d592f-119">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="d592f-119">The name of the country.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d592f-120">-DefaultProfile</span></span>
<span data-ttu-id="d592f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d592f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d592f-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="d592f-122">-Location</span></span>
<span data-ttu-id="d592f-123">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="d592f-123">Optional Azure regions to scope the query to.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d592f-124">-NetworkWatcher</span></span>
<span data-ttu-id="d592f-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="d592f-125">The network watcher resource.</span></span>

```yaml
Type: PSNetworkWatcher
Parameter Sets: SetByResource
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="d592f-126">-NetworkWatcherName</span></span>
<span data-ttu-id="d592f-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d592f-127">The name of network watcher.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: ResourceName, Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d592f-128">-ResourceGroupName</span></span>
<span data-ttu-id="d592f-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="d592f-129">The name of the network watcher resource group.</span></span>

```yaml
Type: String
Parameter Sets: SetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d592f-130">-ResourceId</span></span>
<span data-ttu-id="d592f-131">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="d592f-131">The Id of network watcher resource.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="d592f-132">-State</span></span>
<span data-ttu-id="d592f-133">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="d592f-133">The name of the state.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d592f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d592f-134">CommonParameters</span></span>
<span data-ttu-id="d592f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d592f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d592f-136">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d592f-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d592f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d592f-137">INPUTS</span></span>

### <span data-ttu-id="d592f-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d592f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="d592f-139">System. String System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d592f-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d592f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d592f-140">OUTPUTS</span></span>

### <span data-ttu-id="d592f-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="d592f-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="d592f-142">Note</span><span class="sxs-lookup"><span data-stu-id="d592f-142">NOTES</span></span>
<span data-ttu-id="d592f-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="d592f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="d592f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d592f-144">RELATED LINKS</span></span>

[<span data-ttu-id="d592f-145">New-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d592f-145">New-AzNetworkWatcher</span></span>](./New-AzNetworkWatcher.md)

[<span data-ttu-id="d592f-146">Get-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d592f-146">Get-AzNetworkWatcher</span></span>](./Get-AzNetworkWatcher.md)

[<span data-ttu-id="d592f-147">Remove-AzNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="d592f-147">Remove-AzNetworkWatcher</span></span>](./Remove-AzNetworkWatcher.md)

[<span data-ttu-id="d592f-148">Test-AzNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="d592f-148">Test-AzNetworkWatcherIPFlow</span></span>](./Test-AzNetworkWatcherIPFlow.md)

[<span data-ttu-id="d592f-149">Get-AzNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="d592f-149">Get-AzNetworkWatcherSecurityGroupView</span></span>](./Get-AzNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="d592f-150">Get-AzNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="d592f-150">Get-AzNetworkWatcherTopology</span></span>](./Get-AzNetworkWatcherTopology.md)

[<span data-ttu-id="d592f-151">Start-AzNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="d592f-151">Start-AzNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="d592f-152">New-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d592f-152">New-AzNetworkWatcherPacketCapture</span></span>](./New-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d592f-153">New-AzPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="d592f-153">New-AzPacketCaptureFilterConfig</span></span>](./New-AzPacketCaptureFilterConfig.md)

[<span data-ttu-id="d592f-154">Get-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d592f-154">Get-AzNetworkWatcherPacketCapture</span></span>](./Get-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d592f-155">Remove-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d592f-155">Remove-AzNetworkWatcherPacketCapture</span></span>](./Remove-AzNetworkWatcherPacketCapture.md)

[<span data-ttu-id="d592f-156">Stop-AzNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="d592f-156">Stop-AzNetworkWatcherPacketCapture</span></span>](./Stop-AzNetworkWatcherPacketCapture.md)
