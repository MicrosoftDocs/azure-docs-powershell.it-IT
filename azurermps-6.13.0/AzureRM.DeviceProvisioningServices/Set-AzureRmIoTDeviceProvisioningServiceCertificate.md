---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Set-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Set-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 5132d4c05b49ac4ff41933aa5c157697445cdbe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513844"
---
# <span data-ttu-id="4ff3b-101">Set-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="4ff3b-101">Set-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="4ff3b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4ff3b-102">SYNOPSIS</span></span>
<span data-ttu-id="4ff3b-103">Verificare un certificato del servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-103">Verify an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4ff3b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4ff3b-104">SYNTAX</span></span>

### <span data-ttu-id="4ff3b-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4ff3b-105">ResourceSet (Default)</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-Path] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff3b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4ff3b-106">InputObjectSet</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ff3b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4ff3b-107">ResourceIdSet</span></span>
```
Set-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-Path] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ff3b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4ff3b-108">DESCRIPTION</span></span>
<span data-ttu-id="4ff3b-109">Verificare un certificato caricando un certificato di verifica contenente il codice di verifica ottenuto chiamando genera-verifica-codice.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-109">Verify a certificate by uploading a verification certificate containing the verification code obtained by calling generate-verification-code.</span></span> <span data-ttu-id="4ff3b-110">Questo è l'ultimo passaggio del processo di prova del possesso.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-110">This is the last step in the proof of possession process.</span></span>
<span data-ttu-id="4ff3b-111">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span><span class="sxs-lookup"><span data-stu-id="4ff3b-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates</span></span>

## <span data-ttu-id="4ff3b-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4ff3b-112">EXAMPLES</span></span>

### <span data-ttu-id="4ff3b-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4ff3b-113">Example 1</span></span>
```
PS C:\> Set-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Path "c:\mycertificate.cer" -Etag "AAAAAAFpGcA="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="4ff3b-114">Verificare la proprietà della chiave privata "certificato".</span><span class="sxs-lookup"><span data-stu-id="4ff3b-114">Verify ownership of the "mycertificate" private key.</span></span>

### <span data-ttu-id="4ff3b-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4ff3b-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | Set-AzureRmIoTDpsCertificate -Path "c:\mycertificate.cer"

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
Status              : Verified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="4ff3b-116">Verificare la proprietà della chiave privata "certificato" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-116">Verify ownership of the "mycertificate" private key using pipeline.</span></span>

## <span data-ttu-id="4ff3b-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4ff3b-117">PARAMETERS</span></span>

### <span data-ttu-id="4ff3b-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="4ff3b-118">-CertificateName</span></span>
<span data-ttu-id="4ff3b-119">Nome del certificato del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4ff3b-119">Name of the Iot device provisioning service certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff3b-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ff3b-120">-DefaultProfile</span></span>
<span data-ttu-id="4ff3b-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ff3b-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="4ff3b-122">-Etag</span></span>
<span data-ttu-id="4ff3b-123">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="4ff3b-123">Etag of the Certificate</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet, ResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4ff3b-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4ff3b-124">-InputObject</span></span>
<span data-ttu-id="4ff3b-125">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4ff3b-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="4ff3b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ff3b-126">-Name</span></span>
<span data-ttu-id="4ff3b-127">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4ff3b-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4ff3b-128">-Path</span><span class="sxs-lookup"><span data-stu-id="4ff3b-128">-Path</span></span>
<span data-ttu-id="4ff3b-129">rappresentazione di base-64 del file certificato. cer di X509 o del percorso di file con estensione PEM</span><span class="sxs-lookup"><span data-stu-id="4ff3b-129">base-64 representation of X509 certificate .cer file or .pem file path</span></span>

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

### <span data-ttu-id="4ff3b-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ff3b-130">-ResourceGroupName</span></span>
<span data-ttu-id="4ff3b-131">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4ff3b-131">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4ff3b-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ff3b-132">-ResourceId</span></span>
<span data-ttu-id="4ff3b-133">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4ff3b-133">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="4ff3b-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4ff3b-134">-Confirm</span></span>
<span data-ttu-id="4ff3b-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ff3b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ff3b-136">-WhatIf</span></span>
<span data-ttu-id="4ff3b-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ff3b-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ff3b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ff3b-139">CommonParameters</span></span>
<span data-ttu-id="4ff3b-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ff3b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ff3b-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ff3b-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ff3b-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4ff3b-142">INPUTS</span></span>

### <span data-ttu-id="4ff3b-143">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4ff3b-143">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="4ff3b-144">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="4ff3b-144">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="4ff3b-145">System. String</span><span class="sxs-lookup"><span data-stu-id="4ff3b-145">System.String</span></span>

## <span data-ttu-id="4ff3b-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4ff3b-146">OUTPUTS</span></span>

### <span data-ttu-id="4ff3b-147">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4ff3b-147">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="4ff3b-148">Note</span><span class="sxs-lookup"><span data-stu-id="4ff3b-148">NOTES</span></span>

## <span data-ttu-id="4ff3b-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4ff3b-149">RELATED LINKS</span></span>
