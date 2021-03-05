---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: bb6094644b9f2cbd831aa8d64a142d5888a5bcc4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013646"
---
# <span data-ttu-id="09444-101">New-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="09444-101">New-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="09444-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09444-102">SYNOPSIS</span></span>
<span data-ttu-id="09444-103">Creare un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="09444-103">Create an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="09444-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09444-104">SYNTAX</span></span>

```
New-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Location <String>]
 [-AllocationPolicy <String>] [-SkuName <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09444-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="09444-105">DESCRIPTION</span></span>
<span data-ttu-id="09444-106">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="09444-106">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="09444-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09444-107">EXAMPLES</span></span>

### <span data-ttu-id="09444-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09444-108">Example 1</span></span>
```
PS C:\> $tags = @{}
PS C:\> $tags.Add('key1','value1')
PS C:\> New-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tags

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Location                    : westus
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {[key1, value1]}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="09444-109">Creare un servizio di provisioning di dispositivi Hub Azure IoT con lo standard pricing tier S1 e tag, nell'area del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="09444-109">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1 and tags, in the region of the resource group.</span></span>

### <span data-ttu-id="09444-110">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="09444-110">Example 2</span></span>
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

<span data-ttu-id="09444-111">Crea un servizio di provisioning dei dispositivi Hub Azure IoT con il livello di prezzi standard S1, nell'area "estus".</span><span class="sxs-lookup"><span data-stu-id="09444-111">Create an Azure IoT Hub device provisioning service with the standard pricing tier S1, in the 'eastus' region.</span></span>

## <span data-ttu-id="09444-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="09444-112">PARAMETERS</span></span>

### <span data-ttu-id="09444-113">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="09444-113">-AllocationPolicy</span></span>
<span data-ttu-id="09444-114">Criterio di assegnazione del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="09444-114">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="09444-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09444-115">-DefaultProfile</span></span>
<span data-ttu-id="09444-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09444-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09444-117">-Location</span><span class="sxs-lookup"><span data-stu-id="09444-117">-Location</span></span>
<span data-ttu-id="09444-118">Posizione</span><span class="sxs-lookup"><span data-stu-id="09444-118">Location</span></span>

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

### <span data-ttu-id="09444-119">-Name</span><span class="sxs-lookup"><span data-stu-id="09444-119">-Name</span></span>
<span data-ttu-id="09444-120">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="09444-120">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="09444-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09444-121">-ResourceGroupName</span></span>
<span data-ttu-id="09444-122">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="09444-122">Name of the Resource Group</span></span>

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

### <span data-ttu-id="09444-123">-SKUName</span><span class="sxs-lookup"><span data-stu-id="09444-123">-SkuName</span></span>
<span data-ttu-id="09444-124">SKU</span><span class="sxs-lookup"><span data-stu-id="09444-124">Sku</span></span>

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

### <span data-ttu-id="09444-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="09444-125">-Tag</span></span>
<span data-ttu-id="09444-126">Tag di istanza del servizio di provisioning dei dispositivi IoT.</span><span class="sxs-lookup"><span data-stu-id="09444-126">IoT Device Provisioning Service instance tags.</span></span> <span data-ttu-id="09444-127">Il bag delle proprietà in coppie chiave-valore sotto forma di tabella hash.</span><span class="sxs-lookup"><span data-stu-id="09444-127">Property bag in key-value pairs in the form of a hash table.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09444-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="09444-128">-Confirm</span></span>
<span data-ttu-id="09444-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09444-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09444-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09444-130">-WhatIf</span></span>
<span data-ttu-id="09444-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09444-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09444-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09444-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09444-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09444-133">CommonParameters</span></span>
<span data-ttu-id="09444-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09444-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09444-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09444-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09444-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="09444-136">INPUTS</span></span>

### <span data-ttu-id="09444-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="09444-137">None</span></span>

## <span data-ttu-id="09444-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09444-138">OUTPUTS</span></span>

### <span data-ttu-id="09444-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="09444-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="09444-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="09444-140">NOTES</span></span>

## <span data-ttu-id="09444-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09444-141">RELATED LINKS</span></span>
