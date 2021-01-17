---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 720b81b858799e2930ed3d2cdd45e25220697e6a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365046"
---
# <span data-ttu-id="69327-101">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69327-101">Start-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="69327-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="69327-102">SYNOPSIS</span></span>
<span data-ttu-id="69327-103">Avvia l'operazione di acquisizione di pacchetti in una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="69327-103">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="69327-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69327-104">SYNTAX</span></span>

### <span data-ttu-id="69327-105">ByVpnConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69327-105">ByVpnConnectionName (Default)</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-FilterData <String>] -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69327-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="69327-106">ByVpnConnectionObject</span></span>
```
Start-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-FilterData <String>]
 -LinkConnectionName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69327-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="69327-107">ByVpnConnectionResourceId</span></span>
```
Start-AzVpnConnectionPacketCapture -ResourceId <String> [-FilterData <String>] -LinkConnectionName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69327-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="69327-108">DESCRIPTION</span></span>
<span data-ttu-id="69327-109">Avvia l'operazione di acquisizione di pacchetti in una connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="69327-109">Starts Packet Capture Operation on a Vpn Connection.</span></span>

## <span data-ttu-id="69327-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69327-110">EXAMPLES</span></span>

### <span data-ttu-id="69327-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="69327-111">Example 1</span></span>
```powershell
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1"
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1
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

### <span data-ttu-id="69327-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="69327-112">Example 2</span></span>
```powershell
$a="{`"TracingFlags`":11,`"MaxPacketBufferSize`":120,`"MaxFileSize`":500,`"Filters`":[{`"SourceSubnets`":[`"10.19.0.4/32`",`"10.20.0.4/32`"],`"DestinationSubnets`":[`"10.20.0.4/32`",`"10.19.0.4/32`"],`"IpSubnetValueAsAny`":true,`"TcpFlags`":-1,`"PortValueAsAny`":true,`"CaptureSingleDirectionTrafficOnly`":true}]}"
Start-AzVpnConnectionPacketCapture -ResourceGroupName "PktCaptureTestSite2RG" -Name "PktCaptureTestSite2Site1Cn" -ParentResourceName "VpnGw1" -LinkConnectionName "PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1" -FilterData $a 
Code              : Succeeded
EndTime           : 10/1/2019 12:52:37 AM
StartTime         : 10/1/2019 12:52:25 AM
ResultsText       :
LinkConnectionName: PktCaptureTestSite2Site1CnLink1,PktCaptureTestSite2Site1CnLink1
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

## <span data-ttu-id="69327-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="69327-113">PARAMETERS</span></span>

### <span data-ttu-id="69327-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69327-114">-AsJob</span></span>
<span data-ttu-id="69327-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="69327-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="69327-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69327-116">-DefaultProfile</span></span>
<span data-ttu-id="69327-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69327-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69327-118">-FilterData</span><span class="sxs-lookup"><span data-stu-id="69327-118">-FilterData</span></span>
<span data-ttu-id="69327-119">Opzioni di filtro per avviare l'acquisizione di pacchetti in connessione VPN.</span><span class="sxs-lookup"><span data-stu-id="69327-119">Filter options for start packet capture on Vpn connection.</span></span>

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

### <span data-ttu-id="69327-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69327-120">-InputObject</span></span>
<span data-ttu-id="69327-121">Oggetto connessione VPN in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="69327-121">The Vpn connection object where packet capture to be started.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnConnection
Parameter Sets: ByVpnConnectionObject
Aliases: VpnConnection

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69327-122">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="69327-122">-LinkConnectionName</span></span>
<span data-ttu-id="69327-123">Nomi di SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="69327-123">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="69327-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="69327-124">-Name</span></span>
<span data-ttu-id="69327-125">Il nome della connessione VPN in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="69327-125">The Vpn connection name where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, VpnConnectionName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69327-126">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="69327-126">-ParentResourceName</span></span>
<span data-ttu-id="69327-127">Il nome dell'elemento padre vpngateway.</span><span class="sxs-lookup"><span data-stu-id="69327-127">The name of the Parent Vpngateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ParentVpnGatewayName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69327-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69327-128">-ResourceGroupName</span></span>
<span data-ttu-id="69327-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="69327-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69327-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69327-130">-ResourceId</span></span>
<span data-ttu-id="69327-131">ID risorsa di Azure della VpnConnection in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="69327-131">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="69327-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="69327-132">-Confirm</span></span>
<span data-ttu-id="69327-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69327-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69327-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69327-134">-WhatIf</span></span>
<span data-ttu-id="69327-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69327-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69327-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69327-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69327-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69327-137">CommonParameters</span></span>
<span data-ttu-id="69327-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69327-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69327-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69327-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69327-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="69327-140">INPUTS</span></span>

### <span data-ttu-id="69327-141">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="69327-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="69327-142">System. String</span><span class="sxs-lookup"><span data-stu-id="69327-142">System.String</span></span>

## <span data-ttu-id="69327-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69327-143">OUTPUTS</span></span>

### <span data-ttu-id="69327-144">Microsoft. Azure. Commands. Network. Models. PSVpnConnectionPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="69327-144">Microsoft.Azure.Commands.Network.Models.PSVpnConnectionPacketCaptureResult</span></span>

## <span data-ttu-id="69327-145">Note</span><span class="sxs-lookup"><span data-stu-id="69327-145">NOTES</span></span>

## <span data-ttu-id="69327-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69327-146">RELATED LINKS</span></span>

[<span data-ttu-id="69327-147">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="69327-147">Stop-AzVpnConnectionPacketCapture</span></span>](./Stop-AzVpnConnectionPacketCapture.md)