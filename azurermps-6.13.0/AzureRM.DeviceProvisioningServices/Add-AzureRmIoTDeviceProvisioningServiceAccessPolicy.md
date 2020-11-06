---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 23d9e40fe6d25fbd2a6bb3e23959d1a4bf087af2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520218"
---
# <span data-ttu-id="856df-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="856df-101">Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="856df-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="856df-102">SYNOPSIS</span></span>
<span data-ttu-id="856df-103">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="856df-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="856df-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="856df-104">SYNTAX</span></span>

### <span data-ttu-id="856df-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="856df-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="856df-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="856df-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="856df-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="856df-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="856df-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="856df-108">DESCRIPTION</span></span>
<span data-ttu-id="856df-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="856df-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="856df-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="856df-110">EXAMPLES</span></span>

### <span data-ttu-id="856df-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="856df-111">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="856df-112">Aggiungi un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto con i diritti di EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="856df-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="856df-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="856df-113">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="856df-114">Aggiungi un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto con EnrollmentRead a destra.</span><span class="sxs-lookup"><span data-stu-id="856df-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="856df-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="856df-115">PARAMETERS</span></span>

### <span data-ttu-id="856df-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="856df-116">-DefaultProfile</span></span>
<span data-ttu-id="856df-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="856df-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="856df-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="856df-118">-DpsObject</span></span>
<span data-ttu-id="856df-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="856df-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="856df-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="856df-120">-KeyName</span></span>
<span data-ttu-id="856df-121">Nome chiave criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="856df-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="856df-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="856df-122">-Name</span></span>
<span data-ttu-id="856df-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="856df-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="856df-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="856df-124">-Permissions</span></span>
<span data-ttu-id="856df-125">Autorizzazioni per i criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="856df-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="856df-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="856df-126">-ResourceGroupName</span></span>
<span data-ttu-id="856df-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="856df-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="856df-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="856df-128">-ResourceId</span></span>
<span data-ttu-id="856df-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="856df-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="856df-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="856df-130">-Confirm</span></span>
<span data-ttu-id="856df-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="856df-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="856df-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="856df-132">-WhatIf</span></span>
<span data-ttu-id="856df-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="856df-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="856df-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="856df-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="856df-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="856df-135">CommonParameters</span></span>
<span data-ttu-id="856df-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="856df-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="856df-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="856df-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="856df-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="856df-138">INPUTS</span></span>

### <span data-ttu-id="856df-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="856df-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="856df-140">Parametri: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="856df-140">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="856df-141">System. String</span><span class="sxs-lookup"><span data-stu-id="856df-141">System.String</span></span>

## <span data-ttu-id="856df-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="856df-142">OUTPUTS</span></span>

### <span data-ttu-id="856df-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="856df-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="856df-144">Note</span><span class="sxs-lookup"><span data-stu-id="856df-144">NOTES</span></span>

## <span data-ttu-id="856df-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="856df-145">RELATED LINKS</span></span>
