---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Update-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: 80032ab2a677683ff876aca499f7e0ee682e6fd6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518679"
---
# <span data-ttu-id="b267f-101">Update-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="b267f-101">Update-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="b267f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b267f-102">SYNOPSIS</span></span>
<span data-ttu-id="b267f-103">Aggiornare un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="b267f-103">Update an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b267f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b267f-104">SYNTAX</span></span>

### <span data-ttu-id="b267f-105">ResourceUpdateSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b267f-105">ResourceUpdateSet (Default)</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b267f-106">InputObjectUpdateSet</span><span class="sxs-lookup"><span data-stu-id="b267f-106">InputObjectUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-Tag] <Hashtable>
 [-Reset] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b267f-107">InputObjectCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="b267f-107">InputObjectCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b267f-108">ResourceIdUpdateSet</span><span class="sxs-lookup"><span data-stu-id="b267f-108">ResourceIdUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-Tag] <Hashtable> [-Reset]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b267f-109">ResourceIdCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="b267f-109">ResourceIdCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-AllocationPolicy] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b267f-110">ResourceCreateUpdateSet</span><span class="sxs-lookup"><span data-stu-id="b267f-110">ResourceCreateUpdateSet</span></span>
```
Update-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String>
 [-AllocationPolicy] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b267f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b267f-111">DESCRIPTION</span></span>
<span data-ttu-id="b267f-112">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b267f-112">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b267f-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b267f-113">EXAMPLES</span></span>

### <span data-ttu-id="b267f-114">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b267f-114">Example 1</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -AllocationPolicy "GeoLatency"

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

<span data-ttu-id="b267f-115">Aggiornare i criteri di allocazione a "geolatenza" di un servizio di provisioning del dispositivo hub Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="b267f-115">Update Allocation Policy to "GeoLatency" of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="b267f-116">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b267f-116">Example 2</span></span>
```
PS C:\> Update-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -Tag @tags

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

<span data-ttu-id="b267f-117">Aggiungi " @tags " al contrassegno di un servizio di provisioning del dispositivo hub di Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="b267f-117">Add "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps".</span></span>

### <span data-ttu-id="b267f-118">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="b267f-118">Example 3</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Update-AzureRmIoTDps -Tag @tags -Reset

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

<span data-ttu-id="b267f-119">Elimina tag e Aggiungi nuovo " @tags " al contrassegno di un servizio di provisioning del dispositivo hub di Azure molto "myiotdps" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="b267f-119">Delete Tag and add new "@tags" to the Tag of an Azure IoT Hub device provisioning service "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="b267f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b267f-120">PARAMETERS</span></span>

### <span data-ttu-id="b267f-121">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="b267f-121">-AllocationPolicy</span></span>
<span data-ttu-id="b267f-122">Criteri di allocazione dei servizi per il provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="b267f-122">IoT Device Provisioning Service Allocation policy</span></span>

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

### <span data-ttu-id="b267f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b267f-123">-DefaultProfile</span></span>
<span data-ttu-id="b267f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b267f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b267f-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b267f-125">-InputObject</span></span>
<span data-ttu-id="b267f-126">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="b267f-126">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b267f-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="b267f-127">-Name</span></span>
<span data-ttu-id="b267f-128">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="b267f-128">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b267f-129">-Reset</span><span class="sxs-lookup"><span data-stu-id="b267f-129">-Reset</span></span>
<span data-ttu-id="b267f-130">Reimpostare i tag del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b267f-130">Reset IoT Device Provisioning Service Tags</span></span>

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

### <span data-ttu-id="b267f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b267f-131">-ResourceGroupName</span></span>
<span data-ttu-id="b267f-132">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b267f-132">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b267f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b267f-133">-ResourceId</span></span>
<span data-ttu-id="b267f-134">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b267f-134">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b267f-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="b267f-135">-Tag</span></span>
<span data-ttu-id="b267f-136">Raccolta di tag del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="b267f-136">IoT Device Provisioning Service Tag collection</span></span>

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

### <span data-ttu-id="b267f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b267f-137">-Confirm</span></span>
<span data-ttu-id="b267f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b267f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b267f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b267f-139">-WhatIf</span></span>
<span data-ttu-id="b267f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b267f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b267f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b267f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b267f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b267f-142">CommonParameters</span></span>
<span data-ttu-id="b267f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b267f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b267f-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b267f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b267f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b267f-145">INPUTS</span></span>

### <span data-ttu-id="b267f-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b267f-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="b267f-147">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b267f-147">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b267f-148">System. String</span><span class="sxs-lookup"><span data-stu-id="b267f-148">System.String</span></span>

## <span data-ttu-id="b267f-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b267f-149">OUTPUTS</span></span>

### <span data-ttu-id="b267f-150">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b267f-150">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

## <span data-ttu-id="b267f-151">Note</span><span class="sxs-lookup"><span data-stu-id="b267f-151">NOTES</span></span>

## <span data-ttu-id="b267f-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b267f-152">RELATED LINKS</span></span>
