---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 3102cafabecb5df8daea15a40eb179405c6c0ea8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193467"
---
# <span data-ttu-id="b0d63-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="b0d63-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="b0d63-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b0d63-102">SYNOPSIS</span></span>
<span data-ttu-id="b0d63-103">Creare un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="b0d63-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="b0d63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b0d63-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b0d63-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b0d63-105">DESCRIPTION</span></span>
<span data-ttu-id="b0d63-106">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b0d63-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b0d63-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b0d63-107">EXAMPLES</span></span>

### <span data-ttu-id="b0d63-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b0d63-108">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
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

<span data-ttu-id="b0d63-109">Creare un servizio di provisioning del dispositivo hub Azure molto con il livello di prezzo standard S1 nell'area del gruppo risorse.</span><span class="sxs-lookup"><span data-stu-id="b0d63-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the region of the resource group.</span></span>

### <span data-ttu-id="b0d63-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b0d63-110">Example 2</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Location "eastus"

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
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="b0d63-111">Creare un servizio di provisioning del dispositivo hub di Azure molto con il livello di prezzo standard S1 nella regione "eastus".</span><span class="sxs-lookup"><span data-stu-id="b0d63-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="b0d63-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b0d63-112">PARAMETERS</span></span>

### <span data-ttu-id="b0d63-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="b0d63-113">-AllocationPolicy</span></span>
<span data-ttu-id="b0d63-114">Criteri di allocazione dei servizi per il provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="b0d63-114">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d63-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0d63-115">-DefaultProfile</span></span>
<span data-ttu-id="b0d63-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b0d63-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b0d63-117">-Posizione</span><span class="sxs-lookup"><span data-stu-id="b0d63-117">-Location</span></span>
<span data-ttu-id="b0d63-118">Posizione</span><span class="sxs-lookup"><span data-stu-id="b0d63-118">Location</span></span>

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

### <span data-ttu-id="b0d63-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="b0d63-119">-Name</span></span>
<span data-ttu-id="b0d63-120">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="b0d63-120">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d63-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0d63-121">-ResourceGroupName</span></span>
<span data-ttu-id="b0d63-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b0d63-122">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d63-123">-SkuName</span><span class="sxs-lookup"><span data-stu-id="b0d63-123">-SkuName</span></span>
<span data-ttu-id="b0d63-124">SKU</span><span class="sxs-lookup"><span data-stu-id="b0d63-124">Sku</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: S1

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0d63-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b0d63-125">-Confirm</span></span>
<span data-ttu-id="b0d63-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b0d63-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b0d63-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b0d63-127">-WhatIf</span></span>
<span data-ttu-id="b0d63-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0d63-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b0d63-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b0d63-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b0d63-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0d63-130">CommonParameters</span></span>
<span data-ttu-id="b0d63-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0d63-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0d63-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0d63-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0d63-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b0d63-133">INPUTS</span></span>

### <span data-ttu-id="b0d63-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="b0d63-134">None</span></span>

## <span data-ttu-id="b0d63-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b0d63-135">OUTPUTS</span></span>

### <span data-ttu-id="b0d63-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b0d63-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="b0d63-137">Note</span><span class="sxs-lookup"><span data-stu-id="b0d63-137">NOTES</span></span>

## <span data-ttu-id="b0d63-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b0d63-138">RELATED LINKS</span></span>