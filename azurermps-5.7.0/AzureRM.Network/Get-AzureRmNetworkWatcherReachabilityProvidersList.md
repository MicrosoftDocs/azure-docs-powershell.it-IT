---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermnetworkwatcherreachabilityproviderslist
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmNetworkWatcherReachabilityProvidersList.md
ms.openlocfilehash: 093a847154c75ee7c640bda522ebf16baa04560a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688447"
---
# <span data-ttu-id="f6ddb-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span><span class="sxs-lookup"><span data-stu-id="f6ddb-101">Get-AzureRmNetworkWatcherReachabilityProvidersList</span></span>

## <span data-ttu-id="f6ddb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f6ddb-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ddb-103">Elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-103">Lists all available internet service providers for a specified Azure region.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6ddb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f6ddb-104">SYNTAX</span></span>

### <span data-ttu-id="f6ddb-105">SetByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f6ddb-105">SetByName (Default)</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcherName <String> -ResourceGroupName <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ddb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="f6ddb-106">SetByResource</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -NetworkWatcher <PSNetworkWatcher>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6ddb-107">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ddb-107">SetByResourceId</span></span>
```
Get-AzureRmNetworkWatcherReachabilityProvidersList -ResourceId <String>
 [-Location <System.Collections.Generic.List`1[System.String]>] [-Country <String>] [-State <String>]
 [-City <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ddb-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f6ddb-108">DESCRIPTION</span></span>
<span data-ttu-id="f6ddb-109">La Get-AzureRmNetworkWatcherReachabilityProvidersList elenca tutti i provider di servizi Internet disponibili per un'area di Azure specificata.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-109">The Get-AzureRmNetworkWatcherReachabilityProvidersList lists all available internet service providers for a specified Azure region.</span></span>

## <span data-ttu-id="f6ddb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f6ddb-110">EXAMPLES</span></span>

### <span data-ttu-id="f6ddb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f6ddb-111">Example 1</span></span>
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

<span data-ttu-id="f6ddb-112">Elenca tutti i provider disponibili in Seattle, WA per Azure Data Center in West US.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-112">Lists all available providers in Seattle, WA for Azure Data Center in West US.</span></span>

## <span data-ttu-id="f6ddb-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f6ddb-113">PARAMETERS</span></span>

### <span data-ttu-id="f6ddb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6ddb-114">-AsJob</span></span>
<span data-ttu-id="f6ddb-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f6ddb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6ddb-116">-Città</span><span class="sxs-lookup"><span data-stu-id="f6ddb-116">-City</span></span>
<span data-ttu-id="f6ddb-117">Nome della città.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-117">The name of the city.</span></span>

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

### <span data-ttu-id="f6ddb-118">-Paese</span><span class="sxs-lookup"><span data-stu-id="f6ddb-118">-Country</span></span>
<span data-ttu-id="f6ddb-119">Nome del paese.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-119">The name of the country.</span></span>

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

### <span data-ttu-id="f6ddb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ddb-120">-DefaultProfile</span></span>
<span data-ttu-id="f6ddb-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f6ddb-122">-Posizione</span><span class="sxs-lookup"><span data-stu-id="f6ddb-122">-Location</span></span>
<span data-ttu-id="f6ddb-123">Aree di Azure facoltative per l'ambito della query.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-123">Optional Azure regions to scope the query to.</span></span>

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

### <span data-ttu-id="f6ddb-124">-NetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ddb-124">-NetworkWatcher</span></span>
<span data-ttu-id="f6ddb-125">Risorsa Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-125">The network watcher resource.</span></span>

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

### <span data-ttu-id="f6ddb-126">-NetworkWatcherName</span><span class="sxs-lookup"><span data-stu-id="f6ddb-126">-NetworkWatcherName</span></span>
<span data-ttu-id="f6ddb-127">Nome di Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-127">The name of network watcher.</span></span>

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

### <span data-ttu-id="f6ddb-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ddb-128">-ResourceGroupName</span></span>
<span data-ttu-id="f6ddb-129">Nome del gruppo di risorse di Watcher di rete.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-129">The name of the network watcher resource group.</span></span>

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

### <span data-ttu-id="f6ddb-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6ddb-130">-ResourceId</span></span>
<span data-ttu-id="f6ddb-131">ID della risorsa Network Watcher.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-131">The Id of network watcher resource.</span></span>

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

### <span data-ttu-id="f6ddb-132">-Stato</span><span class="sxs-lookup"><span data-stu-id="f6ddb-132">-State</span></span>
<span data-ttu-id="f6ddb-133">Nome dello stato.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-133">The name of the state.</span></span>

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

### <span data-ttu-id="f6ddb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ddb-134">CommonParameters</span></span>
<span data-ttu-id="f6ddb-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ddb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ddb-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ddb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ddb-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f6ddb-137">INPUTS</span></span>

### <span data-ttu-id="f6ddb-138">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ddb-138">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcher</span></span>
<span data-ttu-id="f6ddb-139">System. String System. Collections. Generic. list ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f6ddb-139">System.String System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f6ddb-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f6ddb-140">OUTPUTS</span></span>

### <span data-ttu-id="f6ddb-141">Microsoft. Azure. Commands. Network. Models. PSAvailableProvidersList</span><span class="sxs-lookup"><span data-stu-id="f6ddb-141">Microsoft.Azure.Commands.Network.Models.PSAvailableProvidersList</span></span>

## <span data-ttu-id="f6ddb-142">Note</span><span class="sxs-lookup"><span data-stu-id="f6ddb-142">NOTES</span></span>
<span data-ttu-id="f6ddb-143">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking, Network Watcher, Next, hop</span><span class="sxs-lookup"><span data-stu-id="f6ddb-143">Keywords: azure, azurerm, arm, resource, management, manager, network, networking, network watcher, next, hop</span></span> 

## <span data-ttu-id="f6ddb-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f6ddb-144">RELATED LINKS</span></span>

[<span data-ttu-id="f6ddb-145">New-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ddb-145">New-AzureRmNetworkWatcher</span></span>](./New-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f6ddb-146">Get-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ddb-146">Get-AzureRmNetworkWatcher</span></span>](./Get-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f6ddb-147">Remove-AzureRmNetworkWatcher</span><span class="sxs-lookup"><span data-stu-id="f6ddb-147">Remove-AzureRmNetworkWatcher</span></span>](./Remove-AzureRmNetworkWatcher.md)

[<span data-ttu-id="f6ddb-148">Test-AzureRmNetworkWatcherIPFlow</span><span class="sxs-lookup"><span data-stu-id="f6ddb-148">Test-AzureRmNetworkWatcherIPFlow</span></span>](./Test-AzureRmNetworkWatcherIPFlow.md)

[<span data-ttu-id="f6ddb-149">Get-AzureRmNetworkWatcherSecurityGroupView</span><span class="sxs-lookup"><span data-stu-id="f6ddb-149">Get-AzureRmNetworkWatcherSecurityGroupView</span></span>](./Get-AzureRmNetworkWatcherSecurityGroupView.md)

[<span data-ttu-id="f6ddb-150">Get-AzureRmNetworkWatcherTopology</span><span class="sxs-lookup"><span data-stu-id="f6ddb-150">Get-AzureRmNetworkWatcherTopology</span></span>](./Get-AzureRmNetworkWatcherTopology.md)

[<span data-ttu-id="f6ddb-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span><span class="sxs-lookup"><span data-stu-id="f6ddb-151">Start-AzureRmNetworkWatcherResourceTroubleshooting</span></span>](./Start-AzureRmNetworkWatcherResourceTroubleshooting.md)

[<span data-ttu-id="f6ddb-152">New-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ddb-152">New-AzureRmNetworkWatcherPacketCapture</span></span>](./New-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ddb-153">New-AzureRmPacketCaptureFilterConfig</span><span class="sxs-lookup"><span data-stu-id="f6ddb-153">New-AzureRmPacketCaptureFilterConfig</span></span>](./New-AzureRmPacketCaptureFilterConfig.md)

[<span data-ttu-id="f6ddb-154">Get-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ddb-154">Get-AzureRmNetworkWatcherPacketCapture</span></span>](./Get-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ddb-155">Remove-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ddb-155">Remove-AzureRmNetworkWatcherPacketCapture</span></span>](./Remove-AzureRmNetworkWatcherPacketCapture.md)

[<span data-ttu-id="f6ddb-156">Stop-AzureRmNetworkWatcherPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f6ddb-156">Stop-AzureRmNetworkWatcherPacketCapture</span></span>](./Stop-AzureRmNetworkWatcherPacketCapture.md)
