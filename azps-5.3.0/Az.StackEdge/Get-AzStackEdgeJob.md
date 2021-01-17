---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeJob.md
ms.openlocfilehash: 957cc5c7dea0b8ea3215a035f68c2528442a7d52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98487388"
---
# <span data-ttu-id="76269-101">Get-AzStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="76269-101">Get-AzStackEdgeJob</span></span>

## <span data-ttu-id="76269-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76269-102">SYNOPSIS</span></span>
<span data-ttu-id="76269-103">Ottiene i processi pianificati in un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="76269-103">Gets the jobs scheduled on a device.</span></span>

## <span data-ttu-id="76269-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76269-104">SYNTAX</span></span>

### <span data-ttu-id="76269-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="76269-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeJob [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76269-106">GetByResourceIdObject</span><span class="sxs-lookup"><span data-stu-id="76269-106">GetByResourceIdObject</span></span>
```
Get-AzStackEdgeJob -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="76269-107">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76269-107">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeJob [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="76269-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76269-108">DESCRIPTION</span></span>
<span data-ttu-id="76269-109">Il cmdlet **Get-AzStackEdgeJob** ottiene i processi attivi in un dispositivo Edge dello stack.</span><span class="sxs-lookup"><span data-stu-id="76269-109">The **Get-AzStackEdgeJob** cmdlet gets the active jobs on a Stack Edge device.</span></span> <span data-ttu-id="76269-110">Puoi menzionare il parametro Name per ottenere i dettagli di un processo specifico.</span><span class="sxs-lookup"><span data-stu-id="76269-110">You can mention the Name parameter to get details of a specific job.</span></span>

## <span data-ttu-id="76269-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76269-111">EXAMPLES</span></span>

### <span data-ttu-id="76269-112">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76269-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeJob -ResourceGroupName resourceGroupName -DeviceName deviceName -Name 1f2d8f1b-9104-49c3-b780-76db9abe7bd1
Name                                   Device-Name    status
------------------                     -------------  -------
1f2d8f1b-9104-49c3-b780-76db9abe7bd1   deviceName    Scheduled
```

## <span data-ttu-id="76269-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76269-113">PARAMETERS</span></span>

### <span data-ttu-id="76269-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76269-114">-DefaultProfile</span></span>
<span data-ttu-id="76269-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76269-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76269-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="76269-116">-DeviceName</span></span>
<span data-ttu-id="76269-117">Nome del dispositivo</span><span class="sxs-lookup"><span data-stu-id="76269-117">Name of the device</span></span>

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

### <span data-ttu-id="76269-118">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="76269-118">-DeviceObject</span></span>
<span data-ttu-id="76269-119">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="76269-119">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="76269-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="76269-120">-Name</span></span>
<span data-ttu-id="76269-121">Nome del processo, in genere un GUID</span><span class="sxs-lookup"><span data-stu-id="76269-121">Name of the Job, Generally a GUID</span></span>

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

### <span data-ttu-id="76269-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76269-122">-ResourceGroupName</span></span>
<span data-ttu-id="76269-123">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="76269-123">Resource Group Name</span></span>

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

### <span data-ttu-id="76269-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76269-124">-ResourceId</span></span>
<span data-ttu-id="76269-125">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="76269-125">Azure ResourceId</span></span>

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

### <span data-ttu-id="76269-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76269-126">CommonParameters</span></span>
<span data-ttu-id="76269-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76269-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76269-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76269-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76269-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76269-129">INPUTS</span></span>

### <span data-ttu-id="76269-130">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="76269-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="76269-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76269-131">OUTPUTS</span></span>

### <span data-ttu-id="76269-132">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeJob</span><span class="sxs-lookup"><span data-stu-id="76269-132">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeJob</span></span>

## <span data-ttu-id="76269-133">Note</span><span class="sxs-lookup"><span data-stu-id="76269-133">NOTES</span></span>

## <span data-ttu-id="76269-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76269-134">RELATED LINKS</span></span>
