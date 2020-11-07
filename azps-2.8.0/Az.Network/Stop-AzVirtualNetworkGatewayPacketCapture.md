---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvirtualnetworkgatewaypacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVirtualNetworkGatewayPacketCapture.md
ms.openlocfilehash: 39bb650333c59bd7d7185449025de7bdd6254fab
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93855114"
---
# <span data-ttu-id="ccae4-101">Stop-AzVirtualNetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ccae4-101">Stop-AzVirtualNetworkGatewayPacketCapture</span></span>

## <span data-ttu-id="ccae4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ccae4-102">SYNOPSIS</span></span>
<span data-ttu-id="ccae4-103">Interrompe l'operazione di acquisizione di pacchetti su un gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccae4-103">Stops Packet Capture Operation on a Virtual Network Gateway.</span></span>

## <span data-ttu-id="ccae4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ccae4-104">SYNTAX</span></span>

### <span data-ttu-id="ccae4-105">ByName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ccae4-105">ByName (Default)</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccae4-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ccae4-106">ByInputObject</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -InputObject <PSVirtualNetworkGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ccae4-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ccae4-107">ByResourceId</span></span>
```
Stop-AzVirtualNetworkGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ccae4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ccae4-108">DESCRIPTION</span></span>
<span data-ttu-id="ccae4-109">Interrompe l'operazione di acquisizione di pacchetti su un gateway di rete virtuale e carica il risultato in un contenitore di archiviazione specifico SasUrl.</span><span class="sxs-lookup"><span data-stu-id="ccae4-109">Stops Packet Capture Operation on a Virtual Network Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="ccae4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ccae4-110">EXAMPLES</span></span>

### <span data-ttu-id="ccae4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ccae4-111">Example 1</span></span>
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

### <span data-ttu-id="ccae4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ccae4-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
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

## <span data-ttu-id="ccae4-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ccae4-113">PARAMETERS</span></span>

### <span data-ttu-id="ccae4-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ccae4-114">-AsJob</span></span>
<span data-ttu-id="ccae4-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ccae4-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ccae4-116">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ccae4-116">-Confirm</span></span>
<span data-ttu-id="ccae4-117">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ccae4-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ccae4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccae4-118">-DefaultProfile</span></span>
<span data-ttu-id="ccae4-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ccae4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccae4-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ccae4-120">-InputObject</span></span>
<span data-ttu-id="ccae4-121">Oggetto gateway di rete virtuale in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ccae4-121">The virtual network gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="ccae4-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ccae4-122">-Name</span></span>
<span data-ttu-id="ccae4-123">Il nome del gateway di rete virtuale in cui avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ccae4-123">The virtual network gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="ccae4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccae4-124">-ResourceGroupName</span></span>
<span data-ttu-id="ccae4-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ccae4-125">The resource group name.</span></span>

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

### <span data-ttu-id="ccae4-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ccae4-126">-ResourceId</span></span>
<span data-ttu-id="ccae4-127">ID risorsa di Azure della VirtualNetworkGateway in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ccae4-127">The Azure resource ID of the VirtualNetworkGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="ccae4-128">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="ccae4-128">-SasUrl</span></span>
<span data-ttu-id="ccae4-129">Acquisizione di pacchetti di URL SAS nel gateway di rete virtuale.</span><span class="sxs-lookup"><span data-stu-id="ccae4-129">SAS URL packet capture on virtual network gateway.</span></span>

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

### <span data-ttu-id="ccae4-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ccae4-130">-WhatIf</span></span>
<span data-ttu-id="ccae4-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccae4-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ccae4-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ccae4-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ccae4-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccae4-133">CommonParameters</span></span>
<span data-ttu-id="ccae4-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccae4-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccae4-135">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccae4-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccae4-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ccae4-136">INPUTS</span></span>

### <span data-ttu-id="ccae4-137">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="ccae4-137">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="ccae4-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ccae4-138">System.String</span></span>

## <span data-ttu-id="ccae4-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ccae4-139">OUTPUTS</span></span>

### <span data-ttu-id="ccae4-140">Microsoft. Azure. Commands. Network. Models. PSVirtualNetworkGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="ccae4-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="ccae4-141">Note</span><span class="sxs-lookup"><span data-stu-id="ccae4-141">NOTES</span></span>

## <span data-ttu-id="ccae4-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ccae4-142">RELATED LINKS</span></span>
[<span data-ttu-id="ccae4-143">Start-AzVirtualnetworkGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ccae4-143">Start-AzVirtualnetworkGatewayPacketCapture</span></span>](./Stop-AzVirtualnetworkGatewayPacketCapture.md)