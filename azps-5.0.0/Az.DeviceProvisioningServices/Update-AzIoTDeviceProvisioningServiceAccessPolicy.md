---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/update-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Update-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: ab23988d5594c2285ac8d6eee02b18b0ae4dbf43
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193442"
---
# <span data-ttu-id="df9d7-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="df9d7-101">Update-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="df9d7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="df9d7-102">SYNOPSIS</span></span>
<span data-ttu-id="df9d7-103">Aggiornare un criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="df9d7-103">Update a shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="df9d7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="df9d7-104">SYNTAX</span></span>

### <span data-ttu-id="df9d7-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="df9d7-105">ResourceSet (Default)</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="df9d7-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="df9d7-106">InputObjectSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-Permissions] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df9d7-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="df9d7-107">ResourceIdSet</span></span>
```
Update-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df9d7-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="df9d7-108">DESCRIPTION</span></span>
<span data-ttu-id="df9d7-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="df9d7-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="df9d7-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="df9d7-110">EXAMPLES</span></span>

### <span data-ttu-id="df9d7-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df9d7-111">Example 1</span></span>
```
PS C:\> Update-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="df9d7-112">Aggiornare i criteri di accesso "criteri" in un servizio di provisioning del dispositivo hub di Azure molto con EnrollmentWrite a destra.</span><span class="sxs-lookup"><span data-stu-id="df9d7-112">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right.</span></span>

### <span data-ttu-id="df9d7-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="df9d7-113">Example 1</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Update-AzIoTDpsAccessPolicy -Permissions "EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : EnrollmentWrite
```

<span data-ttu-id="df9d7-114">Aggiornare i criteri di accesso "criteri" in un servizio di provisioning del dispositivo hub di Azure molto con EnrollmentWrite right using pipeline.</span><span class="sxs-lookup"><span data-stu-id="df9d7-114">Update access policy "mypolicy" in an Azure IoT Hub device provisioning service with EnrollmentWrite right using pipeline.</span></span>

## <span data-ttu-id="df9d7-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="df9d7-115">PARAMETERS</span></span>

### <span data-ttu-id="df9d7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df9d7-116">-DefaultProfile</span></span>
<span data-ttu-id="df9d7-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="df9d7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df9d7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="df9d7-118">-InputObject</span></span>
<span data-ttu-id="df9d7-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="df9d7-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="df9d7-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="df9d7-120">-KeyName</span></span>
<span data-ttu-id="df9d7-121">Nome chiave criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="df9d7-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="df9d7-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="df9d7-122">-Name</span></span>
<span data-ttu-id="df9d7-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="df9d7-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="df9d7-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="df9d7-124">-Permissions</span></span>
<span data-ttu-id="df9d7-125">Autorizzazioni per i criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="df9d7-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="df9d7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df9d7-126">-ResourceGroupName</span></span>
<span data-ttu-id="df9d7-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="df9d7-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="df9d7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df9d7-128">-ResourceId</span></span>
<span data-ttu-id="df9d7-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="df9d7-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="df9d7-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="df9d7-130">-Confirm</span></span>
<span data-ttu-id="df9d7-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df9d7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df9d7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df9d7-132">-WhatIf</span></span>
<span data-ttu-id="df9d7-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df9d7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df9d7-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="df9d7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df9d7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df9d7-135">CommonParameters</span></span>
<span data-ttu-id="df9d7-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df9d7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df9d7-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df9d7-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df9d7-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="df9d7-138">INPUTS</span></span>

### <span data-ttu-id="df9d7-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="df9d7-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="df9d7-140">System. String</span><span class="sxs-lookup"><span data-stu-id="df9d7-140">System.String</span></span>

## <span data-ttu-id="df9d7-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="df9d7-141">OUTPUTS</span></span>

### <span data-ttu-id="df9d7-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="df9d7-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="df9d7-143">Note</span><span class="sxs-lookup"><span data-stu-id="df9d7-143">NOTES</span></span>

## <span data-ttu-id="df9d7-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="df9d7-144">RELATED LINKS</span></span>