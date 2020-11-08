---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193472"
---
# <span data-ttu-id="aa56b-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="aa56b-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="aa56b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa56b-102">SYNOPSIS</span></span>
<span data-ttu-id="aa56b-103">Ottiene lo stato di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa56b-103">Gets the device registration state.</span></span>

## <span data-ttu-id="aa56b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa56b-104">SYNTAX</span></span>

### <span data-ttu-id="aa56b-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa56b-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa56b-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="aa56b-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="aa56b-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="aa56b-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aa56b-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa56b-108">DESCRIPTION</span></span>
<span data-ttu-id="aa56b-109">Ottenere lo stato di registrazione del dispositivo o lo stato di registrazione dei dispositivi in enrollmentGroup in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="aa56b-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="aa56b-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa56b-110">EXAMPLES</span></span>

### <span data-ttu-id="aa56b-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="aa56b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="aa56b-112">Ottenere i dettagli dello stato di registrazione del dispositivo in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="aa56b-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="aa56b-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="aa56b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="aa56b-114">Elencare tutti lo stato di registrazione dei dispositivi in questo enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="aa56b-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="aa56b-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa56b-115">PARAMETERS</span></span>

### <span data-ttu-id="aa56b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa56b-116">-DefaultProfile</span></span>
<span data-ttu-id="aa56b-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa56b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa56b-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="aa56b-118">-DpsName</span></span>
<span data-ttu-id="aa56b-119">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="aa56b-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="aa56b-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="aa56b-120">-DpsObject</span></span>
<span data-ttu-id="aa56b-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="aa56b-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="aa56b-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="aa56b-122">-EnrollmentId</span></span>
<span data-ttu-id="aa56b-123">ID del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="aa56b-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="aa56b-124">-Query</span><span class="sxs-lookup"><span data-stu-id="aa56b-124">-Query</span></span>
<span data-ttu-id="aa56b-125">Query SQL.</span><span class="sxs-lookup"><span data-stu-id="aa56b-125">Sql query.</span></span>

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

### <span data-ttu-id="aa56b-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="aa56b-126">-RegistrationId</span></span>
<span data-ttu-id="aa56b-127">ID della registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="aa56b-127">ID of device registration.</span></span>

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

### <span data-ttu-id="aa56b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa56b-128">-ResourceGroupName</span></span>
<span data-ttu-id="aa56b-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="aa56b-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="aa56b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="aa56b-130">-ResourceId</span></span>
<span data-ttu-id="aa56b-131">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="aa56b-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="aa56b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa56b-132">CommonParameters</span></span>
<span data-ttu-id="aa56b-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa56b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa56b-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa56b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa56b-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa56b-135">INPUTS</span></span>

### <span data-ttu-id="aa56b-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="aa56b-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="aa56b-137">System. String</span><span class="sxs-lookup"><span data-stu-id="aa56b-137">System.String</span></span>

## <span data-ttu-id="aa56b-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa56b-138">OUTPUTS</span></span>

### <span data-ttu-id="aa56b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="aa56b-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="aa56b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="aa56b-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="aa56b-141">Note</span><span class="sxs-lookup"><span data-stu-id="aa56b-141">NOTES</span></span>

## <span data-ttu-id="aa56b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa56b-142">RELATED LINKS</span></span>
