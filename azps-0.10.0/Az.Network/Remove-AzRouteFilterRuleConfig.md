---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Remove-AzRouteFilterRuleConfig.md
ms.openlocfilehash: bcb0d59c564087e02cd152c1ae76f38c91f33e80
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862926"
---
# <span data-ttu-id="ed038-101">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ed038-101">Remove-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ed038-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ed038-102">SYNOPSIS</span></span>
<span data-ttu-id="ed038-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="ed038-103">{{Fill in the Synopsis}}</span></span>

## <span data-ttu-id="ed038-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ed038-104">SYNTAX</span></span>

```
Remove-AzRouteFilterRuleConfig -Name <String> -RouteFilter <PSRouteFilter> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed038-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ed038-105">DESCRIPTION</span></span>
<span data-ttu-id="ed038-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="ed038-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="ed038-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ed038-107">EXAMPLES</span></span>

### <span data-ttu-id="ed038-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ed038-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ed038-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ed038-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ed038-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ed038-110">PARAMETERS</span></span>

### <span data-ttu-id="ed038-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed038-111">-DefaultProfile</span></span>
<span data-ttu-id="ed038-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ed038-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed038-113">-Force</span><span class="sxs-lookup"><span data-stu-id="ed038-113">-Force</span></span>
<span data-ttu-id="ed038-114">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="ed038-114">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ed038-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="ed038-115">-Name</span></span>
<span data-ttu-id="ed038-116">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="ed038-116">The name of the route filter rule</span></span>

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

### <span data-ttu-id="ed038-117">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed038-117">-RouteFilter</span></span>
<span data-ttu-id="ed038-118">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed038-118">The RouteFilter</span></span>

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

### <span data-ttu-id="ed038-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ed038-119">-Confirm</span></span>
<span data-ttu-id="ed038-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed038-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed038-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed038-121">-WhatIf</span></span>
<span data-ttu-id="ed038-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed038-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed038-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ed038-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed038-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed038-124">CommonParameters</span></span>
<span data-ttu-id="ed038-125">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed038-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed038-126">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed038-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed038-127">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ed038-127">INPUTS</span></span>

### <span data-ttu-id="ed038-128">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="ed038-128">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="ed038-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ed038-129">OUTPUTS</span></span>

### <span data-ttu-id="ed038-130">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ed038-130">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ed038-131">Note</span><span class="sxs-lookup"><span data-stu-id="ed038-131">NOTES</span></span>

## <span data-ttu-id="ed038-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ed038-132">RELATED LINKS</span></span>

