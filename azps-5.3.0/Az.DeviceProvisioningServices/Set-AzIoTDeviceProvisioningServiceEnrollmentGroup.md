---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 3982279b8698a84f23bc83aeccd25083d98363f4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475304"
---
# <span data-ttu-id="7c505-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7c505-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="7c505-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c505-102">SYNOPSIS</span></span>
<span data-ttu-id="7c505-103">Aggiornare un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7c505-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="7c505-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c505-104">SYNTAX</span></span>

### <span data-ttu-id="7c505-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c505-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c505-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7c505-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c505-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7c505-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c505-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c505-108">DESCRIPTION</span></span>
<span data-ttu-id="7c505-109">Aggiornare un gruppo di registrazione in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="7c505-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="7c505-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c505-110">EXAMPLES</span></span>

### <span data-ttu-id="7c505-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7c505-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="7c505-112">Aggiornare i criteri di allocazione e gli hub per un gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7c505-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="7c505-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="7c505-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="7c505-114">Aggiornare lo stato Twin iniziale di un gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7c505-114">Update an enrollment group's initial twin state.</span></span>

## <span data-ttu-id="7c505-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c505-115">PARAMETERS</span></span>

### <span data-ttu-id="7c505-116">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="7c505-116">-AllocationPolicy</span></span>
<span data-ttu-id="7c505-117">Tipo di allocazione per il dispositivo assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="7c505-117">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="7c505-118">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="7c505-118">-ApiVersion</span></span>
<span data-ttu-id="7c505-119">Versione API del servizio di provisioning nella richiesta di allocazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="7c505-119">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="7c505-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c505-120">-DefaultProfile</span></span>
<span data-ttu-id="7c505-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c505-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c505-122">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="7c505-122">-Desired</span></span>
<span data-ttu-id="7c505-123">Proprietà desiderate Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="7c505-123">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="7c505-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="7c505-124">-DpsName</span></span>
<span data-ttu-id="7c505-125">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="7c505-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7c505-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="7c505-126">-DpsObject</span></span>
<span data-ttu-id="7c505-127">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="7c505-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="7c505-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="7c505-128">-EdgeEnabled</span></span>
<span data-ttu-id="7c505-129">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="7c505-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="7c505-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="7c505-130">-IotHub</span></span>
<span data-ttu-id="7c505-131">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c505-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="7c505-132">Usare l'elenco separato da spazi per più hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="7c505-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="7c505-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="7c505-133">-IotHubHostName</span></span>
<span data-ttu-id="7c505-134">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="7c505-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="7c505-135">-Nome</span><span class="sxs-lookup"><span data-stu-id="7c505-135">-Name</span></span>
<span data-ttu-id="7c505-136">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7c505-136">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="7c505-137">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="7c505-137">-ProvisioningStatus</span></span>
<span data-ttu-id="7c505-138">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="7c505-138">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="7c505-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="7c505-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="7c505-140">Dati del dispositivo da gestire su ridisposizione a hub molto diversi.</span><span class="sxs-lookup"><span data-stu-id="7c505-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="7c505-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c505-141">-ResourceGroupName</span></span>
<span data-ttu-id="7c505-142">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7c505-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7c505-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c505-143">-ResourceId</span></span>
<span data-ttu-id="7c505-144">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="7c505-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="7c505-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="7c505-145">-Tag</span></span>
<span data-ttu-id="7c505-146">Tag Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="7c505-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="7c505-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="7c505-147">-WebhookUrl</span></span>
<span data-ttu-id="7c505-148">URL di Webhook usato per le richieste di allocazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="7c505-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="7c505-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c505-149">-Confirm</span></span>
<span data-ttu-id="7c505-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c505-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c505-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c505-151">-WhatIf</span></span>
<span data-ttu-id="7c505-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c505-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c505-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c505-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c505-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c505-154">CommonParameters</span></span>
<span data-ttu-id="7c505-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c505-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c505-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c505-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c505-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c505-157">INPUTS</span></span>

### <span data-ttu-id="7c505-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="7c505-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="7c505-159">System. String</span><span class="sxs-lookup"><span data-stu-id="7c505-159">System.String</span></span>

## <span data-ttu-id="7c505-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c505-160">OUTPUTS</span></span>

### <span data-ttu-id="7c505-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="7c505-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="7c505-162">Note</span><span class="sxs-lookup"><span data-stu-id="7c505-162">NOTES</span></span>

## <span data-ttu-id="7c505-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c505-163">RELATED LINKS</span></span>
