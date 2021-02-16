---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209667"
---
# <span data-ttu-id="1cc89-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="1cc89-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="1cc89-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1cc89-102">SYNOPSIS</span></span>
<span data-ttu-id="1cc89-103">Eliminare un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc89-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1cc89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1cc89-104">SYNTAX</span></span>

### <span data-ttu-id="1cc89-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1cc89-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc89-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1cc89-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1cc89-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1cc89-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1cc89-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1cc89-108">DESCRIPTION</span></span>
<span data-ttu-id="1cc89-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1cc89-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1cc89-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1cc89-110">EXAMPLES</span></span>

### <span data-ttu-id="1cc89-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1cc89-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="1cc89-112">Eliminare un servizio di provisioning dei dispositivi Hub IoT di Azure 'myiotdps'.</span><span class="sxs-lookup"><span data-stu-id="1cc89-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="1cc89-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1cc89-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="1cc89-114">Eliminare un servizio di provisioning dei dispositivi Hub IoT di Azure 'myiotdps' usando una pipeline.</span><span class="sxs-lookup"><span data-stu-id="1cc89-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="1cc89-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1cc89-115">PARAMETERS</span></span>

### <span data-ttu-id="1cc89-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1cc89-116">-DefaultProfile</span></span>
<span data-ttu-id="1cc89-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1cc89-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1cc89-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1cc89-118">-InputObject</span></span>
<span data-ttu-id="1cc89-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="1cc89-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1cc89-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1cc89-120">-Name</span></span>
<span data-ttu-id="1cc89-121">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="1cc89-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1cc89-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1cc89-122">-PassThru</span></span>
<span data-ttu-id="1cc89-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1cc89-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1cc89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1cc89-124">-ResourceGroupName</span></span>
<span data-ttu-id="1cc89-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1cc89-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1cc89-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1cc89-126">-ResourceId</span></span>
<span data-ttu-id="1cc89-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="1cc89-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1cc89-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1cc89-128">-Confirm</span></span>
<span data-ttu-id="1cc89-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1cc89-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1cc89-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1cc89-130">-WhatIf</span></span>
<span data-ttu-id="1cc89-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc89-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1cc89-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1cc89-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1cc89-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1cc89-133">CommonParameters</span></span>
<span data-ttu-id="1cc89-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1cc89-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1cc89-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1cc89-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1cc89-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="1cc89-136">INPUTS</span></span>

### <span data-ttu-id="1cc89-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1cc89-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="1cc89-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1cc89-138">System.String</span></span>

## <span data-ttu-id="1cc89-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1cc89-139">OUTPUTS</span></span>

### <span data-ttu-id="1cc89-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1cc89-140">System.Boolean</span></span>

## <span data-ttu-id="1cc89-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="1cc89-141">NOTES</span></span>

## <span data-ttu-id="1cc89-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1cc89-142">RELATED LINKS</span></span>
