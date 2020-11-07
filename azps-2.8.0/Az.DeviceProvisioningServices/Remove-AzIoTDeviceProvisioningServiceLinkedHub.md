---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicelinkedhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: ae7335c6430001affa76894dac6334036d1f04d4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674533"
---
# <span data-ttu-id="7d70b-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="7d70b-101">Remove-AzIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="7d70b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d70b-102">SYNOPSIS</span></span>
<span data-ttu-id="7d70b-103">Elimina un hub collegato in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="7d70b-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7d70b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d70b-104">SYNTAX</span></span>

### <span data-ttu-id="7d70b-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7d70b-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7d70b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7d70b-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7d70b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7d70b-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d70b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d70b-108">DESCRIPTION</span></span>
<span data-ttu-id="7d70b-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="7d70b-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="7d70b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d70b-110">EXAMPLES</span></span>

### <span data-ttu-id="7d70b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d70b-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="7d70b-112">Eliminare l'hub degli altri collegamenti "myiothub" in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="7d70b-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="7d70b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7d70b-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzIoTDpsHub
```

<span data-ttu-id="7d70b-114">Eliminare l'hub degli altri collegamenti "myiothub" in un servizio di provisioning del dispositivo hub di Azure molto usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="7d70b-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="7d70b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d70b-115">PARAMETERS</span></span>

### <span data-ttu-id="7d70b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d70b-116">-DefaultProfile</span></span>
<span data-ttu-id="7d70b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d70b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7d70b-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7d70b-118">-InputObject</span></span>
<span data-ttu-id="7d70b-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="7d70b-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7d70b-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="7d70b-120">-LinkedHubName</span></span>
<span data-ttu-id="7d70b-121">Nome host dell'hub degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="7d70b-121">Host name of linked IoT Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d70b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="7d70b-122">-Name</span></span>
<span data-ttu-id="7d70b-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="7d70b-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7d70b-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7d70b-124">-PassThru</span></span>
<span data-ttu-id="7d70b-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7d70b-125">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d70b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d70b-126">-ResourceGroupName</span></span>
<span data-ttu-id="7d70b-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7d70b-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7d70b-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7d70b-128">-ResourceId</span></span>
<span data-ttu-id="7d70b-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7d70b-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7d70b-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d70b-130">-Confirm</span></span>
<span data-ttu-id="7d70b-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d70b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d70b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d70b-132">-WhatIf</span></span>
<span data-ttu-id="7d70b-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d70b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7d70b-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7d70b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7d70b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d70b-135">CommonParameters</span></span>
<span data-ttu-id="7d70b-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d70b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d70b-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d70b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d70b-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d70b-138">INPUTS</span></span>

### <span data-ttu-id="7d70b-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="7d70b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>

### <span data-ttu-id="7d70b-140">System. String</span><span class="sxs-lookup"><span data-stu-id="7d70b-140">System.String</span></span>

## <span data-ttu-id="7d70b-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d70b-141">OUTPUTS</span></span>

### <span data-ttu-id="7d70b-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d70b-142">System.Boolean</span></span>

## <span data-ttu-id="7d70b-143">Note</span><span class="sxs-lookup"><span data-stu-id="7d70b-143">NOTES</span></span>

## <span data-ttu-id="7d70b-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d70b-144">RELATED LINKS</span></span>
