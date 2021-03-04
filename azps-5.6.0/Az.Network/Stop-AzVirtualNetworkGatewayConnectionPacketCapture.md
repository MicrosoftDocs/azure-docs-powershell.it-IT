---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 9ee9277ccbadf190605d8c9e05a1637011204219
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951853"
---
# <span data-ttu-id="ac4e8-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac4e8-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="ac4e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac4e8-102">SYNOPSIS</span></span>
<span data-ttu-id="ac4e8-103">Interrompe l'operazione di acquisizione pacchetti in una connessione a un Gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="ac4e8-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="ac4e8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ac4e8-104">SYNTAX</span></span>

### <span data-ttu-id="ac4e8-105">ByName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ac4e8-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac4e8-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac4e8-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac4e8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4e8-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac4e8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ac4e8-108">DESCRIPTION</span></span>
<span data-ttu-id="ac4e8-109">Interrompe l'operazione di acquisizione pacchetti in una connessione a un Gateway di rete virtuale e carica il risultato su un determinato valore SasUrl del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="ac4e8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ac4e8-110">EXAMPLES</span></span>

### <span data-ttu-id="ac4e8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ac4e8-111">Example 1</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 New-AzStorageContainer -Name $containerName -Context $context
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

### <span data-ttu-id="ac4e8-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ac4e8-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVirtualNetworkGatewayConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject $conn -SasUrl $sasurl

Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
ResourceGroupName : testRg
Location          : centraluseuap
ResourceGuid      : ac70028f-5b88-4ad4-93d3-0b9a9172c382
Type              :
Tag               :
TagsTable         :
Name              : testconn
Etag              :
Id                :
```

## <span data-ttu-id="ac4e8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac4e8-113">PARAMETERS</span></span>

### <span data-ttu-id="ac4e8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ac4e8-114">-AsJob</span></span>
<span data-ttu-id="ac4e8-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ac4e8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ac4e8-116">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ac4e8-116">-Confirm</span></span>
<span data-ttu-id="ac4e8-117">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac4e8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac4e8-118">-DefaultProfile</span></span>
<span data-ttu-id="ac4e8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac4e8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac4e8-120">-InputObject</span></span>
<span data-ttu-id="ac4e8-121">Oggetto connessione gateway di rete virtuale in cui iniziare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="ac4e8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ac4e8-122">-Name</span></span>
<span data-ttu-id="ac4e8-123">Nome della connessione del gateway di rete virtuale in cui deve essere avviata l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac4e8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac4e8-124">-ResourceGroupName</span></span>
<span data-ttu-id="ac4e8-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-125">The resource group name.</span></span>

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

### <span data-ttu-id="ac4e8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac4e8-126">-ResourceId</span></span>
<span data-ttu-id="ac4e8-127">ID della risorsa Azure di VirtualNetworkGatewayConnection in cui viene avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="ac4e8-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="ac4e8-128">-SasUrl</span></span>
<span data-ttu-id="ac4e8-129">URL della firma di accesso condiviso per l'interruzione dell'acquisizione di pacchetti nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="ac4e8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac4e8-130">-WhatIf</span></span>
<span data-ttu-id="ac4e8-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac4e8-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac4e8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac4e8-133">CommonParameters</span></span>
<span data-ttu-id="ac4e8-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac4e8-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ac4e8-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac4e8-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ac4e8-136">INPUTS</span></span>

### <span data-ttu-id="ac4e8-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="ac4e8-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="ac4e8-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ac4e8-138">System.String</span></span>

## <span data-ttu-id="ac4e8-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ac4e8-139">OUTPUTS</span></span>

### <span data-ttu-id="ac4e8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="ac4e8-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="ac4e8-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="ac4e8-141">NOTES</span></span>

## <span data-ttu-id="ac4e8-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ac4e8-142">RELATED LINKS</span></span>
[<span data-ttu-id="ac4e8-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ac4e8-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)