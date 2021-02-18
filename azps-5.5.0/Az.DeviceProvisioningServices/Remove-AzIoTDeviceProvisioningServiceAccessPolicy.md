---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 5f4cfe702b975bf69098aa3c002c756b5cf3da78
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200414"
---
# <span data-ttu-id="69255-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="69255-101">Remove-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="69255-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69255-102">SYNOPSIS</span></span>
<span data-ttu-id="69255-103">Eliminare i criteri di accesso condiviso in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="69255-103">Delete a shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="69255-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="69255-104">SYNTAX</span></span>

### <span data-ttu-id="69255-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="69255-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="69255-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="69255-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy
 [-InputObject] <PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="69255-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="69255-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="69255-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="69255-108">DESCRIPTION</span></span>
<span data-ttu-id="69255-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="69255-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="69255-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="69255-110">EXAMPLES</span></span>

### <span data-ttu-id="69255-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="69255-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" -PassThru

True
```

<span data-ttu-id="69255-112">Eliminare il criterio di accesso condiviso "mypolicy" in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="69255-112">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="69255-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="69255-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy" | Remove-AzIoTDpsAccessPolicy
```

<span data-ttu-id="69255-114">Eliminare il criterio di accesso condiviso "mypolicy" in un servizio di provisioning dei dispositivi Hub IoT di Azure usando una pipeline.</span><span class="sxs-lookup"><span data-stu-id="69255-114">Delete shared access policy "mypolicy" in an Azure IoT Hub device provisioning service using pipeline.</span></span>

## <span data-ttu-id="69255-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="69255-115">PARAMETERS</span></span>

### <span data-ttu-id="69255-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69255-116">-DefaultProfile</span></span>
<span data-ttu-id="69255-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="69255-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69255-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="69255-118">-InputObject</span></span>
<span data-ttu-id="69255-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="69255-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="69255-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="69255-120">-KeyName</span></span>
<span data-ttu-id="69255-121">Nome della chiave della chiave del criterio di accesso del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="69255-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="69255-122">-Name</span><span class="sxs-lookup"><span data-stu-id="69255-122">-Name</span></span>
<span data-ttu-id="69255-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="69255-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="69255-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="69255-124">-PassThru</span></span>
<span data-ttu-id="69255-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="69255-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="69255-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69255-126">-ResourceGroupName</span></span>
<span data-ttu-id="69255-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="69255-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="69255-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="69255-128">-ResourceId</span></span>
<span data-ttu-id="69255-129">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="69255-129">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="69255-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="69255-130">-Confirm</span></span>
<span data-ttu-id="69255-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="69255-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69255-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69255-132">-WhatIf</span></span>
<span data-ttu-id="69255-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69255-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69255-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="69255-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69255-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69255-135">CommonParameters</span></span>
<span data-ttu-id="69255-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69255-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69255-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69255-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69255-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="69255-138">INPUTS</span></span>

### <span data-ttu-id="69255-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="69255-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

### <span data-ttu-id="69255-140">System.String</span><span class="sxs-lookup"><span data-stu-id="69255-140">System.String</span></span>

## <span data-ttu-id="69255-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="69255-141">OUTPUTS</span></span>

### <span data-ttu-id="69255-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="69255-142">System.Boolean</span></span>

## <span data-ttu-id="69255-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="69255-143">NOTES</span></span>

## <span data-ttu-id="69255-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="69255-144">RELATED LINKS</span></span>
