---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceCertificate.md
ms.openlocfilehash: c44e36a0aa08daf7e4a9ae9822f8a4be85db5d57
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507472"
---
# <span data-ttu-id="e8e5d-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span><span class="sxs-lookup"><span data-stu-id="e8e5d-101">Get-AzureRmIoTDeviceProvisioningServiceCertificate</span></span>

## <span data-ttu-id="e8e5d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e8e5d-102">SYNOPSIS</span></span>
<span data-ttu-id="e8e5d-103">Elenca tutti i certificati o un determinato certificato contenuto in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="e8e5d-103">Lists all certificates or a particular certificate contained within an Azure IoT Hub Device Provisioning Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8e5d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e8e5d-104">SYNTAX</span></span>

### <span data-ttu-id="e8e5d-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e8e5d-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceGroupName] <String> [-Name] <String>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e5d-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e8e5d-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-DpsObject] <PSProvisioningServiceDescription>
 [-CertificateName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e8e5d-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="e8e5d-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceCertificate [-ResourceId] <String> [-CertificateName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8e5d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e8e5d-108">DESCRIPTION</span></span>
<span data-ttu-id="e8e5d-109">Per una spiegazione dettagliata dei certificati della CA nel servizio di provisioning del dispositivo hub di Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates .</span><span class="sxs-lookup"><span data-stu-id="e8e5d-109">For a detailed explanation of CA certificates in Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/how-to-verify-certificates.</span></span>

## <span data-ttu-id="e8e5d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e8e5d-110">EXAMPLES</span></span>

### <span data-ttu-id="e8e5d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e8e5d-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceCertificate -ResourceGroupName "myresourcegroup" -Name "myiotdps" -CertificateName "mycertificate"

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

<span data-ttu-id="e8e5d-112">Mostra i dettagli su "certificato" in un servizio di provisioning del dispositivo hub di Azure molto.</span><span class="sxs-lookup"><span data-stu-id="e8e5d-112">Show details about "mycertificate" in an Azure IoT Hub device provisioning service.</span></span>

### <span data-ttu-id="e8e5d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="e8e5d-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDps -ResourceGroupName "myresourcegroup" -Name "myiotdps" | Get-AzureRmIoTDpsCertificate

ResourceGroupName   Name        CertificateName Status     Expiry
-----------------   ----        --------------- ------     ------
myresourcegroup     myiotdps    mycert1         Unverified 12/04/2027 13:12
myresourcegroup     myiotdps    mycert2         Unverified 12/04/2027 13:12
```

<span data-ttu-id="e8e5d-114">Elenca tutti i certificati in "myiotdps" usando pipeline.</span><span class="sxs-lookup"><span data-stu-id="e8e5d-114">List all certificates in "myiotdps" using pipeline.</span></span>

## <span data-ttu-id="e8e5d-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e8e5d-115">PARAMETERS</span></span>

### <span data-ttu-id="e8e5d-116">-Certificate</span><span class="sxs-lookup"><span data-stu-id="e8e5d-116">-CertificateName</span></span>
<span data-ttu-id="e8e5d-117">Nome del certificato</span><span class="sxs-lookup"><span data-stu-id="e8e5d-117">Name of the Certificate</span></span>

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

### <span data-ttu-id="e8e5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8e5d-118">-DefaultProfile</span></span>
<span data-ttu-id="e8e5d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e8e5d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8e5d-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="e8e5d-120">-DpsObject</span></span>
<span data-ttu-id="e8e5d-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="e8e5d-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="e8e5d-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="e8e5d-122">-Name</span></span>
<span data-ttu-id="e8e5d-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="e8e5d-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="e8e5d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8e5d-124">-ResourceGroupName</span></span>
<span data-ttu-id="e8e5d-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e8e5d-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="e8e5d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8e5d-126">-ResourceId</span></span>
<span data-ttu-id="e8e5d-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e8e5d-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="e8e5d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8e5d-128">CommonParameters</span></span>
<span data-ttu-id="e8e5d-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8e5d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8e5d-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8e5d-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8e5d-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e8e5d-131">INPUTS</span></span>

### <span data-ttu-id="e8e5d-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="e8e5d-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="e8e5d-133">Parametri: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="e8e5d-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="e8e5d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e8e5d-134">System.String</span></span>

## <span data-ttu-id="e8e5d-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e8e5d-135">OUTPUTS</span></span>

### <span data-ttu-id="e8e5d-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSCertificateResponse</span><span class="sxs-lookup"><span data-stu-id="e8e5d-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSCertificateResponse</span></span>

## <span data-ttu-id="e8e5d-137">Note</span><span class="sxs-lookup"><span data-stu-id="e8e5d-137">NOTES</span></span>

## <span data-ttu-id="e8e5d-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e8e5d-138">RELATED LINKS</span></span>
