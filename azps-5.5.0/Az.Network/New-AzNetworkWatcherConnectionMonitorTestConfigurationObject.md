---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100202759"
---
# <span data-ttu-id="495f6-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="495f6-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="495f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="495f6-102">SYNOPSIS</span></span>
<span data-ttu-id="495f6-103">Creare una configurazione di test del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="495f6-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="495f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="495f6-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="495f6-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="495f6-105">DESCRIPTION</span></span>
<span data-ttu-id="495f6-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorTestConfigurationObject crea una configurazione di test di Monitor connessione.</span><span class="sxs-lookup"><span data-stu-id="495f6-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="495f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="495f6-107">EXAMPLES</span></span>

### <span data-ttu-id="495f6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="495f6-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="495f6-109">Nome: httpTC TestFrequencySec : 120 PreferredIPVersion : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="495f6-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="495f6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="495f6-110">PARAMETERS</span></span>

### <span data-ttu-id="495f6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="495f6-111">-DefaultProfile</span></span>
<span data-ttu-id="495f6-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="495f6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="495f6-113">-Name</span><span class="sxs-lookup"><span data-stu-id="495f6-113">-Name</span></span>
<span data-ttu-id="495f6-114">Nome della configurazione di test del monitor di connessione.</span><span class="sxs-lookup"><span data-stu-id="495f6-114">The name of the connection monitor test configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="495f6-115">-PreferredIPVersion</span></span>
<span data-ttu-id="495f6-116">La versione IP preferita da usare nella valutazione di test.</span><span class="sxs-lookup"><span data-stu-id="495f6-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="495f6-117">Il monitor di connessione può scegliere di usare una versione diversa a seconda di altri parametri.</span><span class="sxs-lookup"><span data-stu-id="495f6-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="495f6-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="495f6-119">I parametri usati per eseguire la valutazione dei test su un protocollo.</span><span class="sxs-lookup"><span data-stu-id="495f6-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="495f6-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="495f6-121">La percentuale massima di controlli non riusciti consentita perché un test sia valutato correttamente.</span><span class="sxs-lookup"><span data-stu-id="495f6-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="495f6-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="495f6-123">Il tempo massimo di round trip in millisecondi consentito per valutare l'esito positivo di un test.</span><span class="sxs-lookup"><span data-stu-id="495f6-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="495f6-124">-TestFrequencySec</span></span>
<span data-ttu-id="495f6-125">La frequenza del test di valutazione, in secondi.</span><span class="sxs-lookup"><span data-stu-id="495f6-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="495f6-126">-Confirm</span></span>
<span data-ttu-id="495f6-127">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="495f6-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="495f6-128">-WhatIf</span></span>
<span data-ttu-id="495f6-129">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="495f6-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="495f6-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="495f6-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="495f6-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="495f6-131">CommonParameters</span></span>
<span data-ttu-id="495f6-132">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="495f6-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="495f6-133">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="495f6-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="495f6-134">INPUT</span><span class="sxs-lookup"><span data-stu-id="495f6-134">INPUTS</span></span>

### <span data-ttu-id="495f6-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="495f6-135">None</span></span>

## <span data-ttu-id="495f6-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="495f6-136">OUTPUTS</span></span>

### <span data-ttu-id="495f6-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="495f6-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="495f6-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="495f6-138">NOTES</span></span>

## <span data-ttu-id="495f6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="495f6-139">RELATED LINKS</span></span>
