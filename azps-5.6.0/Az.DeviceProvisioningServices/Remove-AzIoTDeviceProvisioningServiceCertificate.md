---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: fdf6e61b972b2d78db96f88bea502e2d1a4a5865
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956173"
---
# <span data-ttu-id="7fc53-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="7fc53-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="7fc53-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fc53-102">SYNOPSIS</span></span>
<span data-ttu-id="7fc53-103">Eliminare un certificato del servizio di provisioning del dispositivo Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc53-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="7fc53-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7fc53-104">SYNTAX</span></span>

### <span data-ttu-id="7fc53-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7fc53-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc53-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="7fc53-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fc53-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="7fc53-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fc53-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7fc53-108">DESCRIPTION</span></span>
<span data-ttu-id="7fc53-109">Per una spiegazione dettagliata dei certificati CA nel servizio di provisioning dei dispositivi hub IoT di Azure, vedere https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="7fc53-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="7fc53-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7fc53-110">EXAMPLES</span></span>

### <span data-ttu-id="7fc53-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7fc53-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="7fc53-112">Eliminare "mycertificate" in un servizio di provisioning di dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc53-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="7fc53-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fc53-113">PARAMETERS</span></span>

### <span data-ttu-id="7fc53-114">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="7fc53-114">-CertificateName</span></span>
<span data-ttu-id="7fc53-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="7fc53-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="7fc53-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fc53-116">-DefaultProfile</span></span>
<span data-ttu-id="7fc53-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7fc53-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fc53-118">-Etag</span><span class="sxs-lookup"><span data-stu-id="7fc53-118">-Etag</span></span>
<span data-ttu-id="7fc53-119">Etag del certificato</span><span class="sxs-lookup"><span data-stu-id="7fc53-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="7fc53-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fc53-120">-InputObject</span></span>
<span data-ttu-id="7fc53-121">Oggetto certificato del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="7fc53-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="7fc53-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7fc53-122">-Name</span></span>
<span data-ttu-id="7fc53-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="7fc53-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="7fc53-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7fc53-124">-PassThru</span></span>
<span data-ttu-id="7fc53-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="7fc53-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="7fc53-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fc53-126">-ResourceGroupName</span></span>
<span data-ttu-id="7fc53-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="7fc53-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="7fc53-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fc53-128">-ResourceId</span></span>
<span data-ttu-id="7fc53-129">ID risorsa certificato del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="7fc53-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="7fc53-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7fc53-130">-Confirm</span></span>
<span data-ttu-id="7fc53-131">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fc53-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fc53-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fc53-132">-WhatIf</span></span>
<span data-ttu-id="7fc53-133">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fc53-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fc53-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7fc53-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fc53-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fc53-135">CommonParameters</span></span>
<span data-ttu-id="7fc53-136">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fc53-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fc53-137">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fc53-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fc53-138">INPUT</span><span class="sxs-lookup"><span data-stu-id="7fc53-138">INPUTS</span></span>

### <span data-ttu-id="7fc53-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="7fc53-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="7fc53-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7fc53-140">System.String</span></span>

## <span data-ttu-id="7fc53-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7fc53-141">OUTPUTS</span></span>

### <span data-ttu-id="7fc53-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7fc53-142">System.Boolean</span></span>

## <span data-ttu-id="7fc53-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="7fc53-143">NOTES</span></span>

## <span data-ttu-id="7fc53-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7fc53-144">RELATED LINKS</span></span>
