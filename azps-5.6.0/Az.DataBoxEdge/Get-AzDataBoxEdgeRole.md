---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/powershell/module/az.databoxedge/get-azdataboxedgerole
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeRole.md
ms.openlocfilehash: 9dd4925224f2ed91770caff422b8ab6f5d924754
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998632"
---
# <span data-ttu-id="4006f-101">Get-AzDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4006f-101">Get-AzDataBoxEdgeRole</span></span>

## <span data-ttu-id="4006f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4006f-102">SYNOPSIS</span></span>
<span data-ttu-id="4006f-103">Recupera i ruoli disponibili per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="4006f-103">Fetches the available roles for a device.</span></span>

## <span data-ttu-id="4006f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4006f-104">SYNTAX</span></span>

### <span data-ttu-id="4006f-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4006f-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4006f-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="4006f-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeRole -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4006f-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="4006f-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4006f-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="4006f-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeRole [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="4006f-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4006f-109">DESCRIPTION</span></span>
<span data-ttu-id="4006f-110">Il **cmdlet Get-AzDataBoxEdgeRole** recupera i ruoli IoT disponibili per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="4006f-110">The **Get-AzDataBoxEdgeRole** cmdlet fetches the available IoT roles for a Data Box Edge device.</span></span> <span data-ttu-id="4006f-111">È possibile menzionare il parametro Name per ottenere i dettagli di un ruolo IoT specifico.</span><span class="sxs-lookup"><span data-stu-id="4006f-111">You can mention the Name parameter to get the details of a specific IoT role.</span></span>

## <span data-ttu-id="4006f-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4006f-112">EXAMPLES</span></span>

### <span data-ttu-id="4006f-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4006f-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeRole -ResourceGroupName resourceGroupName -DeviceName deviceName

Name    IoTHostHub             Platform Status  IotEdgeDeviceId   IotDeviceId  ResourceGroupName
----    ----------             -------- ------  ---------------   -----------  -----------------
iotrole ehub.azure-devices.net Linux    Enabled iotEdgeDeviceUd   iotDevice    resourceGroupName
```

## <span data-ttu-id="4006f-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4006f-114">PARAMETERS</span></span>

### <span data-ttu-id="4006f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4006f-115">-DefaultProfile</span></span>
<span data-ttu-id="4006f-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4006f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4006f-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="4006f-117">-DeviceName</span></span>
<span data-ttu-id="4006f-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="4006f-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4006f-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="4006f-119">-DeviceObject</span></span>
<span data-ttu-id="4006f-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="4006f-120">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4006f-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4006f-121">-Name</span></span>
<span data-ttu-id="4006f-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="4006f-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4006f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4006f-123">-ResourceGroupName</span></span>
<span data-ttu-id="4006f-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="4006f-124">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet, GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4006f-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4006f-125">-ResourceId</span></span>
<span data-ttu-id="4006f-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="4006f-126">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4006f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4006f-127">CommonParameters</span></span>
<span data-ttu-id="4006f-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4006f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4006f-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4006f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4006f-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="4006f-130">INPUTS</span></span>

### <span data-ttu-id="4006f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="4006f-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="4006f-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4006f-132">OUTPUTS</span></span>

### <span data-ttu-id="4006f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span><span class="sxs-lookup"><span data-stu-id="4006f-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeRole</span></span>

## <span data-ttu-id="4006f-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="4006f-134">NOTES</span></span>

## <span data-ttu-id="4006f-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4006f-135">RELATED LINKS</span></span>
