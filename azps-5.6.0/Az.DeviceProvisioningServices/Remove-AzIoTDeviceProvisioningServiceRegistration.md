---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: f72aa2ab648de33baaf50e181afa98e12ac921a0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985135"
---
# <span data-ttu-id="e51bc-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="e51bc-101">Remove-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="e51bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e51bc-102">SYNOPSIS</span></span>
<span data-ttu-id="e51bc-103">Elimina la registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e51bc-103">Deletes the device registration.</span></span>

## <span data-ttu-id="e51bc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e51bc-104">SYNTAX</span></span>

### <span data-ttu-id="e51bc-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e51bc-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e51bc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e51bc-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e51bc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e51bc-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> -RegistrationId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e51bc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e51bc-108">DESCRIPTION</span></span>
<span data-ttu-id="e51bc-109">Eliminare la registrazione di un dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="e51bc-109">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="e51bc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e51bc-110">EXAMPLES</span></span>

### <span data-ttu-id="e51bc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e51bc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="e51bc-112">Eliminare la registrazione di un dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="e51bc-112">Delete a device registration in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="e51bc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e51bc-113">PARAMETERS</span></span>

### <span data-ttu-id="e51bc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51bc-114">-DefaultProfile</span></span>
<span data-ttu-id="e51bc-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e51bc-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51bc-116">-DpsName</span><span class="sxs-lookup"><span data-stu-id="e51bc-116">-DpsName</span></span>
<span data-ttu-id="e51bc-117">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e51bc-117">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e51bc-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e51bc-118">-DpsObject</span></span>
<span data-ttu-id="e51bc-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e51bc-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e51bc-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e51bc-120">-PassThru</span></span>
<span data-ttu-id="e51bc-121">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="e51bc-121">Allows to return the boolean object.</span></span>
<span data-ttu-id="e51bc-122">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="e51bc-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e51bc-123">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="e51bc-123">-RegistrationId</span></span>
<span data-ttu-id="e51bc-124">ID della registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e51bc-124">ID of device registration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e51bc-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e51bc-125">-ResourceGroupName</span></span>
<span data-ttu-id="e51bc-126">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e51bc-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e51bc-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e51bc-127">-ResourceId</span></span>
<span data-ttu-id="e51bc-128">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="e51bc-128">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e51bc-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e51bc-129">-Confirm</span></span>
<span data-ttu-id="e51bc-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e51bc-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e51bc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e51bc-131">-WhatIf</span></span>
<span data-ttu-id="e51bc-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e51bc-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e51bc-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e51bc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e51bc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51bc-134">CommonParameters</span></span>
<span data-ttu-id="e51bc-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e51bc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51bc-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e51bc-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51bc-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="e51bc-137">INPUTS</span></span>

### <span data-ttu-id="e51bc-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e51bc-138">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="e51bc-139">System.String</span><span class="sxs-lookup"><span data-stu-id="e51bc-139">System.String</span></span>

## <span data-ttu-id="e51bc-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e51bc-140">OUTPUTS</span></span>

### <span data-ttu-id="e51bc-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="e51bc-141">System.Boolean</span></span>

## <span data-ttu-id="e51bc-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="e51bc-142">NOTES</span></span>

## <span data-ttu-id="e51bc-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e51bc-143">RELATED LINKS</span></span>
