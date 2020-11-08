---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: 1bc45aa06db70aff6eaec8eb1ff20b12318bb7e2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191513"
---
# <span data-ttu-id="fdf72-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="fdf72-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="fdf72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fdf72-102">SYNOPSIS</span></span>
<span data-ttu-id="fdf72-103">Stampare un elenco delimitato da virgole di dispositivi figlio assegnati.</span><span class="sxs-lookup"><span data-stu-id="fdf72-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="fdf72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fdf72-104">SYNTAX</span></span>

### <span data-ttu-id="fdf72-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fdf72-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf72-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="fdf72-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fdf72-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="fdf72-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdf72-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fdf72-108">DESCRIPTION</span></span>
<span data-ttu-id="fdf72-109">Mostra tutti i dispositivi non Edge assegnati come elenco delimitato da virgole di tutti i dispositivi Edge o Device specificati.</span><span class="sxs-lookup"><span data-stu-id="fdf72-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="fdf72-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fdf72-110">EXAMPLES</span></span>

### <span data-ttu-id="fdf72-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fdf72-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="fdf72-112">Mostra tutti i dispositivi non Edge assegnati come elenco delimitato da virgole.</span><span class="sxs-lookup"><span data-stu-id="fdf72-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="fdf72-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fdf72-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="fdf72-114">Mostra tutti i dispositivi non Edge assegnati come elenco delimitato da virgole di tutti i dispositivi Edge.</span><span class="sxs-lookup"><span data-stu-id="fdf72-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="fdf72-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fdf72-115">PARAMETERS</span></span>

### <span data-ttu-id="fdf72-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdf72-116">-DefaultProfile</span></span>
<span data-ttu-id="fdf72-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fdf72-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdf72-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="fdf72-118">-DeviceId</span></span>
<span data-ttu-id="fdf72-119">ID del dispositivo Edge.</span><span class="sxs-lookup"><span data-stu-id="fdf72-119">Id of edge device.</span></span>

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

### <span data-ttu-id="fdf72-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdf72-120">-InputObject</span></span>
<span data-ttu-id="fdf72-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="fdf72-121">IotHub object</span></span>

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

### <span data-ttu-id="fdf72-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="fdf72-122">-IotHubName</span></span>
<span data-ttu-id="fdf72-123">Nome dell'hub molto</span><span class="sxs-lookup"><span data-stu-id="fdf72-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="fdf72-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdf72-124">-ResourceGroupName</span></span>
<span data-ttu-id="fdf72-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fdf72-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="fdf72-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdf72-126">-ResourceId</span></span>
<span data-ttu-id="fdf72-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="fdf72-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="fdf72-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdf72-128">CommonParameters</span></span>
<span data-ttu-id="fdf72-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fdf72-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdf72-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fdf72-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdf72-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fdf72-131">INPUTS</span></span>

### <span data-ttu-id="fdf72-132">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="fdf72-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="fdf72-133">System. String</span><span class="sxs-lookup"><span data-stu-id="fdf72-133">System.String</span></span>

## <span data-ttu-id="fdf72-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fdf72-134">OUTPUTS</span></span>

### <span data-ttu-id="fdf72-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="fdf72-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="fdf72-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren []</span><span class="sxs-lookup"><span data-stu-id="fdf72-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="fdf72-137">Note</span><span class="sxs-lookup"><span data-stu-id="fdf72-137">NOTES</span></span>

## <span data-ttu-id="fdf72-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fdf72-138">RELATED LINKS</span></span>
