---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeBandwidthSchedule.md
ms.openlocfilehash: e3453e3359bb800180ebdeb3fa5158b890fd237a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181134"
---
# <span data-ttu-id="fb1fc-101">Get-AzDataBoxEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fb1fc-101">Get-AzDataBoxEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="fb1fc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb1fc-102">SYNOPSIS</span></span>
<span data-ttu-id="fb1fc-103">Ottiene le informazioni sulle pianificazioni della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="fb1fc-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="fb1fc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fb1fc-104">SYNTAX</span></span>

### <span data-ttu-id="fb1fc-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="fb1fc-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb1fc-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb1fc-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fb1fc-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb1fc-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb1fc-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fb1fc-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="fb1fc-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="fb1fc-109">DESCRIPTION</span></span>
<span data-ttu-id="fb1fc-110">Il cmdlet **Get-AzDataBoxEdgeBandwidthSchedule** ottiene le informazioni sulle pianificazioni della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-110">The **Get-AzDataBoxEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="fb1fc-111">È possibile specificare il nome di una pianificazione insieme al nome del gruppo di risorse e del dispositivo per ottenere le informazioni su una specifica pianificazione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="fb1fc-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="fb1fc-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fb1fc-112">EXAMPLES</span></span>

### <span data-ttu-id="fb1fc-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="fb1fc-113">Example 1</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="fb1fc-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="fb1fc-114">Example 2</span></span>
```powershell
PS C:\>Get-AzDataBoxEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="fb1fc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb1fc-115">PARAMETERS</span></span>

### <span data-ttu-id="fb1fc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb1fc-116">-DefaultProfile</span></span>
<span data-ttu-id="fb1fc-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb1fc-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="fb1fc-118">-DeviceName</span></span>
<span data-ttu-id="fb1fc-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="fb1fc-119">Device Name</span></span>

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

### <span data-ttu-id="fb1fc-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="fb1fc-120">-DeviceObject</span></span>
<span data-ttu-id="fb1fc-121">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="fb1fc-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="fb1fc-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fb1fc-122">-Name</span></span>
<span data-ttu-id="fb1fc-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="fb1fc-123">Resource Name</span></span>

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

### <span data-ttu-id="fb1fc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb1fc-124">-ResourceGroupName</span></span>
<span data-ttu-id="fb1fc-125">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="fb1fc-125">Resource Group Name</span></span>

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

### <span data-ttu-id="fb1fc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb1fc-126">-ResourceId</span></span>
<span data-ttu-id="fb1fc-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fb1fc-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="fb1fc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb1fc-128">CommonParameters</span></span>
<span data-ttu-id="fb1fc-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb1fc-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb1fc-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb1fc-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="fb1fc-131">INPUTS</span></span>

### <span data-ttu-id="fb1fc-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="fb1fc-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="fb1fc-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fb1fc-133">OUTPUTS</span></span>

### <span data-ttu-id="fb1fc-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="fb1fc-134">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="fb1fc-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="fb1fc-135">NOTES</span></span>

## <span data-ttu-id="fb1fc-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fb1fc-136">RELATED LINKS</span></span>
