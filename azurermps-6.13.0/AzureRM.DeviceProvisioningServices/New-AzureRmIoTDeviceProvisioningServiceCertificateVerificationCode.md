---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 59445c2e162a7cbfce5cff26bac91d133c8928a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510991"
---
# <span data-ttu-id="8f666-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="8f666-101">New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="8f666-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8f666-102">SYNOPSIS</span></span>
<span data-ttu-id="8f666-103">Genera un codice di verifica per un certificato del servizio di provisioning di un dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="8f666-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8f666-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8f666-104">SYNTAX</span></span>

### <span data-ttu-id="8f666-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8f666-105">ResourceSet (Default)</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String>
 [-Name] <String> [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f666-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="8f666-106">InputObjectSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f666-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="8f666-107">ResourceIdSet</span></span>
```
New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f666-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8f666-108">DESCRIPTION</span></span>
<span data-ttu-id="8f666-109">Questo codice di verifica viene usato per completare il passaggio della prova del possesso per un certificato.</span><span class="sxs-lookup"><span data-stu-id="8f666-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="8f666-110">Usare questo codice di verifica come CN di un nuovo certificato firmato con la chiave privata certificati radice.</span><span class="sxs-lookup"><span data-stu-id="8f666-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="8f666-111">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="8f666-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="8f666-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8f666-112">EXAMPLES</span></span>

### <span data-ttu-id="8f666-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8f666-113">Example 1</span></span>
```
PS C:\> New-AzureRmIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="8f666-114">Genera un codice di verifica per "certificato".</span><span class="sxs-lookup"><span data-stu-id="8f666-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="8f666-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="8f666-115">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzureRmIoTDpsCVC

Id                  : /subscriptions/377cxxxxxxxxxxxx/resourceGroups/myresourcegroup/providers/Microsoft.Devices/provisioningServices/myiotdps/certificates/mycertificate
ResourceGroupName   : myresourcegroup
Name                : myiotdps
CertificateName     : mycertificate
Subject             : CN=mycertificate
Thumbprint          : 38303FC7371EC78DDE3E18D712C8414EE50969C7
VerificationCode    : A901A843EFF75419AC1F0EB460E85DF153092A0547AA30F5
Status              : Unverified
Expiry              : 1/01/2027 16:01
Created             : 1/01/2017 16:01
Etag                : AAAAAAFpGcA=
```

<span data-ttu-id="8f666-116">Genera un codice di verifica per "certificato" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="8f666-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="8f666-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8f666-117">PARAMETERS</span></span>

### <span data-ttu-id="8f666-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="8f666-118">-CertificateName</span></span>
<span data-ttu-id="8f666-119">Nome del certificato del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="8f666-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="8f666-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f666-120">-DefaultProfile</span></span>
<span data-ttu-id="8f666-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8f666-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f666-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="8f666-122">-Etag</span></span>
<span data-ttu-id="8f666-123">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="8f666-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="8f666-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f666-124">-InputObject</span></span>
<span data-ttu-id="8f666-125">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="8f666-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="8f666-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8f666-126">-Name</span></span>
<span data-ttu-id="8f666-127">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="8f666-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="8f666-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f666-128">-ResourceGroupName</span></span>
<span data-ttu-id="8f666-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="8f666-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="8f666-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f666-130">-ResourceId</span></span>
<span data-ttu-id="8f666-131">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="8f666-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="8f666-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8f666-132">-Confirm</span></span>
<span data-ttu-id="8f666-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f666-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f666-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f666-134">-WhatIf</span></span>
<span data-ttu-id="8f666-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f666-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f666-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8f666-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f666-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f666-137">CommonParameters</span></span>
<span data-ttu-id="8f666-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f666-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f666-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8f666-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f666-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8f666-140">INPUTS</span></span>

### <span data-ttu-id="8f666-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="8f666-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="8f666-142">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8f666-142">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="8f666-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8f666-143">System.String</span></span>

## <span data-ttu-id="8f666-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8f666-144">OUTPUTS</span></span>

### <span data-ttu-id="8f666-145">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="8f666-145">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="8f666-146">Note</span><span class="sxs-lookup"><span data-stu-id="8f666-146">NOTES</span></span>

## <span data-ttu-id="8f666-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8f666-147">RELATED LINKS</span></span>
