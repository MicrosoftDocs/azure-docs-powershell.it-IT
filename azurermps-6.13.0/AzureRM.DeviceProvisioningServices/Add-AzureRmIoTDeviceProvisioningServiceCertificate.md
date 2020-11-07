---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Add-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 098689074debe4b9cf5be4d682023186b123d504
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688123"
---
# <span data-ttu-id="f4a26-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="f4a26-101">Add-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="f4a26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4a26-102">SYNOPSIS</span></span>
<span data-ttu-id="f4a26-103">Creare/aggiornare un certificato del servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="f4a26-103">Create/update an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4a26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4a26-104">SYNTAX</span></span>

### <span data-ttu-id="f4a26-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f4a26-105">ResourceSet (Default)</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a26-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f4a26-106">InputObjectSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse>
 [-CertificateName] <String> [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4a26-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f4a26-107">ResourceIdSet</span></span>
```
Add-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName] <String>
 [-Path] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f4a26-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4a26-108">DESCRIPTION</span></span>
<span data-ttu-id="f4a26-109">Carica un nuovo certificato o sostituisce il certificato esistente con lo stesso nome.</span><span class="sxs-lookup"><span data-stu-id="f4a26-109">Uploads a new certificate or to replace the existing certificate with the same name.</span></span>
<span data-ttu-id="f4a26-110">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="f4a26-110">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="f4a26-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4a26-111">EXAMPLES</span></span>

### <span data-ttu-id="f4a26-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f4a26-112">Example 1</span></span>
```
PS C:\> Add-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer"

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

<span data-ttu-id="f4a26-113">Caricare un file CER certificato CA in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="f4a26-113">Upload a CA certificate CER file to an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="f4a26-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f4a26-114">Example 2</span></span>
```
PS C:\> Add-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

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

<span data-ttu-id="f4a26-115">Aggiorna un certificato CA in un servizio di provisioning del dispositivo hub molto utile caricando un nuovo file CER.</span><span class="sxs-lookup"><span data-stu-id="f4a26-115">Updates a CA certificate in an IoT hub device provisioning service by uploading a new CER file.</span></span> 

## <span data-ttu-id="f4a26-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4a26-116">PARAMETERS</span></span>

### <span data-ttu-id="f4a26-117">-Certificate</span><span class="sxs-lookup"><span data-stu-id="f4a26-117">-CertificateName</span></span>
<span data-ttu-id="f4a26-118">Nome del certificato del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="f4a26-118">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="f4a26-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4a26-119">-DefaultProfile</span></span>
<span data-ttu-id="f4a26-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4a26-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f4a26-121">-ETag</span><span class="sxs-lookup"><span data-stu-id="f4a26-121">-Etag</span></span>
<span data-ttu-id="f4a26-122">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="f4a26-122">Etag of the Certificate</span></span>

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

### <span data-ttu-id="f4a26-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4a26-123">-InputObject</span></span>
<span data-ttu-id="f4a26-124">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="f4a26-124">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="f4a26-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="f4a26-125">-Name</span></span>
<span data-ttu-id="f4a26-126">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="f4a26-126">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="f4a26-127">-Path</span><span class="sxs-lookup"><span data-stu-id="f4a26-127">-Path</span></span>
<span data-ttu-id="f4a26-128">rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM</span><span class="sxs-lookup"><span data-stu-id="f4a26-128">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="f4a26-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4a26-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4a26-130">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f4a26-130">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f4a26-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4a26-131">-ResourceId</span></span>
<span data-ttu-id="f4a26-132">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="f4a26-132">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="f4a26-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f4a26-133">-Confirm</span></span>
<span data-ttu-id="f4a26-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4a26-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4a26-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4a26-135">-WhatIf</span></span>
<span data-ttu-id="f4a26-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4a26-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f4a26-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f4a26-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4a26-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4a26-138">CommonParameters</span></span>
<span data-ttu-id="f4a26-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4a26-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4a26-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4a26-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4a26-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4a26-141">INPUTS</span></span>

### <span data-ttu-id="f4a26-142">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="f4a26-142">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="f4a26-143">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f4a26-143">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="f4a26-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f4a26-144">System.String</span></span>

## <span data-ttu-id="f4a26-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4a26-145">OUTPUTS</span></span>

### <span data-ttu-id="f4a26-146">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="f4a26-146">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="f4a26-147">Note</span><span class="sxs-lookup"><span data-stu-id="f4a26-147">NOTES</span></span>

## <span data-ttu-id="f4a26-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4a26-148">RELATED LINKS</span></span>
