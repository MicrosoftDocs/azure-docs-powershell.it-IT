---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningservicecertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: aa51001163e4559dd0d3ef7edfb48abd3448c0b6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193478"
---
# <span data-ttu-id="4d717-101">Get-AzIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="4d717-101">Get-AzIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="4d717-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4d717-102">SYNOPSIS</span></span>
<span data-ttu-id="4d717-103">Elenca tutti i certificati o un determinato certificato contenuto in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4d717-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4d717-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d717-104">SYNTAX</span></span>

### <span data-ttu-id="4d717-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d717-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d717-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4d717-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4d717-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d717-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d717-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4d717-108">DESCRIPTION</span></span>
<span data-ttu-id="4d717-109">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="4d717-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="4d717-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d717-110">EXAMPLES</span></span>

### <span data-ttu-id="4d717-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4d717-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="4d717-112">Mostra i dettagli su "certificato" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="4d717-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="4d717-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4d717-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="4d717-114">Elenca tutti i certificati in "myiotdps" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="4d717-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="4d717-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4d717-115">PARAMETERS</span></span>

### <span data-ttu-id="4d717-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="4d717-116">-CertificateName</span></span>
<span data-ttu-id="4d717-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="4d717-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="4d717-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d717-118">-DefaultProfile</span></span>
<span data-ttu-id="4d717-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4d717-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d717-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4d717-120">-DpsObject</span></span>
<span data-ttu-id="4d717-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4d717-121">IoT Device Provisioning Service Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d717-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4d717-122">-Name</span></span>
<span data-ttu-id="4d717-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="4d717-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4d717-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d717-124">-ResourceGroupName</span></span>
<span data-ttu-id="4d717-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4d717-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4d717-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d717-126">-ResourceId</span></span>
<span data-ttu-id="4d717-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="4d717-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4d717-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d717-128">CommonParameters</span></span>
<span data-ttu-id="4d717-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d717-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d717-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d717-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d717-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4d717-131">INPUTS</span></span>

### <span data-ttu-id="4d717-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4d717-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4d717-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4d717-133">System.String</span></span>

## <span data-ttu-id="4d717-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d717-134">OUTPUTS</span></span>

### <span data-ttu-id="4d717-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="4d717-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="4d717-136">Note</span><span class="sxs-lookup"><span data-stu-id="4d717-136">NOTES</span></span>

## <span data-ttu-id="4d717-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d717-137">RELATED LINKS</span></span>
