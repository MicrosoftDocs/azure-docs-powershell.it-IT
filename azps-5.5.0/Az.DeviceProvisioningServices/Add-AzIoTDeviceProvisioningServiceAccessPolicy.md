---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100209674"
---
# <span data-ttu-id="199f9-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="199f9-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="199f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="199f9-102">SYNOPSIS</span></span>
<span data-ttu-id="199f9-103">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="199f9-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="199f9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="199f9-104">SYNTAX</span></span>

### <span data-ttu-id="199f9-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="199f9-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="199f9-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="199f9-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="199f9-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="199f9-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="199f9-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="199f9-108">DESCRIPTION</span></span>
<span data-ttu-id="199f9-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="199f9-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="199f9-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="199f9-110">EXAMPLES</span></span>

### <span data-ttu-id="199f9-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="199f9-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="199f9-112">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo Hub IoT di Azure con diritti EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="199f9-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="199f9-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="199f9-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="199f9-114">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning di dispositivi Hub IoT di Azure con il diritto EnrollmentRead.</span><span class="sxs-lookup"><span data-stu-id="199f9-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="199f9-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="199f9-115">PARAMETERS</span></span>

### <span data-ttu-id="199f9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="199f9-116">-DefaultProfile</span></span>
<span data-ttu-id="199f9-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="199f9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="199f9-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="199f9-118">-DpsObject</span></span>
<span data-ttu-id="199f9-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="199f9-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="199f9-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="199f9-120">-KeyName</span></span>
<span data-ttu-id="199f9-121">Nome della chiave della chiave del criterio di accesso del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="199f9-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="199f9-122">-Name</span><span class="sxs-lookup"><span data-stu-id="199f9-122">-Name</span></span>
<span data-ttu-id="199f9-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="199f9-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="199f9-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="199f9-124">-Permissions</span></span>
<span data-ttu-id="199f9-125">Autorizzazioni dei criteri di accesso al servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="199f9-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="199f9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="199f9-126">-ResourceGroupName</span></span>
<span data-ttu-id="199f9-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="199f9-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="199f9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="199f9-128">-ResourceId</span></span>
<span data-ttu-id="199f9-129">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="199f9-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="199f9-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="199f9-130">-Confirm</span></span>
<span data-ttu-id="199f9-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="199f9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="199f9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="199f9-132">-WhatIf</span></span>
<span data-ttu-id="199f9-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="199f9-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="199f9-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="199f9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="199f9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="199f9-135">CommonParameters</span></span>
<span data-ttu-id="199f9-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="199f9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="199f9-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="199f9-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="199f9-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="199f9-138">INPUTS</span></span>

### <span data-ttu-id="199f9-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="199f9-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="199f9-140">System.String</span><span class="sxs-lookup"><span data-stu-id="199f9-140">System.String</span></span>

## <span data-ttu-id="199f9-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="199f9-141">OUTPUTS</span></span>

### <span data-ttu-id="199f9-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="199f9-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="199f9-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="199f9-143">NOTES</span></span>

## <span data-ttu-id="199f9-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="199f9-144">RELATED LINKS</span></span>
