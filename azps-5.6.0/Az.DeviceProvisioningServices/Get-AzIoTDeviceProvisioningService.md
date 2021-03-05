---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ee86af7862ad22b34e159f1d5097d5d30a4cba8d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015358"
---
# <span data-ttu-id="92dbe-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="92dbe-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="92dbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="92dbe-102">SYNOPSIS</span></span>
<span data-ttu-id="92dbe-103">Elencare tutti i servizi di provisioning dei dispositivi Hub IoT di Azure o mostrarne i dettagli.</span><span class="sxs-lookup"><span data-stu-id="92dbe-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="92dbe-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="92dbe-104">SYNTAX</span></span>

### <span data-ttu-id="92dbe-105">ListIotDpsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="92dbe-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="92dbe-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="92dbe-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92dbe-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="92dbe-107">DESCRIPTION</span></span>
<span data-ttu-id="92dbe-108">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="92dbe-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="92dbe-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="92dbe-109">EXAMPLES</span></span>

### <span data-ttu-id="92dbe-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="92dbe-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="92dbe-111">Elencare tutti i servizi di provisioning dei dispositivi Hub Azure IoT in una sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="92dbe-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="92dbe-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="92dbe-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="92dbe-113">Elencare tutti i servizi di provisioning dei dispositivi Hub Azure IoT nel gruppo di risorse 'myresourcegroup'.</span><span class="sxs-lookup"><span data-stu-id="92dbe-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="92dbe-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="92dbe-114">Example 3</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : eastus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="92dbe-115">Mostra i dettagli di un servizio di provisioning dei dispositivi Hub IoT di Azure 'myiotdps'.</span><span class="sxs-lookup"><span data-stu-id="92dbe-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="92dbe-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="92dbe-116">PARAMETERS</span></span>

### <span data-ttu-id="92dbe-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92dbe-117">-DefaultProfile</span></span>
<span data-ttu-id="92dbe-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="92dbe-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="92dbe-119">-Name</span><span class="sxs-lookup"><span data-stu-id="92dbe-119">-Name</span></span>
<span data-ttu-id="92dbe-120">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="92dbe-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92dbe-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92dbe-121">-ResourceGroupName</span></span>
<span data-ttu-id="92dbe-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="92dbe-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ListIotDpsByResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetIotDpsByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92dbe-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92dbe-123">CommonParameters</span></span>
<span data-ttu-id="92dbe-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92dbe-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92dbe-125">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92dbe-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92dbe-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="92dbe-126">INPUTS</span></span>

### <span data-ttu-id="92dbe-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="92dbe-127">None</span></span>

## <span data-ttu-id="92dbe-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="92dbe-128">OUTPUTS</span></span>

### <span data-ttu-id="92dbe-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="92dbe-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="92dbe-130">NOTE</span><span class="sxs-lookup"><span data-stu-id="92dbe-130">NOTES</span></span>

## <span data-ttu-id="92dbe-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="92dbe-131">RELATED LINKS</span></span>
