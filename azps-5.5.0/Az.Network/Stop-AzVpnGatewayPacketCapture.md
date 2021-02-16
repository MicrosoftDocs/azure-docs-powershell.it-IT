---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Stop-AzVpnGatewayPacketCapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnGatewayPacketCapture.md
ms.openlocfilehash: e5f753d822911abd79e339412741657dae36628f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179310"
---
# <span data-ttu-id="ea08a-101">Stop-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea08a-101">Stop-AzVpnGatewayPacketCapture</span></span>

## <span data-ttu-id="ea08a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ea08a-102">SYNOPSIS</span></span>
<span data-ttu-id="ea08a-103">Interrompe l'operazione di acquisizione pacchetti in un gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="ea08a-103">Stops Packet Capture Operation on a Vpn Gateway.</span></span>

## <span data-ttu-id="ea08a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ea08a-104">SYNTAX</span></span>

### <span data-ttu-id="ea08a-105">ByVpnGatewayName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ea08a-105">ByVpnGatewayName (Default)</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceGroupName <String> -Name <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea08a-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="ea08a-106">ByVpnGatewayObject</span></span>
```
Stop-AzVpnGatewayPacketCapture -InputObject <PSVpnGateway> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea08a-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="ea08a-107">ByVpnGatewayResourceId</span></span>
```
Stop-AzVpnGatewayPacketCapture -ResourceId <String> -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea08a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ea08a-108">DESCRIPTION</span></span>
<span data-ttu-id="ea08a-109">Interrompe l'operazione di acquisizione pacchetti in un gateway Vpn e carica il risultato su un determinato valore SasUrl del contenitore di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ea08a-109">Stops Packet Capture Operation on a Vpn Gateway and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="ea08a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ea08a-110">EXAMPLES</span></span>

### <span data-ttu-id="ea08a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ea08a-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnGatewayPacketCapture -ResourceGroupName $rgname -Name "testgw" -SasUrl $sasurl
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

### <span data-ttu-id="ea08a-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ea08a-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $gw = Get-AzVpnGateway -ResourceGroupName $rgname -name "testGw"
PS C:\> Stop-AzVpnGatewayPacketCapture -InputObject $gw -SasUrl $sasurl
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

## <span data-ttu-id="ea08a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ea08a-113">PARAMETERS</span></span>

### <span data-ttu-id="ea08a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea08a-114">-AsJob</span></span>
<span data-ttu-id="ea08a-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ea08a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea08a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea08a-116">-DefaultProfile</span></span>
<span data-ttu-id="ea08a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ea08a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea08a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea08a-118">-InputObject</span></span>
<span data-ttu-id="ea08a-119">Oggetto Gateway Vpn in cui iniziare l'acquisizione dei pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ea08a-119">The Vpn Gateway object where packet capture to be started.</span></span>

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

### <span data-ttu-id="ea08a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ea08a-120">-Name</span></span>
<span data-ttu-id="ea08a-121">Nome del Gateway Vpn in cui viene avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ea08a-121">The Vpn Gateway name where packet capture to be started.</span></span>

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

### <span data-ttu-id="ea08a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea08a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ea08a-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ea08a-123">The resource group name.</span></span>

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

### <span data-ttu-id="ea08a-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea08a-124">-ResourceId</span></span>
<span data-ttu-id="ea08a-125">ID della risorsa Azure di VpnGateway da cui iniziare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="ea08a-125">The Azure resource ID of the VpnGateway where packet capture to be started.</span></span>

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

### <span data-ttu-id="ea08a-126">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="ea08a-126">-SasUrl</span></span>
<span data-ttu-id="ea08a-127">Acquisizione di pacchetti dell'URL di firma di accesso condiviso in Gateway Vpn.</span><span class="sxs-lookup"><span data-stu-id="ea08a-127">SAS URL packet capture on Vpn Gateway.</span></span>

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

### <span data-ttu-id="ea08a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ea08a-128">-Confirm</span></span>
<span data-ttu-id="ea08a-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea08a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea08a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea08a-130">-WhatIf</span></span>
<span data-ttu-id="ea08a-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea08a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea08a-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ea08a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea08a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea08a-133">CommonParameters</span></span>
<span data-ttu-id="ea08a-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea08a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea08a-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ea08a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea08a-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="ea08a-136">INPUTS</span></span>

### <span data-ttu-id="ea08a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="ea08a-137">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="ea08a-138">System.String</span><span class="sxs-lookup"><span data-stu-id="ea08a-138">System.String</span></span>

## <span data-ttu-id="ea08a-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ea08a-139">OUTPUTS</span></span>

### <span data-ttu-id="ea08a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="ea08a-140">Microsoft.Azure.Commands.Network.Models.PSVpnGatewayPacketCaptureResult</span></span>

## <span data-ttu-id="ea08a-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="ea08a-141">NOTES</span></span>

## <span data-ttu-id="ea08a-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ea08a-142">RELATED LINKS</span></span>

[<span data-ttu-id="ea08a-143">Start-AzVpnGatewayPacketCapture</span><span class="sxs-lookup"><span data-stu-id="ea08a-143">Start-AzVpnGatewayPacketCapture</span></span>](./Start-AzVpnGatewayPacketCapture.md)