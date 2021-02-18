---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206475"
---
# <span data-ttu-id="344ab-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="344ab-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="344ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="344ab-102">SYNOPSIS</span></span>
<span data-ttu-id="344ab-103">Avvia l'operazione di acquisizione pacchetti in un Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="344ab-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="344ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="344ab-104">SYNTAX</span></span>

### <span data-ttu-id="344ab-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="344ab-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344ab-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="344ab-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="344ab-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="344ab-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="344ab-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="344ab-108">DESCRIPTION</span></span>
<span data-ttu-id="344ab-109">Avvia l'operazione di acquisizione pacchetti in un Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="344ab-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="344ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="344ab-110">EXAMPLES</span></span>

### <span data-ttu-id="344ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="344ab-111">Example 1</span></span>
```powershell
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG"
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

### <span data-ttu-id="344ab-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="344ab-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"TcpFlags`":-1,`"Protocol`":[6],`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnGatewayPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2VNG" -FilterData $a
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

## <span data-ttu-id="344ab-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="344ab-113">PARAMETERS</span></span>

### <span data-ttu-id="344ab-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="344ab-114">-AsJob</span></span>
<span data-ttu-id="344ab-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="344ab-115">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="344ab-116">-DefaultProfile</span></span>
<span data-ttu-id="344ab-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="344ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="344ab-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="344ab-118">-FilterData</span></span>
<span data-ttu-id="344ab-119">Opzioni di filtro per avviare l'acquisizione di pacchetti in Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="344ab-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="344ab-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="344ab-120">-InputObject</span></span>
<span data-ttu-id="344ab-121">Oggetto Gateway Vpn in cui iniziare l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="344ab-121">The Vpn Gateway object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="344ab-122">-Name</span><span class="sxs-lookup"><span data-stu-id="344ab-122">-Name</span></span>
<span data-ttu-id="344ab-123">Nome del Gateway Vpn in cui deve essere avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="344ab-123">The Vpn Gateway name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344ab-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="344ab-124">-ResourceGroupName</span></span>
<span data-ttu-id="344ab-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="344ab-125">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="344ab-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="344ab-126">-ResourceId</span></span>
<span data-ttu-id="344ab-127">ID della risorsa Azure di VpnGateway da cui iniziare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="344ab-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="344ab-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="344ab-128">-Confirm</span></span>
<span data-ttu-id="344ab-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="344ab-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="344ab-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="344ab-130">-WhatIf</span></span>
<span data-ttu-id="344ab-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="344ab-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="344ab-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="344ab-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="344ab-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="344ab-133">CommonParameters</span></span>
<span data-ttu-id="344ab-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="344ab-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="344ab-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="344ab-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="344ab-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="344ab-136">INPUTS</span></span>

### <span data-ttu-id="344ab-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="344ab-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="344ab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="344ab-138">System.String</span></span>

## <span data-ttu-id="344ab-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="344ab-139">OUTPUTS</span></span>

### <span data-ttu-id="344ab-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="344ab-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="344ab-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="344ab-141">NOTES</span></span>

## <span data-ttu-id="344ab-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="344ab-142">RELATED LINKS</span></span>

[<span data-ttu-id="344ab-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="344ab-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)