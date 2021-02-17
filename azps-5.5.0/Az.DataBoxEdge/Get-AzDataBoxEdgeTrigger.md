---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186310"
---
# <span data-ttu-id="3cceb-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="3cceb-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="3cceb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cceb-102">SYNOPSIS</span></span>
<span data-ttu-id="3cceb-103">Configurare i trigger in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="3cceb-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="3cceb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cceb-104">SYNTAX</span></span>

### <span data-ttu-id="3cceb-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cceb-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cceb-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cceb-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cceb-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cceb-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3cceb-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cceb-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="3cceb-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3cceb-109">DESCRIPTION</span></span>
<span data-ttu-id="3cceb-110">Il **cmdlet Get-AzDataBoxEdgeTriger** ottiene i trigger per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="3cceb-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="3cceb-111">È possibile specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico trigger</span><span class="sxs-lookup"><span data-stu-id="3cceb-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="3cceb-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cceb-112">EXAMPLES</span></span>

### <span data-ttu-id="3cceb-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3cceb-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="3cceb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cceb-114">PARAMETERS</span></span>

### <span data-ttu-id="3cceb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cceb-115">-DefaultProfile</span></span>
<span data-ttu-id="3cceb-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cceb-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cceb-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="3cceb-117">-DeviceName</span></span>
<span data-ttu-id="3cceb-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="3cceb-118">Device Name</span></span>

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

### <span data-ttu-id="3cceb-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="3cceb-119">-DeviceObject</span></span>
<span data-ttu-id="3cceb-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="3cceb-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="3cceb-121">-Name</span><span class="sxs-lookup"><span data-stu-id="3cceb-121">-Name</span></span>
<span data-ttu-id="3cceb-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="3cceb-122">Resource Name</span></span>

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

### <span data-ttu-id="3cceb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cceb-123">-ResourceGroupName</span></span>
<span data-ttu-id="3cceb-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="3cceb-124">Resource Group Name</span></span>

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

### <span data-ttu-id="3cceb-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cceb-125">-ResourceId</span></span>
<span data-ttu-id="3cceb-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="3cceb-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="3cceb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cceb-127">CommonParameters</span></span>
<span data-ttu-id="3cceb-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cceb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cceb-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cceb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cceb-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="3cceb-130">INPUTS</span></span>

### <span data-ttu-id="3cceb-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="3cceb-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="3cceb-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cceb-132">OUTPUTS</span></span>

### <span data-ttu-id="3cceb-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="3cceb-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="3cceb-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="3cceb-134">NOTES</span></span>

## <span data-ttu-id="3cceb-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cceb-135">RELATED LINKS</span></span>
