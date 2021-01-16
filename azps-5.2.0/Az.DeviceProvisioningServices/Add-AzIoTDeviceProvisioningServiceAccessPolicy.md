---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 67d1db17dff5214fdeb4fae9429b21b90da38a52
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328798"
---
# <span data-ttu-id="2eeff-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="2eeff-101">Add-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="2eeff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2eeff-102">SYNOPSIS</span></span>
<span data-ttu-id="2eeff-103">Aggiungere un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="2eeff-103">Add a new shared access policy in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="2eeff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2eeff-104">SYNTAX</span></span>

### <span data-ttu-id="2eeff-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2eeff-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2eeff-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2eeff-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName] <String> [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2eeff-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2eeff-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String>
 [-Permissions] <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eeff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2eeff-108">DESCRIPTION</span></span>
<span data-ttu-id="2eeff-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="2eeff-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="2eeff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2eeff-110">EXAMPLES</span></span>

### <span data-ttu-id="2eeff-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2eeff-111">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -Permissions "ServiceConfig, EnrollmentWrite"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, EnrollmentWrite
```

<span data-ttu-id="2eeff-112">Aggiungi un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto con i diritti di EnrollmentWrite e ServiceConfig.</span><span class="sxs-lookup"><span data-stu-id="2eeff-112">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentWrite and ServiceConfig rights.</span></span>

### <span data-ttu-id="2eeff-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2eeff-113">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy2" -Permissions "EnrollmentRead"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, EnrollmentWrite
mypolicy2   EnrollmentRead
```

<span data-ttu-id="2eeff-114">Aggiungi un nuovo criterio di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto con EnrollmentRead a destra.</span><span class="sxs-lookup"><span data-stu-id="2eeff-114">Add a new shared access policy in an Azure IoT Hub device provisioning service with EnrollmentRead right.</span></span>

## <span data-ttu-id="2eeff-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2eeff-115">PARAMETERS</span></span>

### <span data-ttu-id="2eeff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eeff-116">-DefaultProfile</span></span>
<span data-ttu-id="2eeff-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2eeff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2eeff-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2eeff-118">-DpsObject</span></span>
<span data-ttu-id="2eeff-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="2eeff-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2eeff-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="2eeff-120">-KeyName</span></span>
<span data-ttu-id="2eeff-121">Nome chiave criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="2eeff-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="2eeff-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2eeff-122">-Name</span></span>
<span data-ttu-id="2eeff-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="2eeff-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2eeff-124">-Autorizzazioni</span><span class="sxs-lookup"><span data-stu-id="2eeff-124">-Permissions</span></span>
<span data-ttu-id="2eeff-125">Autorizzazioni per i criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="2eeff-125">IoT Device Provisioning Service access policy permissions</span></span>

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

### <span data-ttu-id="2eeff-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eeff-126">-ResourceGroupName</span></span>
<span data-ttu-id="2eeff-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2eeff-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2eeff-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2eeff-128">-ResourceId</span></span>
<span data-ttu-id="2eeff-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2eeff-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2eeff-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2eeff-130">-Confirm</span></span>
<span data-ttu-id="2eeff-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2eeff-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eeff-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eeff-132">-WhatIf</span></span>
<span data-ttu-id="2eeff-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eeff-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2eeff-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2eeff-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eeff-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eeff-135">CommonParameters</span></span>
<span data-ttu-id="2eeff-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eeff-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eeff-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eeff-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eeff-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2eeff-138">INPUTS</span></span>

### <span data-ttu-id="2eeff-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2eeff-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2eeff-140">System. String</span><span class="sxs-lookup"><span data-stu-id="2eeff-140">System.String</span></span>

## <span data-ttu-id="2eeff-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2eeff-141">OUTPUTS</span></span>

### <span data-ttu-id="2eeff-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="2eeff-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="2eeff-143">Note</span><span class="sxs-lookup"><span data-stu-id="2eeff-143">NOTES</span></span>

## <span data-ttu-id="2eeff-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2eeff-144">RELATED LINKS</span></span>
