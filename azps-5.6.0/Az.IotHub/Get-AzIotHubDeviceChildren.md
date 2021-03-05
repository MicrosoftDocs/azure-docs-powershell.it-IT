---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/get-aziothubdevicechildren
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Get-AzIotHubDeviceChildren.md
ms.openlocfilehash: ec84ee72caadc4d49c29a72e1e5171e589dc11d3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988076"
---
# <span data-ttu-id="f0374-101">Get-AzIotHubDeviceChildren</span><span class="sxs-lookup"><span data-stu-id="f0374-101">Get-AzIotHubDeviceChildren</span></span>

## <span data-ttu-id="f0374-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0374-102">SYNOPSIS</span></span>
<span data-ttu-id="f0374-103">Stampa l'elenco dei dispositivi figlio assegnati con valori delimitati da virgole.</span><span class="sxs-lookup"><span data-stu-id="f0374-103">Print comma-separated list of assigned child devices.</span></span>

## <span data-ttu-id="f0374-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f0374-104">SYNTAX</span></span>

### <span data-ttu-id="f0374-105">ResourceSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f0374-105">ResourceSet (Default)</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceGroupName] <String> [-IotHubName] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0374-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f0374-106">InputObjectSet</span></span>
```
Get-AzIotHubDeviceChildren [-InputObject] <PSIotHub> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f0374-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f0374-107">ResourceIdSet</span></span>
```
Get-AzIotHubDeviceChildren [-ResourceId] <String> [-DeviceId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0374-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f0374-108">DESCRIPTION</span></span>
<span data-ttu-id="f0374-109">Mostra tutti i dispositivi non perimetrali assegnati come elenco separato da virgole di tutti i dispositivi perimetrali o di un dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="f0374-109">Show all assigned non-edge devices as comma-separated list of all edge devices or specified device.</span></span>

## <span data-ttu-id="f0374-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f0374-110">EXAMPLES</span></span>

### <span data-ttu-id="f0374-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f0374-111">Example 1</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -DeviceId "myDevice1"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
```

<span data-ttu-id="f0374-112">Mostra tutti i dispositivi non perimetrali assegnati come elenco separato da virgole.</span><span class="sxs-lookup"><span data-stu-id="f0374-112">Show all assigned non-edge devices as comma-separated list.</span></span>

### <span data-ttu-id="f0374-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="f0374-113">Example 2</span></span>
```powershell
PS C:\> Get-AzIotHubDeviceChildren -ResourceGroupName "myresourcegroup" -IotHubName "myiothub"

DeviceId  ChildrenDeviceId
--------  ----------------
myDevice1 {device1, device2}
myDevice2 {device3, device4, device5}
```

<span data-ttu-id="f0374-114">Mostra tutti i dispositivi non perimetrali assegnati come elenco separato da virgole di tutti i dispositivi perimetrali.</span><span class="sxs-lookup"><span data-stu-id="f0374-114">Show all assigned non-edge devices as comma-separated list of all edge devices.</span></span>

## <span data-ttu-id="f0374-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0374-115">PARAMETERS</span></span>

### <span data-ttu-id="f0374-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0374-116">-DefaultProfile</span></span>
<span data-ttu-id="f0374-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f0374-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0374-118">-DeviceId</span><span class="sxs-lookup"><span data-stu-id="f0374-118">-DeviceId</span></span>
<span data-ttu-id="f0374-119">ID del dispositivo perimetrale.</span><span class="sxs-lookup"><span data-stu-id="f0374-119">Id of edge device.</span></span>

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

### <span data-ttu-id="f0374-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f0374-120">-InputObject</span></span>
<span data-ttu-id="f0374-121">Oggetto IotHub</span><span class="sxs-lookup"><span data-stu-id="f0374-121">IotHub object</span></span>

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

### <span data-ttu-id="f0374-122">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="f0374-122">-IotHubName</span></span>
<span data-ttu-id="f0374-123">Nome dell'hub Iot</span><span class="sxs-lookup"><span data-stu-id="f0374-123">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="f0374-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0374-124">-ResourceGroupName</span></span>
<span data-ttu-id="f0374-125">Nome del gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f0374-125">Name of the Resource Group</span></span>

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

### <span data-ttu-id="f0374-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f0374-126">-ResourceId</span></span>
<span data-ttu-id="f0374-127">ID risorsa IotHub</span><span class="sxs-lookup"><span data-stu-id="f0374-127">IotHub Resource Id</span></span>

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

### <span data-ttu-id="f0374-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0374-128">CommonParameters</span></span>
<span data-ttu-id="f0374-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0374-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0374-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0374-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0374-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="f0374-131">INPUTS</span></span>

### <span data-ttu-id="f0374-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="f0374-132">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="f0374-133">System.String</span><span class="sxs-lookup"><span data-stu-id="f0374-133">System.String</span></span>

## <span data-ttu-id="f0374-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f0374-134">OUTPUTS</span></span>

### <span data-ttu-id="f0374-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevice Avi</span><span class="sxs-lookup"><span data-stu-id="f0374-135">Microsoft.Azure.Commands.Management.IotHub.Models.PSDeviceChildren</span></span>

### <span data-ttu-id="f0374-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesSEr[]</span><span class="sxs-lookup"><span data-stu-id="f0374-136">Microsoft.Azure.Commands.Management.IotHub.Models.PSDevicesChildren[]</span></span>

## <span data-ttu-id="f0374-137">NOTE</span><span class="sxs-lookup"><span data-stu-id="f0374-137">NOTES</span></span>

## <span data-ttu-id="f0374-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f0374-138">RELATED LINKS</span></span>
