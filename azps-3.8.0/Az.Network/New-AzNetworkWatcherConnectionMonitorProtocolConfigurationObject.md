---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94018976"
---
# <span data-ttu-id="6a9e0-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="6a9e0-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="6a9e0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a9e0-102">SYNOPSIS</span></span>
<span data-ttu-id="6a9e0-103">Creare la configurazione del protocollo usata per eseguire la valutazione del test su TCP, HTTP o ICMP.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="6a9e0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a9e0-104">SYNTAX</span></span>

### <span data-ttu-id="6a9e0-105">TCP</span><span class="sxs-lookup"><span data-stu-id="6a9e0-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9e0-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="6a9e0-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6a9e0-107">PACCHETTI ICMP</span><span class="sxs-lookup"><span data-stu-id="6a9e0-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6a9e0-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a9e0-108">DESCRIPTION</span></span>
<span data-ttu-id="6a9e0-109">Il cmdlet New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject crea la configurazione del protocollo usata per eseguire la valutazione del test su TCP, HTTP o ICMP.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="6a9e0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a9e0-110">EXAMPLES</span></span>

### <span data-ttu-id="6a9e0-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="6a9e0-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="6a9e0-112">Porta: 80 DisableTraceRoute: false</span><span class="sxs-lookup"><span data-stu-id="6a9e0-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="6a9e0-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a9e0-113">PARAMETERS</span></span>

### <span data-ttu-id="6a9e0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a9e0-114">-DefaultProfile</span></span>
<span data-ttu-id="6a9e0-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6a9e0-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="6a9e0-116">-DisableTraceRoute</span></span>
<span data-ttu-id="6a9e0-117">Valore che indica se la valutazione del percorso con la route di traccia deve essere disabilitata.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="6a9e0-118">-HttpProtocol</span></span>
<span data-ttu-id="6a9e0-119">Opzione protocollo HTTP</span><span class="sxs-lookup"><span data-stu-id="6a9e0-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="6a9e0-120">-IcmpProtocol</span></span>
<span data-ttu-id="6a9e0-121">Switch protocollo ICMP.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-122">-Method</span><span class="sxs-lookup"><span data-stu-id="6a9e0-122">-Method</span></span>
<span data-ttu-id="6a9e0-123">Metodo HTTP da usare.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-124">-Path</span><span class="sxs-lookup"><span data-stu-id="6a9e0-124">-Path</span></span>
<span data-ttu-id="6a9e0-125">Il componente Path dell'URI.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-125">The path component of the URI.</span></span> <span data-ttu-id="6a9e0-126">Ad esempio, \" /dir1/dir2 \" .</span><span class="sxs-lookup"><span data-stu-id="6a9e0-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-127">-Porta</span><span class="sxs-lookup"><span data-stu-id="6a9e0-127">-Port</span></span>
<span data-ttu-id="6a9e0-128">La porta a cui connettersi.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="6a9e0-129">-PreferHTTPS</span></span>
<span data-ttu-id="6a9e0-130">Valore che indica se HTTPS è preferibile rispetto a HTTP nei casi in cui la scelta non è esplicita.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="6a9e0-131">-RequestHeader</span></span>
<span data-ttu-id="6a9e0-132">Intestazioni HTTP da trasmettere con la richiesta.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="6a9e0-133">-TcpProtocol</span></span>
<span data-ttu-id="6a9e0-134">Opzione protocollo TCP.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="6a9e0-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="6a9e0-136">Codici di stato HTTP per valutare l'esito positivo.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="6a9e0-137">Ad esempio, \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="6a9e0-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a9e0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a9e0-138">CommonParameters</span></span>
<span data-ttu-id="6a9e0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a9e0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a9e0-140">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a9e0-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a9e0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a9e0-141">INPUTS</span></span>

### <span data-ttu-id="6a9e0-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="6a9e0-142">None</span></span>

## <span data-ttu-id="6a9e0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a9e0-143">OUTPUTS</span></span>

### <span data-ttu-id="6a9e0-144">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a9e0-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="6a9e0-145">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a9e0-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="6a9e0-146">Microsoft. Azure. Commands. Network. Models. PSConnectionMonitorIcmpConfiguration</span><span class="sxs-lookup"><span data-stu-id="6a9e0-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="6a9e0-147">Note</span><span class="sxs-lookup"><span data-stu-id="6a9e0-147">NOTES</span></span>

## <span data-ttu-id="6a9e0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a9e0-148">RELATED LINKS</span></span>
