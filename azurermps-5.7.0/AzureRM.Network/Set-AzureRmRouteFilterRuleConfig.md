---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 0725b75c15fa6ab977d0b829a1928943bfd9ed31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520680"
---
# <span data-ttu-id="acf6e-101">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="acf6e-101">Set-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="acf6e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="acf6e-102">SYNOPSIS</span></span>
<span data-ttu-id="acf6e-103">{{Fill in Sinossi}}</span><span class="sxs-lookup"><span data-stu-id="acf6e-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acf6e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="acf6e-104">SYNTAX</span></span>

```
Set-AzureRmRouteFilterRuleConfig -RouteFilter <PSRouteFilter> [-Force] -Name <String> -Access <String>
 -RouteFilterRuleType <String> -CommunityList <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="acf6e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="acf6e-105">DESCRIPTION</span></span>
<span data-ttu-id="acf6e-106">{{Fill nella descrizione}}</span><span class="sxs-lookup"><span data-stu-id="acf6e-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="acf6e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="acf6e-107">EXAMPLES</span></span>

### <span data-ttu-id="acf6e-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="acf6e-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="acf6e-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="acf6e-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="acf6e-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="acf6e-110">PARAMETERS</span></span>

### <span data-ttu-id="acf6e-111">-Access</span><span class="sxs-lookup"><span data-stu-id="acf6e-111">-Access</span></span>
<span data-ttu-id="acf6e-112">Tipo di accesso della regola.</span><span class="sxs-lookup"><span data-stu-id="acf6e-112">The access type of the rule.</span></span>
<span data-ttu-id="acf6e-113">I valori possibili sono:' Allow ',' Deny '</span><span class="sxs-lookup"><span data-stu-id="acf6e-113">Possible values are: 'Allow', 'Deny'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Allow, Deny

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf6e-114">-Community</span><span class="sxs-lookup"><span data-stu-id="acf6e-114">-CommunityList</span></span>
<span data-ttu-id="acf6e-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="acf6e-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="acf6e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acf6e-116">-DefaultProfile</span></span>
<span data-ttu-id="acf6e-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="acf6e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acf6e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="acf6e-118">-Force</span></span>
<span data-ttu-id="acf6e-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="acf6e-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="acf6e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="acf6e-120">-Name</span></span>
<span data-ttu-id="acf6e-121">Nome della regola di filtro route</span><span class="sxs-lookup"><span data-stu-id="acf6e-121">The name of the route filter rule</span></span>

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

### <span data-ttu-id="acf6e-122">-RouteFilter</span><span class="sxs-lookup"><span data-stu-id="acf6e-122">-RouteFilter</span></span>
<span data-ttu-id="acf6e-123">RouteFilter</span><span class="sxs-lookup"><span data-stu-id="acf6e-123">The RouteFilter</span></span>

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

### <span data-ttu-id="acf6e-124">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="acf6e-124">-RouteFilterRuleType</span></span>
<span data-ttu-id="acf6e-125">Tipo di regola di filtro route della regola.</span><span class="sxs-lookup"><span data-stu-id="acf6e-125">The route filter rule type of the rule.</span></span>
<span data-ttu-id="acf6e-126">I valori possibili sono:' community '</span><span class="sxs-lookup"><span data-stu-id="acf6e-126">Possible values are: 'Community'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Community

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acf6e-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="acf6e-127">-Confirm</span></span>
<span data-ttu-id="acf6e-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="acf6e-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acf6e-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acf6e-129">-WhatIf</span></span>
<span data-ttu-id="acf6e-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acf6e-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="acf6e-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="acf6e-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acf6e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acf6e-132">CommonParameters</span></span>
<span data-ttu-id="acf6e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acf6e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acf6e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acf6e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acf6e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="acf6e-135">INPUTS</span></span>

### <span data-ttu-id="acf6e-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="acf6e-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="acf6e-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="acf6e-137">OUTPUTS</span></span>

### <span data-ttu-id="acf6e-138">Microsoft. Azure. Commands. Network. Models. PSRouteFilter</span><span class="sxs-lookup"><span data-stu-id="acf6e-138">Microsoft.Azure.Commands.Network.Models.PSRouteFilter</span></span>

## <span data-ttu-id="acf6e-139">Note</span><span class="sxs-lookup"><span data-stu-id="acf6e-139">NOTES</span></span>

## <span data-ttu-id="acf6e-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="acf6e-140">RELATED LINKS</span></span>

