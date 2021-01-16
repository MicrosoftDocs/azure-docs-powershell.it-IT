---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 7000d7cc6922cec022efad9faca2e61e539af0e2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475335"
---
# <span data-ttu-id="af74c-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="af74c-101">Add-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="af74c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="af74c-102">SYNOPSIS</span></span>
<span data-ttu-id="af74c-103">Creare un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="af74c-103">Create a device enrollment group.</span></span>

## <span data-ttu-id="af74c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="af74c-104">SYNTAX</span></span>

### <span data-ttu-id="af74c-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="af74c-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af74c-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="af74c-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af74c-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="af74c-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 -AttestationType <PSAttestationMechanismType> [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af74c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="af74c-108">DESCRIPTION</span></span>
<span data-ttu-id="af74c-109">Creare un gruppo di registrazione in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="af74c-109">Create an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="af74c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="af74c-110">EXAMPLES</span></span>

### <span data-ttu-id="af74c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="af74c-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="af74c-112">Creare una registrazione con il tipo di attestazione</span><span class="sxs-lookup"><span data-stu-id="af74c-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="af74c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="af74c-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="af74c-114">Creare una registrazione con il tipo di attestazione X509</span><span class="sxs-lookup"><span data-stu-id="af74c-114">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="af74c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="af74c-115">Example 3</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="af74c-116">Crea una registrazione con il tipo di attestazione e l'iniziale stato Twin.</span><span class="sxs-lookup"><span data-stu-id="af74c-116">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="af74c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="af74c-117">PARAMETERS</span></span>

### <span data-ttu-id="af74c-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="af74c-118">-AllocationPolicy</span></span>
<span data-ttu-id="af74c-119">Tipo di allocazione per il dispositivo assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="af74c-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="af74c-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="af74c-120">-ApiVersion</span></span>
<span data-ttu-id="af74c-121">Versione API del servizio di provisioning nella richiesta di allocazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="af74c-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="af74c-122">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="af74c-122">-AttestationType</span></span>
<span data-ttu-id="af74c-123">Meccanismo di attestazione.</span><span class="sxs-lookup"><span data-stu-id="af74c-123">Attestation Mechanism.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSAttestationMechanismType
Parameter Sets: (All)
Aliases:
Accepted values: None, Tpm, X509, SymmetricKey

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="af74c-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af74c-124">-DefaultProfile</span></span>
<span data-ttu-id="af74c-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="af74c-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af74c-126">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="af74c-126">-Desired</span></span>
<span data-ttu-id="af74c-127">Proprietà desiderate Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="af74c-127">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="af74c-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="af74c-128">-DpsName</span></span>
<span data-ttu-id="af74c-129">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="af74c-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="af74c-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="af74c-130">-DpsObject</span></span>
<span data-ttu-id="af74c-131">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="af74c-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="af74c-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="af74c-132">-EdgeEnabled</span></span>
<span data-ttu-id="af74c-133">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="af74c-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="af74c-134">-IotHub</span><span class="sxs-lookup"><span data-stu-id="af74c-134">-IotHub</span></span>
<span data-ttu-id="af74c-135">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af74c-135">Host name of target IoT Hub.</span></span>
<span data-ttu-id="af74c-136">Usare l'elenco separato da spazi per più hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="af74c-136">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="af74c-137">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="af74c-137">-IotHubHostName</span></span>
<span data-ttu-id="af74c-138">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="af74c-138">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="af74c-139">-Nome</span><span class="sxs-lookup"><span data-stu-id="af74c-139">-Name</span></span>
<span data-ttu-id="af74c-140">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="af74c-140">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="af74c-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="af74c-141">-PrimaryCAName</span></span>
<span data-ttu-id="af74c-142">Nome del certificato della CA radice principale.</span><span class="sxs-lookup"><span data-stu-id="af74c-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="af74c-143">Se è desiderato l'attestazione con un certificato CA radice, deve essere specificato un nome della CA radice.</span><span class="sxs-lookup"><span data-stu-id="af74c-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="af74c-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="af74c-144">-PrimaryCertificate</span></span>
<span data-ttu-id="af74c-145">Percorso del file contenente il certificato principale.</span><span class="sxs-lookup"><span data-stu-id="af74c-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="af74c-146">Rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="af74c-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="af74c-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="af74c-147">-PrimaryKey</span></span>
<span data-ttu-id="af74c-148">Chiave di accesso condiviso simmetrica primaria archiviata in formato Base64.</span><span class="sxs-lookup"><span data-stu-id="af74c-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="af74c-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="af74c-149">-ProvisioningStatus</span></span>
<span data-ttu-id="af74c-150">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="af74c-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="af74c-151">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="af74c-151">-ReprovisionPolicy</span></span>
<span data-ttu-id="af74c-152">Dati del dispositivo da gestire su ridisposizione a hub molto diversi.</span><span class="sxs-lookup"><span data-stu-id="af74c-152">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="af74c-153">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af74c-153">-ResourceGroupName</span></span>
<span data-ttu-id="af74c-154">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="af74c-154">Name of the Resource Group</span></span>

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

