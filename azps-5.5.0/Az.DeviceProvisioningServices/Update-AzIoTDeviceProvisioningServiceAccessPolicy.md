---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194470"
---
# <span data-ttu-id="0225d-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0225d-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="0225d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0225d-102">SYNOPSIS</span></span>
<span data-ttu-id="0225d-103">Aggiornare i criteri di accesso condiviso in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="0225d-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0225d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0225d-104">SYNTAX</span></span>

### <span data-ttu-id="0225d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0225d-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0225d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0225d-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0225d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0225d-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0225d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0225d-108">DESCRIPTION</span></span>
<span data-ttu-id="0225d-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0225d-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0225d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0225d-110">EXAMPLES</span></span>

### <span data-ttu-id="0225d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0225d-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="0225d-112">Aggiornare il criterio di accesso "mypolicy" in un servizio di provisioning del dispositivo Hub IoT di Azure con destra EnrollmentWrite.</span><span class="sxs-lookup"><span data-stu-id="0225d-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="0225d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0225d-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="0225d-114">Aggiornare il criterio di accesso "mypolicy" in un servizio di provisioning del dispositivo Hub IoT di Azure con il diritto EnrollmentWrite tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="0225d-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="0225d-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0225d-115">PARAMETERS</span></span>

### <span data-ttu-id="0225d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0225d-116">-DefaultProfile</span></span>
<span data-ttu-id="0225d-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0225d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0225d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0225d-118">-InputObject</span></span>
<span data-ttu-id="0225d-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0225d-119">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0225d-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0225d-120">-KeyName</span></span>
<span data-ttu-id="0225d-121">Nome della chiave della chiave del criterio di accesso del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0225d-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="0225d-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0225d-122">-Name</span></span>
<span data-ttu-id="0225d-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0225d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0225d-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="0225d-124">-Permissions</span></span>
<span data-ttu-id="0225d-125">Autorizzazioni dei criteri di accesso al servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0225d-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="0225d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0225d-126">-ResourceGroupName</span></span>
<span data-ttu-id="0225d-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0225d-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0225d-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0225d-128">-ResourceId</span></span>
<span data-ttu-id="0225d-129">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0225d-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0225d-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0225d-130">-Confirm</span></span>
<span data-ttu-id="0225d-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0225d-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0225d-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0225d-132">-WhatIf</span></span>
<span data-ttu-id="0225d-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0225d-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0225d-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0225d-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0225d-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0225d-135">CommonParameters</span></span>
<span data-ttu-id="0225d-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0225d-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0225d-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0225d-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0225d-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="0225d-138">INPUTS</span></span>

### <span data-ttu-id="0225d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0225d-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="0225d-140">System.String</span><span class="sxs-lookup"><span data-stu-id="0225d-140">System.String</span></span>

## <span data-ttu-id="0225d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0225d-141">OUTPUTS</span></span>

### <span data-ttu-id="0225d-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0225d-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="0225d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="0225d-143">NOTES</span></span>

## <span data-ttu-id="0225d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0225d-144">RELATED LINKS</span></span>
