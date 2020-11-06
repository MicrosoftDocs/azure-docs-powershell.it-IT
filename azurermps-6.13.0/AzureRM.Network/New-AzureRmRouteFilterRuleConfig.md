---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermroutefilterruleconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmRouteFilterRuleConfig.md
ms.openlocfilehash: 99ba414f68cc0d465a9bde0678bae9bff6628c1f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521330"
---
# <span data-ttu-id="8cdd6-101">New-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cdd6-101">New-AzureRmRouteFilterRuleConfig</span></span>

## <span data-ttu-id="8cdd6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8cdd6-102">SYNOPSIS</span></span>
<span data-ttu-id="8cdd6-103">Crea una regola di filtro route per un filtro di route.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-103">Creates a route filter rule for a route filter.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cdd6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8cdd6-104">SYNTAX</span></span>

```
New-AzureRmRouteFilterRuleConfig [-Force] -Name <String> -Access <String> -RouteFilterRuleType <String>
 -CommunityList <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8cdd6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8cdd6-105">DESCRIPTION</span></span>
<span data-ttu-id="8cdd6-106">Il cmdlet New-AzureRmRouteFilterRuleConfig crea una regola di filtro route per un filtro di route di Azure.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-106">The New-AzureRmRouteFilterRuleConfig cmdlet creates a route filter rule for an Azure route filter.</span></span>

## <span data-ttu-id="8cdd6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8cdd6-107">EXAMPLES</span></span>

### <span data-ttu-id="8cdd6-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8cdd6-108">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="8cdd6-109">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="8cdd6-109">{{ Add example description here }}</span></span>

## <span data-ttu-id="8cdd6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8cdd6-110">PARAMETERS</span></span>

### <span data-ttu-id="8cdd6-111">-Access</span><span class="sxs-lookup"><span data-stu-id="8cdd6-111">-Access</span></span>
<span data-ttu-id="8cdd6-112">Accesso per la regola di filtro route.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-112">Access for route filter rule.</span></span>
<span data-ttu-id="8cdd6-113">I valori validi sono allow o Deny.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-113">Valid values are Allow or Deny.</span></span>

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

### <span data-ttu-id="8cdd6-114">-Community</span><span class="sxs-lookup"><span data-stu-id="8cdd6-114">-CommunityList</span></span>
<span data-ttu-id="8cdd6-115">Elenco di valori della community a cui il filtro route verrà filtrato</span><span class="sxs-lookup"><span data-stu-id="8cdd6-115">The list of community value that route filter will filter on</span></span>

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

### <span data-ttu-id="8cdd6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cdd6-116">-DefaultProfile</span></span>
<span data-ttu-id="8cdd6-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8cdd6-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8cdd6-118">-Force</span></span>
<span data-ttu-id="8cdd6-119">Non chiedere conferma se si vuole usare una risorsa per un sovrarito</span><span class="sxs-lookup"><span data-stu-id="8cdd6-119">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="8cdd6-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="8cdd6-120">-Name</span></span>
<span data-ttu-id="8cdd6-121">Specifica un nome per la regola di filtro della route.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-121">Specifies a name for the route filter rule.</span></span>

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

### <span data-ttu-id="8cdd6-122">-RouteFilterRuleType</span><span class="sxs-lookup"><span data-stu-id="8cdd6-122">-RouteFilterRuleType</span></span>
<span data-ttu-id="8cdd6-123">Tipo di regola filtro route.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-123">Route Filter Rule Type.</span></span>
<span data-ttu-id="8cdd6-124">I valori validi sono: community</span><span class="sxs-lookup"><span data-stu-id="8cdd6-124">Valid values are: Community</span></span>

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

### <span data-ttu-id="8cdd6-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8cdd6-125">-Confirm</span></span>
<span data-ttu-id="8cdd6-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8cdd6-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cdd6-127">-WhatIf</span></span>
<span data-ttu-id="8cdd6-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8cdd6-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8cdd6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cdd6-130">CommonParameters</span></span>
<span data-ttu-id="8cdd6-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cdd6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cdd6-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cdd6-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cdd6-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8cdd6-133">INPUTS</span></span>

### <span data-ttu-id="8cdd6-134">Nessuno</span><span class="sxs-lookup"><span data-stu-id="8cdd6-134">None</span></span>

## <span data-ttu-id="8cdd6-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8cdd6-135">OUTPUTS</span></span>

### <span data-ttu-id="8cdd6-136">Microsoft. Azure. Commands. Network. Models. PSRouteFilterRule</span><span class="sxs-lookup"><span data-stu-id="8cdd6-136">Microsoft.Azure.Commands.Network.Models.PSRouteFilterRule</span></span>

## <span data-ttu-id="8cdd6-137">Note</span><span class="sxs-lookup"><span data-stu-id="8cdd6-137">NOTES</span></span>
<span data-ttu-id="8cdd6-138">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, Network, networking</span><span class="sxs-lookup"><span data-stu-id="8cdd6-138">Keywords: azure, azurerm, arm, resource, management, manager, network, networking</span></span>

## <span data-ttu-id="8cdd6-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8cdd6-139">RELATED LINKS</span></span>

[<span data-ttu-id="8cdd6-140">Add-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cdd6-140">Add-AzureRmRouteFilterRuleConfig</span></span>](./Add-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8cdd6-141">Get-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cdd6-141">Get-AzureRmRouteFilterRuleConfig</span></span>](./Get-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8cdd6-142">Remove-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cdd6-142">Remove-AzureRmRouteFilterRuleConfig</span></span>](./Remove-AzureRmRouteFilterRuleConfig.md)

[<span data-ttu-id="8cdd6-143">Set-AzureRmRouteFilterRuleConfig</span><span class="sxs-lookup"><span data-stu-id="8cdd6-143">Set-AzureRmRouteFilterRuleConfig</span></span>](./Set-AzureRmRouteFilterRuleConfig.md)

