---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzRouteFilterRuleConfig.md
ms.openlocfilehash: 6f8943fb4e75c96a97ad2b7f128d671a8be7c906
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93860433"
---
# <span data-ttu-id="ce3c6-101">New-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce3c6-101">New-AzRouteFilterRuleConfig</span></span>

## <span data-ttu-id="ce3c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce3c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ce3c6-103">Crea una regola di filtro route per un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-103">Creates a route filter rule for a route filter.</span></span>

## <span data-ttu-id="ce3c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce3c6-104">SYNTAX</span></span>

```
New-AzRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce3c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce3c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ce3c6-106">Il cmdlet New-AzRouteFilterRuleConfig crea una regola di filtro route per un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-106">The New-AzRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="ce3c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce3c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ce3c6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ce3c6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="ce3c6-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="ce3c6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="ce3c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce3c6-110">PARAMETERS</span></span>

### <span data-ttu-id="ce3c6-111">-Access</span><span class="sxs-lookup"><span data-stu-id="ce3c6-111">-Access</span></span>
<span data-ttu-id="ce3c6-112">Accesso per la regola di filtro route.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-112">Access for route filter rule.</span></span>
<span data-ttu-id="ce3c6-113">I valori validi sono allow o Deny.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="ce3c6-114">-Community</span><span class="sxs-lookup"><span data-stu-id="ce3c6-114">-CommunityList</span></span>
<span data-ttu-id="ce3c6-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="ce3c6-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="ce3c6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce3c6-116">-DefaultProfile</span></span>
<span data-ttu-id="ce3c6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce3c6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ce3c6-118">-Force</span></span>
<span data-ttu-id="ce3c6-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="ce3c6-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="ce3c6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ce3c6-120">-Name</span></span>
<span data-ttu-id="ce3c6-121">Specifica un nome per la regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="ce3c6-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="ce3c6-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="ce3c6-123">Tipo di regola filtro route.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="ce3c6-124">I valori validi sono: community</span><span class="sxs-lookup"><span data-stu-id="ce3c6-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="ce3c6-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ce3c6-125">-Confirm</span></span>
<span data-ttu-id="ce3c6-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce3c6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce3c6-127">-WhatIf</span></span>
<span data-ttu-id="ce3c6-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ce3c6-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce3c6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce3c6-130">CommonParameters</span></span>
<span data-ttu-id="ce3c6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce3c6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce3c6-132">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce3c6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce3c6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce3c6-133">INPUTS</span></span>

## <span data-ttu-id="ce3c6-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce3c6-134">OUTPUTS</span></span>

### <span data-ttu-id="ce3c6-135">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="ce3c6-135">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="ce3c6-136">Note</span><span class="sxs-lookup"><span data-stu-id="ce3c6-136">NOTES</span></span>
<span data-ttu-id="ce3c6-137">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="ce3c6-137">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="ce3c6-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce3c6-138">RELATED LINKS</span></span>

[<span data-ttu-id="ce3c6-139">Add-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce3c6-139">Add-AzRouteFilterRuleConfig</span></span>](./Add-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ce3c6-140">Get-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce3c6-140">Get-AzRouteFilterRuleConfig</span></span>](./Get-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ce3c6-141">Remove-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce3c6-141">Remove-AzRouteFilterRuleConfig</span></span>](./Remove-AzRouteFilterRuleConfig.md)

[<span data-ttu-id="ce3c6-142">Set-AzRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="ce3c6-142">Set-AzRouteFilterRuleConfig</span></span>](./Set-AzRouteFilterRuleConfig.md)

