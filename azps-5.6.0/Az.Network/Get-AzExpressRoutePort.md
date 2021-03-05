---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: f9ce00bb5efbe5182143a08f9f205101b9f85611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979582"
---
# <span data-ttu-id="0975d-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0975d-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="0975d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0975d-102">SYNOPSIS</span></span>
<span data-ttu-id="0975d-103">Ottiene una risorsa Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0975d-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="0975d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0975d-104">SYNTAX</span></span>

### <span data-ttu-id="0975d-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0975d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0975d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0975d-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0975d-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0975d-107">DESCRIPTION</span></span>
<span data-ttu-id="0975d-108">Il cmdlet **Get-AzExpressRoutePort** viene usato per recuperare un oggetto ExpressRoutePort dalla sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0975d-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="0975d-109">L'oggetto expressrouteport restituito può essere usato come input per altri cmdlet che operano su ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0975d-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="0975d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0975d-110">EXAMPLES</span></span>

### <span data-ttu-id="0975d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="0975d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="0975d-112">Recupera l'oggetto ExpressRoutePort con nome $PortName nel gruppo di $rg nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="0975d-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="0975d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="0975d-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="0975d-114">Ottiene tutti gli oggetti ExpressRoutePort il cui nome inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="0975d-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="0975d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="0975d-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="0975d-116">Ottiene l'oggetto ExpressRoutePort con resourceId $id.</span><span class="sxs-lookup"><span data-stu-id="0975d-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="0975d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0975d-117">PARAMETERS</span></span>

### <span data-ttu-id="0975d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0975d-118">-DefaultProfile</span></span>
<span data-ttu-id="0975d-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0975d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0975d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0975d-120">-Name</span></span>
<span data-ttu-id="0975d-121">Nome di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0975d-121">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0975d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0975d-122">-ResourceGroupName</span></span>
<span data-ttu-id="0975d-123">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="0975d-123">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="0975d-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0975d-124">-ResourceId</span></span>
<span data-ttu-id="0975d-125">ResourceId della porta express route.</span><span class="sxs-lookup"><span data-stu-id="0975d-125">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0975d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0975d-126">CommonParameters</span></span>
<span data-ttu-id="0975d-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0975d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0975d-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0975d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0975d-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="0975d-129">INPUTS</span></span>

### <span data-ttu-id="0975d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="0975d-130">System.String</span></span>

## <span data-ttu-id="0975d-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0975d-131">OUTPUTS</span></span>

### <span data-ttu-id="0975d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0975d-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="0975d-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="0975d-133">NOTES</span></span>

## <span data-ttu-id="0975d-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0975d-134">RELATED LINKS</span></span>

[<span data-ttu-id="0975d-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0975d-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="0975d-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0975d-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="0975d-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="0975d-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
