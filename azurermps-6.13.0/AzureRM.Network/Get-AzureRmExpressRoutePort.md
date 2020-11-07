---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmExpressRoutePort.md
ms.openlocfilehash: 36c15c9a0bfae9bbf3a14f59877d23c1c8778163
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688086"
---
# <span data-ttu-id="a0de4-101">Get-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0de4-101">Get-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="a0de4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a0de4-102">SYNOPSIS</span></span>
<span data-ttu-id="a0de4-103">Ottiene una risorsa di Azure ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0de4-103">Gets an Azure ExpressRoutePort resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0de4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a0de4-104">SYNTAX</span></span>

### <span data-ttu-id="a0de4-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a0de4-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmExpressRoutePort [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0de4-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0de4-106">ResourceIdParameterSet</span></span>
```
Get-AzureRmExpressRoutePort -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a0de4-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a0de4-107">DESCRIPTION</span></span>
<span data-ttu-id="a0de4-108">Il cmdlet **Get-AzureRmExpressRoutePort** viene usato per recuperare un oggetto ExpressRoutePort dall'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a0de4-108">The **Get-AzureRmExpressRoutePort** cmdlet is used to retrieve an ExpressRoutePort object from your subscription.</span></span> <span data-ttu-id="a0de4-109">L'oggetto expressrouteport restituito può essere usato come input per altri cmdlet che operano in ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0de4-109">The expressrouteport object returned can be used as input to other cmdlets that operate on ExpressRoutePort.</span></span>

## <span data-ttu-id="a0de4-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a0de4-110">EXAMPLES</span></span>

### <span data-ttu-id="a0de4-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a0de4-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="a0de4-112">Ottiene l'oggetto ExpressRoutePort con il nome $PortName nel gruppo di risorse $rg nell'abbonamento.</span><span class="sxs-lookup"><span data-stu-id="a0de4-112">Gets the ExpressRoutePort object with name $PortName in resource group $rg in your subscription.</span></span>

### <span data-ttu-id="a0de4-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a0de4-113">Example 2</span></span>
```powershell
PS C:\> Get-AzureRmExpressRoutePort -ResourceId $id
```

<span data-ttu-id="a0de4-114">Ottiene l'oggetto ExpressRoutePort con ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="a0de4-114">Gets the ExpressRoutePort object with ResourceId $id.</span></span> 

## <span data-ttu-id="a0de4-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a0de4-115">PARAMETERS</span></span>

### <span data-ttu-id="a0de4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0de4-116">-DefaultProfile</span></span>
<span data-ttu-id="a0de4-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a0de4-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a0de4-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="a0de4-118">-Name</span></span>
<span data-ttu-id="a0de4-119">Il nome del ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0de4-119">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0de4-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0de4-120">-ResourceGroupName</span></span>
<span data-ttu-id="a0de4-121">Nome del gruppo di risorse di ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="a0de4-121">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0de4-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a0de4-122">-ResourceId</span></span>
<span data-ttu-id="a0de4-123">ResourceId della porta di route espressa.</span><span class="sxs-lookup"><span data-stu-id="a0de4-123">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="a0de4-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0de4-124">CommonParameters</span></span>
<span data-ttu-id="a0de4-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0de4-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0de4-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0de4-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0de4-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a0de4-127">INPUTS</span></span>

### <span data-ttu-id="a0de4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a0de4-128">System.String</span></span>

## <span data-ttu-id="a0de4-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a0de4-129">OUTPUTS</span></span>

### <span data-ttu-id="a0de4-130">Microsoft. Azure. Commands. Network. Models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="a0de4-130">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="a0de4-131">Note</span><span class="sxs-lookup"><span data-stu-id="a0de4-131">NOTES</span></span>

## <span data-ttu-id="a0de4-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a0de4-132">RELATED LINKS</span></span>
