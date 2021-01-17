---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Start-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: 931c01b925416a7b1357d1eac15806035eef46d4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98486523"
---
# <span data-ttu-id="8cf66-101">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cf66-101">Start-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="8cf66-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cf66-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf66-103">Avvia l'operazione di acquisizione di pacchetti in un gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="8cf66-103">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="8cf66-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cf66-104">SYNTAX</span></span>

### <span data-ttu-id="8cf66-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8cf66-105">ByVpnGatewayName (Default)</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf66-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="8cf66-106">ByVpnGatewayObject</span></span>
```
Start-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf66-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf66-107">ByVpnGatewayResourceId</span></span>
```
Start-AzVpnGatewayPacketCapture -ResourceId <String> [-FilterData <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cf66-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cf66-108">DESCRIPTION</span></span>
<span data-ttu-id="8cf66-109">Avvia l'operazione di acquisizione di pacchetti in un gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="8cf66-109">Starts Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="8cf66-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cf66-110">EXAMPLES</span></span>

### <span data-ttu-id="8cf66-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cf66-111">Example 1</span></span>
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

### <span data-ttu-id="8cf66-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8cf66-112">Example 2</span></span>
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

## <span data-ttu-id="8cf66-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cf66-113">PARAMETERS</span></span>

### <span data-ttu-id="8cf66-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8cf66-114">-AsJob</span></span>
<span data-ttu-id="8cf66-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8cf66-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8cf66-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf66-116">-DefaultProfile</span></span>
<span data-ttu-id="8cf66-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cf66-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cf66-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="8cf66-118">-FilterData</span></span>
<span data-ttu-id="8cf66-119">Opzioni di filtro per avviare l'acquisizione di pacchetti nel gateway VPN.</span><span class="sxs-lookup"><span data-stu-id="8cf66-119">Filter options for start packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="8cf66-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8cf66-120">-InputObject</span></span>
<span data-ttu-id="8cf66-121">Oggetto gateway VPN in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8cf66-121">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="8cf66-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cf66-122">-Name</span></span>
<span data-ttu-id="8cf66-123">Il nome del gateway VPN in cui deve essere avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8cf66-123">The Vpn Gateway name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="8cf66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf66-124">-ResourceGroupName</span></span>
<span data-ttu-id="8cf66-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8cf66-125">The resource group name.</span></span>

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

### <span data-ttu-id="8cf66-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf66-126">-ResourceId</span></span>
<span data-ttu-id="8cf66-127">ID risorsa di Azure della VpnGateway in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="8cf66-127">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="8cf66-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cf66-128">-Confirm</span></span>
<span data-ttu-id="8cf66-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cf66-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cf66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf66-130">-WhatIf</span></span>
<span data-ttu-id="8cf66-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cf66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf66-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cf66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cf66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf66-133">CommonParameters</span></span>
<span data-ttu-id="8cf66-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cf66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf66-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8cf66-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf66-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cf66-136">INPUTS</span></span>

### <span data-ttu-id="8cf66-137">Microsoft. Azure. Commands. Network. Models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="8cf66-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="8cf66-138">System. String</span><span class="sxs-lookup"><span data-stu-id="8cf66-138">System.String</span></span>

## <span data-ttu-id="8cf66-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cf66-139">OUTPUTS</span></span>

### <span data-ttu-id="8cf66-140">Microsoft. Azure. Commands. Network. Models. PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="8cf66-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="8cf66-141">Note</span><span class="sxs-lookup"><span data-stu-id="8cf66-141">NOTES</span></span>

## <span data-ttu-id="8cf66-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cf66-142">RELATED LINKS</span></span>

[<span data-ttu-id="8cf66-143">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="8cf66-143">Stop-AzVpnGatewayPacketCapture</span></span>](./Stop-AzVpnGatewayPacketCapture.md)