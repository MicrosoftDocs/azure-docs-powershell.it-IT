---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100185750"
---
# <span data-ttu-id="5a43d-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="5a43d-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="5a43d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a43d-102">SYNOPSIS</span></span>
<span data-ttu-id="5a43d-103">Ottenere la stringa di connessione di un dispositivo IoT di destinazione in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="5a43d-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="5a43d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5a43d-104">SYNTAX</span></span>

### <span data-ttu-id="5a43d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5a43d-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a43d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5a43d-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a43d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5a43d-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a43d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="5a43d-108">DESCRIPTION</span></span>
<span data-ttu-id="5a43d-109">Elenco della stringa di connessione di tutti i dispositivi o di un dispositivo IoT di destinazione contenuto in un hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="5a43d-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="5a43d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5a43d-110">EXAMPLES</span></span>

### <span data-ttu-id="5a43d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5a43d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="5a43d-112">Mostra la stringa di connessione di tutti i dispositivi in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="5a43d-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="5a43d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5a43d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="5a43d-114">Ottenere la stringa di connessione secondaria di un dispositivo IoT.</span><span class="sxs-lookup"><span data-stu-id="5a43d-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="5a43d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5a43d-115">PARAMETERS</span></span>

### <span data-ttu-id="5a43d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a43d-116">-DefaultProfile</span></span>
<span data-ttu-id="5a43d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5a43d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a43d-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="5a43d-118">-DeviceId</span></span>
<span data-ttu-id="5a43d-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="5a43d-119">Target Device Id.</span></span>

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

### <span data-ttu-id="5a43d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a43d-120">-InputObject</span></span>
<span data-ttu-id="5a43d-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="5a43d-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43d-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="5a43d-122">-IotHubName</span></span>
<span data-ttu-id="5a43d-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="5a43d-123">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a43d-124">-KeyType</span><span class="sxs-lookup"><span data-stu-id="5a43d-124">-KeyType</span></span>
<span data-ttu-id="5a43d-125">Tipo di chiave dei criteri di accesso condiviso per l'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="5a43d-125">Shared access policy key type for auth.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSKeyType
Parameter Sets: (All)
Aliases:
Accepted values: primary, secondary

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a43d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a43d-126">-ResourceGroupName</span></span>
<span data-ttu-id="5a43d-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5a43d-127">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a43d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a43d-128">-ResourceId</span></span>
<span data-ttu-id="5a43d-129">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="5a43d-129">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a43d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a43d-130">CommonParameters</span></span>
<span data-ttu-id="5a43d-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a43d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a43d-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a43d-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a43d-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="5a43d-133">INPUTS</span></span>

### <span data-ttu-id="5a43d-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="5a43d-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="5a43d-135">System.String</span><span class="sxs-lookup"><span data-stu-id="5a43d-135">System.String</span></span>

## <span data-ttu-id="5a43d-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5a43d-136">OUTPUTS</span></span>

### <span data-ttu-id="5a43d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="5a43d-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="5a43d-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="5a43d-138">NOTES</span></span>

## <span data-ttu-id="5a43d-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5a43d-139">RELATED LINKS</span></span>
