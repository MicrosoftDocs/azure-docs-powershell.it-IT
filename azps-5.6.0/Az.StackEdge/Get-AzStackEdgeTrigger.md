---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: a4bcbad5f595efe126ed232b94d5deb368515bc2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976238"
---
# <span data-ttu-id="59275-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="59275-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="59275-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59275-102">SYNOPSIS</span></span>
<span data-ttu-id="59275-103">Configurare i trigger in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="59275-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="59275-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="59275-104">SYNTAX</span></span>

### <span data-ttu-id="59275-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="59275-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59275-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="59275-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59275-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="59275-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59275-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="59275-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="59275-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="59275-109">DESCRIPTION</span></span>
<span data-ttu-id="59275-110">Il cmdlet **Get-AzStackEdgeTriger** ottiene i trigger per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="59275-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="59275-111">È possibile specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico trigger</span><span class="sxs-lookup"><span data-stu-id="59275-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="59275-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="59275-112">EXAMPLES</span></span>

### <span data-ttu-id="59275-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="59275-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="59275-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59275-114">PARAMETERS</span></span>

### <span data-ttu-id="59275-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59275-115">-DefaultProfile</span></span>
<span data-ttu-id="59275-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="59275-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59275-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="59275-117">-DeviceName</span></span>
<span data-ttu-id="59275-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="59275-118">Device Name</span></span>

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

### <span data-ttu-id="59275-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="59275-119">-DeviceObject</span></span>
<span data-ttu-id="59275-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="59275-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="59275-121">-Name</span><span class="sxs-lookup"><span data-stu-id="59275-121">-Name</span></span>
<span data-ttu-id="59275-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="59275-122">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByParentObjectParameterSet
Aliases: TriggerName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59275-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59275-123">-ResourceGroupName</span></span>
<span data-ttu-id="59275-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="59275-124">Resource Group Name</span></span>

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

### <span data-ttu-id="59275-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59275-125">-ResourceId</span></span>
<span data-ttu-id="59275-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="59275-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="59275-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59275-127">CommonParameters</span></span>
<span data-ttu-id="59275-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59275-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59275-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="59275-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59275-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="59275-130">INPUTS</span></span>

### <span data-ttu-id="59275-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="59275-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="59275-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="59275-132">OUTPUTS</span></span>

### <span data-ttu-id="59275-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="59275-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="59275-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="59275-134">NOTES</span></span>

## <span data-ttu-id="59275-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="59275-135">RELATED LINKS</span></span>
