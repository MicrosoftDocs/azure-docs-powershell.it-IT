---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197599"
---
# <span data-ttu-id="99c63-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="99c63-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="99c63-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99c63-102">SYNOPSIS</span></span>
<span data-ttu-id="99c63-103">Recupera i processi pianificati in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="99c63-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="99c63-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="99c63-104">SYNTAX</span></span>

### <span data-ttu-id="99c63-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="99c63-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99c63-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="99c63-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="99c63-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="99c63-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="99c63-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="99c63-108">DESCRIPTION</span></span>
<span data-ttu-id="99c63-109">Il cmdlet **Get-AzStackEdgeJob** ottiene i processi attivi in un dispositivo Stack Edge.</span><span class="sxs-lookup"><span data-stu-id="99c63-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="99c63-110">È possibile menzionare il parametro Name per ottenere i dettagli di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="99c63-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="99c63-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="99c63-111">EXAMPLES</span></span>

### <span data-ttu-id="99c63-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="99c63-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="99c63-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="99c63-113">PARAMETERS</span></span>

### <span data-ttu-id="99c63-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99c63-114">-DefaultProfile</span></span>
<span data-ttu-id="99c63-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="99c63-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="99c63-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="99c63-116">-DeviceName</span></span>
<span data-ttu-id="99c63-117">Nome del dispositivo</span><span class="sxs-lookup"><span data-stu-id="99c63-117">Name of the device</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99c63-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="99c63-118">-DeviceObject</span></span>
<span data-ttu-id="99c63-119">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="99c63-119">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="99c63-120">-Name</span><span class="sxs-lookup"><span data-stu-id="99c63-120">-Name</span></span>
<span data-ttu-id="99c63-121">Nome del processo, in genere un GUID</span><span class="sxs-lookup"><span data-stu-id="99c63-121">Name of the Job, Generally a GUID</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet, GetByParentObjectParameterSet
Aliases: Job

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99c63-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99c63-122">-ResourceGroupName</span></span>
<span data-ttu-id="99c63-123">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="99c63-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99c63-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99c63-124">-ResourceId</span></span>
<span data-ttu-id="99c63-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="99c63-125">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="99c63-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99c63-126">CommonParameters</span></span>
<span data-ttu-id="99c63-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="99c63-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99c63-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="99c63-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99c63-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="99c63-129">INPUTS</span></span>

### <span data-ttu-id="99c63-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="99c63-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="99c63-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="99c63-131">OUTPUTS</span></span>

### <span data-ttu-id="99c63-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="99c63-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="99c63-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="99c63-133">NOTES</span></span>

## <span data-ttu-id="99c63-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="99c63-134">RELATED LINKS</span></span>
