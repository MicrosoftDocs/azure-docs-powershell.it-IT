---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: e02d9c1ca9a5d45f081f168c3d8736d502f52094
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190214"
---
# <span data-ttu-id="4889b-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="4889b-101">Add-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="4889b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4889b-102">SYNOPSIS</span></span>
<span data-ttu-id="4889b-103">Creare un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4889b-103">Create a device enrollment record.</span></span>

## <span data-ttu-id="4889b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4889b-104">SYNTAX</span></span>

### <span data-ttu-id="4889b-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4889b-105">ResourceSet (Default)</span></span>
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

### <span data-ttu-id="4889b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4889b-106">InputObjectSet</span></span>
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

### <span data-ttu-id="4889b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4889b-107">ResourceIdSet</span></span>
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

## <span data-ttu-id="4889b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4889b-108">DESCRIPTION</span></span>
<span data-ttu-id="4889b-109">Crea una registrazione del dispositivo in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4889b-109">Create a device enrollment in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4889b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4889b-110">EXAMPLES</span></span>

### <span data-ttu-id="4889b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4889b-111">Example 1</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey
```

<span data-ttu-id="4889b-112">Creare una registrazione con il tipo di attestazione</span><span class="sxs-lookup"><span data-stu-id="4889b-112">Create an enrollment with attestation type SymmetricKey</span></span>

### <span data-ttu-id="4889b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4889b-113">Example 2</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType Tpm -EndorsementKey "endorementkey"
```

<span data-ttu-id="4889b-114">Creare una registrazione con l'attestazione TPM.</span><span class="sxs-lookup"><span data-stu-id="4889b-114">Create an enrollment with TPM attestation.</span></span>

### <span data-ttu-id="4889b-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="4889b-115">Example 3</span></span>
```powershell
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType X509 -PrimaryCertificate "D:/primary.cer"
```

<span data-ttu-id="4889b-116">Creare una registrazione con il tipo di attestazione X509</span><span class="sxs-lookup"><span data-stu-id="4889b-116">Create an enrollment with attestation type X509</span></span>

