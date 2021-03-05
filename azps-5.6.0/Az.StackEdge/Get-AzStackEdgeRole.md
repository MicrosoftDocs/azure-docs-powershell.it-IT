---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeRole.md
ms.openlocfilehash: c4d33dad9377c6ee53452c90b5d582413e2eee73
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962621"
---
# <span data-ttu-id="08445-101">Get-AzStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="08445-101">Get-AzStackEdgeRole</span></span>

## <span data-ttu-id="08445-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08445-102">SYNOPSIS</span></span>
<span data-ttu-id="08445-103">Recupera i ruoli disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="08445-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="08445-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08445-104">SYNTAX</span></span>

### <span data-ttu-id="08445-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08445-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08445-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="08445-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08445-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="08445-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="08445-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08445-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="08445-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08445-109">DESCRIPTION</span></span>
<span data-ttu-id="08445-110">Il **cmdlet Get-AzStackEdgeRole** recupera i ruoli IoT disponibili per un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="08445-110">The **Get-AzStackEdgeRole** cmdlet fetches the available IoT roles for a Stack Edge device.</span></span> <span data-ttu-id="08445-111">È possibile menzionare il parametro Name per ottenere i dettagli di un ruolo IoT specifico.</span><span class="sxs-lookup"><span data-stu-id="08445-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="08445-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08445-112">EXAMPLES</span></span>

### <span data-ttu-id="08445-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="08445-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="08445-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08445-114">PARAMETERS</span></span>

### <span data-ttu-id="08445-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08445-115">-DefaultProfile</span></span>
<span data-ttu-id="08445-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08445-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08445-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="08445-117">-DeviceName</span></span>
<span data-ttu-id="08445-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="08445-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08445-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="08445-119">-DeviceObject</span></span>
<span data-ttu-id="08445-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="08445-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08445-121">-Name</span><span class="sxs-lookup"><span data-stu-id="08445-121">-Name</span></span>
<span data-ttu-id="08445-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="08445-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: RoleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: RoleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08445-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08445-123">-ResourceGroupName</span></span>
<span data-ttu-id="08445-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="08445-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08445-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="08445-125">-ResourceId</span></span>
<span data-ttu-id="08445-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="08445-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08445-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08445-127">CommonParameters</span></span>
<span data-ttu-id="08445-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08445-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08445-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08445-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08445-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="08445-130">INPUTS</span></span>

### <span data-ttu-id="08445-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="08445-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="08445-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08445-132">OUTPUTS</span></span>

### <span data-ttu-id="08445-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span><span class="sxs-lookup"><span data-stu-id="08445-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeRole</span></span>

## <span data-ttu-id="08445-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="08445-134">NOTES</span></span>

## <span data-ttu-id="08445-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08445-135">RELATED LINKS</span></span>
