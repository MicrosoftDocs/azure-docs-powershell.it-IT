---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/add-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Add-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: d4dcf52a3a705042f994c8106bd931a8b704a049
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196423"
---
# <span data-ttu-id="a5f13-101">Add-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="a5f13-101">Add-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="a5f13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5f13-102">SYNOPSIS</span></span>
<span data-ttu-id="a5f13-103">Creare/aggiornare un certificato del servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5f13-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="a5f13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5f13-104">SYNTAX</span></span>

### <span data-ttu-id="a5f13-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a5f13-105">ResourceSet (Default)</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f13-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a5f13-106">InputObjectSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5f13-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a5f13-107">ResourceIdSet</span></span>
```
Add-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5f13-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a5f13-108">DESCRIPTION</span></span>
<span data-ttu-id="a5f13-109">Carica un nuovo certificato o per sostituire quello esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="a5f13-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="a5f13-110">Per una spiegazione dettagliata dei certificati CA nel servizio di provisioning dei dispositivi hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="a5f13-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="a5f13-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5f13-111">EXAMPLES</span></span>

### <span data-ttu-id="a5f13-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a5f13-112">Example 1</span></span>
```
PS C:\> Add-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="a5f13-113">Caricare un file CER del certificato CA in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5f13-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="a5f13-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a5f13-114">Example 2</span></span>
```
PS C:\> Add-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiothub/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC13DDE3E18D712C8414EE50969C7
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpObE=
```

<span data-ttu-id="a5f13-115">Aggiorna un certificato CA in un servizio di provisioning dei dispositivi hub IoT caricando un nuovo file CER.</span><span class="sxs-lookup"><span data-stu-id="a5f13-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="a5f13-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a5f13-116">PARAMETERS</span></span>

### <span data-ttu-id="a5f13-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="a5f13-117">-CertificateName</span></span>
<span data-ttu-id="a5f13-118">Nome del certificato del servizio di provisioning del dispositivo Iot</span><span class="sxs-lookup"><span data-stu-id="a5f13-118">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5f13-119">-DefaultProfile</span></span>
<span data-ttu-id="a5f13-120">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5f13-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5f13-121">-Etag</span><span class="sxs-lookup"><span data-stu-id="a5f13-121">-Etag</span></span>
<span data-ttu-id="a5f13-122">Etag del certificato</span><span class="sxs-lookup"><span data-stu-id="a5f13-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="a5f13-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5f13-123">-InputObject</span></span>
<span data-ttu-id="a5f13-124">Oggetto certificato del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="a5f13-124">IoT Device Provisioning Service Certificate Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5f13-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a5f13-125">-Name</span></span>
<span data-ttu-id="a5f13-126">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="a5f13-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a5f13-127">-Path</span><span class="sxs-lookup"><span data-stu-id="a5f13-127">-Path</span></span>
<span data-ttu-id="a5f13-128">Rappresentazione in base 64 del file CON ESTENSIONE CER o PEM del certificato X509</span><span class="sxs-lookup"><span data-stu-id="a5f13-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5f13-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5f13-129">-ResourceGroupName</span></span>
<span data-ttu-id="a5f13-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a5f13-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a5f13-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5f13-131">-ResourceId</span></span>
<span data-ttu-id="a5f13-132">ID risorsa certificato del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="a5f13-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="a5f13-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5f13-133">-Confirm</span></span>
<span data-ttu-id="a5f13-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5f13-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5f13-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5f13-135">-WhatIf</span></span>
<span data-ttu-id="a5f13-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5f13-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5f13-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5f13-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5f13-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5f13-138">CommonParameters</span></span>
<span data-ttu-id="a5f13-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5f13-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5f13-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5f13-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5f13-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="a5f13-141">INPUTS</span></span>

### <span data-ttu-id="a5f13-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a5f13-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="a5f13-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a5f13-143">System.String</span></span>

## <span data-ttu-id="a5f13-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5f13-144">OUTPUTS</span></span>

### <span data-ttu-id="a5f13-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="a5f13-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="a5f13-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="a5f13-146">NOTES</span></span>

## <span data-ttu-id="a5f13-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5f13-147">RELATED LINKS</span></span>