### <span data-ttu-id="4889b-117">Esempio 4</span><span class="sxs-lookup"><span data-stu-id="4889b-117">Example 4</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","test")
PS C:\> Add-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1" -AttestationType SymmetricKey -tag $tag
```

<span data-ttu-id="4889b-118">Crea una registrazione con il tipo di attestazione e l'iniziale stato Twin.</span><span class="sxs-lookup"><span data-stu-id="4889b-118">Create an enrollment with attestation type SymmetricKey and initial twin state.</span></span>

## <span data-ttu-id="4889b-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4889b-119">PARAMETERS</span></span>

### <span data-ttu-id="4889b-120">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="4889b-120">-AllocationPolicy</span></span>
<span data-ttu-id="4889b-121">Tipo di allocazione per il dispositivo assegnato all'hub.</span><span class="sxs-lookup"><span data-stu-id="4889b-121">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="4889b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4889b-122">-ApiVersion</span></span>
<span data-ttu-id="4889b-123">Versione API del servizio di provisioning nella richiesta di allocazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="4889b-123">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="4889b-124">-AttestationType</span><span class="sxs-lookup"><span data-stu-id="4889b-124">-AttestationType</span></span>
<span data-ttu-id="4889b-125">Meccanismo di attestazione.</span><span class="sxs-lookup"><span data-stu-id="4889b-125">Attestation Mechanism.</span></span>

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

### <span data-ttu-id="4889b-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4889b-126">-DefaultProfile</span></span>
<span data-ttu-id="4889b-127">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4889b-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4889b-128">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="4889b-128">-Desired</span></span>
<span data-ttu-id="4889b-129">Proprietà desiderate Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="4889b-129">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="4889b-130">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="4889b-130">-DeviceId</span></span>
<span data-ttu-id="4889b-131">ID dispositivo hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="4889b-131">IoT Hub Device ID.</span></span>

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

### <span data-ttu-id="4889b-132">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4889b-132">-DpsName</span></span>
<span data-ttu-id="4889b-133">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4889b-133">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4889b-134">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4889b-134">-DpsObject</span></span>
<span data-ttu-id="4889b-135">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4889b-135">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4889b-136">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="4889b-136">-EdgeEnabled</span></span>
<span data-ttu-id="4889b-137">Contrassegno che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="4889b-137">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="4889b-138">-EndorsementKey</span><span class="sxs-lookup"><span data-stu-id="4889b-138">-EndorsementKey</span></span>
<span data-ttu-id="4889b-139">Chiave di approvazione TPM per un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="4889b-139">TPM endorsement key for a TPM device.</span></span>

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

### <span data-ttu-id="4889b-140">-IotHub</span><span class="sxs-lookup"><span data-stu-id="4889b-140">-IotHub</span></span>
<span data-ttu-id="4889b-141">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4889b-141">Host name of target IoT Hub.</span></span>
<span data-ttu-id="4889b-142">Usare l'elenco separato da spazi per più hub di un sacco.</span><span class="sxs-lookup"><span data-stu-id="4889b-142">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="4889b-143">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="4889b-143">-IotHubHostName</span></span>
<span data-ttu-id="4889b-144">Nome host dell'hub di destinazione.</span><span class="sxs-lookup"><span data-stu-id="4889b-144">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="4889b-145">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="4889b-145">-PrimaryCAName</span></span>
<span data-ttu-id="4889b-146">Nome del certificato della CA radice principale.</span><span class="sxs-lookup"><span data-stu-id="4889b-146">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="4889b-147">Se è desiderato l'attestazione con un certificato CA radice, deve essere specificato un nome della CA radice.</span><span class="sxs-lookup"><span data-stu-id="4889b-147">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="4889b-148">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="4889b-148">-PrimaryCertificate</span></span>
<span data-ttu-id="4889b-149">Percorso del file contenente il certificato principale.</span><span class="sxs-lookup"><span data-stu-id="4889b-149">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="4889b-150">Rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="4889b-150">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="4889b-151">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="4889b-151">-PrimaryKey</span></span>
<span data-ttu-id="4889b-152">Chiave di accesso condiviso simmetrica primaria archiviata in formato Base64.</span><span class="sxs-lookup"><span data-stu-id="4889b-152">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="4889b-153">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="4889b-153">-ProvisioningStatus</span></span>
<span data-ttu-id="4889b-154">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4889b-154">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="4889b-155">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="4889b-155">-RegistrationId</span></span>
<span data-ttu-id="4889b-156">ID di registrazione dell'iscrizione individuale.</span><span class="sxs-lookup"><span data-stu-id="4889b-156">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="4889b-157">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="4889b-157">-ReprovisionPolicy</span></span>
<span data-ttu-id="4889b-158">Dati del dispositivo da gestire su ridisposizione a hub molto diversi.</span><span class="sxs-lookup"><span data-stu-id="4889b-158">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="4889b-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4889b-159">-ResourceGroupName</span></span>
<span data-ttu-id="4889b-160">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4889b-160">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4889b-161">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4889b-161">-ResourceId</span></span>
<span data-ttu-id="4889b-162">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4889b-162">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4889b-163">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="4889b-163">-RootCertificate</span></span>
<span data-ttu-id="4889b-164">Consente di creare X509attestation usando i certificati radice.</span><span class="sxs-lookup"><span data-stu-id="4889b-164">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="4889b-165">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="4889b-165">-SecondaryCAName</span></span>
<span data-ttu-id="4889b-166">Nome del certificato della CA radice secondaria.</span><span class="sxs-lookup"><span data-stu-id="4889b-166">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="4889b-167">Se è desiderato l'attestazione con un certificato CA radice, deve essere specificato un nome della CA radice.</span><span class="sxs-lookup"><span data-stu-id="4889b-167">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="4889b-168">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="4889b-168">-SecondaryCertificate</span></span>
<span data-ttu-id="4889b-169">Percorso del file contenente il certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="4889b-169">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="4889b-170">Rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM.</span><span class="sxs-lookup"><span data-stu-id="4889b-170">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="4889b-171">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="4889b-171">-SecondaryKey</span></span>
<span data-ttu-id="4889b-172">Chiave di accesso condiviso simmetrica secondaria archiviata in formato Base64.</span><span class="sxs-lookup"><span data-stu-id="4889b-172">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="4889b-173">-StorageRootKey</span><span class="sxs-lookup"><span data-stu-id="4889b-173">-StorageRootKey</span></span>
<span data-ttu-id="4889b-174">Chiave radice di archiviazione TPM per un dispositivo TPM.</span><span class="sxs-lookup"><span data-stu-id="4889b-174">TPM storage root key for a TPM device.</span></span>

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

### <span data-ttu-id="4889b-175">-Tag</span><span class="sxs-lookup"><span data-stu-id="4889b-175">-Tag</span></span>
<span data-ttu-id="4889b-176">Tag Twin iniziali.</span><span class="sxs-lookup"><span data-stu-id="4889b-176">Initial twin tags.</span></span>

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

### <span data-ttu-id="4889b-177">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="4889b-177">-WebhookUrl</span></span>
<span data-ttu-id="4889b-178">URL di Webhook usato per le richieste di allocazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="4889b-178">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="4889b-179">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4889b-179">-Confirm</span></span>
<span data-ttu-id="4889b-180">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4889b-180">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4889b-181">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4889b-181">-WhatIf</span></span>
<span data-ttu-id="4889b-182">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4889b-182">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4889b-183">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4889b-183">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4889b-184">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4889b-184">CommonParameters</span></span>
<span data-ttu-id="4889b-185">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4889b-185">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4889b-186">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4889b-186">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4889b-187">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4889b-187">INPUTS</span></span>

### <span data-ttu-id="4889b-188">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4889b-188">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4889b-189">System. String</span><span class="sxs-lookup"><span data-stu-id="4889b-189">System.String</span></span>

## <span data-ttu-id="4889b-190">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4889b-190">OUTPUTS</span></span>

### <span data-ttu-id="4889b-191">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="4889b-191">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

## <span data-ttu-id="4889b-192">Note</span><span class="sxs-lookup"><span data-stu-id="4889b-192">NOTES</span></span>

## <span data-ttu-id="4889b-193">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4889b-193">RELATED LINKS</span></span>