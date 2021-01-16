---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeviceProvisioningServices.dll-Help.xml
Module Name: Az.DeviceProvisioningServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.deviceprovisioningservices/get-aziotdeviceprovisioningserviceregistration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeviceProvisioningServices/DeviceProvisioningServices/help/Get-AzIoTDeviceProvisioningServiceRegistration.md
ms.openlocfilehash: 4951c75af3935d982d044ab02648915f980ff16e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98328745"
---
# <span data-ttu-id="a2490-101">Get-AzIoTDeviceProvisioningServiceRegistration</span><span class="sxs-lookup"><span data-stu-id="a2490-101">Get-AzIoTDeviceProvisioningServiceRegistration</span></span>

## <span data-ttu-id="a2490-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a2490-102">SYNOPSIS</span></span>
<span data-ttu-id="a2490-103">Ottiene lo stato di registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2490-103">Gets the device registration state.</span></span>

## <span data-ttu-id="a2490-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a2490-104">SYNTAX</span></span>

### <span data-ttu-id="a2490-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a2490-105">ResourceSet (Default)</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceGroupName] <String> [-DpsName] <String>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2490-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="a2490-106">InputObjectSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-DpsObject] <PSProvisioningServiceDescription>
 [-RegistrationId <String>] [-EnrollmentId <String>] [-Query <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2490-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="a2490-107">ResourceIdSet</span></span>
```
Get-AzIoTDeviceProvisioningServiceRegistration [-ResourceId] <String> [-RegistrationId <String>]
 [-EnrollmentId <String>] [-Query <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2490-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a2490-108">DESCRIPTION</span></span>
<span data-ttu-id="a2490-109">Ottenere lo stato di registrazione del dispositivo o lo stato di registrazione dei dispositivi in enrollmentGroup in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="a2490-109">Get the device registration state or the registration state of devices under the enrollmentGroup in an Azure IoT Hub Device Provisioning Service.</span></span>

## <span data-ttu-id="a2490-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a2490-110">EXAMPLES</span></span>

### <span data-ttu-id="a2490-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a2490-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -RegistrationId "enroll1"
```

<span data-ttu-id="a2490-112">Ottenere i dettagli dello stato di registrazione del dispositivo in un servizio di provisioning del dispositivo hub Azure molto.</span><span class="sxs-lookup"><span data-stu-id="a2490-112">Get the device registration state details in an Azure IoT Hub Device Provisioning Service.</span></span>

### <span data-ttu-id="a2490-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a2490-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIoTDeviceProvisioningServiceRegistration -ResourceGroupName "myresourcegroup" -DpsName "mydps" -EnrollmentId "grp-enroll1"
```

<span data-ttu-id="a2490-114">Elencare tutti lo stato di registrazione dei dispositivi in questo enrollmentGroup.</span><span class="sxs-lookup"><span data-stu-id="a2490-114">List all the registration state of devices in this enrollmentGroup.</span></span>

## <span data-ttu-id="a2490-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a2490-115">PARAMETERS</span></span>

### <span data-ttu-id="a2490-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2490-116">-DefaultProfile</span></span>
<span data-ttu-id="a2490-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a2490-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a2490-118">-DpsName</span><span class="sxs-lookup"><span data-stu-id="a2490-118">-DpsName</span></span>
<span data-ttu-id="a2490-119">Nome del servizio di provisioning dei dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="a2490-119">Name of the IoT Device Provisioning Service</span></span>

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

### <span data-ttu-id="a2490-120">-DpsObject</span><span class="sxs-lookup"><span data-stu-id="a2490-120">-DpsObject</span></span>
<span data-ttu-id="a2490-121">Oggetto servizio di provisioning per dispositivi molto</span><span class="sxs-lookup"><span data-stu-id="a2490-121">IoT Device Provisioning Service Object</span></span>

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

### <span data-ttu-id="a2490-122">-EnrollmentId</span><span class="sxs-lookup"><span data-stu-id="a2490-122">-EnrollmentId</span></span>
<span data-ttu-id="a2490-123">ID del gruppo di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a2490-123">ID of enrollment group.</span></span>

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

### <span data-ttu-id="a2490-124">-Query</span><span class="sxs-lookup"><span data-stu-id="a2490-124">-Query</span></span>
<span data-ttu-id="a2490-125">Query SQL.</span><span class="sxs-lookup"><span data-stu-id="a2490-125">Sql query.</span></span>

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

### <span data-ttu-id="a2490-126">-RegistrationId</span><span class="sxs-lookup"><span data-stu-id="a2490-126">-RegistrationId</span></span>
<span data-ttu-id="a2490-127">ID della registrazione del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a2490-127">ID of device registration.</span></span>

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

### <span data-ttu-id="a2490-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2490-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2490-129">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="a2490-129">Name of the Resource Group</span></span>

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

### <span data-ttu-id="a2490-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a2490-130">-ResourceId</span></span>
<span data-ttu-id="a2490-131">ID risorsa del servizio di provisioning del dispositivo</span><span class="sxs-lookup"><span data-stu-id="a2490-131">IoT Device Provisioning Service Resource Id</span></span>

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

### <span data-ttu-id="a2490-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2490-132">CommonParameters</span></span>
<span data-ttu-id="a2490-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2490-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2490-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2490-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2490-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a2490-135">INPUTS</span></span>

### <span data-ttu-id="a2490-136">Microsoft. Azure. Commands. Management. DeviceProvisioningServices. Models. PSProvisioningServiceDescription</span><span class="sxs-lookup"><span data-stu-id="a2490-136">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSProvisioningServiceDescription</span></span>

### <span data-ttu-id="a2490-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a2490-137">System.String</span></span>

## <span data-ttu-id="a2490-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a2490-138">OUTPUTS</span></span>

### <span data-ttu-id="a2490-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span><span class="sxs-lookup"><span data-stu-id="a2490-139">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationState</span></span>

### <span data-ttu-id="a2490-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates []</span><span class="sxs-lookup"><span data-stu-id="a2490-140">Microsoft.Azure.Commands.Management.DeviceProvisioningServices.Models.PSDeviceRegistrationStates[]</span></span>

## <span data-ttu-id="a2490-141">Note</span><span class="sxs-lookup"><span data-stu-id="a2490-141">NOTES</span></span>

## <span data-ttu-id="a2490-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a2490-142">RELATED LINKS</span></span>
