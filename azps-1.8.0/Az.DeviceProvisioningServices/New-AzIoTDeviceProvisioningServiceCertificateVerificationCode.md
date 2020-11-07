---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/new-aziotdeviceprovisioningservicecertificateverificationcode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/New-AzIoTDeviceProvisioningServiceCertificateVerificationCode.md
ms.openlocfilehash: 7bf897cdb3a3967a94dcb932859bad24f496c441
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93678879"
---
# <span data-ttu-id="12f13-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span><span class="sxs-lookup"><span data-stu-id="12f13-101">New-AzIoTDeviceProvisioningServiceCertificateVerificationCode</span></span>

## <span data-ttu-id="12f13-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="12f13-102">SYNOPSIS</span></span>
<span data-ttu-id="12f13-103">Genera un codice di verifica per un certificato del servizio di provisioning di un dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="12f13-103">Generate a verification code for an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="12f13-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="12f13-104">SYNTAX</span></span>

### <span data-ttu-id="12f13-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="12f13-105">ResourceSet (Default)</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12f13-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="12f13-106">InputObjectSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-InputObject] <PSCertificateResponse>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12f13-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="12f13-107">ResourceIdSet</span></span>
```
New-AzIoTDeviceProvisioningServiceCertificateVerificationCode [-ResourceId] <String> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12f13-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="12f13-108">DESCRIPTION</span></span>
<span data-ttu-id="12f13-109">Questo codice di verifica viene usato per completare il passaggio della prova del possesso per un certificato.</span><span class="sxs-lookup"><span data-stu-id="12f13-109">This verification code is used to complete the proof of possession step for a certificate.</span></span> <span data-ttu-id="12f13-110">Usare questo codice di verifica come CN di un nuovo certificato firmato con la chiave privata certificati radice.</span><span class="sxs-lookup"><span data-stu-id="12f13-110">Use this verification code as the CN of a new certificate signed with the root certificates private key.</span></span>
<span data-ttu-id="12f13-111">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="12f13-111">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="12f13-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="12f13-112">EXAMPLES</span></span>

### <span data-ttu-id="12f13-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="12f13-113">Example 1</span></span>
```
PS C:\> New-AzIoTDeviceProvisioningServiceCertificateVerificationCode -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE="

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

<span data-ttu-id="12f13-114">Genera un codice di verifica per "certificato".</span><span class="sxs-lookup"><span data-stu-id="12f13-114">Generate a verification code for "mycertificate".</span></span>

### <span data-ttu-id="12f13-115">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="12f13-115">Example 2</span></span>
```
PS C:\> Get-AzIoTDpsCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" | New-AzIoTDpsCVC

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

<span data-ttu-id="12f13-116">Genera un codice di verifica per "certificato" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="12f13-116">Generate a verification code for "mycertificate" using pipeline.</span></span>

## <span data-ttu-id="12f13-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="12f13-117">PARAMETERS</span></span>

### <span data-ttu-id="12f13-118">-Certificate</span><span class="sxs-lookup"><span data-stu-id="12f13-118">-CertificateName</span></span>
<span data-ttu-id="12f13-119">Nome del certificato del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="12f13-119">Name of the Iot device provisioning service certificate</span></span>

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

### <span data-ttu-id="12f13-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12f13-120">-DefaultProfile</span></span>
<span data-ttu-id="12f13-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="12f13-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12f13-122">-ETag</span><span class="sxs-lookup"><span data-stu-id="12f13-122">-Etag</span></span>
<span data-ttu-id="12f13-123">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="12f13-123">Etag of the Certificate</span></span>

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

### <span data-ttu-id="12f13-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12f13-124">-InputObject</span></span>
<span data-ttu-id="12f13-125">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="12f13-125">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="12f13-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="12f13-126">-Name</span></span>
<span data-ttu-id="12f13-127">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="12f13-127">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="12f13-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12f13-128">-ResourceGroupName</span></span>
<span data-ttu-id="12f13-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="12f13-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="12f13-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12f13-130">-ResourceId</span></span>
<span data-ttu-id="12f13-131">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="12f13-131">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="12f13-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="12f13-132">-Confirm</span></span>
<span data-ttu-id="12f13-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12f13-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12f13-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12f13-134">-WhatIf</span></span>
<span data-ttu-id="12f13-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12f13-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12f13-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="12f13-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12f13-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12f13-137">CommonParameters</span></span>
<span data-ttu-id="12f13-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12f13-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12f13-139">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12f13-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12f13-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="12f13-140">INPUTS</span></span>

### <span data-ttu-id="12f13-141">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="12f13-141">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="12f13-142">System. String</span><span class="sxs-lookup"><span data-stu-id="12f13-142">System.String</span></span>

## <span data-ttu-id="12f13-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="12f13-143">OUTPUTS</span></span>

### <span data-ttu-id="12f13-144">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSVerificationCodeResponse</span><span class="sxs-lookup"><span data-stu-id="12f13-144">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSVerificationCodeResponse</span></span>

## <span data-ttu-id="12f13-145">Note</span><span class="sxs-lookup"><span data-stu-id="12f13-145">NOTES</span></span>

## <span data-ttu-id="12f13-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="12f13-146">RELATED LINKS</span></span>
