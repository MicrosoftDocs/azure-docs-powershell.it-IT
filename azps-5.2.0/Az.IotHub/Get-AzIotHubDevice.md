---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: 792992208f4862a0b818aeb890c34cfa361242ca
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330004"
---
# <span data-ttu-id="fad40-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="fad40-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="fad40-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fad40-102">SYNOPSIS</span></span>
<span data-ttu-id="fad40-103">Elenca tutti i dispositivi o un particolare dispositivo contenuto in un hub di Azure.</span><span class="sxs-lookup"><span data-stu-id="fad40-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="fad40-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fad40-104">SYNTAX</span></span>

### <span data-ttu-id="fad40-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fad40-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fad40-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fad40-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fad40-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fad40-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fad40-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fad40-108">DESCRIPTION</span></span>
<span data-ttu-id="fad40-109">Ottenere i dettagli di un dispositivo hub o un elenco di tutti i dispositivi in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="fad40-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="fad40-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fad40-110">EXAMPLES</span></span>

### <span data-ttu-id="fad40-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fad40-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="fad40-112">Mostra tutti i dispositivi in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="fad40-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="fad40-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fad40-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
Status                     : Disabled
StatusReason               : Reason1
StatusUpdatedTime          : 1/17/2020 10:15:04 PM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
EdgeEnabled                : False
DeviceScope                :
```

<span data-ttu-id="fad40-114">Ottenere i dettagli di un dispositivo hub molto.</span><span class="sxs-lookup"><span data-stu-id="fad40-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="fad40-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fad40-115">PARAMETERS</span></span>

### <span data-ttu-id="fad40-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fad40-116">-DefaultProfile</span></span>
<span data-ttu-id="fad40-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fad40-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fad40-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fad40-118">-DeviceId</span></span>
<span data-ttu-id="fad40-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="fad40-119">Target Device Id.</span></span>

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

### <span data-ttu-id="fad40-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fad40-120">-InputObject</span></span>
<span data-ttu-id="fad40-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fad40-121">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fad40-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fad40-122">-IotHubName</span></span>
<span data-ttu-id="fad40-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fad40-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fad40-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fad40-124">-ResourceGroupName</span></span>
<span data-ttu-id="fad40-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fad40-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fad40-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fad40-126">-ResourceId</span></span>
<span data-ttu-id="fad40-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fad40-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fad40-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fad40-128">CommonParameters</span></span>
<span data-ttu-id="fad40-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fad40-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fad40-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fad40-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fad40-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fad40-131">INPUTS</span></span>

### <span data-ttu-id="fad40-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fad40-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fad40-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fad40-133">System.String</span></span>

## <span data-ttu-id="fad40-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fad40-134">OUTPUTS</span></span>

### <span data-ttu-id="fad40-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span><span class="sxs-lookup"><span data-stu-id="fad40-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="fad40-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDrecchi []</span><span class="sxs-lookup"><span data-stu-id="fad40-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="fad40-137">Note</span><span class="sxs-lookup"><span data-stu-id="fad40-137">NOTES</span></span>

## <span data-ttu-id="fad40-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fad40-138">RELATED LINKS</span></span>
