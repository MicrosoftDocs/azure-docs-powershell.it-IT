---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: dd9bc81ef24530369a26ff290270a39c8ab1ff40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507471"
---
# <span data-ttu-id="c1442-101">Get-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="c1442-101">Get-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="c1442-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c1442-102">SYNOPSIS</span></span>
<span data-ttu-id="c1442-103">Elenca tutti o Mostra i dettagli dei servizi di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="c1442-103">List all or show details of Azure IoT Hub device provisioning services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c1442-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c1442-104">SYNTAX</span></span>

### <span data-ttu-id="c1442-105">ListIotDpsByResourceGroup (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c1442-105">ListIotDpsByResourceGroup (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningService [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c1442-106">GetIotDpsByName</span><span class="sxs-lookup"><span data-stu-id="c1442-106">GetIotDpsByName</span></span>
```
Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1442-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c1442-107">DESCRIPTION</span></span>
<span data-ttu-id="c1442-108">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="c1442-108">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="c1442-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c1442-109">EXAMPLES</span></span>

### <span data-ttu-id="c1442-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="c1442-110">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----   
myresourcegroup0    myiotdps0   eastus      myiotdps0.azure-devices-provisioning.net    0       Static              0       Active
myresourcegroup1    myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    4       Hashed              0       Active
myresourcegroup1    myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c1442-111">Elenca tutti i servizi di provisioning del dispositivo hub di Azure molto in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c1442-111">List all Azure IoT Hub device provisioning services in a subscription.</span></span>

### <span data-ttu-id="c1442-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="c1442-112">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup"

ResourceGroupName   Name        Location    ServiceOperationsHostName                   IotHubs AllocationPolicy    Tags    State
-----------------   ----        --------    -------------------------                   ------- ----------------    ----    -----
myresourcegroup     myiotdps1   eastus      myiotdps1.azure-devices-provisioning.net    1       Hashed              0       Active
myresourcegroup     myiotdps2   westus      myiotdps2.azure-devices-provisioning.net    4       GeoLatency          0       Active
```

<span data-ttu-id="c1442-113">Elenca tutti i servizi di provisioning del dispositivo hub di Azure molto nel gruppo di risorse "myresourcegroup".</span><span class="sxs-lookup"><span data-stu-id="c1442-113">List all Azure IoT Hub device provisioning services in the resource group 'myresourcegroup'.</span></span>

### <span data-ttu-id="c1442-114">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="c1442-114">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

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

<span data-ttu-id="c1442-115">Mostra i dettagli di un servizio di provisioning del dispositivo hub di Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="c1442-115">Show details of an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

## <span data-ttu-id="c1442-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c1442-116">PARAMETERS</span></span>

### <span data-ttu-id="c1442-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1442-117">-DefaultProfile</span></span>
<span data-ttu-id="c1442-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c1442-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1442-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="c1442-119">-Name</span></span>
<span data-ttu-id="c1442-120">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="c1442-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="c1442-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1442-121">-ResourceGroupName</span></span>
<span data-ttu-id="c1442-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="c1442-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c1442-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1442-123">CommonParameters</span></span>
<span data-ttu-id="c1442-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1442-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1442-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1442-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1442-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c1442-126">INPUTS</span></span>

### <span data-ttu-id="c1442-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c1442-127">None</span></span>

## <span data-ttu-id="c1442-128">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c1442-128">OUTPUTS</span></span>

### <span data-ttu-id="c1442-129">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="c1442-129">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="c1442-130">Note</span><span class="sxs-lookup"><span data-stu-id="c1442-130">NOTES</span></span>

## <span data-ttu-id="c1442-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c1442-131">RELATED LINKS</span></span>
