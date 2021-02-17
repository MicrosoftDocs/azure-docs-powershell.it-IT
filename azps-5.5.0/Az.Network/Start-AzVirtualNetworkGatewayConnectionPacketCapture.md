---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: d01fad830b9edcd8eced13a4f1e9317bb4930f9c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193319"
---
# <span data-ttu-id="a39ab-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a39ab-101">Start-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="a39ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a39ab-102">SYNOPSIS</span></span>
<span data-ttu-id="a39ab-103">Avvia l'operazione di acquisizione pacchetti in una connessione a un Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a39ab-103">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="a39ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a39ab-104">SYNTAX</span></span>

### <span data-ttu-id="a39ab-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a39ab-105">ByName (Default)</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a39ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a39ab-106">ByInputObject</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 [-FilterData <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a39ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a39ab-107">ByResourceId</span></span>
```
Start-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a39ab-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a39ab-108">DESCRIPTION</span></span>
<span data-ttu-id="a39ab-109">Avvia l'operazione di acquisizione pacchetti in una connessione a un Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a39ab-109">Starts Packet Capture Operation on a Virtual Network Gateway Connection.</span></span>

## <span data-ttu-id="a39ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a39ab-110">EXAMPLES</span></span>

### <span data-ttu-id="a39ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a39ab-111">Example 1</span></span>
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
### <span data-ttu-id="a39ab-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a39ab-112">Example 2</span></span>
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
### <span data-ttu-id="a39ab-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a39ab-113">Example 3</span></span>
<span data-ttu-id="a39ab-114">Esempio di acquisizione pacchetti per l'acquisizione di tutti i pacchetti interni ed esterni</span><span class="sxs-lookup"><span data-stu-id="a39ab-114">Packet Capture example for capture all inner and outer packets</span></span>
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

## <span data-ttu-id="a39ab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a39ab-115">PARAMETERS</span></span>

### <span data-ttu-id="a39ab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a39ab-116">-AsJob</span></span>
<span data-ttu-id="a39ab-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a39ab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a39ab-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a39ab-118">-Confirm</span></span>
<span data-ttu-id="a39ab-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a39ab-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a39ab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a39ab-120">-DefaultProfile</span></span>
<span data-ttu-id="a39ab-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a39ab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a39ab-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="a39ab-122">-FilterData</span></span>
<span data-ttu-id="a39ab-123">Opzioni di filtro per avviare l'acquisizione di pacchetti nella connessione del Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="a39ab-123">Filter options for start packet capture on virtual network gateway connection.</span></span>

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

### <span data-ttu-id="a39ab-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a39ab-124">-InputObject</span></span>
<span data-ttu-id="a39ab-125">Oggetto connessione gateway di rete virtuale in cui iniziare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a39ab-125">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="a39ab-126">-Name</span><span class="sxs-lookup"><span data-stu-id="a39ab-126">-Name</span></span>
<span data-ttu-id="a39ab-127">Nome della connessione del gateway di rete virtuale in cui viene avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a39ab-127">The virtual network gateway connection name where packet capture to be started.</span></span>

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

### <span data-ttu-id="a39ab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a39ab-128">-ResourceGroupName</span></span>
<span data-ttu-id="a39ab-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a39ab-129">The resource group name.</span></span>

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

### <span data-ttu-id="a39ab-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a39ab-130">-ResourceId</span></span>
<span data-ttu-id="a39ab-131">ID della risorsa Azure di VirtualNetworkGatewayConnection in cui viene avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="a39ab-131">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="a39ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a39ab-132">-WhatIf</span></span>
<span data-ttu-id="a39ab-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a39ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a39ab-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a39ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a39ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a39ab-135">CommonParameters</span></span>
<span data-ttu-id="a39ab-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a39ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a39ab-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a39ab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a39ab-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="a39ab-138">INPUTS</span></span>

### <span data-ttu-id="a39ab-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="a39ab-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="a39ab-140">System.String</span><span class="sxs-lookup"><span data-stu-id="a39ab-140">System.String</span></span>

## <span data-ttu-id="a39ab-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a39ab-141">OUTPUTS</span></span>

### <span data-ttu-id="a39ab-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="a39ab-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="a39ab-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="a39ab-143">NOTES</span></span>

## <span data-ttu-id="a39ab-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a39ab-144">RELATED LINKS</span></span>
[<span data-ttu-id="a39ab-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="a39ab-145">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>](./Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md)