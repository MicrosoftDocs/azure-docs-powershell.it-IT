---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgebandwidthschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeBandwidthSchedule.md
ms.openlocfilehash: 5f2dfec045364852d9846fa3bb35bd903c78ca5a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032069"
---
# <span data-ttu-id="9a372-101">Get-AzStackEdgeBandwidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9a372-101">Get-AzStackEdgeBandwidthSchedule</span></span>

## <span data-ttu-id="9a372-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a372-102">SYNOPSIS</span></span>
<span data-ttu-id="9a372-103">Ottiene le informazioni sulle pianificazioni della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="9a372-103">Gets the information about the Bandwidth schedules</span></span>

## <span data-ttu-id="9a372-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a372-104">SYNTAX</span></span>

### <span data-ttu-id="9a372-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9a372-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a372-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a372-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9a372-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a372-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a372-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a372-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeBandwidthSchedule [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="9a372-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a372-109">DESCRIPTION</span></span>
<span data-ttu-id="9a372-110">Il cmdlet **Get-AzStackEdgeBandwidthSchedule** ottiene le informazioni sulle pianificazioni della larghezza di banda.</span><span class="sxs-lookup"><span data-stu-id="9a372-110">The **Get-AzStackEdgeBandwidthSchedule** cmdlet gets the information about the Bandwidth Schedules.</span></span> <span data-ttu-id="9a372-111">È possibile specificare il nome di una pianificazione insieme al nome del gruppo di risorse e al nome del dispositivo per ottenere le informazioni su una specifica pianificazione della larghezza di banda</span><span class="sxs-lookup"><span data-stu-id="9a372-111">You can specify the Name of a Schedule along with the Resource Group name and Device name to get the information about a specific Bandwidth schedule</span></span>

## <span data-ttu-id="9a372-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a372-112">EXAMPLES</span></span>

### <span data-ttu-id="9a372-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a372-113">Example 1</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name

Name              DaysOfWeek         RateInMbps StartTime StopTime
----              ----------         ---------- --------- --------
schedule-name     Sunday,Saturday    unlimited  13:00:00  14:00:00
Schedule-1        Tuesday,Friday     unlimited  00:00:00  23:59:00
Schedule-2        Thursday           50         00:01:00  05:00:00
```

### <span data-ttu-id="9a372-114">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a372-114">Example 2</span></span>
```powershell
PS C:\>Get-AzStackEdgeBandwidthSchedule -ResourceGroupname resource-group-name -DeviceName device-name -Name Schedule-1

Name              DaysOfWeek      RateInMbps StartTime StopTime
----              ----------      ---------- --------- --------
Schedule-1        Sunday,Saturday unlimited  13:00:00  14:00:00
```

## <span data-ttu-id="9a372-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a372-115">PARAMETERS</span></span>

### <span data-ttu-id="9a372-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a372-116">-DefaultProfile</span></span>
<span data-ttu-id="9a372-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a372-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a372-118">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="9a372-118">-DeviceName</span></span>
<span data-ttu-id="9a372-119">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="9a372-119">Device Name</span></span>

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

### <span data-ttu-id="9a372-120">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="9a372-120">-DeviceObject</span></span>
<span data-ttu-id="9a372-121">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="9a372-121">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="9a372-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a372-122">-Name</span></span>
<span data-ttu-id="9a372-123">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="9a372-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: BandwidthScheduleName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: BandwidthScheduleName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a372-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a372-124">-ResourceGroupName</span></span>
<span data-ttu-id="9a372-125">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="9a372-125">Resource Group Name</span></span>

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

### <span data-ttu-id="9a372-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a372-126">-ResourceId</span></span>
<span data-ttu-id="9a372-127">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a372-127">Azure ResourceId</span></span>

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

### <span data-ttu-id="9a372-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a372-128">CommonParameters</span></span>
<span data-ttu-id="9a372-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a372-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a372-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a372-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a372-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a372-131">INPUTS</span></span>

### <span data-ttu-id="9a372-132">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="9a372-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="9a372-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a372-133">OUTPUTS</span></span>

### <span data-ttu-id="9a372-134">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeBandWidthSchedule</span><span class="sxs-lookup"><span data-stu-id="9a372-134">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeBandWidthSchedule</span></span>

## <span data-ttu-id="9a372-135">Note</span><span class="sxs-lookup"><span data-stu-id="9a372-135">NOTES</span></span>

## <span data-ttu-id="9a372-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a372-136">RELATED LINKS</span></span>
