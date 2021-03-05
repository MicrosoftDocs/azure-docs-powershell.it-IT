---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: 4087cb324f55d6445458fce2a8b79f5c39308b69
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985080"
---
# <span data-ttu-id="923c5-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="923c5-101">Set-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="923c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="923c5-102">SYNOPSIS</span></span>
<span data-ttu-id="923c5-103">Aggiornare un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="923c5-103">Update a device enrollment record.</span></span>

## <span data-ttu-id="923c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="923c5-104">SYNTAX</span></span>

### <span data-ttu-id="923c5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="923c5-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="923c5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="923c5-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>]
 [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>]
 [-ProvisioningStatus <PSProvisioningStatus>] [-IotHubHostName <String>] [-IotHub <String[]>]
 [-WebhookUrl <String>] [-ApiVersion <String>] [-EndorsementKey <String>] [-StorageRootKey <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="923c5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="923c5-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 [-DeviceId <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="923c5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="923c5-108">DESCRIPTION</span></span>
<span data-ttu-id="923c5-109">Aggiornare la registrazione di un dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="923c5-109">Update a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="923c5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="923c5-110">EXAMPLES</span></span>

### <span data-ttu-id="923c5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="923c5-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="923c5-112">Aggiornare i criteri di assegnazione e gli hub per un record di registrazione.</span><span class="sxs-lookup"><span data-stu-id="923c5-112">Update allocation policy and hubs for an enrollment record.</span></span>

### <span data-ttu-id="923c5-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="923c5-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="923c5-114">Aggiornare lo stato iniziale della registrazione.</span><span class="sxs-lookup"><span data-stu-id="923c5-114">Update an enrollment's initial twin state.</span></span>

### <span data-ttu-id="923c5-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="923c5-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -PrimaryCertificate ".\primaryCertificate.cer" -SecondaryCertificate ".\secondaryCertificate.cer"
```

<span data-ttu-id="923c5-116">Aggiornare i certificati primario e secondario di una chiave simmetrica</span><span class="sxs-lookup"><span data-stu-id="923c5-116">Update a symmetric key enrollment's primary and secondary certificates</span></span>

## <span data-ttu-id="923c5-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="923c5-117">PARAMETERS</span></span>

### <span data-ttu-id="923c5-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="923c5-118">-AllocationPolicy</span></span>
<span data-ttu-id="923c5-119">Tipo di allocazione per il dispositivo assegnato all'Hub.</span><span class="sxs-lookup"><span data-stu-id="923c5-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="923c5-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="923c5-120">-ApiVersion</span></span>
<span data-ttu-id="923c5-121">Versione API del servizio di provisioning nella richiesta di assegnazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="923c5-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="923c5-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="923c5-122">-DefaultProfile</span></span>
<span data-ttu-id="923c5-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="923c5-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="923c5-124">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="923c5-124">-Desired</span></span>
<span data-ttu-id="923c5-125">Proprietà iniziali desiderate.</span><span class="sxs-lookup"><span data-stu-id="923c5-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="923c5-126">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="923c5-126">-DeviceId</span></span>
<span data-ttu-id="923c5-127">ID dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="923c5-127">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="923c5-128">-DpsName</span><span class="sxs-lookup"><span data-stu-id="923c5-128">-DpsName</span></span>
<span data-ttu-id="923c5-129">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="923c5-129">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="923c5-130">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="923c5-130">-DpsObject</span></span>
<span data-ttu-id="923c5-131">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="923c5-131">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="923c5-132">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="923c5-132">-EdgeEnabled</span></span>
<span data-ttu-id="923c5-133">Flag che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="923c5-133">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="923c5-134">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="923c5-134">-EndorsementKey</span></span>
<span data-ttu-id="923c5-135">Chiave di supporto TPM per un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="923c5-135">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="923c5-136">-IotHub</span><span class="sxs-lookup"><span data-stu-id="923c5-136">-IotHub</span></span>
<span data-ttu-id="923c5-137">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="923c5-137">Host name of target IoT Hub.</span></span>
<span data-ttu-id="923c5-138">Usare un elenco separato da spazi per più hub IoT.</span><span class="sxs-lookup"><span data-stu-id="923c5-138">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="923c5-139">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="923c5-139">-IotHubHostName</span></span>
<span data-ttu-id="923c5-140">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="923c5-140">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="923c5-141">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="923c5-141">-PrimaryCAName</span></span>
<span data-ttu-id="923c5-142">Nome del certificato CA radice principale.</span><span class="sxs-lookup"><span data-stu-id="923c5-142">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="923c5-143">Se si desidera l'attestazione con un certificato CA radice, è necessario specificare un nome di ca radice.</span><span class="sxs-lookup"><span data-stu-id="923c5-143">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="923c5-144">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="923c5-144">-PrimaryCertificate</span></span>
<span data-ttu-id="923c5-145">Percorso del file che contiene il certificato principale.</span><span class="sxs-lookup"><span data-stu-id="923c5-145">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="923c5-146">Rappresentazione in base 64 del file con estensione cer o pem del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="923c5-146">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="923c5-147">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="923c5-147">-PrimaryKey</span></span>
<span data-ttu-id="923c5-148">Chiave di accesso condiviso simmetrica primaria archiviata in formato base64.</span><span class="sxs-lookup"><span data-stu-id="923c5-148">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="923c5-149">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="923c5-149">-ProvisioningStatus</span></span>
<span data-ttu-id="923c5-150">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="923c5-150">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="923c5-151">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="923c5-151">-RegistrationId</span></span>
<span data-ttu-id="923c5-152">ID registrazione individuale.</span><span class="sxs-lookup"><span data-stu-id="923c5-152">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="923c5-153">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="923c5-153">-ReprovisionPolicy</span></span>
<span data-ttu-id="923c5-154">Dati del dispositivo da gestire durante il nuovo provisioning al diverso Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="923c5-154">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="923c5-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="923c5-155">-ResourceGroupName</span></span>
<span data-ttu-id="923c5-156">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="923c5-156">Name of the Resource Group</span></span>

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

### <span data-ttu-id="923c5-157">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="923c5-157">-ResourceId</span></span>
<span data-ttu-id="923c5-158">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="923c5-158">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="923c5-159">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="923c5-159">-RootCertificate</span></span>
<span data-ttu-id="923c5-160">Passare all'aggiornamento X509attestation mediante certificati radice.</span><span class="sxs-lookup"><span data-stu-id="923c5-160">Switch to update X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="923c5-161">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="923c5-161">-SecondaryCAName</span></span>
<span data-ttu-id="923c5-162">Nome del certificato CA radice secondario.</span><span class="sxs-lookup"><span data-stu-id="923c5-162">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="923c5-163">Se si desidera l'attestazione con un certificato CA radice, è necessario specificare un nome di ca radice.</span><span class="sxs-lookup"><span data-stu-id="923c5-163">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="923c5-164">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="923c5-164">-SecondaryCertificate</span></span>
<span data-ttu-id="923c5-165">Percorso del file che contiene il certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="923c5-165">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="923c5-166">Rappresentazione in base 64 del file con estensione cer o pem del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="923c5-166">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="923c5-167">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="923c5-167">-SecondaryKey</span></span>
<span data-ttu-id="923c5-168">Chiave di accesso condiviso simmetrica secondaria archiviata in formato base64.</span><span class="sxs-lookup"><span data-stu-id="923c5-168">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="923c5-169">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="923c5-169">-StorageRootKey</span></span>
<span data-ttu-id="923c5-170">Chiave radice di archiviazione TPM per un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="923c5-170">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="923c5-171">-Tag</span><span class="sxs-lookup"><span data-stu-id="923c5-171">-Tag</span></span>
<span data-ttu-id="923c5-172">Tag tag tag iniziali.</span><span class="sxs-lookup"><span data-stu-id="923c5-172">Initial twin tags.</span></span>

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

### <span data-ttu-id="923c5-173">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="923c5-173">-WebhookUrl</span></span>
<span data-ttu-id="923c5-174">URL webhook usato per le richieste di assegnazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="923c5-174">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="923c5-175">-Confirm</span><span class="sxs-lookup"><span data-stu-id="923c5-175">-Confirm</span></span>
<span data-ttu-id="923c5-176">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="923c5-176">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="923c5-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="923c5-177">-WhatIf</span></span>
<span data-ttu-id="923c5-178">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="923c5-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="923c5-179">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="923c5-179">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="923c5-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="923c5-180">CommonParameters</span></span>
<span data-ttu-id="923c5-181">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="923c5-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="923c5-182">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="923c5-182">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="923c5-183">INPUT</span><span class="sxs-lookup"><span data-stu-id="923c5-183">INPUTS</span></span>

### <span data-ttu-id="923c5-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="923c5-184">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="923c5-185">System.String</span><span class="sxs-lookup"><span data-stu-id="923c5-185">System.String</span></span>

## <span data-ttu-id="923c5-186">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="923c5-186">OUTPUTS</span></span>

### <span data-ttu-id="923c5-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="923c5-187">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="923c5-188">NOTE</span><span class="sxs-lookup"><span data-stu-id="923c5-188">NOTES</span></span>

## <span data-ttu-id="923c5-189">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="923c5-189">RELATED LINKS</span></span>
