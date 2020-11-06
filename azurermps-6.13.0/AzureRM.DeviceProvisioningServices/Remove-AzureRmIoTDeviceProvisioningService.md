---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningService.md
ms.openlocfilehash: ecc91bb19b3d5d40f8c5aa3e4f25812a9999e45b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513848"
---
# <span data-ttu-id="b97ec-101">Remove-AzureRmIoTDeviceProvisioningService</span><span class="sxs-lookup"><span data-stu-id="b97ec-101">Remove-AzureRmIoTDeviceProvisioningService</span></span>

## <span data-ttu-id="b97ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b97ec-102">SYNOPSIS</span></span>
<span data-ttu-id="b97ec-103">Eliminare un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="b97ec-103">Delete an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b97ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b97ec-104">SYNTAX</span></span>

### <span data-ttu-id="b97ec-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b97ec-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b97ec-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="b97ec-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-InputObject] <PSProvisioningServiceDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b97ec-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="b97ec-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningService [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b97ec-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b97ec-108">DESCRIPTION</span></span>
<span data-ttu-id="b97ec-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="b97ec-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="b97ec-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b97ec-110">EXAMPLES</span></span>

### <span data-ttu-id="b97ec-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="b97ec-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningService -ResourceGroupName "myresourcegroup" -Name "myiotdps" -PassThru

True
```

<span data-ttu-id="b97ec-112">Eliminare un servizio di provisioning del dispositivo hub di Azure molto "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="b97ec-112">Delete an Azure IoT Hub device provisioning service 'myiotdps'.</span></span>

### <span data-ttu-id="b97ec-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="b97ec-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIotDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Remove-AzureRmIotDps
```

<span data-ttu-id="b97ec-114">Eliminare un dispositivo hub di Azure molto per il provisioning del servizio "myiotdps" tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="b97ec-114">Delete an Azure IoT Hub device provisioning service 'myiotdps' using pipeline.</span></span>

## <span data-ttu-id="b97ec-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b97ec-115">PARAMETERS</span></span>

### <span data-ttu-id="b97ec-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b97ec-116">-DefaultProfile</span></span>
<span data-ttu-id="b97ec-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="b97ec-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b97ec-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b97ec-118">-InputObject</span></span>
<span data-ttu-id="b97ec-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="b97ec-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="b97ec-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b97ec-120">-Name</span></span>
<span data-ttu-id="b97ec-121">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="b97ec-121">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="b97ec-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b97ec-122">-PassThru</span></span>
<span data-ttu-id="b97ec-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="b97ec-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b97ec-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b97ec-124">-ResourceGroupName</span></span>
<span data-ttu-id="b97ec-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="b97ec-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="b97ec-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b97ec-126">-ResourceId</span></span>
<span data-ttu-id="b97ec-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="b97ec-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="b97ec-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="b97ec-128">-Confirm</span></span>
<span data-ttu-id="b97ec-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b97ec-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b97ec-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b97ec-130">-WhatIf</span></span>
<span data-ttu-id="b97ec-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b97ec-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b97ec-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="b97ec-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b97ec-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b97ec-133">CommonParameters</span></span>
<span data-ttu-id="b97ec-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b97ec-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b97ec-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b97ec-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b97ec-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b97ec-136">INPUTS</span></span>

### <span data-ttu-id="b97ec-137">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="b97ec-137">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="b97ec-138">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="b97ec-138">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="b97ec-139">System. String</span><span class="sxs-lookup"><span data-stu-id="b97ec-139">System.String</span></span>

## <span data-ttu-id="b97ec-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b97ec-140">OUTPUTS</span></span>

### <span data-ttu-id="b97ec-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b97ec-141">System.Boolean</span></span>

## <span data-ttu-id="b97ec-142">Note</span><span class="sxs-lookup"><span data-stu-id="b97ec-142">NOTES</span></span>

## <span data-ttu-id="b97ec-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b97ec-143">RELATED LINKS</span></span>
