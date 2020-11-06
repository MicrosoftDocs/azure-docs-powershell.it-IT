---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: f5b2a3f66a1972edbf6d3e475f5f30fc9530929f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513184"
---
# <span data-ttu-id="1505a-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="1505a-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="1505a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1505a-102">SYNOPSIS</span></span>
<span data-ttu-id="1505a-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="1505a-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1505a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1505a-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1505a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1505a-105">DESCRIPTION</span></span>
<span data-ttu-id="1505a-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="1505a-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="1505a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1505a-107">EXAMPLES</span></span>

### <span data-ttu-id="1505a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1505a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="1505a-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="1505a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="1505a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1505a-110">PARAMETERS</span></span>

### <span data-ttu-id="1505a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="1505a-111">-Access</span></span>
<span data-ttu-id="1505a-112">Tipo di accesso della regola.</span><span class="sxs-lookup"><span data-stu-id="1505a-112">The access type of the rule.</span></span>
<span data-ttu-id="1505a-113">I valori possibili sono:' Allow ',' Deny '</span><span class="sxs-lookup"><span data-stu-id="1505a-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-114">-Community</span><span class="sxs-lookup"><span data-stu-id="1505a-114">-CommunityList</span></span>
<span data-ttu-id="1505a-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="1505a-115">The list of community value that route filter will filter on</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-116">-Force</span><span class="sxs-lookup"><span data-stu-id="1505a-116">-Force</span></span>
<span data-ttu-id="1505a-117">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="1505a-117">Do not ask for confirmation if you want to overrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1505a-118">-Name</span></span>
<span data-ttu-id="1505a-119">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="1505a-119">The name of the route filter rule</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-120">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1505a-120">-RouteFilter</span></span>
<span data-ttu-id="1505a-121">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="1505a-121">The RouteFilter</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSRouteFilter
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="1505a-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="1505a-123">Tipo di regola di filtro route della regola.</span><span class="sxs-lookup"><span data-stu-id="1505a-123">The route filter rule type of the rule.</span></span>
<span data-ttu-id="1505a-124">I valori possibili sono:' community '</span><span class="sxs-lookup"><span data-stu-id="1505a-124">Possible values are: 'Community'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1505a-125">-Confirm</span></span>
<span data-ttu-id="1505a-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1505a-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1505a-127">-WhatIf</span></span>
<span data-ttu-id="1505a-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1505a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1505a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1505a-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1505a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1505a-130">-DefaultProfile</span></span>
<span data-ttu-id="1505a-131">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1505a-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1505a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1505a-132">CommonParameters</span></span>
<span data-ttu-id="1505a-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1505a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1505a-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1505a-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1505a-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1505a-135">INPUTS</span></span>

### <span data-ttu-id="1505a-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1505a-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1505a-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1505a-137">OUTPUTS</span></span>

### <span data-ttu-id="1505a-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="1505a-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="1505a-139">Note</span><span class="sxs-lookup"><span data-stu-id="1505a-139">NOTES</span></span>

## <span data-ttu-id="1505a-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1505a-140">RELATED LINKS</span></span>

