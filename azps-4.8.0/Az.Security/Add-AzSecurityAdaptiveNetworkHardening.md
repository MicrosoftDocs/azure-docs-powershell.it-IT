---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188864"
---
# <span data-ttu-id="d335d-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="d335d-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="d335d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d335d-102">SYNOPSIS</span></span>
<span data-ttu-id="d335d-103">Impone le regole specificate per gli NSG elencati nella richiesta</span><span class="sxs-lookup"><span data-stu-id="d335d-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="d335d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d335d-104">SYNTAX</span></span>

### <span data-ttu-id="d335d-105">ResourceGroupLevelResource (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d335d-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d335d-106">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d335d-106">DESCRIPTION</span></span>
<span data-ttu-id="d335d-107">Gli indurimenti di rete adattivi vengono calcolati automaticamente da Azure Security Center, usano questo cmdlet per applicare le regole specificate nei NSG elencati nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="d335d-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="d335d-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d335d-108">EXAMPLES</span></span>

### <span data-ttu-id="d335d-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d335d-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="d335d-110">Impone le regole specificate per gli NSG elencati nella richiesta</span><span class="sxs-lookup"><span data-stu-id="d335d-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="d335d-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d335d-111">PARAMETERS</span></span>

### <span data-ttu-id="d335d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d335d-112">-DefaultProfile</span></span>
<span data-ttu-id="d335d-113">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d335d-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d335d-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="d335d-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="d335d-115">Nome della risorsa di protezione avanzata della rete adattiva.</span><span class="sxs-lookup"><span data-stu-id="d335d-115">The name of the Adaptive Network Hardening resource.</span></span>

```yaml
Type: System.String
Parameter Sets: AdaptiveNetworkHardeningResourceName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d335d-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d335d-116">-ResourceGroupName</span></span>
<span data-ttu-id="d335d-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d335d-117">Resource group name.</span></span>

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

### <span data-ttu-id="d335d-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="d335d-118">-ResourceName</span></span>
<span data-ttu-id="d335d-119">Nome risorsa.</span><span class="sxs-lookup"><span data-stu-id="d335d-119">Resource name.</span></span>

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

### <span data-ttu-id="d335d-120">-ResourceNamespace</span><span class="sxs-lookup"><span data-stu-id="d335d-120">-ResourceNamespace</span></span>
<span data-ttu-id="d335d-121">Lo spazio dei nomi della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d335d-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="d335d-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="d335d-122">-ResourceType</span></span>
<span data-ttu-id="d335d-123">Tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="d335d-123">The type of the resource.</span></span>

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

### <span data-ttu-id="d335d-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d335d-124">-SubscriptionId</span></span>
<span data-ttu-id="d335d-125">ID abbonamento di Azure.</span><span class="sxs-lookup"><span data-stu-id="d335d-125">Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d335d-126">-Regole</span><span class="sxs-lookup"><span data-stu-id="d335d-126">-Rules</span></span>
<span data-ttu-id="d335d-127">Le regole da applicare.</span><span class="sxs-lookup"><span data-stu-id="d335d-127">The rules to enforce.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule
Parameter Sets: Rules
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d335d-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="d335d-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="d335d-129">ID delle risorse di Azure dei gruppi di sicurezza di rete effettivi che verranno aggiornati con le regole di sicurezza create dalle regole di protezione avanzata della rete adattiva.</span><span class="sxs-lookup"><span data-stu-id="d335d-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

```yaml
Type: System.Collections.Generic.List<System.String>
Parameter Sets: NetworkSecurityGroups
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d335d-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d335d-130">-PassThru</span></span>
<span data-ttu-id="d335d-131">Restituire un valore che indica l'esito positivo o negativo</span><span class="sxs-lookup"><span data-stu-id="d335d-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="d335d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d335d-132">CommonParameters</span></span>
<span data-ttu-id="d335d-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d335d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d335d-134">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d335d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d335d-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d335d-135">INPUTS</span></span>

### <span data-ttu-id="d335d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="d335d-136">System.String</span></span>

### <span data-ttu-id="d335d-137">Microsoft. Azure. Commands. SecurityCenter. Models. AdaptiveNetworkHardenings. PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="d335d-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="d335d-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d335d-138">OUTPUTS</span></span>

### <span data-ttu-id="d335d-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d335d-139">System.Boolean</span></span>

## <span data-ttu-id="d335d-140">Note</span><span class="sxs-lookup"><span data-stu-id="d335d-140">NOTES</span></span>

## <span data-ttu-id="d335d-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d335d-141">RELATED LINKS</span></span>