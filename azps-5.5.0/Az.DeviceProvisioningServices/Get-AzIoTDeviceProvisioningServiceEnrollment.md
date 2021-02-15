---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204179"
---
# <span data-ttu-id="72c88-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="72c88-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="72c88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="72c88-102">SYNOPSIS</span></span>
<span data-ttu-id="72c88-103">Ottenere un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72c88-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="72c88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72c88-104">SYNTAX</span></span>

### <span data-ttu-id="72c88-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72c88-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72c88-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="72c88-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72c88-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="72c88-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72c88-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="72c88-108">DESCRIPTION</span></span>
<span data-ttu-id="72c88-109">Ottenere i dettagli di registrazione del dispositivo o elencare le registrazioni dei dispositivi in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="72c88-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="72c88-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72c88-110">EXAMPLES</span></span>

### <span data-ttu-id="72c88-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72c88-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="72c88-112">Ottenere i dettagli di registrazione del dispositivo in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="72c88-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="72c88-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="72c88-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="72c88-114">Elencare le registrazioni dei dispositivi in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="72c88-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="72c88-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="72c88-115">PARAMETERS</span></span>

### <span data-ttu-id="72c88-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72c88-116">-DefaultProfile</span></span>
<span data-ttu-id="72c88-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72c88-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72c88-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="72c88-118">-DpsName</span></span>
<span data-ttu-id="72c88-119">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="72c88-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="72c88-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="72c88-120">-DpsObject</span></span>
<span data-ttu-id="72c88-121">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="72c88-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="72c88-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="72c88-122">-RegistrationId</span></span>
<span data-ttu-id="72c88-123">ID registrazione individuale.</span><span class="sxs-lookup"><span data-stu-id="72c88-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="72c88-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72c88-124">-ResourceGroupName</span></span>
<span data-ttu-id="72c88-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="72c88-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="72c88-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72c88-126">-ResourceId</span></span>
<span data-ttu-id="72c88-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="72c88-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="72c88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72c88-128">CommonParameters</span></span>
<span data-ttu-id="72c88-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72c88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72c88-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="72c88-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72c88-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="72c88-131">INPUTS</span></span>

### <span data-ttu-id="72c88-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="72c88-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="72c88-133">System.String</span><span class="sxs-lookup"><span data-stu-id="72c88-133">System.String</span></span>

## <span data-ttu-id="72c88-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72c88-134">OUTPUTS</span></span>

### <span data-ttu-id="72c88-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="72c88-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="72c88-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span><span class="sxs-lookup"><span data-stu-id="72c88-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="72c88-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="72c88-137">NOTES</span></span>

## <span data-ttu-id="72c88-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72c88-138">RELATED LINKS</span></span>
