---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181110"
---
# <span data-ttu-id="d0ac2-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d0ac2-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d0ac2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0ac2-102">SYNOPSIS</span></span>
<span data-ttu-id="d0ac2-103">Ottenere i dettagli dell'ordine per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="d0ac2-103">Get the order details for a device</span></span>

## <span data-ttu-id="d0ac2-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d0ac2-104">SYNTAX</span></span>

### <span data-ttu-id="d0ac2-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d0ac2-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d0ac2-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0ac2-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d0ac2-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0ac2-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d0ac2-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d0ac2-108">DESCRIPTION</span></span>
<span data-ttu-id="d0ac2-109">Il **cmdlet Get-AzDataBoxEdgeOrder** ottiene i dettagli dell'ordine per un dispositivo Data Box Edge.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="d0ac2-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d0ac2-110">EXAMPLES</span></span>

### <span data-ttu-id="d0ac2-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d0ac2-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="d0ac2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0ac2-112">PARAMETERS</span></span>

### <span data-ttu-id="d0ac2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0ac2-113">-DefaultProfile</span></span>
<span data-ttu-id="d0ac2-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0ac2-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="d0ac2-115">-DeviceName</span></span>
<span data-ttu-id="d0ac2-116">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d0ac2-116">Resource Group Name</span></span>

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

### <span data-ttu-id="d0ac2-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="d0ac2-117">-DeviceObject</span></span>
<span data-ttu-id="d0ac2-118">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="d0ac2-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice
Parameter Sets: GetByDeviceObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d0ac2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0ac2-119">-ResourceGroupName</span></span>
<span data-ttu-id="d0ac2-120">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="d0ac2-120">Resource Group Name</span></span>

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

### <span data-ttu-id="d0ac2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0ac2-121">-ResourceId</span></span>
<span data-ttu-id="d0ac2-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="d0ac2-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="d0ac2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0ac2-123">CommonParameters</span></span>
<span data-ttu-id="d0ac2-124">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0ac2-125">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d0ac2-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0ac2-126">INPUT</span><span class="sxs-lookup"><span data-stu-id="d0ac2-126">INPUTS</span></span>

### <span data-ttu-id="d0ac2-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="d0ac2-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="d0ac2-128">System.String</span><span class="sxs-lookup"><span data-stu-id="d0ac2-128">System.String</span></span>

## <span data-ttu-id="d0ac2-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d0ac2-129">OUTPUTS</span></span>

### <span data-ttu-id="d0ac2-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="d0ac2-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="d0ac2-131">NOTE</span><span class="sxs-lookup"><span data-stu-id="d0ac2-131">NOTES</span></span>

## <span data-ttu-id="d0ac2-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d0ac2-132">RELATED LINKS</span></span>
