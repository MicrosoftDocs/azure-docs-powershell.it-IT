---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: f533bd07d0c7b123f1d109e7abd933736093cd79
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194471"
---
# <span data-ttu-id="3582f-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="3582f-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="3582f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3582f-102">SYNOPSIS</span></span>
<span data-ttu-id="3582f-103">Aggiornare un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="3582f-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="3582f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3582f-104">SYNTAX</span></span>

### <span data-ttu-id="3582f-105">ResourceUpdateSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3582f-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3582f-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="3582f-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3582f-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="3582f-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3582f-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="3582f-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3582f-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="3582f-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3582f-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="3582f-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3582f-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3582f-111">DESCRIPTION</span></span>
<span data-ttu-id="3582f-112">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="3582f-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="3582f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3582f-113">EXAMPLES</span></span>

### <span data-ttu-id="3582f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3582f-114">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : GeoLatency
Tags                        : {}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAT52k=
```

<span data-ttu-id="3582f-115">Aggiornare i criteri di assegnazione a "GeoLatency" di un servizio di provisioning del dispositivo Hub IoT di Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="3582f-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="3582f-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="3582f-116">Example 2</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Update-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag $tag

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAPoOk=
```

<span data-ttu-id="3582f-117">Aggiungere tag a un servizio di provisioning dei dispositivi Hub IoT di Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="3582f-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="3582f-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="3582f-118">Example 3</span></span>
```
PS C:\> $tag = @{}
PS C:\> $tag.Add("key1","Value1")
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzIoTDps -Tag $tag -Reset

ResourceGroupName           : myresourcegroup
Name                        : myiotdps
Type                        : Microsoft.Devices/provisioningServices
ServiceOperationsHostName   : myiotdps.azure-devices-provisioning.net
IotHubs                     : 0
State                       : Active
AllocationPolicy            : Hashed
Tags                        : {['key1','Value1']}
SkuName                     : S1
SkuTier                     : Standard
Etag                        : AAAAAAAS1dY=
```

<span data-ttu-id="3582f-119">Eliminare il tag e aggiungere nuovi tag a un servizio di provisioning dei dispositivi Hub IoT di Azure "myiotdps" usando una pipeline.</span><span class="sxs-lookup"><span data-stu-id="3582f-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="3582f-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3582f-120">PARAMETERS</span></span>

### <span data-ttu-id="3582f-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="3582f-121">-AllocationPolicy</span></span>
<span data-ttu-id="3582f-122">Criterio di assegnazione del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3582f-122">IoT Device Provisioning Service Allocation policy</span></span>

```yaml
Type: System.String
Parameter Sets: InputObjectCreateUpdateSet, ResourceIdCreateUpdateSet, ResourceCreateUpdateSet
Aliases:
Accepted values: Hashed, GeoLatency, Static

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3582f-123">-DefaultProfile</span></span>
<span data-ttu-id="3582f-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3582f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3582f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3582f-125">-InputObject</span></span>
<span data-ttu-id="3582f-126">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3582f-126">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectUpdateSet, InputObjectCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-127">-Name</span><span class="sxs-lookup"><span data-stu-id="3582f-127">-Name</span></span>
<span data-ttu-id="3582f-128">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3582f-128">Name of the IoT Device Provisioning Service</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-129">-Reimposta</span><span class="sxs-lookup"><span data-stu-id="3582f-129">-Reset</span></span>
<span data-ttu-id="3582f-130">Reimpostare i tag di servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3582f-130">Reset IoT Device Provisioning Service Tags</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3582f-131">-ResourceGroupName</span></span>
<span data-ttu-id="3582f-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3582f-132">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceUpdateSet, ResourceCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3582f-133">-ResourceId</span></span>
<span data-ttu-id="3582f-134">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3582f-134">IoT Device Provisioning Service Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdUpdateSet, ResourceIdCreateUpdateSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="3582f-135">-Tag</span></span>
<span data-ttu-id="3582f-136">Raccolta di tag di servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="3582f-136">IoT Device Provisioning Service Tag collection</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ResourceUpdateSet, InputObjectUpdateSet, ResourceIdUpdateSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3582f-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3582f-137">-Confirm</span></span>
<span data-ttu-id="3582f-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3582f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3582f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3582f-139">-WhatIf</span></span>
<span data-ttu-id="3582f-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3582f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3582f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3582f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3582f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3582f-142">CommonParameters</span></span>
<span data-ttu-id="3582f-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3582f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3582f-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3582f-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3582f-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="3582f-145">INPUTS</span></span>

### <span data-ttu-id="3582f-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3582f-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="3582f-147">System.String</span><span class="sxs-lookup"><span data-stu-id="3582f-147">System.String</span></span>

## <span data-ttu-id="3582f-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3582f-148">OUTPUTS</span></span>

### <span data-ttu-id="3582f-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="3582f-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="3582f-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="3582f-150">NOTES</span></span>

## <span data-ttu-id="3582f-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3582f-151">RELATED LINKS</span></span>
