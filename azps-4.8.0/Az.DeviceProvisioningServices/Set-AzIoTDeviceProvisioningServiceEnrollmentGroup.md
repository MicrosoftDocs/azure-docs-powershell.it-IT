---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: e7b0a5296147408633316ed27f0cba87a65d3a2a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031755"
---
# <span data-ttu-id="387a5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="387a5-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="387a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="387a5-102">SYNOPSIS</span></span>
<span data-ttu-id="387a5-103">Aggiornare un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="387a5-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="387a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="387a5-104">SYNTAX</span></span>

### <span data-ttu-id="387a5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="387a5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387a5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="387a5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="387a5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="387a5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="387a5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="387a5-108">DESCRIPTION</span></span>
<span data-ttu-id="387a5-109">Aggiornare un gruppo di registrazione in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="387a5-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="387a5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="387a5-110">EXAMPLES</span></span>

### <span data-ttu-id="387a5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="387a5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="387a5-112">Aggiornare i criteri di allocazione e gli hub per un gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="387a5-112">Update allocation policy and hubs for an enrollment group.</span></span>

## <span data-ttu-id="387a5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="387a5-113">PARAMETERS</span></span>

### <span data-ttu-id="387a5-114">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="387a5-114">-AllocationPolicy</span></span>
<span data-ttu-id="387a5-115">Tipo di allocazione per il dispositivo assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="387a5-115">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="387a5-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="387a5-116">-ApiVersion</span></span>
<span data-ttu-id="387a5-117">Versione API del servizio di provisioning nella richiesta di allocazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="387a5-117">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="387a5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="387a5-118">-DefaultProfile</span></span>
<span data-ttu-id="387a5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="387a5-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="387a5-120">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="387a5-120">-Desired</span></span>
<span data-ttu-id="387a5-121">Proprietà desiderate Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="387a5-121">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="387a5-122">-DpsName</span><span class="sxs-lookup"><span data-stu-id="387a5-122">-DpsName</span></span>
<span data-ttu-id="387a5-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="387a5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="387a5-124">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="387a5-124">-DpsObject</span></span>
<span data-ttu-id="387a5-125">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="387a5-125">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="387a5-126">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="387a5-126">-EdgeEnabled</span></span>
<span data-ttu-id="387a5-127">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="387a5-127">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="387a5-128">-IotHub</span><span class="sxs-lookup"><span data-stu-id="387a5-128">-IotHub</span></span>
<span data-ttu-id="387a5-129">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="387a5-129">Host name of target IoT Hub.</span></span>
<span data-ttu-id="387a5-130">Usare l'elenco separato da spazi per più hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="387a5-130">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="387a5-131">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="387a5-131">-IotHubHostName</span></span>
<span data-ttu-id="387a5-132">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="387a5-132">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="387a5-133">-Nome</span><span class="sxs-lookup"><span data-stu-id="387a5-133">-Name</span></span>
<span data-ttu-id="387a5-134">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="387a5-134">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="387a5-135">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="387a5-135">-ProvisioningStatus</span></span>
<span data-ttu-id="387a5-136">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="387a5-136">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="387a5-137">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="387a5-137">-ReprovisionPolicy</span></span>
<span data-ttu-id="387a5-138">Dati del dispositivo da gestire su ridisposizione a hub molto diversi.</span><span class="sxs-lookup"><span data-stu-id="387a5-138">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="387a5-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="387a5-139">-ResourceGroupName</span></span>
<span data-ttu-id="387a5-140">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="387a5-140">Name of the Resource Group</span></span>

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

### <span data-ttu-id="387a5-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="387a5-141">-ResourceId</span></span>
<span data-ttu-id="387a5-142">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="387a5-142">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="387a5-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="387a5-143">-Tag</span></span>
<span data-ttu-id="387a5-144">Tag Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="387a5-144">Initial twin tags.</span></span>

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

### <span data-ttu-id="387a5-145">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="387a5-145">-WebhookUrl</span></span>
<span data-ttu-id="387a5-146">URL di Webhook usato per le richieste di allocazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="387a5-146">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="387a5-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="387a5-147">-Confirm</span></span>
<span data-ttu-id="387a5-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="387a5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="387a5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="387a5-149">-WhatIf</span></span>
<span data-ttu-id="387a5-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="387a5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="387a5-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="387a5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="387a5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="387a5-152">CommonParameters</span></span>
<span data-ttu-id="387a5-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="387a5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="387a5-154">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="387a5-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="387a5-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="387a5-155">INPUTS</span></span>

### <span data-ttu-id="387a5-156">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="387a5-156">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="387a5-157">System. String</span><span class="sxs-lookup"><span data-stu-id="387a5-157">System.String</span></span>

## <span data-ttu-id="387a5-158">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="387a5-158">OUTPUTS</span></span>

### <span data-ttu-id="387a5-159">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="387a5-159">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="387a5-160">Note</span><span class="sxs-lookup"><span data-stu-id="387a5-160">NOTES</span></span>

## <span data-ttu-id="387a5-161">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="387a5-161">RELATED LINKS</span></span>
