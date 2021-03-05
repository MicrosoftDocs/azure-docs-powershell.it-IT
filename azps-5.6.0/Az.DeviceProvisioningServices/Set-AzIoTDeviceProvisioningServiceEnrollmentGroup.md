---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/set-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Set-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: 511d0445f7c27acf7ace059852f6e4a8b23655b1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101985079"
---
# <span data-ttu-id="696dc-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="696dc-101">Set-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="696dc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696dc-102">SYNOPSIS</span></span>
<span data-ttu-id="696dc-103">Aggiornare un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="696dc-103">Update a device enrollment group.</span></span>

## <span data-ttu-id="696dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="696dc-104">SYNTAX</span></span>

### <span data-ttu-id="696dc-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="696dc-105">ResourceSet (Default)</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="696dc-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="696dc-106">InputObjectSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 -Name <String> [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>]
 [-Desired <Hashtable>] [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="696dc-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="696dc-107">ResourceIdSet</span></span>
```
Set-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> -Name <String>
 [-ReprovisionPolicy <PSReprovisionType>] [-EdgeEnabled <Boolean>] [-Tag <Hashtable>] [-Desired <Hashtable>]
 [-AllocationPolicy <PSAllocationPolicy>] [-ProvisioningStatus <PSProvisioningStatus>]
 [-IotHubHostName <String>] [-IotHub <String[]>] [-WebhookUrl <String>] [-ApiVersion <String>]
 [-PrimaryKey <String>] [-SecondaryKey <String>] [-PrimaryCertificate <String>]
 [-SecondaryCertificate <String>] [-RootCertificate] [-PrimaryCAName <String>] [-SecondaryCAName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="696dc-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="696dc-108">DESCRIPTION</span></span>
<span data-ttu-id="696dc-109">Aggiornare un gruppo di registrazione in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="696dc-109">Update an enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="696dc-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="696dc-110">EXAMPLES</span></span>

### <span data-ttu-id="696dc-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="696dc-111">Example 1</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -AllocationPolicy Hashed -IotHub "hub1","hub2"
```

<span data-ttu-id="696dc-112">Aggiornare i criteri di assegnazione e gli hub per un gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="696dc-112">Update allocation policy and hubs for an enrollment group.</span></span>

### <span data-ttu-id="696dc-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="696dc-113">Example 2</span></span>
```powershell
PS C:\> $tag = @{}
PS C:\> $tag.Add("environment","updatedenv")
PS C:\> $desired = @{}
PS C:\> $desired.add("version_dps", "updateddps")
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -tag $tag -Desired $desired
```

<span data-ttu-id="696dc-114">Aggiornare lo stato iniziale del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="696dc-114">Update an enrollment group's initial twin state.</span></span>

### <span data-ttu-id="696dc-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="696dc-115">Example 3</span></span>
```powershell
PS C:\> Set-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1" -PrimaryKey "newPrimaryKey" -SecondaryKey "newSecondaryKey"
```

<span data-ttu-id="696dc-116">Aggiornare le chiavi primaria e secondaria di un gruppo di registrazione con chiave simmetrica</span><span class="sxs-lookup"><span data-stu-id="696dc-116">Update a symmetric key enrollment group's primary and secondary keys</span></span>

## <span data-ttu-id="696dc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696dc-117">PARAMETERS</span></span>

### <span data-ttu-id="696dc-118">-AllocationPolicy</span><span class="sxs-lookup"><span data-stu-id="696dc-118">-AllocationPolicy</span></span>
<span data-ttu-id="696dc-119">Tipo di allocazione per il dispositivo assegnato all'Hub.</span><span class="sxs-lookup"><span data-stu-id="696dc-119">Type of allocation for device assigned to the Hub.</span></span>

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

### <span data-ttu-id="696dc-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="696dc-120">-ApiVersion</span></span>
<span data-ttu-id="696dc-121">Versione API del servizio di provisioning nella richiesta di assegnazione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="696dc-121">The API version of the provisioning service in the custom allocation request.</span></span>

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

### <span data-ttu-id="696dc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696dc-122">-DefaultProfile</span></span>
<span data-ttu-id="696dc-123">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="696dc-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="696dc-124">-Desiderato</span><span class="sxs-lookup"><span data-stu-id="696dc-124">-Desired</span></span>
<span data-ttu-id="696dc-125">Proprietà iniziali desiderate.</span><span class="sxs-lookup"><span data-stu-id="696dc-125">Initial twin desired properties.</span></span>

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

### <span data-ttu-id="696dc-126">-DpsName</span><span class="sxs-lookup"><span data-stu-id="696dc-126">-DpsName</span></span>
<span data-ttu-id="696dc-127">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="696dc-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="696dc-128">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="696dc-128">-DpsObject</span></span>
<span data-ttu-id="696dc-129">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="696dc-129">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="696dc-130">-EdgeEnabled</span><span class="sxs-lookup"><span data-stu-id="696dc-130">-EdgeEnabled</span></span>
<span data-ttu-id="696dc-131">Flag che indica l'abilitazione del bordo.</span><span class="sxs-lookup"><span data-stu-id="696dc-131">Flag indicating edge enablement.</span></span>

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

### <span data-ttu-id="696dc-132">-IotHub</span><span class="sxs-lookup"><span data-stu-id="696dc-132">-IotHub</span></span>
<span data-ttu-id="696dc-133">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="696dc-133">Host name of target IoT Hub.</span></span>
<span data-ttu-id="696dc-134">Usare un elenco separato da spazi per più hub IoT.</span><span class="sxs-lookup"><span data-stu-id="696dc-134">Use space-separated list for multiple IoT Hubs.</span></span>

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

### <span data-ttu-id="696dc-135">-IotHubHostName</span><span class="sxs-lookup"><span data-stu-id="696dc-135">-IotHubHostName</span></span>
<span data-ttu-id="696dc-136">Nome host dell'hub IoT di destinazione.</span><span class="sxs-lookup"><span data-stu-id="696dc-136">Host name of the target IoT Hub.</span></span>

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

### <span data-ttu-id="696dc-137">-Name</span><span class="sxs-lookup"><span data-stu-id="696dc-137">-Name</span></span>
<span data-ttu-id="696dc-138">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="696dc-138">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="696dc-139">-PrimaryCAName</span><span class="sxs-lookup"><span data-stu-id="696dc-139">-PrimaryCAName</span></span>
<span data-ttu-id="696dc-140">Nome del certificato CA radice principale.</span><span class="sxs-lookup"><span data-stu-id="696dc-140">The name of the primary root CA certificate.</span></span>
<span data-ttu-id="696dc-141">Se si desidera l'attestazione con un certificato CA radice, è necessario specificare un nome di ca radice.</span><span class="sxs-lookup"><span data-stu-id="696dc-141">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="696dc-142">-PrimaryCertificate</span><span class="sxs-lookup"><span data-stu-id="696dc-142">-PrimaryCertificate</span></span>
<span data-ttu-id="696dc-143">Percorso del file che contiene il certificato principale.</span><span class="sxs-lookup"><span data-stu-id="696dc-143">The path to the file containing the primary certificate.</span></span>
<span data-ttu-id="696dc-144">Rappresentazione in base 64 del file con estensione cer o pem del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="696dc-144">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="696dc-145">-PrimaryKey</span><span class="sxs-lookup"><span data-stu-id="696dc-145">-PrimaryKey</span></span>
<span data-ttu-id="696dc-146">Chiave di accesso condiviso simmetrica primaria archiviata in formato base64.</span><span class="sxs-lookup"><span data-stu-id="696dc-146">The primary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="696dc-147">-ProvisioningStatus</span><span class="sxs-lookup"><span data-stu-id="696dc-147">-ProvisioningStatus</span></span>
<span data-ttu-id="696dc-148">Abilitare o disabilitare la voce di registrazione.</span><span class="sxs-lookup"><span data-stu-id="696dc-148">Enable or disable enrollment entry.</span></span>

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

### <span data-ttu-id="696dc-149">-ReprovisionPolicy</span><span class="sxs-lookup"><span data-stu-id="696dc-149">-ReprovisionPolicy</span></span>
<span data-ttu-id="696dc-150">Dati del dispositivo da gestire durante il nuovo provisioning al diverso Hub Iot.</span><span class="sxs-lookup"><span data-stu-id="696dc-150">Device data to be handled on re-provision to different Iot Hub.</span></span>

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

### <span data-ttu-id="696dc-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696dc-151">-ResourceGroupName</span></span>
<span data-ttu-id="696dc-152">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="696dc-152">Name of the Resource Group</span></span>

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

### <span data-ttu-id="696dc-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="696dc-153">-ResourceId</span></span>
<span data-ttu-id="696dc-154">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="696dc-154">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="696dc-155">-RootCertificate</span><span class="sxs-lookup"><span data-stu-id="696dc-155">-RootCertificate</span></span>
<span data-ttu-id="696dc-156">Consente di creare la crittografia X509 con i certificati radice.</span><span class="sxs-lookup"><span data-stu-id="696dc-156">Allows to create X509attestation using root certificates.</span></span>

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

### <span data-ttu-id="696dc-157">-SecondaryCAName</span><span class="sxs-lookup"><span data-stu-id="696dc-157">-SecondaryCAName</span></span>
<span data-ttu-id="696dc-158">Nome del certificato CA radice secondario.</span><span class="sxs-lookup"><span data-stu-id="696dc-158">The name of the secondary root CA certificate.</span></span>
<span data-ttu-id="696dc-159">Se si desidera l'attestazione con un certificato CA radice, è necessario specificare un nome di ca radice.</span><span class="sxs-lookup"><span data-stu-id="696dc-159">If attestation with a root CA certificate is desired then a root ca name must be provided.</span></span>

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

### <span data-ttu-id="696dc-160">-SecondaryCertificate</span><span class="sxs-lookup"><span data-stu-id="696dc-160">-SecondaryCertificate</span></span>
<span data-ttu-id="696dc-161">Percorso del file che contiene il certificato secondario.</span><span class="sxs-lookup"><span data-stu-id="696dc-161">The path to the file containing the secondary certificate.</span></span>
<span data-ttu-id="696dc-162">Rappresentazione in base 64 del file con estensione cer o pem del certificato X509.</span><span class="sxs-lookup"><span data-stu-id="696dc-162">Base-64 representation of X509 certificate .cer file or .pem file path.</span></span>

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

### <span data-ttu-id="696dc-163">-SecondaryKey</span><span class="sxs-lookup"><span data-stu-id="696dc-163">-SecondaryKey</span></span>
<span data-ttu-id="696dc-164">Chiave di accesso condiviso simmetrica secondaria archiviata in formato base64.</span><span class="sxs-lookup"><span data-stu-id="696dc-164">The secondary symmetric shared access key stored in base64 format.</span></span>

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

### <span data-ttu-id="696dc-165">-Tag</span><span class="sxs-lookup"><span data-stu-id="696dc-165">-Tag</span></span>
<span data-ttu-id="696dc-166">Tag tag tag iniziali.</span><span class="sxs-lookup"><span data-stu-id="696dc-166">Initial twin tags.</span></span>

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

### <span data-ttu-id="696dc-167">-WebhookUrl</span><span class="sxs-lookup"><span data-stu-id="696dc-167">-WebhookUrl</span></span>
<span data-ttu-id="696dc-168">URL webhook usato per le richieste di assegnazione personalizzate.</span><span class="sxs-lookup"><span data-stu-id="696dc-168">The webhook URL used for custom allocation requests.</span></span>

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

### <span data-ttu-id="696dc-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="696dc-169">-Confirm</span></span>
<span data-ttu-id="696dc-170">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="696dc-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="696dc-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="696dc-171">-WhatIf</span></span>
<span data-ttu-id="696dc-172">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="696dc-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="696dc-173">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="696dc-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="696dc-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696dc-174">CommonParameters</span></span>
<span data-ttu-id="696dc-175">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696dc-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696dc-176">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696dc-176">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696dc-177">INPUT</span><span class="sxs-lookup"><span data-stu-id="696dc-177">INPUTS</span></span>

### <span data-ttu-id="696dc-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="696dc-178">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="696dc-179">System.String</span><span class="sxs-lookup"><span data-stu-id="696dc-179">System.String</span></span>

## <span data-ttu-id="696dc-180">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="696dc-180">OUTPUTS</span></span>

### <span data-ttu-id="696dc-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="696dc-181">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

## <span data-ttu-id="696dc-182">NOTE</span><span class="sxs-lookup"><span data-stu-id="696dc-182">NOTES</span></span>

## <span data-ttu-id="696dc-183">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="696dc-183">RELATED LINKS</span></span>
