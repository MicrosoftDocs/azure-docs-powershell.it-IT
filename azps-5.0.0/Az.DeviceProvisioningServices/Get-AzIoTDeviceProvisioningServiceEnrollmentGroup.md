---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceenrollmentgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceEnrollmentGroup.md
ms.openlocfilehash: f4cac1380a6ed089d3b3e7b368eb15486e4c12d4
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193473"
---
# <span data-ttu-id="2783e-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="2783e-101">Get-AzIoTDeviceProvisioningServiceEnrollmentGroup</span></span>

## <span data-ttu-id="2783e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2783e-102">SYNOPSIS</span></span>
<span data-ttu-id="2783e-103">Ottenere un gruppo di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2783e-103">Get a device enrollment group.</span></span>

## <span data-ttu-id="2783e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2783e-104">SYNTAX</span></span>

### <span data-ttu-id="2783e-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2783e-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceGroupName] <String> [-DpsName] <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2783e-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2783e-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-DpsObject] <PSProvisioningServiceDescription>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2783e-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="2783e-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceEnrollmentGroup [-ResourceId] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2783e-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2783e-108">DESCRIPTION</span></span>
<span data-ttu-id="2783e-109">Ottenere i dettagli di un gruppo di registrazione o un elenco di tutti i gruppi di registrazione in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="2783e-109">Get the details of an enrollment group or list all enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2783e-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2783e-110">EXAMPLES</span></span>

### <span data-ttu-id="2783e-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2783e-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps" -Name "enroll1"
```

<span data-ttu-id="2783e-112">Ottenere un gruppo di registrazione del dispositivo in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="2783e-112">Get device enrollment group in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="2783e-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="2783e-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceEnrollmentGroup -ResourceGroupName "myresourcegroup" -DpsName "mydps"
```

<span data-ttu-id="2783e-114">Elenca tutti i gruppi di registrazione dei dispositivi in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="2783e-114">List all device enrollment groups in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="2783e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2783e-115">PARAMETERS</span></span>

### <span data-ttu-id="2783e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2783e-116">-DefaultProfile</span></span>
<span data-ttu-id="2783e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2783e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2783e-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="2783e-118">-DpsName</span></span>
<span data-ttu-id="2783e-119">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="2783e-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="2783e-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="2783e-120">-DpsObject</span></span>
<span data-ttu-id="2783e-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="2783e-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="2783e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="2783e-122">-Name</span></span>
<span data-ttu-id="2783e-123">Nome del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="2783e-123">Name of the enrollment group.</span></span>

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

### <span data-ttu-id="2783e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2783e-124">-ResourceGroupName</span></span>
<span data-ttu-id="2783e-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="2783e-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="2783e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2783e-126">-ResourceId</span></span>
<span data-ttu-id="2783e-127">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="2783e-127">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="2783e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2783e-128">CommonParameters</span></span>
<span data-ttu-id="2783e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2783e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2783e-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2783e-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2783e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2783e-131">INPUTS</span></span>

### <span data-ttu-id="2783e-132">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="2783e-132">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="2783e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="2783e-133">System.String</span></span>

## <span data-ttu-id="2783e-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2783e-134">OUTPUTS</span></span>

### <span data-ttu-id="2783e-135">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroup</span><span class="sxs-lookup"><span data-stu-id="2783e-135">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroup</span></span>

### <span data-ttu-id="2783e-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSEnrollmentGroups []</span><span class="sxs-lookup"><span data-stu-id="2783e-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSEnrollmentGroups[]</span></span>

## <span data-ttu-id="2783e-137">Note</span><span class="sxs-lookup"><span data-stu-id="2783e-137">NOTES</span></span>

## <span data-ttu-id="2783e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2783e-138">RELATED LINKS</span></span>