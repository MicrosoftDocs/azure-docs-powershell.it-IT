---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceAccessPolicy.md
ms.openlocfilehash: 87c6bdd72229baec8e65c40d4e2e4309bde59aba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200423"
---
# <span data-ttu-id="0b820-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="0b820-101">Get-AzIoTDeviceProvisioningServiceAccessPolicy</span></span>

## <span data-ttu-id="0b820-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b820-102">SYNOPSIS</span></span>
<span data-ttu-id="0b820-103">Elencare tutti i criteri di accesso condiviso o mostrarne i dettagli in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b820-103">List all or show details of shared access policies in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0b820-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0b820-104">SYNTAX</span></span>

### <span data-ttu-id="0b820-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0b820-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceGroupName] <String> [-Name] <String>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b820-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="0b820-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-DpsObject] <PSProvisioningServiceDescription>
 [-KeyName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0b820-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="0b820-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceAccessPolicy [-ResourceId] <String> [-KeyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0b820-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0b820-108">DESCRIPTION</span></span>
<span data-ttu-id="0b820-109">Per un'introduzione al servizio di provisioning dei dispositivi Hub IoT di Azure, vedere https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps .</span><span class="sxs-lookup"><span data-stu-id="0b820-109">For an introduction to Azure IoT Hub Device Provisioning Service, see https://docs.microsoft.com/en-us/azure/iot-dps/about-iot-dps.</span></span>

## <span data-ttu-id="0b820-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0b820-110">EXAMPLES</span></span>

### <span data-ttu-id="0b820-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0b820-111">Example 1</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps"

KeyName     Rights      
-------     ------  
mypolicy1   ServiceConfig, DeviceConnect, EnrollmentWrite
mypolicy2   EnrollmentWrite
```

<span data-ttu-id="0b820-112">Elencare tutti i criteri di accesso condiviso in "myiotdps".</span><span class="sxs-lookup"><span data-stu-id="0b820-112">List all shared access policies in "myiotdps".</span></span>

### <span data-ttu-id="0b820-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0b820-113">Example 2</span></span>
```
PS C:\> Get-AzIoTDeviceProvisioningServiceAccessPolicy -ResourceGroupName "myresourcegroup" -Name "myiotdps" -KeyName "mypolicy"

ResourceGroupName   : myresourcegroup
Name                : myiotdps
KeyName             : mypolicy
PrimaryKey          : hyZJm8W7rra9O7eKhkLu9m/CIPPt9x1NXVMbMJa1rvg=
SecondaryKey        : vbIwGCBQCIbS5BKFKdddM6uZHLhNTuz9r8CZYgmTmpY=
Rights              : ServiceConfig, DeviceConnect, EnrollmentWrite
```

<span data-ttu-id="0b820-114">Mostra i dettagli del criterio di accesso condiviso "mypolicy" in un servizio di provisioning dei dispositivi Hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="0b820-114">Show details of shared access policy "mypolicy" in an Azure IoT Hub device provisioning service.</span></span>

## <span data-ttu-id="0b820-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0b820-115">PARAMETERS</span></span>

### <span data-ttu-id="0b820-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b820-116">-DefaultProfile</span></span>
<span data-ttu-id="0b820-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0b820-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b820-118">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="0b820-118">-DpsObject</span></span>
<span data-ttu-id="0b820-119">Oggetto del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0b820-119">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="0b820-120">-KeyName</span><span class="sxs-lookup"><span data-stu-id="0b820-120">-KeyName</span></span>
<span data-ttu-id="0b820-121">Nome della chiave della chiave del criterio di accesso del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0b820-121">IoT Device Provisioning Service access policy key name</span></span>

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

### <span data-ttu-id="0b820-122">-Name</span><span class="sxs-lookup"><span data-stu-id="0b820-122">-Name</span></span>
<span data-ttu-id="0b820-123">Nome del servizio di provisioning dei dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0b820-123">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="0b820-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b820-124">-ResourceGroupName</span></span>
<span data-ttu-id="0b820-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="0b820-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="0b820-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b820-126">-ResourceId</span></span>
<span data-ttu-id="0b820-127">ID risorsa del servizio di provisioning dispositivi IoT</span><span class="sxs-lookup"><span data-stu-id="0b820-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="0b820-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b820-128">CommonParameters</span></span>
<span data-ttu-id="0b820-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b820-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b820-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b820-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b820-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="0b820-131">INPUTS</span></span>

### <span data-ttu-id="0b820-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="0b820-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="0b820-133">System.String</span><span class="sxs-lookup"><span data-stu-id="0b820-133">System.String</span></span>

## <span data-ttu-id="0b820-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0b820-134">OUTPUTS</span></span>

### <span data-ttu-id="0b820-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span><span class="sxs-lookup"><span data-stu-id="0b820-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSSharedAccessSignatureAuthorizationRuleAccessRightsDescription</span></span>

## <span data-ttu-id="0b820-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="0b820-136">NOTES</span></span>

## <span data-ttu-id="0b820-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0b820-137">RELATED LINKS</span></span>
