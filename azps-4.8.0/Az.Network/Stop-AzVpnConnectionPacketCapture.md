---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azvpnconnectionpacketcapture
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzVpnConnectionPacketCapture.md
ms.openlocfilehash: 88cbb5417e8a82ede25cc77274294a5dc4f64b9c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188347"
---
# <span data-ttu-id="5af5f-101">Stop-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5af5f-101">Stop-AzVpnConnectionPacketCapture</span></span>

## <span data-ttu-id="5af5f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5af5f-102">SYNOPSIS</span></span>
<span data-ttu-id="5af5f-103">Interrompe l'operazione di acquisizione di pacchetti in una connessione VPN</span><span class="sxs-lookup"><span data-stu-id="5af5f-103">Stops Packet Capture Operation on a Vpn connection</span></span>

## <span data-ttu-id="5af5f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5af5f-104">SYNTAX</span></span>

### <span data-ttu-id="5af5f-105">ByVpnConnectionName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5af5f-105">ByVpnConnectionName (Default)</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-LinkConnectionName <String>] -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af5f-106">ByVpnConnectionObject</span><span class="sxs-lookup"><span data-stu-id="5af5f-106">ByVpnConnectionObject</span></span>
```
Stop-AzVpnConnectionPacketCapture -InputObject <PSVpnConnection> [-LinkConnectionName <String>]
 -SasUrl <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5af5f-107">ByVpnConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="5af5f-107">ByVpnConnectionResourceId</span></span>
```
Stop-AzVpnConnectionPacketCapture -ResourceId <String> [-LinkConnectionName <String>] -SasUrl <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5af5f-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5af5f-108">DESCRIPTION</span></span>
<span data-ttu-id="5af5f-109">Interrompe l'operazione di acquisizione di pacchetti in una connessione VPN e carica il risultato in un contenitore di archiviazione specifico SasUrl.</span><span class="sxs-lookup"><span data-stu-id="5af5f-109">Stops Packet Capture Operation on a Vpn connection and will upload the result on given SasUrl of storage container.</span></span>

## <span data-ttu-id="5af5f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5af5f-110">EXAMPLES</span></span>

### <span data-ttu-id="5af5f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5af5f-111">Example 1</span></span>
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
PS C:\> Stop-AzVpnConnectionPacketCapture -ResourceGroupName $rgname -Name "testconn" -ParentResourceName "VpnGw1" -LinkConnectionName "SiteLink1,SiteLink2" -SasUrl $sasurl
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

