---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8b16d95d582e29be6f49cac9eaeb00bcda67de0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193457"
---
# <span data-ttu-id="357ff-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="357ff-101">Remove-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="357ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="357ff-102">SYNOPSIS</span></span>
<span data-ttu-id="357ff-103">Eliminare un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="357ff-103">Delete a device enrollment record.</span></span>

## <span data-ttu-id="357ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="357ff-104">SYNTAX</span></span>

### <span data-ttu-id="357ff-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="357ff-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="357ff-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="357ff-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="357ff-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="357ff-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="357ff-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="357ff-108">DESCRIPTION</span></span>
<span data-ttu-id="357ff-109">Eliminare una registrazione di un dispositivo in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="357ff-109">Delete a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="357ff-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="357ff-110">EXAMPLES</span></span>

### <span data-ttu-id="357ff-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="357ff-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -Passthru
```

<span data-ttu-id="357ff-112">Eliminare un record di registrazione specificato.</span><span class="sxs-lookup"><span data-stu-id="357ff-112">Delete a specified enrollment record.</span></span>

### <span data-ttu-id="357ff-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="357ff-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Passthru
```

<span data-ttu-id="357ff-114">Eliminare tutti i record di registrazione.</span><span class="sxs-lookup"><span data-stu-id="357ff-114">Delete all enrollment records.</span></span>

## <span data-ttu-id="357ff-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="357ff-115">PARAMETERS</span></span>

### <span data-ttu-id="357ff-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="357ff-116">-DefaultProfile</span></span>
<span data-ttu-id="357ff-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="357ff-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="357ff-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="357ff-118">-DpsName</span></span>
<span data-ttu-id="357ff-119">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="357ff-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="357ff-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="357ff-120">-DpsObject</span></span>
<span data-ttu-id="357ff-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="357ff-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="357ff-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="357ff-122">-PassThru</span></span>
<span data-ttu-id="357ff-123">Consente di restituire l'oggetto Boolean.</span><span class="sxs-lookup"><span data-stu-id="357ff-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="357ff-124">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="357ff-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="357ff-125">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="357ff-125">-RegistrationId</span></span>
<span data-ttu-id="357ff-126">ID di registrazione dell'iscrizione individuale.</span><span class="sxs-lookup"><span data-stu-id="357ff-126">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="357ff-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="357ff-127">-ResourceGroupName</span></span>
<span data-ttu-id="357ff-128">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="357ff-128">Name of the Resource Group</span></span>

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

### <span data-ttu-id="357ff-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="357ff-129">-ResourceId</span></span>
<span data-ttu-id="357ff-130">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="357ff-130">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="357ff-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="357ff-131">-Confirm</span></span>
<span data-ttu-id="357ff-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="357ff-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="357ff-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="357ff-133">-WhatIf</span></span>
<span data-ttu-id="357ff-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="357ff-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="357ff-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="357ff-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="357ff-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="357ff-136">CommonParameters</span></span>
<span data-ttu-id="357ff-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="357ff-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="357ff-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="357ff-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="357ff-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="357ff-139">INPUTS</span></span>

### <span data-ttu-id="357ff-140">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="357ff-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="357ff-141">System. String</span><span class="sxs-lookup"><span data-stu-id="357ff-141">System.String</span></span>

## <span data-ttu-id="357ff-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="357ff-142">OUTPUTS</span></span>

### <span data-ttu-id="357ff-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="357ff-143">System.Boolean</span></span>

## <span data-ttu-id="357ff-144">Note</span><span class="sxs-lookup"><span data-stu-id="357ff-144">NOTES</span></span>

## <span data-ttu-id="357ff-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="357ff-145">RELATED LINKS</span></span>