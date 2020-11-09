---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeOrder.md
ms.openlocfilehash: c1b5c52233b6887dc3221e49174b45d907716c10
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298855"
---
# <span data-ttu-id="a850c-101">Get-AzDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a850c-101">Get-AzDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a850c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a850c-102">SYNOPSIS</span></span>
<span data-ttu-id="a850c-103">Ottenere i dettagli dell'ordine per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="a850c-103">Get the order details for a device</span></span>

## <span data-ttu-id="a850c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a850c-104">SYNTAX</span></span>

### <span data-ttu-id="a850c-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a850c-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a850c-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a850c-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -DeviceObject <PSDataBoxEdgeDevice> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a850c-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a850c-107">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a850c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a850c-108">DESCRIPTION</span></span>
<span data-ttu-id="a850c-109">Il cmdlet **Get-AzDataBoxEdgeOrder** ottiene i dettagli dell'ordine per un dispositivo Edge della casella dati.</span><span class="sxs-lookup"><span data-stu-id="a850c-109">The **Get-AzDataBoxEdgeOrder** cmdlet gets the order details for a Data Box Edge device.</span></span> 

## <span data-ttu-id="a850c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a850c-110">EXAMPLES</span></span>

### <span data-ttu-id="a850c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a850c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="a850c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a850c-112">PARAMETERS</span></span>

### <span data-ttu-id="a850c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a850c-113">-DefaultProfile</span></span>
<span data-ttu-id="a850c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a850c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a850c-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="a850c-115">-DeviceName</span></span>
<span data-ttu-id="a850c-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a850c-116">Resource Group Name</span></span>

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

### <span data-ttu-id="a850c-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="a850c-117">-DeviceObject</span></span>
<span data-ttu-id="a850c-118">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="a850c-118">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="a850c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a850c-119">-ResourceGroupName</span></span>
<span data-ttu-id="a850c-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="a850c-120">Resource Group Name</span></span>

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

### <span data-ttu-id="a850c-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-121">-ResourceId</span></span>
<span data-ttu-id="a850c-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="a850c-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="a850c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a850c-123">CommonParameters</span></span>
<span data-ttu-id="a850c-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a850c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a850c-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a850c-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a850c-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a850c-126">INPUTS</span></span>

### <span data-ttu-id="a850c-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="a850c-127">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

### <span data-ttu-id="a850c-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a850c-128">System.String</span></span>

## <span data-ttu-id="a850c-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a850c-129">OUTPUTS</span></span>

### <span data-ttu-id="a850c-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="a850c-130">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeOrder</span></span>

## <span data-ttu-id="a850c-131">Note</span><span class="sxs-lookup"><span data-stu-id="a850c-131">NOTES</span></span>

## <span data-ttu-id="a850c-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a850c-132">RELATED LINKS</span></span>
