---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186015"
---
# <span data-ttu-id="4b4a6-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="4b4a6-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="4b4a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4a6-103">Ottenere un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="4b4a6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b4a6-104">SYNTAX</span></span>

### <span data-ttu-id="4b4a6-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4b4a6-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4a6-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4b4a6-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4b4a6-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4b4a6-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4a6-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4b4a6-108">DESCRIPTION</span></span>
<span data-ttu-id="4b4a6-109">Ottenere i dettagli di un gruppo di registrazione o elencare tutti i gruppi di registrazione in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4b4a6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b4a6-110">EXAMPLES</span></span>

### <span data-ttu-id="4b4a6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b4a6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="4b4a6-112">Ottenere un gruppo di registrazione del dispositivo in un servizio di provisioning dei dispositivi hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="4b4a6-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4b4a6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="4b4a6-114">Elencare tutti i gruppi di registrazione dei dispositivi in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="4b4a6-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b4a6-115">PARAMETERS</span></span>

### <span data-ttu-id="4b4a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4a6-116">-DefaultProfile</span></span>
<span data-ttu-id="4b4a6-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b4a6-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="4b4a6-118">-DpsName</span></span>
<span data-ttu-id="4b4a6-119">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="4b4a6-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="4b4a6-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="4b4a6-120">-DpsObject</span></span>
<span data-ttu-id="4b4a6-121">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="4b4a6-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="4b4a6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="4b4a6-122">-Name</span></span>
<span data-ttu-id="4b4a6-123">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="4b4a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4b4a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="4b4a6-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4b4a6-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="4b4a6-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4b4a6-126">-ResourceId</span></span>
<span data-ttu-id="4b4a6-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="4b4a6-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="4b4a6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4a6-128">CommonParameters</span></span>
<span data-ttu-id="4b4a6-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4a6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4a6-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b4a6-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4a6-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="4b4a6-131">INPUTS</span></span>

### <span data-ttu-id="4b4a6-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="4b4a6-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="4b4a6-133">System.String</span><span class="sxs-lookup"><span data-stu-id="4b4a6-133">System.String</span></span>

## <span data-ttu-id="4b4a6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b4a6-134">OUTPUTS</span></span>

### <span data-ttu-id="4b4a6-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="4b4a6-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="4b4a6-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span><span class="sxs-lookup"><span data-stu-id="4b4a6-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="4b4a6-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="4b4a6-137">NOTES</span></span>

## <span data-ttu-id="4b4a6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b4a6-138">RELATED LINKS</span></span>
