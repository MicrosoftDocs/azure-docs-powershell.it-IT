---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194478"
---
# <span data-ttu-id="9bbbc-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9bbbc-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="9bbbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9bbbc-102">SYNOPSIS</span></span>
<span data-ttu-id="9bbbc-103">Aggiornare un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="9bbbc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9bbbc-104">SYNTAX</span></span>

### <span data-ttu-id="9bbbc-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9bbbc-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bbbc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9bbbc-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9bbbc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9bbbc-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9bbbc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9bbbc-108">DESCRIPTION</span></span>
<span data-ttu-id="9bbbc-109">Aggiornare un gruppo di registrazione in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9bbbc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9bbbc-110">EXAMPLES</span></span>

### <span data-ttu-id="9bbbc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9bbbc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="9bbbc-112">Aggiornare i criteri di assegnazione e gli hub per un gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="9bbbc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9bbbc-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="9bbbc-114">Aggiornare lo stato iniziale del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="9bbbc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9bbbc-115">PARAMETERS</span></span>

### <span data-ttu-id="9bbbc-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9bbbc-116">-AllocationPolicy</span></span>
<span data-ttu-id="9bbbc-117">Tipo di allocazione per il dispositivo assegnato all'Hub.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="9bbbc-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9bbbc-118">-ApiVersion</span></span>
<span data-ttu-id="9bbbc-119">Versione API del servizio di provisioning nella richiesta di assegnazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="9bbbc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bbbc-120">-DefaultProfile</span></span>
<span data-ttu-id="9bbbc-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9bbbc-122">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="9bbbc-122">-Desired</span></span>
<span data-ttu-id="9bbbc-123">Proprietà iniziali desiderate.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="9bbbc-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="9bbbc-124">-DpsName</span></span>
<span data-ttu-id="9bbbc-125">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="9bbbc-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9bbbc-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9bbbc-126">-DpsObject</span></span>
<span data-ttu-id="9bbbc-127">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="9bbbc-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9bbbc-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9bbbc-128">-EdgeEnabled</span></span>
<span data-ttu-id="9bbbc-129">Flag che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="9bbbc-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9bbbc-130">-IotHub</span></span>
<span data-ttu-id="9bbbc-131">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="9bbbc-132">Usare un elenco separato da spazi per più hub IoT.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="9bbbc-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="9bbbc-133">-IotHubHostName</span></span>
<span data-ttu-id="9bbbc-134">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="9bbbc-135">-Name</span><span class="sxs-lookup"><span data-stu-id="9bbbc-135">-Name</span></span>
<span data-ttu-id="9bbbc-136">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="9bbbc-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="9bbbc-137">-ProvisioningStatus</span></span>
<span data-ttu-id="9bbbc-138">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="9bbbc-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="9bbbc-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="9bbbc-140">Dati del dispositivo da gestire durante il nuovo provisioning al diverso Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="9bbbc-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9bbbc-141">-ResourceGroupName</span></span>
<span data-ttu-id="9bbbc-142">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9bbbc-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9bbbc-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9bbbc-143">-ResourceId</span></span>
<span data-ttu-id="9bbbc-144">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="9bbbc-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9bbbc-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="9bbbc-145">-Tag</span></span>
<span data-ttu-id="9bbbc-146">Tag tag tag iniziali.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="9bbbc-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="9bbbc-147">-WebhookUrl</span></span>
<span data-ttu-id="9bbbc-148">URL webhook usato per le richieste di assegnazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="9bbbc-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9bbbc-149">-Confirm</span></span>
<span data-ttu-id="9bbbc-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9bbbc-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9bbbc-151">-WhatIf</span></span>
<span data-ttu-id="9bbbc-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9bbbc-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9bbbc-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bbbc-154">CommonParameters</span></span>
<span data-ttu-id="9bbbc-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bbbc-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bbbc-156">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bbbc-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bbbc-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="9bbbc-157">INPUTS</span></span>

### <span data-ttu-id="9bbbc-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9bbbc-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9bbbc-159">System.String</span><span class="sxs-lookup"><span data-stu-id="9bbbc-159">System.String</span></span>

## <span data-ttu-id="9bbbc-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9bbbc-160">OUTPUTS</span></span>

### <span data-ttu-id="9bbbc-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="9bbbc-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="9bbbc-162">NOTE</span><span class="sxs-lookup"><span data-stu-id="9bbbc-162">NOTES</span></span>

## <span data-ttu-id="9bbbc-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9bbbc-163">RELATED LINKS</span></span>
