---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193462"
---
# <span data-ttu-id="ded96-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="ded96-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="ded96-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ded96-102">SYNOPSIS</span></span>
<span data-ttu-id="ded96-103">Eliminare i criteri di accesso condiviso in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="ded96-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="ded96-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ded96-104">SYNTAX</span></span>

### <span data-ttu-id="ded96-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ded96-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ded96-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="ded96-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ded96-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="ded96-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ded96-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ded96-108">DESCRIPTION</span></span>
<span data-ttu-id="ded96-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="ded96-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="ded96-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ded96-110">EXAMPLES</span></span>

### <span data-ttu-id="ded96-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ded96-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="ded96-112">Eliminare i criteri di accesso condiviso "criteri" in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="ded96-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="ded96-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="ded96-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="ded96-114">Eliminare i criteri di accesso condiviso "criteri" in un servizio di provisioning del dispositivo hub di Azure molto tramite pipeline.</span><span class="sxs-lookup"><span data-stu-id="ded96-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="ded96-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ded96-115">PARAMETERS</span></span>

### <span data-ttu-id="ded96-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded96-116">-DefaultProfile</span></span>
<span data-ttu-id="ded96-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ded96-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ded96-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ded96-118">-InputObject</span></span>
<span data-ttu-id="ded96-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="ded96-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="ded96-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="ded96-120">-KeyName</span></span>
<span data-ttu-id="ded96-121">Nome chiave criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="ded96-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="ded96-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="ded96-122">-Name</span></span>
<span data-ttu-id="ded96-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="ded96-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="ded96-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ded96-124">-PassThru</span></span>
<span data-ttu-id="ded96-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="ded96-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ded96-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded96-126">-ResourceGroupName</span></span>
<span data-ttu-id="ded96-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="ded96-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="ded96-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ded96-128">-ResourceId</span></span>
<span data-ttu-id="ded96-129">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="ded96-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="ded96-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ded96-130">-Confirm</span></span>
<span data-ttu-id="ded96-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ded96-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ded96-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ded96-132">-WhatIf</span></span>
<span data-ttu-id="ded96-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ded96-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ded96-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ded96-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ded96-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded96-135">CommonParameters</span></span>
<span data-ttu-id="ded96-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded96-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded96-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ded96-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded96-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ded96-138">INPUTS</span></span>

### <span data-ttu-id="ded96-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="ded96-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="ded96-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ded96-140">System.String</span></span>

## <span data-ttu-id="ded96-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ded96-141">OUTPUTS</span></span>

### <span data-ttu-id="ded96-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ded96-142">System.Boolean</span></span>

## <span data-ttu-id="ded96-143">Note</span><span class="sxs-lookup"><span data-stu-id="ded96-143">NOTES</span></span>

## <span data-ttu-id="ded96-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ded96-144">RELATED LINKS</span></span>
