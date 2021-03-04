---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 2838d3d18aaa1cdf450eed184c5ebfe9a803c20a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951837"
---
# <span data-ttu-id="f2468-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2468-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="f2468-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2468-102">SYNOPSIS</span></span>
<span data-ttu-id="f2468-103">Interrompe l'operazione di acquisizione pacchetti in un Gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2468-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="f2468-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2468-104">SYNTAX</span></span>

### <span data-ttu-id="f2468-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f2468-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2468-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f2468-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2468-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2468-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2468-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f2468-108">DESCRIPTION</span></span>
<span data-ttu-id="f2468-109">Interrompe l'operazione di acquisizione pacchetti in un Gateway di rete virtuale e carica il risultato su un determinato valore SasUrl del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f2468-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="f2468-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2468-110">EXAMPLES</span></span>

### <span data-ttu-id="f2468-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f2468-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

### <span data-ttu-id="f2468-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f2468-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVirtualNetworkGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVirtualNetworkGatewayPacketCapture -InputObject $gw -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:59:37 AM
StartTime         : 10/1/2019 12:58:26 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : 161c0fff-f3fd-4698-9ab3-8ca9470de975
Type              :
Tag               :
TagsTable         :
Name              : testgw
Etag              :
Id                :
```

## <span data-ttu-id="f2468-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f2468-113">PARAMETERS</span></span>

### <span data-ttu-id="f2468-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2468-114">-AsJob</span></span>
<span data-ttu-id="f2468-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f2468-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2468-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f2468-116">-Confirm</span></span>
<span data-ttu-id="f2468-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2468-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2468-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2468-118">-DefaultProfile</span></span>
<span data-ttu-id="f2468-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2468-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2468-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2468-120">-InputObject</span></span>
<span data-ttu-id="f2468-121">Oggetto gateway di rete virtuale in cui iniziare l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f2468-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="f2468-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f2468-122">-Name</span></span>
<span data-ttu-id="f2468-123">Nome del gateway di rete virtuale in cui viene avviata l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f2468-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="f2468-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2468-124">-ResourceGroupName</span></span>
<span data-ttu-id="f2468-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f2468-125">The resource group name.</span></span>

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

### <span data-ttu-id="f2468-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2468-126">-ResourceId</span></span>
<span data-ttu-id="f2468-127">ID della risorsa Azure di VirtualNetworkGateway in cui viene avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="f2468-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="f2468-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="f2468-128">-SasUrl</span></span>
<span data-ttu-id="f2468-129">Acquisizione di pacchetti dell'URL di firma di accesso condiviso nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="f2468-129">SAS URL packet capture on virtual network gateway.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2468-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2468-130">-WhatIf</span></span>
<span data-ttu-id="f2468-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2468-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2468-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2468-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2468-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2468-133">CommonParameters</span></span>
<span data-ttu-id="f2468-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2468-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2468-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f2468-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2468-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="f2468-136">INPUTS</span></span>

### <span data-ttu-id="f2468-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f2468-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f2468-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f2468-138">System.String</span></span>

## <span data-ttu-id="f2468-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2468-139">OUTPUTS</span></span>

### <span data-ttu-id="f2468-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="f2468-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="f2468-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="f2468-141">NOTES</span></span>

## <span data-ttu-id="f2468-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2468-142">RELATED LINKS</span></span>
[<span data-ttu-id="f2468-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="f2468-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
