---
external help file: Microsoft.Azure.Commands.DeviceProvisioningServices.dll-Help.xml
Module Name: AzureRM.DeviceProvisioningServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DeviceProvisioningServices/Commands.DeviceProvisioningServices/help/Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: e0685e82a4db2c786d4bb578544f6cbbd5dbadc7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507475"
---
# <span data-ttu-id="1b722-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b722-101">Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="1b722-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b722-102">SYNOPSIS</span></span>
<span data-ttu-id="1b722-103">Elenca tutti o Mostra i dettagli dei criteri di accesso condiviso in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="1b722-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b722-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b722-104">SYNTAX</span></span>

### <span data-ttu-id="1b722-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1b722-105">ResourceSet (Default)</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b722-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1b722-106">InputObjectSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b722-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1b722-107">ResourceIdSet</span></span>
```
Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b722-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b722-108">DESCRIPTION</span></span>
<span data-ttu-id="1b722-109">Per un'introduzione al servizio di provisioning del dispositivo hub Azure molto, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="1b722-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="1b722-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b722-110">EXAMPLES</span></span>

### <span data-ttu-id="1b722-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1b722-111">Example 1</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="1b722-112">Elenca tutti i criteri di accesso condiviso in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="1b722-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="1b722-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1b722-113">Example 2</span></span>
```
PS C:\> Get-AzureRmIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="1b722-114">Mostra i dettagli del criterio di accesso condiviso "criteri" in un servizio di provisioning di un dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="1b722-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="1b722-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b722-115">PARAMETERS</span></span>

### <span data-ttu-id="1b722-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b722-116">-DefaultProfile</span></span>
<span data-ttu-id="1b722-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b722-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b722-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="1b722-118">-DpsObject</span></span>
<span data-ttu-id="1b722-119">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="1b722-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="1b722-120">-Nome di file</span><span class="sxs-lookup"><span data-stu-id="1b722-120">-KeyName</span></span>
<span data-ttu-id="1b722-121">Nome chiave criteri di accesso al servizio di provisioning dei dispositivi</span><span class="sxs-lookup"><span data-stu-id="1b722-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="1b722-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b722-122">-Name</span></span>
<span data-ttu-id="1b722-123">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="1b722-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="1b722-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b722-124">-ResourceGroupName</span></span>
<span data-ttu-id="1b722-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="1b722-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="1b722-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1b722-126">-ResourceId</span></span>
<span data-ttu-id="1b722-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b722-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="1b722-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b722-128">CommonParameters</span></span>
<span data-ttu-id="1b722-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b722-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b722-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b722-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b722-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b722-131">INPUTS</span></span>

### <span data-ttu-id="1b722-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="1b722-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>
<span data-ttu-id="1b722-133">Parametri: DpsObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="1b722-133">Parameters: DpsObject (ByValue)</span></span>

### <span data-ttu-id="1b722-134">System. String</span><span class="sxs-lookup"><span data-stu-id="1b722-134">System.String</span></span>

## <span data-ttu-id="1b722-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b722-135">OUTPUTS</span></span>

### <span data-ttu-id="1b722-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="1b722-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="1b722-137">Note</span><span class="sxs-lookup"><span data-stu-id="1b722-137">NOTES</span></span>

## <span data-ttu-id="1b722-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b722-138">RELATED LINKS</span></span>
