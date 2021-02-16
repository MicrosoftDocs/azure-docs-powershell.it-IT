---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183231"
---
# <span data-ttu-id="e607d-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e607d-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="e607d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e607d-102">SYNOPSIS</span></span>
<span data-ttu-id="e607d-103">Configurare i trigger in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="e607d-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="e607d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e607d-104">SYNTAX</span></span>

### <span data-ttu-id="e607d-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e607d-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e607d-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e607d-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e607d-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e607d-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e607d-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e607d-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="e607d-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e607d-109">DESCRIPTION</span></span>
<span data-ttu-id="e607d-110">Il cmdlet **Get-AzStackEdgeTriger** ottiene i trigger per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e607d-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="e607d-111">È possibile specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico trigger</span><span class="sxs-lookup"><span data-stu-id="e607d-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="e607d-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e607d-112">EXAMPLES</span></span>

### <span data-ttu-id="e607d-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e607d-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="e607d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e607d-114">PARAMETERS</span></span>

### <span data-ttu-id="e607d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e607d-115">-DefaultProfile</span></span>
<span data-ttu-id="e607d-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e607d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e607d-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="e607d-117">-DeviceName</span></span>
<span data-ttu-id="e607d-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="e607d-118">Device Name</span></span>

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

### <span data-ttu-id="e607d-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="e607d-119">-DeviceObject</span></span>
<span data-ttu-id="e607d-120">Specifica l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="e607d-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="e607d-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e607d-121">-Name</span></span>
<span data-ttu-id="e607d-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="e607d-122">Resource Name</span></span>

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

### <span data-ttu-id="e607d-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e607d-123">-ResourceGroupName</span></span>
<span data-ttu-id="e607d-124">Nome gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="e607d-124">Resource Group Name</span></span>

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

### <span data-ttu-id="e607d-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e607d-125">-ResourceId</span></span>
<span data-ttu-id="e607d-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="e607d-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="e607d-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e607d-127">CommonParameters</span></span>
<span data-ttu-id="e607d-128">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e607d-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e607d-129">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e607d-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e607d-130">INPUT</span><span class="sxs-lookup"><span data-stu-id="e607d-130">INPUTS</span></span>

### <span data-ttu-id="e607d-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="e607d-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="e607d-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e607d-132">OUTPUTS</span></span>

### <span data-ttu-id="e607d-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="e607d-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="e607d-134">NOTE</span><span class="sxs-lookup"><span data-stu-id="e607d-134">NOTES</span></span>

## <span data-ttu-id="e607d-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e607d-135">RELATED LINKS</span></span>
