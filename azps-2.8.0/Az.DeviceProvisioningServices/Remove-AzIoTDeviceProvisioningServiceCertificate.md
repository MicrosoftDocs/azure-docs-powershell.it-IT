---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: e03bb9f8f996c274abe07dd3e1b005760756d632
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674535"
---
# <span data-ttu-id="faca5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="faca5-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="faca5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faca5-102">SYNOPSIS</span></span>
<span data-ttu-id="faca5-103">Eliminare un certificato del servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="faca5-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="faca5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faca5-104">SYNTAX</span></span>

### <span data-ttu-id="faca5-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="faca5-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faca5-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="faca5-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="faca5-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="faca5-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="faca5-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faca5-108">DESCRIPTION</span></span>
<span data-ttu-id="faca5-109">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="faca5-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="faca5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faca5-110">EXAMPLES</span></span>

### <span data-ttu-id="faca5-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="faca5-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="faca5-112">Eliminare "certificato" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="faca5-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="faca5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faca5-113">PARAMETERS</span></span>

### <span data-ttu-id="faca5-114">-Certificate</span><span class="sxs-lookup"><span data-stu-id="faca5-114">-CertificateName</span></span>
<span data-ttu-id="faca5-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="faca5-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="faca5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faca5-116">-DefaultProfile</span></span>
<span data-ttu-id="faca5-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="faca5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="faca5-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="faca5-118">-Etag</span></span>
<span data-ttu-id="faca5-119">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="faca5-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="faca5-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="faca5-120">-InputObject</span></span>
<span data-ttu-id="faca5-121">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="faca5-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="faca5-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="faca5-122">-Name</span></span>
<span data-ttu-id="faca5-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="faca5-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="faca5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faca5-124">-PassThru</span></span>
<span data-ttu-id="faca5-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="faca5-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="faca5-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faca5-126">-ResourceGroupName</span></span>
<span data-ttu-id="faca5-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="faca5-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="faca5-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="faca5-128">-ResourceId</span></span>
<span data-ttu-id="faca5-129">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="faca5-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="faca5-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="faca5-130">-Confirm</span></span>
<span data-ttu-id="faca5-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faca5-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faca5-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faca5-132">-WhatIf</span></span>
<span data-ttu-id="faca5-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faca5-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faca5-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faca5-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faca5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faca5-135">CommonParameters</span></span>
<span data-ttu-id="faca5-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faca5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faca5-137">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faca5-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faca5-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faca5-138">INPUTS</span></span>

### <span data-ttu-id="faca5-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="faca5-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="faca5-140">System. String</span><span class="sxs-lookup"><span data-stu-id="faca5-140">System.String</span></span>

## <span data-ttu-id="faca5-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faca5-141">OUTPUTS</span></span>

### <span data-ttu-id="faca5-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="faca5-142">System.Boolean</span></span>

## <span data-ttu-id="faca5-143">Note</span><span class="sxs-lookup"><span data-stu-id="faca5-143">NOTES</span></span>

## <span data-ttu-id="faca5-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faca5-144">RELATED LINKS</span></span>
