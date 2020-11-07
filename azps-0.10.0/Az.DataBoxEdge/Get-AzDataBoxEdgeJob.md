---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeJob.md
ms.openlocfilehash: 4f5626059e4185e5440e7d5a11346c82ce472bbd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93863306"
---
# <span data-ttu-id="20a1d-101">Get-AzDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="20a1d-101">Get-AzDataBoxEdgeJob</span></span>

## <span data-ttu-id="20a1d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="20a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="20a1d-103">Ottiene i processi pianificati in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="20a1d-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="20a1d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="20a1d-104">SYNTAX</span></span>

### <span data-ttu-id="20a1d-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="20a1d-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a1d-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="20a1d-106">GetByResourceIdObject</span></span>
```
Get-AzDataBoxEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20a1d-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20a1d-107">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="20a1d-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="20a1d-108">DESCRIPTION</span></span>
<span data-ttu-id="20a1d-109">Il cmdlet **Get-AzDataBoxEdgeJob** ottiene i processi attivi in un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="20a1d-109">The **Get-AzDataBoxEdgeJob** cmdlet gets the active jobs on a Data Box Edge device.</span></span> <span data-ttu-id="20a1d-110">Puoi menzionare il parametro Name per ottenere i dettagli di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="20a1d-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="20a1d-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="20a1d-111">EXAMPLES</span></span>

### <span data-ttu-id="20a1d-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="20a1d-112">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="20a1d-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="20a1d-113">PARAMETERS</span></span>

### <span data-ttu-id="20a1d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20a1d-114">-DefaultProfile</span></span>
<span data-ttu-id="20a1d-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="20a1d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20a1d-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="20a1d-116">-DeviceName</span></span>
<span data-ttu-id="20a1d-117">Nome del dispositivo</span><span class="sxs-lookup"><span data-stu-id="20a1d-117">Name of the device</span></span>

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

### <span data-ttu-id="20a1d-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="20a1d-118">-DeviceObject</span></span>
<span data-ttu-id="20a1d-119">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="20a1d-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="20a1d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="20a1d-120">-Name</span></span>
<span data-ttu-id="20a1d-121">Nome del processo, in genere un GUID</span><span class="sxs-lookup"><span data-stu-id="20a1d-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="20a1d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20a1d-122">-ResourceGroupName</span></span>
<span data-ttu-id="20a1d-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="20a1d-123">Resource Group Name</span></span>

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

### <span data-ttu-id="20a1d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20a1d-124">-ResourceId</span></span>
<span data-ttu-id="20a1d-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="20a1d-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="20a1d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20a1d-126">CommonParameters</span></span>
<span data-ttu-id="20a1d-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20a1d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20a1d-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="20a1d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20a1d-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="20a1d-129">INPUTS</span></span>

### <span data-ttu-id="20a1d-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="20a1d-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="20a1d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="20a1d-131">OUTPUTS</span></span>

### <span data-ttu-id="20a1d-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span><span class="sxs-lookup"><span data-stu-id="20a1d-132">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeJob</span></span>

## <span data-ttu-id="20a1d-133">Note</span><span class="sxs-lookup"><span data-stu-id="20a1d-133">NOTES</span></span>

## <span data-ttu-id="20a1d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="20a1d-134">RELATED LINKS</span></span>
