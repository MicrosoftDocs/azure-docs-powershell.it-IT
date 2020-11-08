---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 46d097d2985b39e1d757e2d530e67775c1b8a28d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188349"
---
# <span data-ttu-id="cae6c-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cae6c-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="cae6c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cae6c-102">SYNOPSIS</span></span>
<span data-ttu-id="cae6c-103">Interrompe l'operazione di acquisizione di pacchetti su un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="cae6c-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="cae6c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cae6c-104">SYNTAX</span></span>

### <span data-ttu-id="cae6c-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cae6c-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae6c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cae6c-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cae6c-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="cae6c-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cae6c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cae6c-108">DESCRIPTION</span></span>
<span data-ttu-id="cae6c-109">Interrompe l'operazione di acquisizione di pacchetti su un gateway di rete virtuale e carica il risultato in un contenitore di archiviazione specifico SasUrl.</span><span class="sxs-lookup"><span data-stu-id="cae6c-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="cae6c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cae6c-110">EXAMPLES</span></span>

### <span data-ttu-id="cae6c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cae6c-111">Example 1</span></span>
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

### <span data-ttu-id="cae6c-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cae6c-112">Example 2</span></span>
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

## <span data-ttu-id="cae6c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cae6c-113">PARAMETERS</span></span>

### <span data-ttu-id="cae6c-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cae6c-114">-AsJob</span></span>
<span data-ttu-id="cae6c-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cae6c-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cae6c-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cae6c-116">-Confirm</span></span>
<span data-ttu-id="cae6c-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cae6c-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cae6c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cae6c-118">-DefaultProfile</span></span>
<span data-ttu-id="cae6c-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cae6c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cae6c-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cae6c-120">-InputObject</span></span>
<span data-ttu-id="cae6c-121">Oggetto gateway di rete virtuale in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="cae6c-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="cae6c-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cae6c-122">-Name</span></span>
<span data-ttu-id="cae6c-123">Il nome del gateway di rete virtuale in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="cae6c-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="cae6c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cae6c-124">-ResourceGroupName</span></span>
<span data-ttu-id="cae6c-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cae6c-125">The resource group name.</span></span>

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

### <span data-ttu-id="cae6c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cae6c-126">-ResourceId</span></span>
<span data-ttu-id="cae6c-127">ID risorsa di Azure della VirtualNetworkGateway in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="cae6c-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="cae6c-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="cae6c-128">-SasUrl</span></span>
<span data-ttu-id="cae6c-129">Acquisizione di pacchetti di URL SAS nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="cae6c-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="cae6c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cae6c-130">-WhatIf</span></span>
<span data-ttu-id="cae6c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cae6c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cae6c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cae6c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cae6c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cae6c-133">CommonParameters</span></span>
<span data-ttu-id="cae6c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cae6c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cae6c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cae6c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cae6c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cae6c-136">INPUTS</span></span>

### <span data-ttu-id="cae6c-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="cae6c-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="cae6c-138">System. String</span><span class="sxs-lookup"><span data-stu-id="cae6c-138">System.String</span></span>

## <span data-ttu-id="cae6c-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cae6c-139">OUTPUTS</span></span>

### <span data-ttu-id="cae6c-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="cae6c-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="cae6c-141">Note</span><span class="sxs-lookup"><span data-stu-id="cae6c-141">NOTES</span></span>

## <span data-ttu-id="cae6c-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cae6c-142">RELATED LINKS</span></span>
[<span data-ttu-id="cae6c-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="cae6c-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)
