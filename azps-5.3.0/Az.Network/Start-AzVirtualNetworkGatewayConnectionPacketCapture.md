---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486531"
---
# <span data-ttu-id="54c68-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54c68-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="54c68-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="54c68-102">SYNOPSIS</span></span>
<span data-ttu-id="54c68-103">Avvia l'operazione di acquisizione di pacchetti in una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="54c68-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="54c68-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="54c68-104">SYNTAX</span></span>

### <span data-ttu-id="54c68-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="54c68-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54c68-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="54c68-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="54c68-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="54c68-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="54c68-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="54c68-108">DESCRIPTION</span></span>
<span data-ttu-id="54c68-109">Avvia l'operazione di acquisizione di pacchetti in una connessione di gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="54c68-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="54c68-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="54c68-110">EXAMPLES</span></span>

### <span data-ttu-id="54c68-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="54c68-111">Example 1</span></span>
```powershell
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn"

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="54c68-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="54c68-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```
### <span data-ttu-id="54c68-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="54c68-113">Example 3</span></span>
<span data-ttu-id="54c68-114">Esempio di acquisizione di pacchetti per l'acquisizione di tutti i pacchetti interni ed esterni</span><span class="sxs-lookup"><span data-stu-id="54c68-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2Site1Cn
Etag              :
Id                :
```

## <span data-ttu-id="54c68-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="54c68-115">PARAMETERS</span></span>

### <span data-ttu-id="54c68-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54c68-116">-AsJob</span></span>
<span data-ttu-id="54c68-117">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="54c68-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54c68-118">-Confermare</span><span class="sxs-lookup"><span data-stu-id="54c68-118">-Confirm</span></span>
<span data-ttu-id="54c68-119">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="54c68-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54c68-120">-DefaultProfile</span></span>
<span data-ttu-id="54c68-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="54c68-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="54c68-122">-FilterData</span></span>
<span data-ttu-id="54c68-123">Opzioni di filtro per avviare l'acquisizione di pacchetti sulla connessione gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="54c68-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="54c68-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="54c68-124">-InputObject</span></span>
<span data-ttu-id="54c68-125">Oggetto connessione di Virtual Network Gateway in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="54c68-125">The virtual network gateway connection object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGatewayConnection
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGatewayConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="54c68-126">-Name</span></span>
<span data-ttu-id="54c68-127">Il nome della connessione del gateway di rete virtuale in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="54c68-127">The virtual network gateway connection name where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54c68-128">-ResourceGroupName</span></span>
<span data-ttu-id="54c68-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="54c68-129">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="54c68-130">-ResourceId</span></span>
<span data-ttu-id="54c68-131">ID risorsa di Azure della VirtualNetworkGatewayConnection in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="54c68-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54c68-132">-WhatIf</span></span>
<span data-ttu-id="54c68-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54c68-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54c68-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="54c68-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="54c68-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54c68-135">CommonParameters</span></span>
<span data-ttu-id="54c68-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54c68-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54c68-137">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54c68-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54c68-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="54c68-138">INPUTS</span></span>

### <span data-ttu-id="54c68-139">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="54c68-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="54c68-140">System. String</span><span class="sxs-lookup"><span data-stu-id="54c68-140">System.String</span></span>

## <span data-ttu-id="54c68-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="54c68-141">OUTPUTS</span></span>

### <span data-ttu-id="54c68-142">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="54c68-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="54c68-143">Note</span><span class="sxs-lookup"><span data-stu-id="54c68-143">NOTES</span></span>

## <span data-ttu-id="54c68-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="54c68-144">RELATED LINKS</span></span>
[<span data-ttu-id="54c68-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="54c68-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)