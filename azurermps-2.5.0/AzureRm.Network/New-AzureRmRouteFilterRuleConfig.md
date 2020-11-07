---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
ms.openlocfilehash: 2309d49dcd91ddefbcbe0e40379a759d50d5ba2a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866872"
---
# <span data-ttu-id="8000a-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8000a-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8000a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8000a-102">SYNOPSIS</span></span>
<span data-ttu-id="8000a-103">Crea una regola di filtro route per un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="8000a-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8000a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8000a-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8000a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8000a-105">DESCRIPTION</span></span>
<span data-ttu-id="8000a-106">Il cmdlet New-AzureRmRouteFilterRuleConfig crea una regola di filtro route per un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="8000a-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="8000a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8000a-107">EXAMPLES</span></span>

### <span data-ttu-id="8000a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8000a-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8000a-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="8000a-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8000a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8000a-110">PARAMETERS</span></span>

### <span data-ttu-id="8000a-111">-Access</span><span class="sxs-lookup"><span data-stu-id="8000a-111">-Access</span></span>
<span data-ttu-id="8000a-112">Accesso per la regola di filtro route.</span><span class="sxs-lookup"><span data-stu-id="8000a-112">Access for route filter rule.</span></span>
<span data-ttu-id="8000a-113">I valori validi sono allow o Deny.</span><span class="sxs-lookup"><span data-stu-id="8000a-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="8000a-114">-Community</span><span class="sxs-lookup"><span data-stu-id="8000a-114">-CommunityList</span></span>
<span data-ttu-id="8000a-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="8000a-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="8000a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8000a-116">-DefaultProfile</span></span>
<span data-ttu-id="8000a-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8000a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8000a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8000a-118">-Force</span></span>
<span data-ttu-id="8000a-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="8000a-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8000a-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8000a-120">-Name</span></span>
<span data-ttu-id="8000a-121">Specifica un nome per la regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="8000a-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="8000a-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="8000a-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="8000a-123">Tipo di regola filtro route.</span><span class="sxs-lookup"><span data-stu-id="8000a-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="8000a-124">I valori validi sono: community</span><span class="sxs-lookup"><span data-stu-id="8000a-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="8000a-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8000a-125">-Confirm</span></span>
<span data-ttu-id="8000a-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8000a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8000a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8000a-127">-WhatIf</span></span>
<span data-ttu-id="8000a-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8000a-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8000a-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8000a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8000a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8000a-130">CommonParameters</span></span>
<span data-ttu-id="8000a-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8000a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8000a-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8000a-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8000a-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8000a-133">INPUTS</span></span>

## <span data-ttu-id="8000a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8000a-134">OUTPUTS</span></span>

### <span data-ttu-id="8000a-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8000a-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8000a-136">Note</span><span class="sxs-lookup"><span data-stu-id="8000a-136">NOTES</span></span>
<span data-ttu-id="8000a-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="8000a-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8000a-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8000a-138">RELATED LINKS</span></span>

[<span data-ttu-id="8000a-139">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8000a-139">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8000a-140">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8000a-140">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8000a-141">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8000a-141">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8000a-142">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8000a-142">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

