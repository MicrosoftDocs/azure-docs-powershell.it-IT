---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzExpressRoutePort.md
ms.openlocfilehash: 670880a9fa82e4845f37cdb5f0d108533a2b72c5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021319"
---
# <span data-ttu-id="72077-101">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="72077-101">Get-AzExpressRoutePort</span></span>

## <span data-ttu-id="72077-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="72077-102">SYNOPSIS</span></span>
<span data-ttu-id="72077-103">Ottiene una risorsa di Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="72077-103">Gets an Azure ExpressRoutePort resource.</span></span>

## <span data-ttu-id="72077-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="72077-104">SYNTAX</span></span>

### <span data-ttu-id="72077-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="72077-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72077-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="72077-106">ResourceIdParameterSet</span></span>
```
Get-AzExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72077-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="72077-107">DESCRIPTION</span></span>
<span data-ttu-id="72077-108">Il cmdlet **Get-AzExpressRoutePort** viene usato per recuperare un oggetto ExpressRoutePort dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72077-108">The **Get-AzExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="72077-109">L'oggetto expressrouteport restituito può essere usato come input per altri cmdlet che operano in ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="72077-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="72077-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="72077-110">EXAMPLES</span></span>

### <span data-ttu-id="72077-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="72077-111">Example 1</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="72077-112">Ottiene l'oggetto ExpressRoutePort con il nome $PortName nel gruppo di risorse $rg nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="72077-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="72077-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="72077-113">Example 2</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -Name test*
```

<span data-ttu-id="72077-114">Ottiene tutti gli oggetti ExpressRoutePort il cui nome inizia con "test".</span><span class="sxs-lookup"><span data-stu-id="72077-114">Gets all of the ExpressRoutePort objects whose name starts with "test".</span></span>

### <span data-ttu-id="72077-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="72077-115">Example 3</span></span>
```powershell
PS C:\> Get-AzExpressRoutePort -ResourceId $id
```

<span data-ttu-id="72077-116">Ottiene l'oggetto ExpressRoutePort con ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="72077-116">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="72077-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="72077-117">PARAMETERS</span></span>

### <span data-ttu-id="72077-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72077-118">-DefaultProfile</span></span>
<span data-ttu-id="72077-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="72077-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="72077-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="72077-120">-Name</span></span>
<span data-ttu-id="72077-121">Il nome del ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="72077-121">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="72077-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="72077-122">-ResourceGroupName</span></span>
<span data-ttu-id="72077-123">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="72077-123">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="72077-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="72077-124">-ResourceId</span></span>
<span data-ttu-id="72077-125">ResourceId della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="72077-125">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="72077-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72077-126">CommonParameters</span></span>
<span data-ttu-id="72077-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72077-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72077-128">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72077-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72077-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="72077-129">INPUTS</span></span>

### <span data-ttu-id="72077-130">System. String</span><span class="sxs-lookup"><span data-stu-id="72077-130">System.String</span></span>

## <span data-ttu-id="72077-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="72077-131">OUTPUTS</span></span>

### <span data-ttu-id="72077-132">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="72077-132">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="72077-133">Note</span><span class="sxs-lookup"><span data-stu-id="72077-133">NOTES</span></span>

## <span data-ttu-id="72077-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="72077-134">RELATED LINKS</span></span>

[<span data-ttu-id="72077-135">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="72077-135">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="72077-136">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="72077-136">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="72077-137">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="72077-137">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
