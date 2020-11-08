---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubModule.md
ms.openlocfilehash: ca2381ecff9822bac7a4613566e2da42e79cc5b7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021344"
---
# <span data-ttu-id="38afa-101">Get-AzIotHubModule</span><span class="sxs-lookup"><span data-stu-id="38afa-101">Get-AzIotHubModule</span></span>

## <span data-ttu-id="38afa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="38afa-102">SYNOPSIS</span></span>
<span data-ttu-id="38afa-103">Ottenere i dettagli di un modulo di un dispositivo o di un elenco di moduli in un dispositivo molto in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="38afa-103">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="38afa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38afa-104">SYNTAX</span></span>

### <span data-ttu-id="38afa-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="38afa-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubModule [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId] <String>
 [-ModuleId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38afa-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="38afa-106">InputObjectSet</span></span>
```
Get-AzIotHubModule [-InputObject] <PSIotHub> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38afa-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="38afa-107">ResourceIdSet</span></span>
```
Get-AzIotHubModule [-ResourceId] <String> [-DeviceId] <String> [-ModuleId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38afa-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="38afa-108">DESCRIPTION</span></span>
<span data-ttu-id="38afa-109">Ottenere i dettagli di un modulo di un dispositivo o di un elenco di moduli in un dispositivo molto in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="38afa-109">Get the details of an IoT device module or list modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="38afa-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38afa-110">EXAMPLES</span></span>

### <span data-ttu-id="38afa-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="38afa-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" -ModuleId "myModule1"

ModuleId                   : myModule1
DeviceId                   : myDevice1
GenerationId               : 637148941292917073
ETag                       : "NzIyMDI4MTk3"
LastActivityTime           : 1/1/0001 12:00:00 AM
ConnectionState            : Disconnected
ConnectionStateUpdatedTime : 1/1/0001 12:00:00 AM
CloudToDeviceMessageCount  : 0
Authentication             : Sas
ManagedBy                  :
```

<span data-ttu-id="38afa-112">Ottenere i dettagli di un modulo dispositivo molto in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="38afa-112">Get the details of an IoT device module in an IoT Hub.</span></span>

### <span data-ttu-id="38afa-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="38afa-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubModule -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1" 

Module Id Device Id Connection State Authentication Last Activity Time
--------- --------- ---------------- -------------- ------------------
module1   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
module2   myDevice1 Disconnected     Sas            1/1/0001 12:00:00 AM
```

<span data-ttu-id="38afa-114">Mostra tutti i moduli presenti in un dispositivo molto in un hub molto.</span><span class="sxs-lookup"><span data-stu-id="38afa-114">Show all modules located on an IoT device in an IoT Hub.</span></span>

## <span data-ttu-id="38afa-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="38afa-115">PARAMETERS</span></span>

### <span data-ttu-id="38afa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38afa-116">-DefaultProfile</span></span>
<span data-ttu-id="38afa-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38afa-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38afa-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="38afa-118">-DeviceId</span></span>
<span data-ttu-id="38afa-119">ID dispositivo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38afa-119">Target Device Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="38afa-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="38afa-120">-InputObject</span></span>
<span data-ttu-id="38afa-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="38afa-121">IotHub object</span></span>

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

### <span data-ttu-id="38afa-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="38afa-122">-IotHubName</span></span>
<span data-ttu-id="38afa-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="38afa-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="38afa-124">-ModuleId</span><span class="sxs-lookup"><span data-stu-id="38afa-124">-ModuleId</span></span>
<span data-ttu-id="38afa-125">ID modulo di destinazione.</span><span class="sxs-lookup"><span data-stu-id="38afa-125">Target Module Id.</span></span>

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

### <span data-ttu-id="38afa-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38afa-126">-ResourceGroupName</span></span>
<span data-ttu-id="38afa-127">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="38afa-127">Name of the Resource Group</span></span>

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

### <span data-ttu-id="38afa-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="38afa-128">-ResourceId</span></span>
<span data-ttu-id="38afa-129">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="38afa-129">IotHub Resource Id</span></span>

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

### <span data-ttu-id="38afa-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38afa-130">CommonParameters</span></span>
<span data-ttu-id="38afa-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38afa-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38afa-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38afa-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38afa-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="38afa-133">INPUTS</span></span>

### <span data-ttu-id="38afa-134">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="38afa-134">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="38afa-135">System. String</span><span class="sxs-lookup"><span data-stu-id="38afa-135">System.String</span></span>

## <span data-ttu-id="38afa-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38afa-136">OUTPUTS</span></span>

### <span data-ttu-id="38afa-137">Microsoft. Azure. Commands. Management. IotHub. Models. PSModule</span><span class="sxs-lookup"><span data-stu-id="38afa-137">Microsoft.Azure.Commands.Management.IotHub.Models.PSModule</span></span>

### <span data-ttu-id="38afa-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSModules []</span><span class="sxs-lookup"><span data-stu-id="38afa-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSModules[]</span></span>

## <span data-ttu-id="38afa-139">Note</span><span class="sxs-lookup"><span data-stu-id="38afa-139">NOTES</span></span>

## <span data-ttu-id="38afa-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38afa-140">RELATED LINKS</span></span>
