---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/remove-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Remove-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: 566594fef5741808e4f27ccb6d1996783b5c880b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328686"
---
# <span data-ttu-id="d8981-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="d8981-101">Remove-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="d8981-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d8981-102">SYNOPSIS</span></span>
<span data-ttu-id="d8981-103">Eliminare un certificato del servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="d8981-103">Delete an Azure IoT Hub Device Provisioning Service certificate.</span></span>

## <span data-ttu-id="d8981-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d8981-104">SYNTAX</span></span>

### <span data-ttu-id="d8981-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d8981-105">ResourceSet (Default)</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName] <String> [-Etag] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8981-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="d8981-106">InputObjectSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-InputObject] <PSCertificateResponse> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8981-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="d8981-107">ResourceIdSet</span></span>
```
Remove-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-Etag] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8981-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d8981-108">DESCRIPTION</span></span>
<span data-ttu-id="d8981-109">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="d8981-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="d8981-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d8981-110">EXAMPLES</span></span>

### <span data-ttu-id="d8981-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d8981-111">Example 1</span></span>
```
PS C:\> Remove-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate" -Etag "AAAAAAFPazE=" -PassThru

True
```

<span data-ttu-id="d8981-112">Eliminare "certificato" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="d8981-112">Delete "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="d8981-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d8981-113">PARAMETERS</span></span>

### <span data-ttu-id="d8981-114">-Certificate</span><span class="sxs-lookup"><span data-stu-id="d8981-114">-CertificateName</span></span>
<span data-ttu-id="d8981-115">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="d8981-115">Name of the Certificate</span></span>

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

### <span data-ttu-id="d8981-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8981-116">-DefaultProfile</span></span>
<span data-ttu-id="d8981-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d8981-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8981-118">-ETag</span><span class="sxs-lookup"><span data-stu-id="d8981-118">-Etag</span></span>
<span data-ttu-id="d8981-119">ETag del certificato</span><span class="sxs-lookup"><span data-stu-id="d8981-119">Etag of the Certificate</span></span>

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

### <span data-ttu-id="d8981-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d8981-120">-InputObject</span></span>
<span data-ttu-id="d8981-121">Oggetto certificato del servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="d8981-121">IoT Device Provisioning Service Certificate Object</span></span>

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

### <span data-ttu-id="d8981-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="d8981-122">-Name</span></span>
<span data-ttu-id="d8981-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="d8981-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="d8981-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8981-124">-PassThru</span></span>
<span data-ttu-id="d8981-125">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d8981-125">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d8981-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8981-126">-ResourceGroupName</span></span>
<span data-ttu-id="d8981-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d8981-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="d8981-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8981-128">-ResourceId</span></span>
<span data-ttu-id="d8981-129">ID risorsa certificato del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="d8981-129">IoT Device Provisioning Service Certificate Resource Id</span></span>

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

### <span data-ttu-id="d8981-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d8981-130">-Confirm</span></span>
<span data-ttu-id="d8981-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8981-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8981-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8981-132">-WhatIf</span></span>
<span data-ttu-id="d8981-133">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8981-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8981-134">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d8981-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8981-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8981-135">CommonParameters</span></span>
<span data-ttu-id="d8981-136">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8981-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8981-137">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8981-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8981-138">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d8981-138">INPUTS</span></span>

### <span data-ttu-id="d8981-139">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="d8981-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

### <span data-ttu-id="d8981-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d8981-140">System.String</span></span>

## <span data-ttu-id="d8981-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d8981-141">OUTPUTS</span></span>

### <span data-ttu-id="d8981-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d8981-142">System.Boolean</span></span>

## <span data-ttu-id="d8981-143">Note</span><span class="sxs-lookup"><span data-stu-id="d8981-143">NOTES</span></span>

## <span data-ttu-id="d8981-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d8981-144">RELATED LINKS</span></span>
