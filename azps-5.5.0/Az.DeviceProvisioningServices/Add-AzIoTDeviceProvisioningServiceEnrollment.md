---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: b3c97abdee88615eedb2bb1f4452309326a4ebfa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196407"
---
# <span data-ttu-id="9cb42-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="9cb42-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="9cb42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9cb42-102">SYNOPSIS</span></span>
<span data-ttu-id="9cb42-103">Creare un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9cb42-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="9cb42-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9cb42-104">SYNTAX</span></span>

### <span data-ttu-id="9cb42-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9cb42-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb42-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="9cb42-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 -RegistrationId <String> -AttestationType <PSAttestationMechanismType> [-DeviceId <String>]
 [-EndorsementKey <String>] [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>]
 [-PrimaryCertificate <String>] [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>]
 [-SecondaryCAName <String>] [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9cb42-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="9cb42-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> -RegistrationId <String>
 -AttestationType <PSAttestationMechanismType> [-DeviceId <String>] [-EndorsementKey <String>]
 [-StorageRootKey <String>] [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9cb42-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9cb42-108">DESCRIPTION</span></span>
<span data-ttu-id="9cb42-109">Creare una registrazione del dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb42-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="9cb42-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9cb42-110">EXAMPLES</span></span>

### <span data-ttu-id="9cb42-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9cb42-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="9cb42-112">Creare una registrazione con il tipo di attestazione SymmetricKey</span><span class="sxs-lookup"><span data-stu-id="9cb42-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="9cb42-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9cb42-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="9cb42-114">Creare una registrazione con attestazione TPM.</span><span class="sxs-lookup"><span data-stu-id="9cb42-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="9cb42-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9cb42-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="9cb42-116">Creare una registrazione con tipo di attestazione X509</span><span class="sxs-lookup"><span data-stu-id="9cb42-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="9cb42-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="9cb42-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "dps1")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag -Desired $desired
```

<span data-ttu-id="9cb42-118">Creare una registrazione con il tipo di attestazione SymmetricKey e lo stato iniziale della classe.</span><span class="sxs-lookup"><span data-stu-id="9cb42-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="9cb42-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9cb42-119">PARAMETERS</span></span>

### <span data-ttu-id="9cb42-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="9cb42-120">-AllocationPolicy</span></span>
<span data-ttu-id="9cb42-121">Tipo di allocazione per il dispositivo assegnato all'Hub.</span><span class="sxs-lookup"><span data-stu-id="9cb42-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="9cb42-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9cb42-122">-ApiVersion</span></span>
<span data-ttu-id="9cb42-123">Versione API del servizio di provisioning nella richiesta di assegnazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="9cb42-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="9cb42-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="9cb42-124">-AttestationType</span></span>
<span data-ttu-id="9cb42-125">Meccanismo di attestazione.</span><span class="sxs-lookup"><span data-stu-id="9cb42-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="9cb42-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9cb42-126">-DefaultProfile</span></span>
<span data-ttu-id="9cb42-127">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9cb42-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9cb42-128">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="9cb42-128">-Desired</span></span>
<span data-ttu-id="9cb42-129">Proprietà iniziali desiderate.</span><span class="sxs-lookup"><span data-stu-id="9cb42-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="9cb42-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="9cb42-130">-DeviceId</span></span>
<span data-ttu-id="9cb42-131">ID dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="9cb42-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="9cb42-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="9cb42-132">-DpsName</span></span>
<span data-ttu-id="9cb42-133">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="9cb42-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="9cb42-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="9cb42-134">-DpsObject</span></span>
<span data-ttu-id="9cb42-135">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="9cb42-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="9cb42-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="9cb42-136">-EdgeEnabled</span></span>
<span data-ttu-id="9cb42-137">Flag che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="9cb42-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="9cb42-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="9cb42-138">-EndorsementKey</span></span>
<span data-ttu-id="9cb42-139">Chiave di supporto TPM per un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="9cb42-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="9cb42-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="9cb42-140">-IotHub</span></span>
<span data-ttu-id="9cb42-141">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9cb42-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="9cb42-142">Usare un elenco separato da spazi per più hub IoT.</span><span class="sxs-lookup"><span data-stu-id="9cb42-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="9cb42-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="9cb42-143">-IotHubHostName</span></span>
<span data-ttu-id="9cb42-144">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="9cb42-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="9cb42-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="9cb42-145">-PrimaryCAName</span></span>
<span data-ttu-id="9cb42-146">Nome del certificato CA radice principale.</span><span class="sxs-lookup"><span data-stu-id="9cb42-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="9cb42-147">Se si desidera l'attestazione con un certificato CA radice, è necessario specificare un nome di ca radice.</span><span class="sxs-lookup"><span data-stu-id="9cb42-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="9cb42-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="9cb42-148">-PrimaryCertificate</span></span>
<span data-ttu-id="9cb42-149">Percorso del file che contiene il certificato principale.</span><span class="sxs-lookup"><span data-stu-id="9cb42-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="9cb42-150">Rappresentazione in base 64 del file con estensione cer o pem del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="9cb42-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9cb42-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="9cb42-151">-PrimaryKey</span></span>
<span data-ttu-id="9cb42-152">Chiave di accesso condiviso simmetrica primaria archiviata in formato base64.</span><span class="sxs-lookup"><span data-stu-id="9cb42-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="9cb42-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="9cb42-153">-ProvisioningStatus</span></span>
<span data-ttu-id="9cb42-154">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="9cb42-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="9cb42-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="9cb42-155">-RegistrationId</span></span>
<span data-ttu-id="9cb42-156">ID registrazione individuale.</span><span class="sxs-lookup"><span data-stu-id="9cb42-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="9cb42-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="9cb42-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="9cb42-158">Dati del dispositivo da gestire durante il nuovo provisioning al diverso Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="9cb42-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="9cb42-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9cb42-159">-ResourceGroupName</span></span>
<span data-ttu-id="9cb42-160">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="9cb42-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="9cb42-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9cb42-161">-ResourceId</span></span>
<span data-ttu-id="9cb42-162">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="9cb42-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="9cb42-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="9cb42-163">-RootCertificate</span></span>
<span data-ttu-id="9cb42-164">Consente di creare la crittografia X509 con i certificati radice.</span><span class="sxs-lookup"><span data-stu-id="9cb42-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="9cb42-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="9cb42-165">-SecondaryCAName</span></span>
<span data-ttu-id="9cb42-166">Nome del certificato CA radice secondario.</span><span class="sxs-lookup"><span data-stu-id="9cb42-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="9cb42-167">Se si desidera l'attestazione con un certificato CA radice, è necessario specificare un nome di ca radice.</span><span class="sxs-lookup"><span data-stu-id="9cb42-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="9cb42-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="9cb42-168">-SecondaryCertificate</span></span>
<span data-ttu-id="9cb42-169">Percorso del file che contiene il certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="9cb42-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="9cb42-170">Rappresentazione in base 64 del file con estensione cer o pem del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="9cb42-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="9cb42-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="9cb42-171">-SecondaryKey</span></span>
<span data-ttu-id="9cb42-172">Chiave di accesso condiviso simmetrica secondaria archiviata in formato base64.</span><span class="sxs-lookup"><span data-stu-id="9cb42-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="9cb42-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="9cb42-173">-StorageRootKey</span></span>
<span data-ttu-id="9cb42-174">Chiave radice di archiviazione TPM per un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="9cb42-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="9cb42-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="9cb42-175">-Tag</span></span>
<span data-ttu-id="9cb42-176">Tag tag tag iniziali.</span><span class="sxs-lookup"><span data-stu-id="9cb42-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="9cb42-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="9cb42-177">-WebhookUrl</span></span>
<span data-ttu-id="9cb42-178">URL webhook usato per le richieste di assegnazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="9cb42-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="9cb42-179">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9cb42-179">-Confirm</span></span>
<span data-ttu-id="9cb42-180">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9cb42-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9cb42-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9cb42-181">-WhatIf</span></span>
<span data-ttu-id="9cb42-182">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cb42-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9cb42-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9cb42-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9cb42-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9cb42-184">CommonParameters</span></span>
<span data-ttu-id="9cb42-185">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9cb42-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9cb42-186">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9cb42-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9cb42-187">INPUT</span><span class="sxs-lookup"><span data-stu-id="9cb42-187">INPUTS</span></span>

### <span data-ttu-id="9cb42-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="9cb42-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="9cb42-189">System.String</span><span class="sxs-lookup"><span data-stu-id="9cb42-189">System.String</span></span>

## <span data-ttu-id="9cb42-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9cb42-190">OUTPUTS</span></span>

### <span data-ttu-id="9cb42-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="9cb42-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="9cb42-192">NOTE</span><span class="sxs-lookup"><span data-stu-id="9cb42-192">NOTES</span></span>

## <span data-ttu-id="9cb42-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9cb42-193">RELATED LINKS</span></span>
