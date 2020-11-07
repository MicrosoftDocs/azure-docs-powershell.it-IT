---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 8465a9b86d701ef4ec21058d39734098f91f2a7a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678893"
---
# <span data-ttu-id="5182a-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5182a-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="5182a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5182a-102">SYNOPSIS</span></span>
<span data-ttu-id="5182a-103">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="5182a-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="5182a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5182a-104">SYNTAX</span></span>

### <span data-ttu-id="5182a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="5182a-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5182a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="5182a-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5182a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="5182a-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5182a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5182a-108">DESCRIPTION</span></span>
<span data-ttu-id="5182a-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="5182a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="5182a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5182a-110">EXAMPLES</span></span>

### <span data-ttu-id="5182a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="5182a-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="5182a-112">Aggiungi un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto con i diritti di EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="5182a-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="5182a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="5182a-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="5182a-114">Aggiungi un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto con EnrollmentRead a destra.</span><span class="sxs-lookup"><span data-stu-id="5182a-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="5182a-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5182a-115">PARAMETERS</span></span>

### <span data-ttu-id="5182a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5182a-116">-DefaultProfile</span></span>
<span data-ttu-id="5182a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5182a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5182a-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="5182a-118">-DpsObject</span></span>
<span data-ttu-id="5182a-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="5182a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="5182a-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="5182a-120">-KeyName</span></span>
<span data-ttu-id="5182a-121">Nome chiave criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="5182a-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="5182a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="5182a-122">-Name</span></span>
<span data-ttu-id="5182a-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="5182a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="5182a-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="5182a-124">-Permissions</span></span>
<span data-ttu-id="5182a-125">Autorizzazioni per i criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="5182a-125">IoT Device Provisioning Service access policy permissions</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ServiceConfig, EnrollmentRead, EnrollmentWrite, DeviceConnect, RegistrationStatusRead, RegistrationStatusWrite

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5182a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5182a-126">-ResourceGroupName</span></span>
<span data-ttu-id="5182a-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="5182a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="5182a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5182a-128">-ResourceId</span></span>
<span data-ttu-id="5182a-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="5182a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="5182a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5182a-130">-Confirm</span></span>
<span data-ttu-id="5182a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5182a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5182a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5182a-132">-WhatIf</span></span>
<span data-ttu-id="5182a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5182a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5182a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5182a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5182a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5182a-135">CommonParameters</span></span>
<span data-ttu-id="5182a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5182a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5182a-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5182a-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5182a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5182a-138">INPUTS</span></span>

### <span data-ttu-id="5182a-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="5182a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="5182a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5182a-140">System.String</span></span>

## <span data-ttu-id="5182a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5182a-141">OUTPUTS</span></span>

### <span data-ttu-id="5182a-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="5182a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="5182a-143">Note</span><span class="sxs-lookup"><span data-stu-id="5182a-143">NOTES</span></span>

## <span data-ttu-id="5182a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5182a-144">RELATED LINKS</span></span>
