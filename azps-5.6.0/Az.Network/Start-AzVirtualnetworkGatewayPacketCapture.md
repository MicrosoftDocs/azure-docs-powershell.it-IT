---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/start-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVirtualnetworkGatewayPacketCapture.md
ms.openlocfilehash: 4f17777d366884f2b71c16c289e50dbf8425d729
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951886"
---
# <span data-ttu-id="9caab-101">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9caab-101">Start-AzVirtualnetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="9caab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9caab-102">SYNOPSIS</span></span>
<span data-ttu-id="9caab-103">Avvia l'operazione di acquisizione pacchetti in un Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9caab-103">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="9caab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9caab-104">SYNTAX</span></span>

### <span data-ttu-id="9caab-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9caab-105">ByName (Default)</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9caab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9caab-106">ByInputObject</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> [-FilterData <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9caab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9caab-107">ByResourceId</span></span>
```
Start-AzVirtualnetworkGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9caab-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9caab-108">DESCRIPTION</span></span>
<span data-ttu-id="9caab-109">Avvia l'operazione di acquisizione pacchetti in un Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9caab-109">Starts Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="9caab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9caab-110">EXAMPLES</span></span>

### <span data-ttu-id="9caab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9caab-111">Example 1</span></span>
```powershell
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="9caab-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9caab-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```
### <span data-ttu-id="9caab-113">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9caab-113">Example 3</span></span>
<span data-ttu-id="9caab-114">Esempio di Acquisizione pacchetti per l'acquisizione di tutti i pacchetti interni ed esterni</span><span class="sxs-lookup"><span data-stu-id="9caab-114">Packet Capture example for capture all inner and outer packets</span></span>
```powershell
$a = "{`"TracingFlags`": 11,`"MaxPacketBufferSize`": 120,`"MaxFileSize`": 500,`"Filters`" :[{`"CaptureSingleDirectionTrafficOnly`": false}]}"
Start-AzVirtualnetworkGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a

Code              : Succeeded
EndTime           : 10/1/2019 12:57:27 AM
StartTime         : 10/1/2019 12:57:16 AM
ResultsText       :
ResourceGroupName : PktCaptureTestSite2RG
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : PktCaptureTestSite2VNG
Etag              :
Id                :
```

## <span data-ttu-id="9caab-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9caab-115">PARAMETERS</span></span>

### <span data-ttu-id="9caab-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9caab-116">-AsJob</span></span>
<span data-ttu-id="9caab-117">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9caab-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9caab-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9caab-118">-Confirm</span></span>
<span data-ttu-id="9caab-119">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9caab-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9caab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9caab-120">-DefaultProfile</span></span>
<span data-ttu-id="9caab-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9caab-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9caab-122">-FilterData</span><span class="sxs-lookup"><span data-stu-id="9caab-122">-FilterData</span></span>
<span data-ttu-id="9caab-123">Opzioni di filtro per avviare l'acquisizione di pacchetti nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="9caab-123">Filter options for start packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="9caab-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9caab-124">-InputObject</span></span>
<span data-ttu-id="9caab-125">Oggetto gateway di rete virtuale in cui iniziare l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9caab-125">The virtual network gateway object where packet capture to be started.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: ByInputObject
Aliases: VirtualNetworkGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9caab-126">-Name</span><span class="sxs-lookup"><span data-stu-id="9caab-126">-Name</span></span>
<span data-ttu-id="9caab-127">Nome del gateway di rete virtuale in cui deve essere avviata l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9caab-127">The virtual network gateway name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, VirtualNetworkGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9caab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9caab-128">-ResourceGroupName</span></span>
<span data-ttu-id="9caab-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9caab-129">The resource group name.</span></span>

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

### <span data-ttu-id="9caab-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9caab-130">-ResourceId</span></span>
<span data-ttu-id="9caab-131">ID della risorsa Azure di VirtualNetworkGateway in cui viene avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="9caab-131">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="9caab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9caab-132">-WhatIf</span></span>
<span data-ttu-id="9caab-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9caab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9caab-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9caab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9caab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9caab-135">CommonParameters</span></span>
<span data-ttu-id="9caab-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9caab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9caab-137">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9caab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9caab-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="9caab-138">INPUTS</span></span>

### <span data-ttu-id="9caab-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="9caab-139">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="9caab-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9caab-140">System.String</span></span>

## <span data-ttu-id="9caab-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9caab-141">OUTPUTS</span></span>

### <span data-ttu-id="9caab-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="9caab-142">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="9caab-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="9caab-143">NOTES</span></span>

## <span data-ttu-id="9caab-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9caab-144">RELATED LINKS</span></span>
[<span data-ttu-id="9caab-145">Stop-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="9caab-145">Stop-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)