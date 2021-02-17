---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Get-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Get-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: cd28e66466239bf7fb0478774c1914180d2ede42
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208346"
---
# <span data-ttu-id="429f1-101">Get-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="429f1-101">Get-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="429f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="429f1-102">SYNOPSIS</span></span>
<span data-ttu-id="429f1-103">Ottiene un elenco di risorse di Hardenings adattivi di rete nell'ambito di una risorsa estesa.</span><span class="sxs-lookup"><span data-stu-id="429f1-103">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="429f1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="429f1-104">SYNTAX</span></span>

### <span data-ttu-id="429f1-105">ResourceGroupLevelResource</span><span class="sxs-lookup"><span data-stu-id="429f1-105">ResourceGroupLevelResource</span></span>
```
Get-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```
## <span data-ttu-id="429f1-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="429f1-106">DESCRIPTION</span></span>
<span data-ttu-id="429f1-107">Gli hardening adattivi di rete vengono calcolati automaticamente da Centro sicurezza di Azure. Usare questo cmdlet per ottenere un elenco delle risorse di Hardening adattivi di rete nell'ambito di una risorsa estesa.</span><span class="sxs-lookup"><span data-stu-id="429f1-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to get a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

## <span data-ttu-id="429f1-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="429f1-108">EXAMPLES</span></span>

### <span data-ttu-id="429f1-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="429f1-109">Example 1</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```

<span data-ttu-id="429f1-110">Ottiene un elenco di risorse di Hardenings adattivi di rete nell'ambito di una risorsa estesa.</span><span class="sxs-lookup"><span data-stu-id="429f1-110">Gets a list of Adaptive Network Hardenings resources in scope of an extended resource.</span></span>

### <span data-ttu-id="429f1-111">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="429f1-111">Example 2</span></span>
```powershell
PS C:\> Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869

Id                                                                                                                                                                                                                      Name    Type                                         Properties
--                                                                                                                                                                                                                      ----    ----                                         ----------
/subscriptions/3eeab341-f466-499c-a8be-85427e154baf7612f869/resourceGroups/myService1/providers/Microsoft.Compute/virtualMachines/myResource1/providers/Microsoft.Security/adaptiveNetworkHardenings/default default Microsoft.Security/adaptiveNetworkHardenings Microsoft.Azure.Commands.SecurityCenter.Models…
```
<span data-ttu-id="429f1-112">Ottenere una singola risorsa Hardenings di rete adattiva</span><span class="sxs-lookup"><span data-stu-id="429f1-112">Get  a single Adaptive Network Hardenings resource</span></span>

## <span data-ttu-id="429f1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="429f1-113">PARAMETERS</span></span>

### <span data-ttu-id="429f1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429f1-114">-DefaultProfile</span></span>
<span data-ttu-id="429f1-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="429f1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="429f1-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="429f1-116">-ResourceGroupName</span></span>
<span data-ttu-id="429f1-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="429f1-117">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f1-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="429f1-118">-ResourceName</span></span>
<span data-ttu-id="429f1-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="429f1-119">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f1-120">-ResourceEnne</span><span class="sxs-lookup"><span data-stu-id="429f1-120">-ResourceNamespace</span></span>
<span data-ttu-id="429f1-121">Spazio dei nomi della risorsa.</span><span class="sxs-lookup"><span data-stu-id="429f1-121">The Namespace of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNamespace
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f1-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="429f1-122">-ResourceType</span></span>
<span data-ttu-id="429f1-123">Tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="429f1-123">The type of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceType
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f1-124">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="429f1-124">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="429f1-125">Il nome della risorsa Protezione avanzata rete adattiva.</span><span class="sxs-lookup"><span data-stu-id="429f1-125">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429f1-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="429f1-126">-SubscriptionId</span></span>
<span data-ttu-id="429f1-127">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="429f1-127">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: false
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="429f1-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429f1-128">CommonParameters</span></span>
<span data-ttu-id="429f1-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429f1-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429f1-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="429f1-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429f1-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="429f1-131">INPUTS</span></span>

### <span data-ttu-id="429f1-132">System.String</span><span class="sxs-lookup"><span data-stu-id="429f1-132">System.String</span></span>

## <span data-ttu-id="429f1-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="429f1-133">OUTPUTS</span></span>

### <span data-ttu-id="429f1-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span><span class="sxs-lookup"><span data-stu-id="429f1-134">Microsoft.Azure.Commands.Security.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardenings</span></span>

## <span data-ttu-id="429f1-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="429f1-135">NOTES</span></span>

## <span data-ttu-id="429f1-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="429f1-136">RELATED LINKS</span></span>