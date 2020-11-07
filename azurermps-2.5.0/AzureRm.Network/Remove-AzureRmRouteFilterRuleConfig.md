---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: d11de748c8c86c974b45ac2f171b5eb54b97ee6f
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866464"
---
# <span data-ttu-id="8df14-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8df14-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8df14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8df14-102">SYNOPSIS</span></span>
<span data-ttu-id="8df14-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="8df14-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8df14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8df14-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8df14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8df14-105">DESCRIPTION</span></span>
<span data-ttu-id="8df14-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="8df14-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8df14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8df14-107">EXAMPLES</span></span>

### <span data-ttu-id="8df14-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8df14-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8df14-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="8df14-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8df14-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8df14-110">PARAMETERS</span></span>

### <span data-ttu-id="8df14-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8df14-111">-DefaultProfile</span></span>
<span data-ttu-id="8df14-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8df14-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df14-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8df14-113">-Force</span></span>
<span data-ttu-id="8df14-114">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="8df14-114">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df14-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="8df14-115">-Name</span></span>
<span data-ttu-id="8df14-116">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="8df14-116">The name of the route filter rule</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df14-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8df14-117">-RouteFilter</span></span>
<span data-ttu-id="8df14-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="8df14-118">The RouteFilter</span></span>

```yaml
Type: PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8df14-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8df14-119">-Confirm</span></span>
<span data-ttu-id="8df14-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8df14-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df14-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8df14-121">-WhatIf</span></span>
<span data-ttu-id="8df14-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8df14-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8df14-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8df14-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8df14-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8df14-124">CommonParameters</span></span>
<span data-ttu-id="8df14-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8df14-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8df14-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8df14-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8df14-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8df14-127">INPUTS</span></span>

### <span data-ttu-id="8df14-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="8df14-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="8df14-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8df14-129">OUTPUTS</span></span>

### <span data-ttu-id="8df14-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8df14-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8df14-131">Note</span><span class="sxs-lookup"><span data-stu-id="8df14-131">NOTES</span></span>

## <span data-ttu-id="8df14-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8df14-132">RELATED LINKS</span></span>

