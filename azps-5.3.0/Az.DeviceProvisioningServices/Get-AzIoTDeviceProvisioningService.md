---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: ab6dd43cff746d670fe05d66d983836433323728
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475324"
---
# <span data-ttu-id="33d47-101">Get-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="33d47-101">Get-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="33d47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33d47-102">SYNOPSIS</span></span>
<span data-ttu-id="33d47-103">Elenca tutti o Mostra i dettagli dei servizi di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="33d47-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

## <span data-ttu-id="33d47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33d47-104">SYNTAX</span></span>

### <span data-ttu-id="33d47-105">ListIotDpsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33d47-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzIoTDeviceProvisioningService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="33d47-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="33d47-106">GetIotDpsByName</span></span>
```
Get-AzIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33d47-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33d47-107">DESCRIPTION</span></span>
<span data-ttu-id="33d47-108">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="33d47-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="33d47-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33d47-109">EXAMPLES</span></span>

### <span data-ttu-id="33d47-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="33d47-110">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="33d47-111">Elenca tutti i servizi di provisioning del dispositivo hub di Azure molto in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="33d47-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="33d47-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="33d47-112">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="33d47-113">Elenca tutti i servizi di provisioning del dispositivo hub di Azure molto nel gruppo di risorse "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="33d47-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="33d47-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="33d47-114">Example 3</span></span>
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

<span data-ttu-id="33d47-115">Mostra i dettagli di un servizio di provisioning del dispositivo hub di Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="33d47-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="33d47-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33d47-116">PARAMETERS</span></span>

### <span data-ttu-id="33d47-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33d47-117">-DefaultProfile</span></span>
<span data-ttu-id="33d47-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33d47-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33d47-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="33d47-119">-Name</span></span>
<span data-ttu-id="33d47-120">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="33d47-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="33d47-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33d47-121">-ResourceGroupName</span></span>
<span data-ttu-id="33d47-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="33d47-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="33d47-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33d47-123">CommonParameters</span></span>
<span data-ttu-id="33d47-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33d47-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33d47-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33d47-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33d47-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33d47-126">INPUTS</span></span>

### <span data-ttu-id="33d47-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="33d47-127">None</span></span>

## <span data-ttu-id="33d47-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33d47-128">OUTPUTS</span></span>

### <span data-ttu-id="33d47-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="33d47-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="33d47-130">Note</span><span class="sxs-lookup"><span data-stu-id="33d47-130">NOTES</span></span>

## <span data-ttu-id="33d47-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33d47-131">RELATED LINKS</span></span>
