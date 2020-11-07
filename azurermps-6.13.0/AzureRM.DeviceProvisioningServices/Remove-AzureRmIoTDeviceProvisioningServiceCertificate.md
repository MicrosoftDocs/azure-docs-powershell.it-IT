---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Remove-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 64de44e74b5c6ea21d9d49b1911bcd34a74a374a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686408"
---
# <span data-ttu-id="50446-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="50446-101">Remove-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="50446-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50446-102">SYNOPSIS</span></span>
<span data-ttu-id="50446-103">Eliminare un certificato del servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="50446-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50446-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50446-104">SYNTAX</span></span>

### <span data-ttu-id="50446-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="50446-105">ResourceSet (Default)</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50446-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="50446-106">InputObjectSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50446-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="50446-107">ResourceIdSet</span></span>
```
Remove-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50446-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50446-108">DESCRIPTION</span></span>
<span data-ttu-id="50446-109">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="50446-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="50446-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50446-110">EXAMPLES</span></span>

### <span data-ttu-id="50446-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="50446-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="50446-112">Eliminare "certificato" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="50446-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="50446-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50446-113">PARAMETERS</span></span>

### <span data-ttu-id="50446-114">-Certificate</span><span class="sxs-lookup"><span data-stu-id="50446-114">-CertificateName</span></span>
<span data-ttu-id="50446-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="50446-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="50446-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50446-116">-DefaultProfile</span></span>
<span data-ttu-id="50446-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="50446-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50446-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="50446-118">-Etag</span></span>
<span data-ttu-id="50446-119">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="50446-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="50446-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50446-120">-InputObject</span></span>
<span data-ttu-id="50446-121">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="50446-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="50446-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="50446-122">-Name</span></span>
<span data-ttu-id="50446-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="50446-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="50446-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50446-124">-PassThru</span></span>
<span data-ttu-id="50446-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="50446-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="50446-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50446-126">-ResourceGroupName</span></span>
<span data-ttu-id="50446-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="50446-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="50446-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="50446-128">-ResourceId</span></span>
<span data-ttu-id="50446-129">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="50446-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="50446-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50446-130">-Confirm</span></span>
<span data-ttu-id="50446-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50446-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50446-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50446-132">-WhatIf</span></span>
<span data-ttu-id="50446-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50446-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50446-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50446-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50446-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50446-135">CommonParameters</span></span>
<span data-ttu-id="50446-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50446-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50446-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50446-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50446-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50446-138">INPUTS</span></span>

### <span data-ttu-id="50446-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="50446-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>
<span data-ttu-id="50446-140">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="50446-140">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="50446-141">System. String</span><span class="sxs-lookup"><span data-stu-id="50446-141">System.String</span></span>

## <span data-ttu-id="50446-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50446-142">OUTPUTS</span></span>

### <span data-ttu-id="50446-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50446-143">System.Boolean</span></span>

## <span data-ttu-id="50446-144">Note</span><span class="sxs-lookup"><span data-stu-id="50446-144">NOTES</span></span>

## <span data-ttu-id="50446-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50446-145">RELATED LINKS</span></span>
