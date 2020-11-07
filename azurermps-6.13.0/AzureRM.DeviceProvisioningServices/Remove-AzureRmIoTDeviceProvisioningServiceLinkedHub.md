---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub.md
ms.openlocfilehash: f50c0955d56b42c341b6a1a6b64b1993ee66175e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688121"
---
# <span data-ttu-id="ab0ab-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span><span class="sxs-lookup"><span data-stu-id="ab0ab-101">Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub</span></span>

## <span data-ttu-id="ab0ab-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab0ab-102">SYNOPSIS</span></span>
<span data-ttu-id="ab0ab-103">Elimina un hub collegato in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-103">Delete a linked IoT hub in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab0ab-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab0ab-104">SYNTAX</span></span>

### <span data-ttu-id="ab0ab-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ab0ab-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceGroupName] <String> [-Name] <String>
 [-LinkedHubName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ab0ab-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ab0ab-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-InputObject] <PSIotHubDefinitionDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab0ab-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ab0ab-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub [-ResourceId] <String> [-LinkedHubName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab0ab-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab0ab-108">DESCRIPTION</span></span>
<span data-ttu-id="ab0ab-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ab0ab-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ab0ab-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab0ab-110">EXAMPLES</span></span>

### <span data-ttu-id="ab0ab-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ab0ab-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceLinkedHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" -PassThru

True
```

<span data-ttu-id="ab0ab-112">Eliminare l'hub degli altri collegamenti "myiothub" in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-112">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="ab0ab-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ab0ab-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsHub -ResourceGroupName "myresourcegroup" -Name "myiotdps" -LinkedHubName "myiothub" | Remove-AzureRmIoTDpsHub
```

<span data-ttu-id="ab0ab-114">Eliminare l'hub degli altri collegamenti "myiothub" in un servizio di provisioning del dispositivo hub di Azure molto usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-114">Delete linked IoT hub "myiothub" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="ab0ab-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab0ab-115">PARAMETERS</span></span>

### <span data-ttu-id="ab0ab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab0ab-116">-DefaultProfile</span></span>
<span data-ttu-id="ab0ab-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab0ab-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ab0ab-118">-InputObject</span></span>
<span data-ttu-id="ab0ab-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="ab0ab-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ab0ab-120">-LinkedHubName</span><span class="sxs-lookup"><span data-stu-id="ab0ab-120">-LinkedHubName</span></span>
<span data-ttu-id="ab0ab-121">Nome host dell'hub degli Stati Uniti</span><span class="sxs-lookup"><span data-stu-id="ab0ab-121">Host name of linked IoT Hub</span></span>

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

### <span data-ttu-id="ab0ab-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab0ab-122">-Name</span></span>
<span data-ttu-id="ab0ab-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="ab0ab-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ab0ab-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab0ab-124">-PassThru</span></span>
<span data-ttu-id="ab0ab-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ab0ab-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ab0ab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ab0ab-126">-ResourceGroupName</span></span>
<span data-ttu-id="ab0ab-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ab0ab-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ab0ab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab0ab-128">-ResourceId</span></span>
<span data-ttu-id="ab0ab-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ab0ab-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ab0ab-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab0ab-130">-Confirm</span></span>
<span data-ttu-id="ab0ab-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab0ab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab0ab-132">-WhatIf</span></span>
<span data-ttu-id="ab0ab-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab0ab-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab0ab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab0ab-135">CommonParameters</span></span>
<span data-ttu-id="ab0ab-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab0ab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab0ab-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab0ab-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab0ab-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab0ab-138">INPUTS</span></span>

### <span data-ttu-id="ab0ab-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIotHubDefinitionDescription</span><span class="sxs-lookup"><span data-stu-id="ab0ab-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIotHubDefinitionDescription</span></span>
<span data-ttu-id="ab0ab-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="ab0ab-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="ab0ab-141">System. String</span><span class="sxs-lookup"><span data-stu-id="ab0ab-141">System.String</span></span>

## <span data-ttu-id="ab0ab-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab0ab-142">OUTPUTS</span></span>

### <span data-ttu-id="ab0ab-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab0ab-143">System.Boolean</span></span>

## <span data-ttu-id="ab0ab-144">Note</span><span class="sxs-lookup"><span data-stu-id="ab0ab-144">NOTES</span></span>

## <span data-ttu-id="ab0ab-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab0ab-145">RELATED LINKS</span></span>