### <span data-ttu-id="5af5f-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5af5f-112">Example 2</span></span>
```powershell
PS C:\> $rgname = "testRg"
 $storeName = "teststorage"
 $containerName = "packetcaptureresults"
 $key = Get-AzStorageAccountKey -ResourceGroupName $rgname -Name $storeName
 $context = New-AzStorageContext -StorageAccountName $storeName -StorageAccountKey $key[0].Value
 $container = Get-AzStorageContainer -Name $containerName -Context $context
 $now=get-date
 $sasurl = New-AzureStorageContainerSASToken -Name $containerName -Context $context -Permission "rwd" -StartTime $now.AddHours(-1) -ExpiryTime $now.AddDays(1) -FullUri
 $conn = Get-AzVpnConnection -name "testconn" -ResourceGroupName $rgname
PS C:\> Stop-AzVpnConnectionPacketCapture -InputObject $conn -SasUrl $sasurl -LinkConnectionName "SiteLink1,SiteLink2"
Code              : Succeeded
EndTime           : 10/1/2019 12:54:51 AM
StartTime         : 10/1/2019 12:53:40 AM
ResultsText       :
LinkConnectionName: SiteLink1,SiteLink2
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

## <span data-ttu-id="5af5f-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5af5f-113">PARAMETERS</span></span>

### <span data-ttu-id="5af5f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5af5f-114">-AsJob</span></span>
<span data-ttu-id="5af5f-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="5af5f-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5af5f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5af5f-116">-DefaultProfile</span></span>
<span data-ttu-id="5af5f-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5af5f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5af5f-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5af5f-118">-InputObject</span></span>
<span data-ttu-id="5af5f-119">Oggetto connessione VPN in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5af5f-119">The Vpn connection object where packet capture to be started.</span></span>

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

### <span data-ttu-id="5af5f-120">-LinkConnectionName</span><span class="sxs-lookup"><span data-stu-id="5af5f-120">-LinkConnectionName</span></span>
<span data-ttu-id="5af5f-121">Nomi di SiteLinkConnection.</span><span class="sxs-lookup"><span data-stu-id="5af5f-121">The names of the SiteLinkConnection.</span></span>

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

### <span data-ttu-id="5af5f-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5af5f-122">-Name</span></span>
<span data-ttu-id="5af5f-123">Il nome della connessione VPN in cui deve essere avviata l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5af5f-123">The Vpn connection name where packet capture is to be started.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnConnectionName
Aliases: ResourceName, ConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5af5f-124">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="5af5f-124">-ParentResourceName</span></span>
<span data-ttu-id="5af5f-125">Il nome della risorsa padre.</span><span class="sxs-lookup"><span data-stu-id="5af5f-125">The parent resource name.</span></span>

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

### <span data-ttu-id="5af5f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5af5f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5af5f-127">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="5af5f-127">The resource group name.</span></span>

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

### <span data-ttu-id="5af5f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5af5f-128">-ResourceId</span></span>
<span data-ttu-id="5af5f-129">ID risorsa di Azure della VpnConnection in cui è possibile avviare l'acquisizione di pacchetti.</span><span class="sxs-lookup"><span data-stu-id="5af5f-129">The Azure resource ID of the VpnConnection where packet capture to be started.</span></span>

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

### <span data-ttu-id="5af5f-130">-SasUrl</span><span class="sxs-lookup"><span data-stu-id="5af5f-130">-SasUrl</span></span>
<span data-ttu-id="5af5f-131">URL SAS per l'acquisizione di pacchetti stop su VPN.</span><span class="sxs-lookup"><span data-stu-id="5af5f-131">SAS Url for stop packet capture on Vpn.</span></span>

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

### <span data-ttu-id="5af5f-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5af5f-132">-Confirm</span></span>
<span data-ttu-id="5af5f-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5af5f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5af5f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5af5f-134">-WhatIf</span></span>
<span data-ttu-id="5af5f-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5af5f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5af5f-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5af5f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5af5f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5af5f-137">CommonParameters</span></span>
<span data-ttu-id="5af5f-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5af5f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5af5f-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5af5f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5af5f-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5af5f-140">INPUTS</span></span>

### <span data-ttu-id="5af5f-141">Microsoft. Azure. Commands. Network. Models. PSVpnConnection</span><span class="sxs-lookup"><span data-stu-id="5af5f-141">Microsoft.Azure.Commands.Network.Models.PSVpnConnection</span></span>

### <span data-ttu-id="5af5f-142">System. String</span><span class="sxs-lookup"><span data-stu-id="5af5f-142">System.String</span></span>

## <span data-ttu-id="5af5f-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5af5f-143">OUTPUTS</span></span>

### <span data-ttu-id="5af5f-144">Microsoft. Azure. Commands. Network. Models. PSVpnPacketCaptureResult</span><span class="sxs-lookup"><span data-stu-id="5af5f-144">Microsoft.Azure.Commands.Network.Models.PSVpnPacketCaptureResult</span></span>

## <span data-ttu-id="5af5f-145">Note</span><span class="sxs-lookup"><span data-stu-id="5af5f-145">NOTES</span></span>

## <span data-ttu-id="5af5f-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5af5f-146">RELATED LINKS</span></span>

[<span data-ttu-id="5af5f-147">Start-AzVpnConnectionPacketCapture</span><span class="sxs-lookup"><span data-stu-id="5af5f-147">Start-AzVpnConnectionPacketCapture</span></span>](./Start-AzVpnConnectionPacketCapture.md)