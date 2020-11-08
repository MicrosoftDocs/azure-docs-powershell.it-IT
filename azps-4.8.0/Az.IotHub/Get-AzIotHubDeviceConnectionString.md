---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdeviceconnectionstring
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceConnectionString.md
ms.openlocfilehash: 53887f7dc63ba849c9eac021f6f309497b512763
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189929"
---
# <span data-ttu-id="d9240-101">Get-AzIotHubDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="d9240-101">Get-AzIotHubDeviceConnectionString</span></span>

## <span data-ttu-id="d9240-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d9240-102">SYNOPSIS</span></span>
<span data-ttu-id="d9240-103">Ottenere la stringa di connessione di un dispositivo con un sacco di destinazione in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="d9240-103">Get the connection string of a target IoT device in an Iot Hub.</span></span>

## <span data-ttu-id="d9240-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d9240-104">SYNTAX</span></span>

### <span data-ttu-id="d9240-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d9240-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-KeyType <PSKeyType>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9240-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d9240-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-InputObject] <PSIotHub> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d9240-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d9240-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceConnectionString [-ResourceId] <String> [-DeviceId <String>] [-KeyType <PSKeyType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d9240-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d9240-108">DESCRIPTION</span></span>
<span data-ttu-id="d9240-109">Stringa di connessione elenco di tutti i dispositivi o di un dispositivo di destinazione per gli altri contenuti all'interno di un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="d9240-109">List connection string of all devices or a target IoT device contained within an Azure IoT Hub.</span></span>

## <span data-ttu-id="d9240-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d9240-110">EXAMPLES</span></span>

### <span data-ttu-id="d9240-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d9240-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceConnectionString -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******     
device2   HostName=myiothub.azure-devices.net;DeviceId=device2;x509=true
```

<span data-ttu-id="d9240-112">Mostra la stringa di connessione tutti i dispositivi in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="d9240-112">Show all devices connection string in an Iot Hub.</span></span>

### <span data-ttu-id="d9240-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d9240-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDCS -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "device1" -KeyType secondary

Device Id Connection String
--------- -----------------
device1   HostName=myiothub.azure-devices.net;DeviceId=device1;SharedAccessKey=/X4y******
```

<span data-ttu-id="d9240-114">Ottenere la stringa di connessione secondaria di un dispositivo di un sacco.</span><span class="sxs-lookup"><span data-stu-id="d9240-114">Get the secondary connection string of an IoT device.</span></span>

## <span data-ttu-id="d9240-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d9240-115">PARAMETERS</span></span>

### <span data-ttu-id="d9240-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9240-116">-DefaultProfile</span></span>
<span data-ttu-id="d9240-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d9240-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9240-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="d9240-118">-DeviceId</span></span>
<span data-ttu-id="d9240-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="d9240-119">Target Device Id.</span></span>

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

### <span data-ttu-id="d9240-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d9240-120">-InputObject</span></span>
<span data-ttu-id="d9240-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="d9240-121">IotHub object</span></span>

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

### <span data-ttu-id="d9240-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="d9240-122">-IotHubName</span></span>
<span data-ttu-id="d9240-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="d9240-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="d9240-124">-Tipo di digitare</span><span class="sxs-lookup"><span data-stu-id="d9240-124">-KeyType</span></span>
<span data-ttu-id="d9240-125">Tipo di chiave dei criteri di accesso condiviso per auth.</span><span class="sxs-lookup"><span data-stu-id="d9240-125">Shared access policy key type for auth.</span></span>

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

### <span data-ttu-id="d9240-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9240-126">-ResourceGroupName</span></span>
<span data-ttu-id="d9240-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d9240-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d9240-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d9240-128">-ResourceId</span></span>
<span data-ttu-id="d9240-129">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="d9240-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="d9240-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9240-130">CommonParameters</span></span>
<span data-ttu-id="d9240-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9240-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9240-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d9240-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9240-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d9240-133">INPUTS</span></span>

### <span data-ttu-id="d9240-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="d9240-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="d9240-135">System. String</span><span class="sxs-lookup"><span data-stu-id="d9240-135">System.String</span></span>

## <span data-ttu-id="d9240-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d9240-136">OUTPUTS</span></span>

### <span data-ttu-id="d9240-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span><span class="sxs-lookup"><span data-stu-id="d9240-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceConnectionString</span></span>

## <span data-ttu-id="d9240-138">Note</span><span class="sxs-lookup"><span data-stu-id="d9240-138">NOTES</span></span>

## <span data-ttu-id="d9240-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d9240-139">RELATED LINKS</span></span>
