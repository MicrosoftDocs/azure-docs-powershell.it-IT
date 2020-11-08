---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgeorder
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeOrder.md
ms.openlocfilehash: 2ef7b7ac2a06da0ef0f4b09d82f9a4ed447618ce
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190052"
---
# <span data-ttu-id="2fee4-101">Get-AzStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="2fee4-101">Get-AzStackEdgeOrder</span></span>

## <span data-ttu-id="2fee4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2fee4-102">SYNOPSIS</span></span>
<span data-ttu-id="2fee4-103">Ottenere i dettagli dell'ordine per un dispositivo</span><span class="sxs-lookup"><span data-stu-id="2fee4-103">Get the order details for a device</span></span>

## <span data-ttu-id="2fee4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2fee4-104">SYNTAX</span></span>

### <span data-ttu-id="2fee4-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2fee4-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzStackEdgeOrder [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fee4-106">GetByDeviceObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fee4-106">GetByDeviceObjectParameterSet</span></span>
```
Get-AzStackEdgeOrder -DeviceObject <PSStackEdgeOrder> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2fee4-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2fee4-107">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeOrder -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fee4-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2fee4-108">DESCRIPTION</span></span>
<span data-ttu-id="2fee4-109">Il cmdlet **Get-AzStackEdgeOrder** ottiene i dettagli dell'ordine per un dispositivo di bordo dello stack.</span><span class="sxs-lookup"><span data-stu-id="2fee4-109">The **Get-AzStackEdgeOrder** cmdlet gets the order details for a Stack Edge device.</span></span> 

## <span data-ttu-id="2fee4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2fee4-110">EXAMPLES</span></span>

### <span data-ttu-id="2fee4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2fee4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeOrder -ResourceGroupName resourceGroupName -DeviceName deviceName
DeviceName  ResourceGroupName Status    UpdatedDatetime
----------  ----------------- ------    ---------------
deviceName  resourceGroupName Untracked 01-Jan-01 12:00:00 AM
```

## <span data-ttu-id="2fee4-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2fee4-112">PARAMETERS</span></span>

### <span data-ttu-id="2fee4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fee4-113">-DefaultProfile</span></span>
<span data-ttu-id="2fee4-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2fee4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2fee4-115">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="2fee4-115">-DeviceName</span></span>
<span data-ttu-id="2fee4-116">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2fee4-116">Resource Group Name</span></span>

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

### <span data-ttu-id="2fee4-117">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="2fee4-117">-DeviceObject</span></span>
<span data-ttu-id="2fee4-118">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="2fee4-118">Please provide corresponding device object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder
Parameter Sets: GetByDeviceObjectParameterSet
Aliases: Device

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fee4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fee4-119">-ResourceGroupName</span></span>
<span data-ttu-id="2fee4-120">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="2fee4-120">Resource Group Name</span></span>

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

### <span data-ttu-id="2fee4-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fee4-121">-ResourceId</span></span>
<span data-ttu-id="2fee4-122">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="2fee4-122">Azure ResourceId</span></span>

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

### <span data-ttu-id="2fee4-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fee4-123">CommonParameters</span></span>
<span data-ttu-id="2fee4-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fee4-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fee4-125">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2fee4-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fee4-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2fee4-126">INPUTS</span></span>

### <span data-ttu-id="2fee4-127">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="2fee4-127">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

### <span data-ttu-id="2fee4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2fee4-128">System.String</span></span>

## <span data-ttu-id="2fee4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2fee4-129">OUTPUTS</span></span>

### <span data-ttu-id="2fee4-130">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeOrder</span><span class="sxs-lookup"><span data-stu-id="2fee4-130">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeOrder</span></span>

## <span data-ttu-id="2fee4-131">Note</span><span class="sxs-lookup"><span data-stu-id="2fee4-131">NOTES</span></span>

## <span data-ttu-id="2fee4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2fee4-132">RELATED LINKS</span></span>
