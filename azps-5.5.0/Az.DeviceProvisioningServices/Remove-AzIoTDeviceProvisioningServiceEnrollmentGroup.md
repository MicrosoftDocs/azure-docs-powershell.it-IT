---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: ce1fe3b50d8198dd9ee1965a3a3ab7a2409e1145
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196383"
---
# <span data-ttu-id="f348e-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="f348e-101">Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="f348e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f348e-102">SYNOPSIS</span></span>
<span data-ttu-id="f348e-103">Eliminare un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f348e-103">Delete a device enrollment group.</span></span>

## <span data-ttu-id="f348e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f348e-104">SYNTAX</span></span>

### <span data-ttu-id="f348e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f348e-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f348e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f348e-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f348e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f348e-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f348e-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f348e-108">DESCRIPTION</span></span>
<span data-ttu-id="f348e-109">Eliminare un gruppo di registrazione in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="f348e-109">Delete an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="f348e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f348e-110">EXAMPLES</span></span>

### <span data-ttu-id="f348e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f348e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -Passthru
```

<span data-ttu-id="f348e-112">Eliminare un gruppo di registrazione specificato.</span><span class="sxs-lookup"><span data-stu-id="f348e-112">Delete a specified enrollment group.</span></span>

### <span data-ttu-id="f348e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f348e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="f348e-114">Eliminare tutti i gruppi di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f348e-114">Delete all enrollment groups.</span></span>

## <span data-ttu-id="f348e-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f348e-115">PARAMETERS</span></span>

### <span data-ttu-id="f348e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f348e-116">-DefaultProfile</span></span>
<span data-ttu-id="f348e-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f348e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f348e-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="f348e-118">-DpsName</span></span>
<span data-ttu-id="f348e-119">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="f348e-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f348e-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="f348e-120">-DpsObject</span></span>
<span data-ttu-id="f348e-121">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="f348e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="f348e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f348e-122">-Name</span></span>
<span data-ttu-id="f348e-123">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="f348e-123">Name of the enrollment group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f348e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f348e-124">-PassThru</span></span>
<span data-ttu-id="f348e-125">Consente di restituire l'oggetto booleano.</span><span class="sxs-lookup"><span data-stu-id="f348e-125">Allows to return the boolean object.</span></span>
<span data-ttu-id="f348e-126">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="f348e-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f348e-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f348e-127">-ResourceGroupName</span></span>
<span data-ttu-id="f348e-128">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f348e-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f348e-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f348e-129">-ResourceId</span></span>
<span data-ttu-id="f348e-130">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="f348e-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="f348e-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f348e-131">-Confirm</span></span>
<span data-ttu-id="f348e-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f348e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f348e-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f348e-133">-WhatIf</span></span>
<span data-ttu-id="f348e-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f348e-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f348e-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f348e-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f348e-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f348e-136">CommonParameters</span></span>
<span data-ttu-id="f348e-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f348e-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f348e-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f348e-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f348e-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="f348e-139">INPUTS</span></span>

### <span data-ttu-id="f348e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="f348e-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="f348e-141">System.String</span><span class="sxs-lookup"><span data-stu-id="f348e-141">System.String</span></span>

## <span data-ttu-id="f348e-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f348e-142">OUTPUTS</span></span>

### <span data-ttu-id="f348e-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f348e-143">System.Boolean</span></span>

## <span data-ttu-id="f348e-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="f348e-144">NOTES</span></span>

## <span data-ttu-id="f348e-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f348e-145">RELATED LINKS</span></span>
