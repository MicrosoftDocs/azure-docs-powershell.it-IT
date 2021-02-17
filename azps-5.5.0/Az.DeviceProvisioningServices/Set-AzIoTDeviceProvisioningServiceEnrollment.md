---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 47c5c5119e41f3feeaccda66871d902e631c9ac2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194487"
---
# <span data-ttu-id="cafdb-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="cafdb-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="cafdb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cafdb-102">SYNOPSIS</span></span>
<span data-ttu-id="cafdb-103">Aggiornare un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cafdb-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="cafdb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cafdb-104">SYNTAX</span></span>

### <span data-ttu-id="cafdb-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cafdb-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cafdb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="cafdb-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cafdb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="cafdb-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cafdb-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cafdb-108">DESCRIPTION</span></span>
<span data-ttu-id="cafdb-109">Aggiornare la registrazione di un dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="cafdb-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="cafdb-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cafdb-110">EXAMPLES</span></span>

### <span data-ttu-id="cafdb-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cafdb-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="cafdb-112">Aggiornare i criteri di assegnazione e gli hub per un record di registrazione.</span><span class="sxs-lookup"><span data-stu-id="cafdb-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="cafdb-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cafdb-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="cafdb-114">Aggiornare lo stato iniziale della registrazione.</span><span class="sxs-lookup"><span data-stu-id="cafdb-114">Update an enrollment's initial twin state.</span></span>

## <span data-ttu-id="cafdb-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cafdb-115">PARAMETERS</span></span>

### <span data-ttu-id="cafdb-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="cafdb-116">-AllocationPolicy</span></span>
<span data-ttu-id="cafdb-117">Tipo di allocazione per il dispositivo assegnato all'Hub.</span><span class="sxs-lookup"><span data-stu-id="cafdb-117">Type of allocation for device assigned to the Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAllocationPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Hashed, GeoLatency, Static, Custom

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="cafdb-118">-ApiVersion</span></span>
<span data-ttu-id="cafdb-119">Versione API del servizio di provisioning nella richiesta di assegnazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="cafdb-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="cafdb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cafdb-120">-DefaultProfile</span></span>
<span data-ttu-id="cafdb-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cafdb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cafdb-122">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="cafdb-122">-Desired</span></span>
<span data-ttu-id="cafdb-123">Proprietà iniziali desiderate.</span><span class="sxs-lookup"><span data-stu-id="cafdb-123">Initial twin desired properties.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-124">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="cafdb-124">-DeviceId</span></span>
<span data-ttu-id="cafdb-125">ID dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="cafdb-125">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="cafdb-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="cafdb-126">-DpsName</span></span>
<span data-ttu-id="cafdb-127">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="cafdb-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="cafdb-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="cafdb-128">-DpsObject</span></span>
<span data-ttu-id="cafdb-129">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="cafdb-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="cafdb-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="cafdb-130">-EdgeEnabled</span></span>
<span data-ttu-id="cafdb-131">Flag che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="cafdb-131">Flag indicating edge enablement.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="cafdb-132">-IotHub</span></span>
<span data-ttu-id="cafdb-133">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cafdb-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="cafdb-134">Usare un elenco separato da spazi per più hub IoT.</span><span class="sxs-lookup"><span data-stu-id="cafdb-134">Use space-separated list for multiple IoT Hubs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="cafdb-135">-IotHubHostName</span></span>
<span data-ttu-id="cafdb-136">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="cafdb-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="cafdb-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="cafdb-137">-ProvisioningStatus</span></span>
<span data-ttu-id="cafdb-138">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="cafdb-138">Enable or disable enrollment entry.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningStatus
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-139">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="cafdb-139">-RegistrationId</span></span>
<span data-ttu-id="cafdb-140">ID registrazione individuale.</span><span class="sxs-lookup"><span data-stu-id="cafdb-140">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="cafdb-141">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="cafdb-141">-ReprovisionPolicy</span></span>
<span data-ttu-id="cafdb-142">Dati del dispositivo da gestire durante il nuovo provisioning al diverso Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="cafdb-142">Device data to be handled on re-provision to different Iot Hub.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSReprovisionType
Parameter Sets: (All)
Aliases:
Accepted values: reprovisionandmigratedata, reprovisionandresetdata, never

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cafdb-143">-ResourceGroupName</span></span>
<span data-ttu-id="cafdb-144">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="cafdb-144">Name of the Resource Group</span></span>

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

### <span data-ttu-id="cafdb-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cafdb-145">-ResourceId</span></span>
<span data-ttu-id="cafdb-146">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="cafdb-146">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="cafdb-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="cafdb-147">-Tag</span></span>
<span data-ttu-id="cafdb-148">Tag tag tag iniziali.</span><span class="sxs-lookup"><span data-stu-id="cafdb-148">Initial twin tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cafdb-149">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="cafdb-149">-WebhookUrl</span></span>
<span data-ttu-id="cafdb-150">URL webhook usato per le richieste di assegnazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="cafdb-150">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="cafdb-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cafdb-151">-Confirm</span></span>
<span data-ttu-id="cafdb-152">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cafdb-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cafdb-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cafdb-153">-WhatIf</span></span>
<span data-ttu-id="cafdb-154">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cafdb-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cafdb-155">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cafdb-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cafdb-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cafdb-156">CommonParameters</span></span>
<span data-ttu-id="cafdb-157">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cafdb-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cafdb-158">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cafdb-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cafdb-159">INPUT</span><span class="sxs-lookup"><span data-stu-id="cafdb-159">INPUTS</span></span>

### <span data-ttu-id="cafdb-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="cafdb-160">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="cafdb-161">System.String</span><span class="sxs-lookup"><span data-stu-id="cafdb-161">System.String</span></span>

## <span data-ttu-id="cafdb-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cafdb-162">OUTPUTS</span></span>

### <span data-ttu-id="cafdb-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="cafdb-163">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="cafdb-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="cafdb-164">NOTES</span></span>

## <span data-ttu-id="cafdb-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cafdb-165">RELATED LINKS</span></span>
