---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningService.md
ms.openlocfilehash: 4701070ae7810b86ff7567f73b39606909d7fa10
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190209"
---
# <span data-ttu-id="d5ecc-101">Remove-AzIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="d5ecc-101">Remove-AzIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="d5ecc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d5ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ecc-103">Eliminare un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-103">Delete an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d5ecc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d5ecc-104">SYNTAX</span></span>

### <span data-ttu-id="d5ecc-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d5ecc-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5ecc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d5ecc-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5ecc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d5ecc-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5ecc-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d5ecc-108">DESCRIPTION</span></span>
<span data-ttu-id="d5ecc-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="d5ecc-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="d5ecc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d5ecc-110">EXAMPLES</span></span>

### <span data-ttu-id="d5ecc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d5ecc-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="d5ecc-112">Eliminare un servizio di provisioning del dispositivo hub di Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="d5ecc-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="d5ecc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="d5ecc-113">Example 2</span></span>
```
PS C:\> Get-AzIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzIotDps
```

<span data-ttu-id="d5ecc-114">Eliminare un dispositivo hub di Azure molto per il provisioning del servizio "myiotdps" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="d5ecc-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d5ecc-115">PARAMETERS</span></span>

### <span data-ttu-id="d5ecc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ecc-116">-DefaultProfile</span></span>
<span data-ttu-id="d5ecc-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5ecc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5ecc-118">-InputObject</span></span>
<span data-ttu-id="d5ecc-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="d5ecc-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="d5ecc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="d5ecc-120">-Name</span></span>
<span data-ttu-id="d5ecc-121">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="d5ecc-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d5ecc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d5ecc-122">-PassThru</span></span>
<span data-ttu-id="d5ecc-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d5ecc-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d5ecc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d5ecc-124">-ResourceGroupName</span></span>
<span data-ttu-id="d5ecc-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d5ecc-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d5ecc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d5ecc-126">-ResourceId</span></span>
<span data-ttu-id="d5ecc-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d5ecc-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="d5ecc-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d5ecc-128">-Confirm</span></span>
<span data-ttu-id="d5ecc-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d5ecc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5ecc-130">-WhatIf</span></span>
<span data-ttu-id="d5ecc-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5ecc-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d5ecc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ecc-133">CommonParameters</span></span>
<span data-ttu-id="d5ecc-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ecc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ecc-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d5ecc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ecc-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d5ecc-136">INPUTS</span></span>

### <span data-ttu-id="d5ecc-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="d5ecc-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="d5ecc-138">System. String</span><span class="sxs-lookup"><span data-stu-id="d5ecc-138">System.String</span></span>

## <span data-ttu-id="d5ecc-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d5ecc-139">OUTPUTS</span></span>

### <span data-ttu-id="d5ecc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d5ecc-140">System.Boolean</span></span>

## <span data-ttu-id="d5ecc-141">Note</span><span class="sxs-lookup"><span data-stu-id="d5ecc-141">NOTES</span></span>

## <span data-ttu-id="d5ecc-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d5ecc-142">RELATED LINKS</span></span>