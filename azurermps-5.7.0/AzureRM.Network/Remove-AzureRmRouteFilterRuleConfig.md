---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 59a8ff1467bf70cea2eafe2117850d3423236f18
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687634"
---
# <span data-ttu-id="4b8f0-101">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="4b8f0-101">Remove-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="4b8f0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b8f0-102">SYNOPSIS</span></span>
<span data-ttu-id="4b8f0-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="4b8f0-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4b8f0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b8f0-104">SYNTAX</span></span>

```
Remove-AzureRmRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b8f0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b8f0-105">DESCRIPTION</span></span>
<span data-ttu-id="4b8f0-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="4b8f0-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="4b8f0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b8f0-107">EXAMPLES</span></span>

### <span data-ttu-id="4b8f0-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4b8f0-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="4b8f0-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="4b8f0-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="4b8f0-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b8f0-110">PARAMETERS</span></span>

### <span data-ttu-id="4b8f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b8f0-111">-DefaultProfile</span></span>
<span data-ttu-id="4b8f0-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4b8f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4b8f0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4b8f0-113">-Force</span></span>
<span data-ttu-id="4b8f0-114">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="4b8f0-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="4b8f0-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="4b8f0-115">-Name</span></span>
<span data-ttu-id="4b8f0-116">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="4b8f0-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="4b8f0-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b8f0-117">-RouteFilter</span></span>
<span data-ttu-id="4b8f0-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b8f0-118">The RouteFilter</span></span>

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

### <span data-ttu-id="4b8f0-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b8f0-119">-Confirm</span></span>
<span data-ttu-id="4b8f0-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b8f0-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b8f0-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b8f0-121">-WhatIf</span></span>
<span data-ttu-id="4b8f0-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b8f0-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4b8f0-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b8f0-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b8f0-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b8f0-124">CommonParameters</span></span>
<span data-ttu-id="4b8f0-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b8f0-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b8f0-126">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b8f0-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b8f0-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b8f0-127">INPUTS</span></span>

### <span data-ttu-id="4b8f0-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="4b8f0-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="4b8f0-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b8f0-129">OUTPUTS</span></span>

### <span data-ttu-id="4b8f0-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="4b8f0-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="4b8f0-131">Note</span><span class="sxs-lookup"><span data-stu-id="4b8f0-131">NOTES</span></span>

## <span data-ttu-id="4b8f0-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b8f0-132">RELATED LINKS</span></span>

