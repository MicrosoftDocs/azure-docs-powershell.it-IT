---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollment.md
ms.openlocfilehash: dfca2885c644f35ba26a0cf9e15bff16c6156528
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94031757"
---
# <span data-ttu-id="58ed8-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span><span class="sxs-lookup"><span data-stu-id="58ed8-101">Get-AzIoTDeviceProvisioningServiceEnrollment</span></span>

## <span data-ttu-id="58ed8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="58ed8-102">SYNOPSIS</span></span>
<span data-ttu-id="58ed8-103">Ottenere un record di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="58ed8-103">Get a device enrollment record.</span></span>

## <span data-ttu-id="58ed8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="58ed8-104">SYNTAX</span></span>

### <span data-ttu-id="58ed8-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="58ed8-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58ed8-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="58ed8-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="58ed8-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="58ed8-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollment [-ResourceId] <String> [-RegistrationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="58ed8-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="58ed8-108">DESCRIPTION</span></span>
<span data-ttu-id="58ed8-109">Ottenere i dettagli di registrazione del dispositivo o le iscrizioni del dispositivo di elenco in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="58ed8-109">Get device enrollment details or List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="58ed8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="58ed8-110">EXAMPLES</span></span>

### <span data-ttu-id="58ed8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="58ed8-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="58ed8-112">Ottenere i dettagli di registrazione del dispositivo in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="58ed8-112">Get device enrollment details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="58ed8-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="58ed8-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollment -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="58ed8-114">Elencare le iscrizioni del dispositivo in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="58ed8-114">List device enrollments in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="58ed8-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="58ed8-115">PARAMETERS</span></span>

### <span data-ttu-id="58ed8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58ed8-116">-DefaultProfile</span></span>
<span data-ttu-id="58ed8-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="58ed8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58ed8-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="58ed8-118">-DpsName</span></span>
<span data-ttu-id="58ed8-119">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="58ed8-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="58ed8-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="58ed8-120">-DpsObject</span></span>
<span data-ttu-id="58ed8-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="58ed8-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="58ed8-122">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="58ed8-122">-RegistrationId</span></span>
<span data-ttu-id="58ed8-123">ID di registrazione dell'iscrizione individuale.</span><span class="sxs-lookup"><span data-stu-id="58ed8-123">Individual enrollment registration id.</span></span>

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

### <span data-ttu-id="58ed8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58ed8-124">-ResourceGroupName</span></span>
<span data-ttu-id="58ed8-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="58ed8-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="58ed8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58ed8-126">-ResourceId</span></span>
<span data-ttu-id="58ed8-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="58ed8-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="58ed8-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58ed8-128">CommonParameters</span></span>
<span data-ttu-id="58ed8-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58ed8-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58ed8-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="58ed8-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58ed8-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="58ed8-131">INPUTS</span></span>

### <span data-ttu-id="58ed8-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="58ed8-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="58ed8-133">System. String</span><span class="sxs-lookup"><span data-stu-id="58ed8-133">System.String</span></span>

## <span data-ttu-id="58ed8-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="58ed8-134">OUTPUTS</span></span>

### <span data-ttu-id="58ed8-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollment</span><span class="sxs-lookup"><span data-stu-id="58ed8-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollment</span></span>

### <span data-ttu-id="58ed8-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSIndividualEnrollments []</span><span class="sxs-lookup"><span data-stu-id="58ed8-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSIndividualEnrollments[]</span></span>

## <span data-ttu-id="58ed8-137">Note</span><span class="sxs-lookup"><span data-stu-id="58ed8-137">NOTES</span></span>

## <span data-ttu-id="58ed8-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="58ed8-138">RELATED LINKS</span></span>
