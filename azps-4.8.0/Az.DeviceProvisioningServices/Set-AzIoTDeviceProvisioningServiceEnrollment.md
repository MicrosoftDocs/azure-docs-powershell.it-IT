---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: f8a81df2081420f8d218e094ff43f22e8dd9cc5c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191569"
---
# <span data-ttu-id="2861e-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="2861e-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="2861e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2861e-102">SYNOPSIS</span></span>
<span data-ttu-id="2861e-103">Aggiornare un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2861e-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="2861e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2861e-104">SYNTAX</span></span>

### <span data-ttu-id="2861e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2861e-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2861e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2861e-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2861e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2861e-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2861e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2861e-108">DESCRIPTION</span></span>
<span data-ttu-id="2861e-109">Aggiornare una registrazione del dispositivo in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="2861e-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2861e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2861e-110">EXAMPLES</span></span>

### <span data-ttu-id="2861e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2861e-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="2861e-112">Aggiornare i criteri di allocazione e gli hub per un record di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2861e-112">Update allocation policy and hubs for an enrollment record.</span></span>

## <span data-ttu-id="2861e-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2861e-113">PARAMETERS</span></span>

### <span data-ttu-id="2861e-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="2861e-114">-AllocationPolicy</span></span>
<span data-ttu-id="2861e-115">Tipo di allocazione per il dispositivo assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="2861e-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="2861e-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2861e-116">-ApiVersion</span></span>
<span data-ttu-id="2861e-117">Versione API del servizio di provisioning nella richiesta di allocazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="2861e-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="2861e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2861e-118">-DefaultProfile</span></span>
<span data-ttu-id="2861e-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2861e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2861e-120">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="2861e-120">-Desired</span></span>
<span data-ttu-id="2861e-121">Proprietà desiderate Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="2861e-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="2861e-122">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="2861e-122">-DeviceId</span></span>
<span data-ttu-id="2861e-123">ID dispositivo hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="2861e-123">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="2861e-124">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2861e-124">-DpsName</span></span>
<span data-ttu-id="2861e-125">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="2861e-125">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2861e-126">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2861e-126">-DpsObject</span></span>
<span data-ttu-id="2861e-127">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="2861e-127">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2861e-128">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="2861e-128">-EdgeEnabled</span></span>
<span data-ttu-id="2861e-129">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="2861e-129">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="2861e-130">-IotHub</span><span class="sxs-lookup"><span data-stu-id="2861e-130">-IotHub</span></span>
<span data-ttu-id="2861e-131">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2861e-131">Host name of target IoT Hub.</span></span>
<span data-ttu-id="2861e-132">Usare l'elenco separato da spazi per più hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="2861e-132">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="2861e-133">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="2861e-133">-IotHubHostName</span></span>
<span data-ttu-id="2861e-134">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="2861e-134">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="2861e-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="2861e-135">-ProvisioningStatus</span></span>
<span data-ttu-id="2861e-136">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2861e-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="2861e-137">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="2861e-137">-RegistrationId</span></span>
<span data-ttu-id="2861e-138">ID di registrazione dell'iscrizione individuale.</span><span class="sxs-lookup"><span data-stu-id="2861e-138">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="2861e-139">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="2861e-139">-ReprovisionPolicy</span></span>
<span data-ttu-id="2861e-140">Dati del dispositivo da gestire su ridisposizione a hub molto diversi.</span><span class="sxs-lookup"><span data-stu-id="2861e-140">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="2861e-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2861e-141">-ResourceGroupName</span></span>
<span data-ttu-id="2861e-142">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2861e-142">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2861e-143">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2861e-143">-ResourceId</span></span>
<span data-ttu-id="2861e-144">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2861e-144">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2861e-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="2861e-145">-Tag</span></span>
<span data-ttu-id="2861e-146">Tag Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="2861e-146">Initial twin tags.</span></span>

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

### <span data-ttu-id="2861e-147">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="2861e-147">-WebhookUrl</span></span>
<span data-ttu-id="2861e-148">URL di Webhook usato per le richieste di allocazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="2861e-148">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="2861e-149">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2861e-149">-Confirm</span></span>
<span data-ttu-id="2861e-150">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2861e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2861e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2861e-151">-WhatIf</span></span>
<span data-ttu-id="2861e-152">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2861e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2861e-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2861e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2861e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2861e-154">CommonParameters</span></span>
<span data-ttu-id="2861e-155">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2861e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2861e-156">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2861e-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2861e-157">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2861e-157">INPUTS</span></span>

### <span data-ttu-id="2861e-158">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2861e-158">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2861e-159">System. String</span><span class="sxs-lookup"><span data-stu-id="2861e-159">System.String</span></span>

## <span data-ttu-id="2861e-160">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2861e-160">OUTPUTS</span></span>

### <span data-ttu-id="2861e-161">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="2861e-161">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="2861e-162">Note</span><span class="sxs-lookup"><span data-stu-id="2861e-162">NOTES</span></span>

## <span data-ttu-id="2861e-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2861e-163">RELATED LINKS</span></span>
