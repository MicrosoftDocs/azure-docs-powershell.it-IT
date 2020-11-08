---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019871"
---
# <span data-ttu-id="09e6a-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="09e6a-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="09e6a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09e6a-102">SYNOPSIS</span></span>
<span data-ttu-id="09e6a-103">Eliminare un certificato del servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="09e6a-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="09e6a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09e6a-104">SYNTAX</span></span>

### <span data-ttu-id="09e6a-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="09e6a-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e6a-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="09e6a-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="09e6a-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="09e6a-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09e6a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09e6a-108">DESCRIPTION</span></span>
<span data-ttu-id="09e6a-109">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="09e6a-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="09e6a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09e6a-110">EXAMPLES</span></span>

### <span data-ttu-id="09e6a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="09e6a-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="09e6a-112">Eliminare "certificato" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="09e6a-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="09e6a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09e6a-113">PARAMETERS</span></span>

### <span data-ttu-id="09e6a-114">-Certificate</span><span class="sxs-lookup"><span data-stu-id="09e6a-114">-CertificateName</span></span>
<span data-ttu-id="09e6a-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="09e6a-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="09e6a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09e6a-116">-DefaultProfile</span></span>
<span data-ttu-id="09e6a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09e6a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09e6a-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="09e6a-118">-Etag</span></span>
<span data-ttu-id="09e6a-119">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="09e6a-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="09e6a-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="09e6a-120">-InputObject</span></span>
<span data-ttu-id="09e6a-121">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="09e6a-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="09e6a-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="09e6a-122">-Name</span></span>
<span data-ttu-id="09e6a-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="09e6a-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="09e6a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="09e6a-124">-PassThru</span></span>
<span data-ttu-id="09e6a-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="09e6a-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="09e6a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09e6a-126">-ResourceGroupName</span></span>
<span data-ttu-id="09e6a-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="09e6a-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="09e6a-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="09e6a-128">-ResourceId</span></span>
<span data-ttu-id="09e6a-129">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="09e6a-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="09e6a-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09e6a-130">-Confirm</span></span>
<span data-ttu-id="09e6a-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09e6a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="09e6a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09e6a-132">-WhatIf</span></span>
<span data-ttu-id="09e6a-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09e6a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09e6a-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09e6a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="09e6a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09e6a-135">CommonParameters</span></span>
<span data-ttu-id="09e6a-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09e6a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09e6a-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09e6a-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09e6a-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09e6a-138">INPUTS</span></span>

### <span data-ttu-id="09e6a-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="09e6a-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="09e6a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="09e6a-140">System.String</span></span>

## <span data-ttu-id="09e6a-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09e6a-141">OUTPUTS</span></span>

### <span data-ttu-id="09e6a-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="09e6a-142">System.Boolean</span></span>

## <span data-ttu-id="09e6a-143">Note</span><span class="sxs-lookup"><span data-stu-id="09e6a-143">NOTES</span></span>

## <span data-ttu-id="09e6a-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09e6a-144">RELATED LINKS</span></span>
