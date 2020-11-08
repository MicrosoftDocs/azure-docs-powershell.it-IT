---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190948"
---
# <span data-ttu-id="28541-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="28541-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="28541-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28541-102">SYNOPSIS</span></span>
<span data-ttu-id="28541-103">Creare una configurazione di test per il monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="28541-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="28541-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28541-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28541-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28541-105">DESCRIPTION</span></span>
<span data-ttu-id="28541-106">Il cmdlet New-AzNetworkWatcherConnectionMonitorTestConfigurationObject crea una configurazione di test per il monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="28541-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="28541-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28541-107">EXAMPLES</span></span>

### <span data-ttu-id="28541-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="28541-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="28541-109">Nome: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443, "Method": "GET", "RequestHeaders": [{"Name": "Allow", "value": "GET"}], "ValidStatusCodeRanges": ["2xx", "300-308"], "PreferHTTPS": true} SuccessThreshold: {"ChecksFailedPercent": 20, "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="28541-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="28541-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28541-110">PARAMETERS</span></span>

### <span data-ttu-id="28541-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28541-111">-DefaultProfile</span></span>
<span data-ttu-id="28541-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="28541-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28541-113">-Nome</span><span class="sxs-lookup"><span data-stu-id="28541-113">-Name</span></span>
<span data-ttu-id="28541-114">Nome della configurazione del test di monitoraggio della connessione.</span><span class="sxs-lookup"><span data-stu-id="28541-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="28541-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="28541-115">-PreferredIPVersion</span></span>
<span data-ttu-id="28541-116">La versione IP preferita da usare nella valutazione dei test.</span><span class="sxs-lookup"><span data-stu-id="28541-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="28541-117">Il monitor di connessione può scegliere di usare una versione diversa a seconda di altri parametri.</span><span class="sxs-lookup"><span data-stu-id="28541-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="28541-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="28541-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="28541-119">Parametri usati per eseguire la valutazione del test su alcuni protocolli.</span><span class="sxs-lookup"><span data-stu-id="28541-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="28541-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="28541-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="28541-121">La percentuale massima di controlli non riusciti consentiti per un test da valutare come riuscito.</span><span class="sxs-lookup"><span data-stu-id="28541-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="28541-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="28541-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="28541-123">Il tempo massimo di andata e ritorno in millisecondi consentito per un test da valutare come riuscito.</span><span class="sxs-lookup"><span data-stu-id="28541-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="28541-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="28541-124">-TestFrequencySec</span></span>
<span data-ttu-id="28541-125">Frequenza della valutazione del test, in secondi.</span><span class="sxs-lookup"><span data-stu-id="28541-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="28541-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="28541-126">-Confirm</span></span>
<span data-ttu-id="28541-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28541-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28541-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28541-128">-WhatIf</span></span>
<span data-ttu-id="28541-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28541-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28541-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="28541-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28541-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28541-131">CommonParameters</span></span>
<span data-ttu-id="28541-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28541-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28541-133">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="28541-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28541-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28541-134">INPUTS</span></span>

### <span data-ttu-id="28541-135">Nessuno</span><span class="sxs-lookup"><span data-stu-id="28541-135">None</span></span>

## <span data-ttu-id="28541-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28541-136">OUTPUTS</span></span>

### <span data-ttu-id="28541-137">Microsoft. Azure. Commands. Network. Models. PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="28541-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="28541-138">Note</span><span class="sxs-lookup"><span data-stu-id="28541-138">NOTES</span></span>

## <span data-ttu-id="28541-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28541-139">RELATED LINKS</span></span>