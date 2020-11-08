---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewayconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayConnectionPacketCapture.md
ms.openlocfilehash: 1303f8c8d2bb7b1de4401072ce1e968373aed28b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188354"
---
# <span data-ttu-id="fdeac-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fdeac-101">Stop-AzVirtualNetworkGatewayConnectionPacketCapture</span></span>

## <span data-ttu-id="fdeac-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdeac-102">SYNOPSIS</span></span>
<span data-ttu-id="fdeac-103">Interrompe l'operazione di acquisizione di pacchetti in una connessione di gateway di rete virtuale</span><span class="sxs-lookup"><span data-stu-id="fdeac-103">Stops Packet Capture Operation on a Virtual Network Gateway connection</span></span>

## <span data-ttu-id="fdeac-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdeac-104">SYNTAX</span></span>

### <span data-ttu-id="fdeac-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdeac-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdeac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fdeac-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -InputObject <PSVirtualNetworkGatewayConnection>
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdeac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fdeac-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayConnectionPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdeac-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdeac-108">DESCRIPTION</span></span>
<span data-ttu-id="fdeac-109">Interrompe l'operazione di acquisizione di pacchetti in una connessione di gateway di rete virtuale e carica il risultato in un contenitore di archiviazione specifico SasUrl.</span><span class="sxs-lookup"><span data-stu-id="fdeac-109">Stops Packet Capture Operation on a Virtual Network Gateway connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="fdeac-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdeac-110">EXAMPLES</span></span>

### <span data-ttu-id="fdeac-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdeac-111">Example 1</span></span>
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

### <span data-ttu-id="fdeac-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fdeac-112">Example 2</span></span>
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

## <span data-ttu-id="fdeac-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdeac-113">PARAMETERS</span></span>

### <span data-ttu-id="fdeac-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdeac-114">-AsJob</span></span>
<span data-ttu-id="fdeac-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="fdeac-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdeac-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fdeac-116">-Confirm</span></span>
<span data-ttu-id="fdeac-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fdeac-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdeac-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdeac-118">-DefaultProfile</span></span>
<span data-ttu-id="fdeac-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdeac-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdeac-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdeac-120">-InputObject</span></span>
<span data-ttu-id="fdeac-121">Oggetto connessione di Virtual Network Gateway in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="fdeac-121">The virtual network gateway connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="fdeac-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="fdeac-122">-Name</span></span>
<span data-ttu-id="fdeac-123">Il nome della connessione del gateway di rete virtuale in cui deve essere avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="fdeac-123">The virtual network gateway connection name where packet capture is to be started.</span></span>

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

### <span data-ttu-id="fdeac-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdeac-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdeac-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="fdeac-125">The resource group name.</span></span>

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

### <span data-ttu-id="fdeac-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdeac-126">-ResourceId</span></span>
<span data-ttu-id="fdeac-127">ID risorsa di Azure della VirtualNetworkGatewayConnection in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="fdeac-127">The Azure resource ID of the VirtualNetworkGatewayConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="fdeac-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="fdeac-128">-SasUrl</span></span>
<span data-ttu-id="fdeac-129">URL SAS per interrompere l'acquisizione di pacchetti nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="fdeac-129">SAS Url for stop packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="fdeac-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdeac-130">-WhatIf</span></span>
<span data-ttu-id="fdeac-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdeac-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fdeac-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fdeac-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdeac-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdeac-133">CommonParameters</span></span>
<span data-ttu-id="fdeac-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdeac-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdeac-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fdeac-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdeac-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdeac-136">INPUTS</span></span>

### <span data-ttu-id="fdeac-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="fdeac-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="fdeac-138">System. String</span><span class="sxs-lookup"><span data-stu-id="fdeac-138">System.String</span></span>

## <span data-ttu-id="fdeac-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdeac-139">OUTPUTS</span></span>

### <span data-ttu-id="fdeac-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="fdeac-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="fdeac-141">Note</span><span class="sxs-lookup"><span data-stu-id="fdeac-141">NOTES</span></span>

## <span data-ttu-id="fdeac-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdeac-142">RELATED LINKS</span></span>
[<span data-ttu-id="fdeac-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="fdeac-143">Start-AzVirtualnetworkGatewayConnectionPacketCapture</span></span>](./Start-AzVirtualnetworkGatewayConnectionPacketCapture.md)