### <span data-ttu-id="af74c-155">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af74c-155">-ResourceId</span></span>
<span data-ttu-id="af74c-156">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="af74c-156">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="af74c-157">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="af74c-157">-RootCertificate</span></span>
<span data-ttu-id="af74c-158">Consente di creare X509attestation usando i certificati radice.</span><span class="sxs-lookup"><span data-stu-id="af74c-158">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="af74c-159">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="af74c-159">-SecondaryCAName</span></span>
<span data-ttu-id="af74c-160">Nome del certificato della CA radice secondaria.</span><span class="sxs-lookup"><span data-stu-id="af74c-160">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="af74c-161">Se è desiderato l'attestazione con un certificato CA radice, deve essere specificato un nome della CA radice.</span><span class="sxs-lookup"><span data-stu-id="af74c-161">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="af74c-162">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="af74c-162">-SecondaryCertificate</span></span>
<span data-ttu-id="af74c-163">Percorso del file contenente il certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="af74c-163">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="af74c-164">Rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="af74c-164">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="af74c-165">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="af74c-165">-SecondaryKey</span></span>
<span data-ttu-id="af74c-166">Chiave di accesso condiviso simmetrica secondaria archiviata in formato Base64.</span><span class="sxs-lookup"><span data-stu-id="af74c-166">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="af74c-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="af74c-167">-Tag</span></span>
<span data-ttu-id="af74c-168">Tag Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="af74c-168">Initial twin tags.</span></span>

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

### <span data-ttu-id="af74c-169">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="af74c-169">-WebhookUrl</span></span>
<span data-ttu-id="af74c-170">URL di Webhook usato per le richieste di allocazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="af74c-170">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="af74c-171">-Confermare</span><span class="sxs-lookup"><span data-stu-id="af74c-171">-Confirm</span></span>
<span data-ttu-id="af74c-172">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af74c-172">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af74c-173">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af74c-173">-WhatIf</span></span>
<span data-ttu-id="af74c-174">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af74c-174">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af74c-175">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="af74c-175">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af74c-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af74c-176">CommonParameters</span></span>
<span data-ttu-id="af74c-177">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af74c-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af74c-178">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af74c-178">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af74c-179">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="af74c-179">INPUTS</span></span>

### <span data-ttu-id="af74c-180">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="af74c-180">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="af74c-181">System. String</span><span class="sxs-lookup"><span data-stu-id="af74c-181">System.String</span></span>

## <span data-ttu-id="af74c-182">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="af74c-182">OUTPUTS</span></span>

### <span data-ttu-id="af74c-183">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="af74c-183">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="af74c-184">Note</span><span class="sxs-lookup"><span data-stu-id="af74c-184">NOTES</span></span>

## <span data-ttu-id="af74c-185">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="af74c-185">RELATED LINKS</span></span>
