---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
ms.openlocfilehash: c5a681f8be210e76ecbf3bc965e7e9e9c108a94a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865911"
---
# <span data-ttu-id="7f24f-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="7f24f-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="7f24f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f24f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f24f-103">Elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="7f24f-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f24f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f24f-104">SYNTAX</span></span>

### <span data-ttu-id="7f24f-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7f24f-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f24f-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="7f24f-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7f24f-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="7f24f-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7f24f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f24f-108">DESCRIPTION</span></span>
<span data-ttu-id="7f24f-109">La Get-AzureRmNetworkWatcherReachabilityProvidersList elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="7f24f-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="7f24f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f24f-110">EXAMPLES</span></span>

### <span data-ttu-id="7f24f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7f24f-111">Example 1</span></span>
```
PS C:\> $nw = Get-AzureRmNetworkWatcher -Name NetworkWatcher -ResourceGroupName NetworkWatcherRG
PS C:\> Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher $nw -Location "West US" -Country "United States" -State "washington" -City "seattle"

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

<span data-ttu-id="7f24f-112">Elenca tutti i provider disponibili in Seattle, WA per Azure Data Center in West US.</span><span class="sxs-lookup"><span data-stu-id="7f24f-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="7f24f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f24f-113">PARAMETERS</span></span>

### <span data-ttu-id="7f24f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7f24f-114">-AsJob</span></span>
<span data-ttu-id="7f24f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="7f24f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7f24f-116">-Città</span><span class="sxs-lookup"><span data-stu-id="7f24f-116">-City</span></span>
<span data-ttu-id="7f24f-117">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="7f24f-117">The name of the city.</span></span>

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

### <span data-ttu-id="7f24f-118">-Paese</span><span class="sxs-lookup"><span data-stu-id="7f24f-118">-Country</span></span>
<span data-ttu-id="7f24f-119">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="7f24f-119">The name of the country.</span></span>

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

### <span data-ttu-id="7f24f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f24f-120">-DefaultProfile</span></span>
<span data-ttu-id="7f24f-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f24f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f24f-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="7f24f-122">-Location</span></span>
<span data-ttu-id="7f24f-123">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="7f24f-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="7f24f-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f24f-124">-NetworkWatcher</span></span>
<span data-ttu-id="7f24f-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7f24f-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="7f24f-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="7f24f-126">-NetworkWatcherName</span></span>
<span data-ttu-id="7f24f-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7f24f-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="7f24f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f24f-128">-ResourceGroupName</span></span>
<span data-ttu-id="7f24f-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="7f24f-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="7f24f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7f24f-130">-ResourceId</span></span>
<span data-ttu-id="7f24f-131">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="7f24f-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="7f24f-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="7f24f-132">-State</span></span>
<span data-ttu-id="7f24f-133">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="7f24f-133">The name of the state.</span></span>

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

### <span data-ttu-id="7f24f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f24f-134">CommonParameters</span></span>
<span data-ttu-id="7f24f-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f24f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f24f-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f24f-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f24f-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f24f-137">INPUTS</span></span>

### <span data-ttu-id="7f24f-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f24f-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="7f24f-139">System. String System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7f24f-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="7f24f-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f24f-140">OUTPUTS</span></span>

### <span data-ttu-id="7f24f-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="7f24f-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="7f24f-142">Note</span><span class="sxs-lookup"><span data-stu-id="7f24f-142">NOTES</span></span>
<span data-ttu-id="7f24f-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="7f24f-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="7f24f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f24f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7f24f-145">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f24f-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f24f-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f24f-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f24f-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="7f24f-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="7f24f-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="7f24f-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="7f24f-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="7f24f-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="7f24f-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="7f24f-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="7f24f-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="7f24f-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="7f24f-152">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f24f-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f24f-153">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="7f24f-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="7f24f-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f24f-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f24f-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f24f-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="7f24f-156">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="7f24f-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
