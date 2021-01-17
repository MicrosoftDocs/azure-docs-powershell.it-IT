---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/get-azdataboxedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Get-AzDataBoxEdgeTrigger.md
ms.openlocfilehash: 390646984cbe18c6fed0e6552e8034ae7afe311c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98477259"
---
# <span data-ttu-id="8fcb8-101">Get-AzDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="8fcb8-101">Get-AzDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="8fcb8-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fcb8-102">SYNOPSIS</span></span>
<span data-ttu-id="8fcb8-103">Ottenere i trigger configurati in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="8fcb8-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="8fcb8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fcb8-104">SYNTAX</span></span>

### <span data-ttu-id="8fcb8-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8fcb8-105">ListParameterSet (Default)</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fcb8-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fcb8-106">GetByResourceIdParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fcb8-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fcb8-107">GetByNameParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8fcb8-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8fcb8-108">GetByParentObjectParameterSet</span></span>
```
Get-AzDataBoxEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSDataBoxEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="8fcb8-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fcb8-109">DESCRIPTION</span></span>
<span data-ttu-id="8fcb8-110">Il cmdlet **Get-AzDataBoxEdgeTriger** ottiene i trigger per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8fcb8-110">The **Get-AzDataBoxEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="8fcb8-111">Puoi specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico trigger specifico</span><span class="sxs-lookup"><span data-stu-id="8fcb8-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="8fcb8-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fcb8-112">EXAMPLES</span></span>

### <span data-ttu-id="8fcb8-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8fcb8-113">Example 1</span></span>
```powershell
PS C:\> Get-AzDataBoxEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="8fcb8-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fcb8-114">PARAMETERS</span></span>

### <span data-ttu-id="8fcb8-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fcb8-115">-DefaultProfile</span></span>
<span data-ttu-id="8fcb8-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fcb8-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8fcb8-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="8fcb8-117">-DeviceName</span></span>
<span data-ttu-id="8fcb8-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="8fcb8-118">Device Name</span></span>

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

### <span data-ttu-id="8fcb8-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="8fcb8-119">-DeviceObject</span></span>
<span data-ttu-id="8fcb8-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="8fcb8-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="8fcb8-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="8fcb8-121">-Name</span></span>
<span data-ttu-id="8fcb8-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="8fcb8-122">Resource Name</span></span>

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

### <span data-ttu-id="8fcb8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8fcb8-123">-ResourceGroupName</span></span>
<span data-ttu-id="8fcb8-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="8fcb8-124">Resource Group Name</span></span>

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

### <span data-ttu-id="8fcb8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fcb8-125">-ResourceId</span></span>
<span data-ttu-id="8fcb8-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="8fcb8-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="8fcb8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fcb8-127">CommonParameters</span></span>
<span data-ttu-id="8fcb8-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fcb8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fcb8-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8fcb8-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fcb8-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fcb8-130">INPUTS</span></span>

### <span data-ttu-id="8fcb8-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="8fcb8-131">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeDevice</span></span>

## <span data-ttu-id="8fcb8-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fcb8-132">OUTPUTS</span></span>

### <span data-ttu-id="8fcb8-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="8fcb8-133">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeTrigger</span></span>

## <span data-ttu-id="8fcb8-134">Note</span><span class="sxs-lookup"><span data-stu-id="8fcb8-134">NOTES</span></span>

## <span data-ttu-id="8fcb8-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fcb8-135">RELATED LINKS</span></span>
