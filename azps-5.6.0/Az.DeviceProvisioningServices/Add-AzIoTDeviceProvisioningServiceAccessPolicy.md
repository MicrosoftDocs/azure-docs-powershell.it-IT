---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: f34816ca77955c86f68b421efa221eab57e552cd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010510"
---
# <span data-ttu-id="e0d6a-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e0d6a-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="e0d6a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0d6a-102">SYNOPSIS</span></span>
<span data-ttu-id="e0d6a-103">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="e0d6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e0d6a-104">SYNTAX</span></span>

### <span data-ttu-id="e0d6a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e0d6a-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0d6a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e0d6a-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e0d6a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e0d6a-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0d6a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e0d6a-108">DESCRIPTION</span></span>
<span data-ttu-id="e0d6a-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="e0d6a-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="e0d6a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e0d6a-110">EXAMPLES</span></span>

### <span data-ttu-id="e0d6a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e0d6a-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="e0d6a-112">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo Hub IoT di Azure con i diritti EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="e0d6a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e0d6a-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="e0d6a-114">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo Hub IoT di Azure con il diritto EnrollmentRead.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="e0d6a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0d6a-115">PARAMETERS</span></span>

### <span data-ttu-id="e0d6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0d6a-116">-DefaultProfile</span></span>
<span data-ttu-id="e0d6a-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e0d6a-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e0d6a-118">-DpsObject</span></span>
<span data-ttu-id="e0d6a-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e0d6a-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e0d6a-120">-KeyName</span></span>
<span data-ttu-id="e0d6a-121">Nome della chiave della chiave del criterio di accesso del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="e0d6a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="e0d6a-122">-Name</span></span>
<span data-ttu-id="e0d6a-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e0d6a-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="e0d6a-124">-Permissions</span></span>
<span data-ttu-id="e0d6a-125">Autorizzazioni dei criteri di accesso al servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="e0d6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e0d6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="e0d6a-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e0d6a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e0d6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e0d6a-128">-ResourceId</span></span>
<span data-ttu-id="e0d6a-129">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e0d6a-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e0d6a-130">-Confirm</span></span>
<span data-ttu-id="e0d6a-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0d6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0d6a-132">-WhatIf</span></span>
<span data-ttu-id="e0d6a-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0d6a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0d6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0d6a-135">CommonParameters</span></span>
<span data-ttu-id="e0d6a-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0d6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0d6a-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0d6a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0d6a-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-138">INPUTS</span></span>

### <span data-ttu-id="e0d6a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e0d6a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="e0d6a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="e0d6a-140">System.String</span></span>

## <span data-ttu-id="e0d6a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e0d6a-141">OUTPUTS</span></span>

### <span data-ttu-id="e0d6a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="e0d6a-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="e0d6a-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="e0d6a-143">NOTES</span></span>

## <span data-ttu-id="e0d6a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e0d6a-144">RELATED LINKS</span></span>
