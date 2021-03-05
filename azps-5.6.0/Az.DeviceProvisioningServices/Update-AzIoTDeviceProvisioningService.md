---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 7e1181ba837f0d2447a46f051765b0430399b123
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985066"
---
# <span data-ttu-id="ab2b2-101">Update-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="ab2b2-101">Update-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="ab2b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ab2b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ab2b2-103">Aggiornare un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-103">Update an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ab2b2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab2b2-104">SYNTAX</span></span>

### <span data-ttu-id="ab2b2-105">ResourceUpdateSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab2b2-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2b2-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="ab2b2-106">InputObjectUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2b2-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="ab2b2-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab2b2-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="ab2b2-108">ResourceIdUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2b2-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="ab2b2-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab2b2-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="ab2b2-110">ResourceCreateUpdateSet</span></span>
```
Update-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ab2b2-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ab2b2-111">DESCRIPTION</span></span>
<span data-ttu-id="ab2b2-112">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ab2b2-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ab2b2-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab2b2-113">EXAMPLES</span></span>

### <span data-ttu-id="ab2b2-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab2b2-114">Example 1</span></span>
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

<span data-ttu-id="ab2b2-115">Aggiornare i criteri di assegnazione a "GeoLatency" di un servizio di provisioning del dispositivo Hub IoT di Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="ab2b2-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="ab2b2-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ab2b2-116">Example 2</span></span>
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

<span data-ttu-id="ab2b2-117">Aggiungere tag a un servizio di provisioning dei dispositivi Hub IoT di Azure "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="ab2b2-117">Add tags to an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="ab2b2-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="ab2b2-118">Example 3</span></span>
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

<span data-ttu-id="ab2b2-119">Eliminare il tag e aggiungere nuovi tag a un servizio di provisioning dei dispositivi Hub IoT di Azure "myiotdps" usando una pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-119">Delete Tag and add new tags to an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="ab2b2-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ab2b2-120">PARAMETERS</span></span>

### <span data-ttu-id="ab2b2-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="ab2b2-121">-AllocationPolicy</span></span>
<span data-ttu-id="ab2b2-122">Criterio di assegnazione del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="ab2b2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab2b2-123">-DefaultProfile</span></span>
<span data-ttu-id="ab2b2-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab2b2-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab2b2-125">-InputObject</span></span>
<span data-ttu-id="ab2b2-126">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ab2b2-127">-Name</span><span class="sxs-lookup"><span data-stu-id="ab2b2-127">-Name</span></span>
<span data-ttu-id="ab2b2-128">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ab2b2-129">-Reimposta</span><span class="sxs-lookup"><span data-stu-id="ab2b2-129">-Reset</span></span>
<span data-ttu-id="ab2b2-130">Reimpostare i tag di servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="ab2b2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab2b2-131">-ResourceGroupName</span></span>
<span data-ttu-id="ab2b2-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ab2b2-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ab2b2-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab2b2-133">-ResourceId</span></span>
<span data-ttu-id="ab2b2-134">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ab2b2-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="ab2b2-135">-Tag</span></span>
<span data-ttu-id="ab2b2-136">Raccolta di tag di servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="ab2b2-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ab2b2-137">-Confirm</span></span>
<span data-ttu-id="ab2b2-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab2b2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab2b2-139">-WhatIf</span></span>
<span data-ttu-id="ab2b2-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab2b2-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab2b2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab2b2-142">CommonParameters</span></span>
<span data-ttu-id="ab2b2-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab2b2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab2b2-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab2b2-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab2b2-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-145">INPUTS</span></span>

### <span data-ttu-id="ab2b2-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ab2b2-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="ab2b2-147">System.String</span><span class="sxs-lookup"><span data-stu-id="ab2b2-147">System.String</span></span>

## <span data-ttu-id="ab2b2-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab2b2-148">OUTPUTS</span></span>

### <span data-ttu-id="ab2b2-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="ab2b2-149">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="ab2b2-150">NOTE</span><span class="sxs-lookup"><span data-stu-id="ab2b2-150">NOTES</span></span>

## <span data-ttu-id="ab2b2-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab2b2-151">RELATED LINKS</span></span>
