---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: c2d97f4a7d713482a5e442e1fcb712ccb18797c0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298860"
---
# <span data-ttu-id="72259-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="72259-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="72259-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72259-102">SYNOPSIS</span></span>
<span data-ttu-id="72259-103">Ottiene i processi pianificati in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="72259-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="72259-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72259-104">SYNTAX</span></span>

### <span data-ttu-id="72259-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72259-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72259-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="72259-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72259-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="72259-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="72259-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72259-108">DESCRIPTION</span></span>
<span data-ttu-id="72259-109">Il cmdlet **Get-AzDataBoxEdgeJob** ottiene i processi attivi in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="72259-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="72259-110">Puoi menzionare il parametro Name per ottenere i dettagli di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="72259-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="72259-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72259-111">EXAMPLES</span></span>

### <span data-ttu-id="72259-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72259-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="72259-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72259-113">PARAMETERS</span></span>

### <span data-ttu-id="72259-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72259-114">-DefaultProfile</span></span>
<span data-ttu-id="72259-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72259-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72259-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="72259-116">-DeviceName</span></span>
<span data-ttu-id="72259-117">Nome del dispositivo</span><span class="sxs-lookup"><span data-stu-id="72259-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="72259-118">-DeviceObject</span></span>
<span data-ttu-id="72259-119">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="72259-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="72259-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="72259-120">-Name</span></span>
<span data-ttu-id="72259-121">Nome del processo, in genere un GUID</span><span class="sxs-lookup"><span data-stu-id="72259-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72259-122">-ResourceGroupName</span></span>
<span data-ttu-id="72259-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="72259-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72259-124">-ResourceId</span></span>
<span data-ttu-id="72259-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="72259-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="72259-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72259-126">CommonParameters</span></span>
<span data-ttu-id="72259-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72259-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72259-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72259-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72259-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72259-129">INPUTS</span></span>

### <span data-ttu-id="72259-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="72259-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="72259-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72259-131">OUTPUTS</span></span>

### <span data-ttu-id="72259-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="72259-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="72259-133">Note</span><span class="sxs-lookup"><span data-stu-id="72259-133">NOTES</span></span>

## <span data-ttu-id="72259-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72259-134">RELATED LINKS</span></span>
