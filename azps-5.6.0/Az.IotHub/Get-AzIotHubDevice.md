---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDevice.md
ms.openlocfilehash: f90aabda20192c046692f357432728dc46581cd0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988103"
---
# <span data-ttu-id="15a9f-101">Get-AzIotHubDevice</span><span class="sxs-lookup"><span data-stu-id="15a9f-101">Get-AzIotHubDevice</span></span>

## <span data-ttu-id="15a9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15a9f-102">SYNOPSIS</span></span>
<span data-ttu-id="15a9f-103">Elenca tutti i dispositivi o un dispositivo specifico contenuto in un hub IoT di Azure.</span><span class="sxs-lookup"><span data-stu-id="15a9f-103">Lists all devices or a particular device contained within an Azure IoT Hub.</span></span> 

## <span data-ttu-id="15a9f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="15a9f-104">SYNTAX</span></span>

### <span data-ttu-id="15a9f-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="15a9f-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDevice [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15a9f-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="15a9f-106">InputObjectSet</span></span>
```
Get-AzIotHubDevice [-InputObject] <PSIotHub> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="15a9f-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="15a9f-107">ResourceIdSet</span></span>
```
Get-AzIotHubDevice [-ResourceId] <String> [-DeviceId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="15a9f-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="15a9f-108">DESCRIPTION</span></span>
<span data-ttu-id="15a9f-109">Ottenere i dettagli di un dispositivo hub Iot o elencare tutti i dispositivi in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="15a9f-109">Get the details of an Iot Hub device or list all devices in an Iot Hub.</span></span>

## <span data-ttu-id="15a9f-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="15a9f-110">EXAMPLES</span></span>

### <span data-ttu-id="15a9f-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="15a9f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDevice -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

Device Id Status   Connection State Authentication       Edge Enabled Last Activity Time
--------- ------   ---------------- --------------       ------------ ------------------
device1   Enabled  Disconnected     CertificateAuthority True         1/1/0001 12:00:00 AM
device2   Disabled Disconnected     Sas                  False        1/1/0001 12:00:00 AM
device3   Enabled  Disconnected     SelfSigned           False        1/1/0001 12:00:00 AM
```

<span data-ttu-id="15a9f-112">Visualizzare tutti i dispositivi in un hub Iot.</span><span class="sxs-lookup"><span data-stu-id="15a9f-112">Show all devices in an Iot Hub.</span></span>

### <span data-ttu-id="15a9f-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="15a9f-113">Example 2</span></span>
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

<span data-ttu-id="15a9f-114">Ottenere i dettagli di un dispositivo Hub IoT.</span><span class="sxs-lookup"><span data-stu-id="15a9f-114">Get the details of an IoT Hub device.</span></span>

## <span data-ttu-id="15a9f-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15a9f-115">PARAMETERS</span></span>

### <span data-ttu-id="15a9f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15a9f-116">-DefaultProfile</span></span>
<span data-ttu-id="15a9f-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="15a9f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="15a9f-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="15a9f-118">-DeviceId</span></span>
<span data-ttu-id="15a9f-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="15a9f-119">Target Device Id.</span></span>

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

### <span data-ttu-id="15a9f-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="15a9f-120">-InputObject</span></span>
<span data-ttu-id="15a9f-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="15a9f-121">IotHub object</span></span>

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

### <span data-ttu-id="15a9f-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="15a9f-122">-IotHubName</span></span>
<span data-ttu-id="15a9f-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="15a9f-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="15a9f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15a9f-124">-ResourceGroupName</span></span>
<span data-ttu-id="15a9f-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="15a9f-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="15a9f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="15a9f-126">-ResourceId</span></span>
<span data-ttu-id="15a9f-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="15a9f-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="15a9f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15a9f-128">CommonParameters</span></span>
<span data-ttu-id="15a9f-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15a9f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15a9f-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15a9f-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15a9f-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="15a9f-131">INPUTS</span></span>

### <span data-ttu-id="15a9f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="15a9f-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="15a9f-133">System.String</span><span class="sxs-lookup"><span data-stu-id="15a9f-133">System.String</span></span>

## <span data-ttu-id="15a9f-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="15a9f-134">OUTPUTS</span></span>

### <span data-ttu-id="15a9f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevaso</span><span class="sxs-lookup"><span data-stu-id="15a9f-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice</span></span>

### <span data-ttu-id="15a9f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevase[]</span><span class="sxs-lookup"><span data-stu-id="15a9f-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevices[]</span></span>

## <span data-ttu-id="15a9f-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="15a9f-137">NOTES</span></span>

## <span data-ttu-id="15a9f-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="15a9f-138">RELATED LINKS</span></span>
