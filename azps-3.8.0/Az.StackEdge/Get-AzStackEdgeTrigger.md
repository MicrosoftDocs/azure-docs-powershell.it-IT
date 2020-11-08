---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/get-azstackedgetrigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Get-AzStackEdgeTrigger.md
ms.openlocfilehash: 238290778d47de673f9db89280f500c2fc31ea28
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019011"
---
# <span data-ttu-id="969ad-101">Get-AzStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="969ad-101">Get-AzStackEdgeTrigger</span></span>

## <span data-ttu-id="969ad-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="969ad-102">SYNOPSIS</span></span>
<span data-ttu-id="969ad-103">Ottenere i trigger configurati in un dispositivo</span><span class="sxs-lookup"><span data-stu-id="969ad-103">Get the Triggers configured on a device</span></span>
 

## <span data-ttu-id="969ad-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="969ad-104">SYNTAX</span></span>

### <span data-ttu-id="969ad-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="969ad-105">ListParameterSet (Default)</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="969ad-106">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="969ad-106">GetByResourceIdParameterSet</span></span>
```
Get-AzStackEdgeTrigger -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="969ad-107">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="969ad-107">GetByNameParameterSet</span></span>
```
Get-AzStackEdgeTrigger [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="969ad-108">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="969ad-108">GetByParentObjectParameterSet</span></span>
```
Get-AzStackEdgeTrigger [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 -DeviceObject <PSStackEdgeDevice> [<CommonParameters>]
```

## <span data-ttu-id="969ad-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="969ad-109">DESCRIPTION</span></span>
<span data-ttu-id="969ad-110">Il cmdlet **Get-AzStackEdgeTriger** ottiene i trigger per un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="969ad-110">The **Get-AzStackEdgeTriger** cmdlet gets the triggers for a device.</span></span> <span data-ttu-id="969ad-111">Puoi specificare il nome come parametro nel cmdlet per recuperare i dettagli di uno specifico trigger specifico</span><span class="sxs-lookup"><span data-stu-id="969ad-111">You can specify the name as a parameter in the cmdlet to fetch the details of a specific  specific Triggers</span></span>
 

## <span data-ttu-id="969ad-112">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="969ad-112">EXAMPLES</span></span>

### <span data-ttu-id="969ad-113">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="969ad-113">Example 1</span></span>
```powershell
PS C:\> Get-AzStackEdgeTrigger -ResourceGroupName resourceGroupName -DeviceName deviceName
Name                  Kind               
----                  ----               
triggerName          PeriodicTimerEvent
```

## <span data-ttu-id="969ad-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="969ad-114">PARAMETERS</span></span>

### <span data-ttu-id="969ad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969ad-115">-DefaultProfile</span></span>
<span data-ttu-id="969ad-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="969ad-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969ad-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="969ad-117">-DeviceName</span></span>
<span data-ttu-id="969ad-118">Nome dispositivo</span><span class="sxs-lookup"><span data-stu-id="969ad-118">Device Name</span></span>

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

### <span data-ttu-id="969ad-119">-DeviceObject</span><span class="sxs-lookup"><span data-stu-id="969ad-119">-DeviceObject</span></span>
<span data-ttu-id="969ad-120">Immettere l'oggetto dispositivo corrispondente</span><span class="sxs-lookup"><span data-stu-id="969ad-120">Please provide corresponding device object</span></span>

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

### <span data-ttu-id="969ad-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="969ad-121">-Name</span></span>
<span data-ttu-id="969ad-122">Nome risorsa</span><span class="sxs-lookup"><span data-stu-id="969ad-122">Resource Name</span></span>

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

### <span data-ttu-id="969ad-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969ad-123">-ResourceGroupName</span></span>
<span data-ttu-id="969ad-124">Nome gruppo risorse</span><span class="sxs-lookup"><span data-stu-id="969ad-124">Resource Group Name</span></span>

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

### <span data-ttu-id="969ad-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="969ad-125">-ResourceId</span></span>
<span data-ttu-id="969ad-126">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="969ad-126">Azure ResourceId</span></span>

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

### <span data-ttu-id="969ad-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969ad-127">CommonParameters</span></span>
<span data-ttu-id="969ad-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969ad-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969ad-129">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="969ad-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969ad-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="969ad-130">INPUTS</span></span>

### <span data-ttu-id="969ad-131">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeDevice</span><span class="sxs-lookup"><span data-stu-id="969ad-131">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeDevice</span></span>

## <span data-ttu-id="969ad-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="969ad-132">OUTPUTS</span></span>

### <span data-ttu-id="969ad-133">Microsoft. Azure. PowerShell. Cmdlets. StackEdge. Models. PSStackEdgeTrigger</span><span class="sxs-lookup"><span data-stu-id="969ad-133">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeTrigger</span></span>

## <span data-ttu-id="969ad-134">Note</span><span class="sxs-lookup"><span data-stu-id="969ad-134">NOTES</span></span>

## <span data-ttu-id="969ad-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="969ad-135">RELATED LINKS</span></span>
