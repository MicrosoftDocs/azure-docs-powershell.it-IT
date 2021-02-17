---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Security.dll-Help.xml
Module Name: Az.Security
online version: https://docs.microsoft.com/en-us/powershell/module/az.security/Add-AzSecurityAdaptiveNetworkHardening
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Security/Security/help/Add-AzSecurityAdaptiveNetworkHardening.md
ms.openlocfilehash: daccafa4d0100d333d2e686e8b03bb21d8a38736
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178663"
---
# <span data-ttu-id="25e7f-101">Add-AzSecurityAdaptiveNetworkHardening</span><span class="sxs-lookup"><span data-stu-id="25e7f-101">Add-AzSecurityAdaptiveNetworkHardening</span></span>

## <span data-ttu-id="25e7f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="25e7f-103">Applica le regole fornite ai server dei criteri di rete elencati nella richiesta</span><span class="sxs-lookup"><span data-stu-id="25e7f-103">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="25e7f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="25e7f-104">SYNTAX</span></span>

### <span data-ttu-id="25e7f-105">ResourceGroupLevelResource (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="25e7f-105">ResourceGroupLevelResource (Default)</span></span>
```
Add-AzSecurityAdaptiveNetworkHardening [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="25e7f-106">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="25e7f-106">DESCRIPTION</span></span>
<span data-ttu-id="25e7f-107">Le hardening adattive di rete vengono calcolate automaticamente da Centro sicurezza di Azure. Usare questo cmdlet per applicare le regole fornite nei gruppi NSG elencati nella richiesta.</span><span class="sxs-lookup"><span data-stu-id="25e7f-107">Adaptive Network Hardenings are automatically calculated by Azure Security Center, use this cmdlet to enforces the given rules on the NSG(s) listed in the request.</span></span>

## <span data-ttu-id="25e7f-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="25e7f-108">EXAMPLES</span></span>

### <span data-ttu-id="25e7f-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="25e7f-109">Example 1</span></span>
```powershell
PS C:\> $anh = Get-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines | Select -First 1
PS C:\> Add-AzSecurityAdaptiveNetworkHardening -AdaptiveNetworkHardeningResourceName default -ResourceGroupName myService1 -ResourceName myResource1 -ResourceNamespace Microsoft.Compute -ResourceType virtualMachines -SubscriptionId 3eeab341-f466-499c-a8be-85427e154baf7612f869 -Rules $anh.Properties.Rules -NetworkSecurityGroups $anh.Properties.EffectiveNetworkSecurityGroups[0].NetworkSecurityGroups

True
```
<span data-ttu-id="25e7f-110">Applica le regole fornite ai server dei criteri di rete elencati nella richiesta</span><span class="sxs-lookup"><span data-stu-id="25e7f-110">Enforces the given rules on the NSG(s) listed in the request</span></span>

## <span data-ttu-id="25e7f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e7f-111">PARAMETERS</span></span>

### <span data-ttu-id="25e7f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e7f-112">-DefaultProfile</span></span>
<span data-ttu-id="25e7f-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="25e7f-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="25e7f-114">-AdaptiveNetworkHardeningResourceName</span><span class="sxs-lookup"><span data-stu-id="25e7f-114">-AdaptiveNetworkHardeningResourceName</span></span>
<span data-ttu-id="25e7f-115">Il nome della risorsa Protezione avanzata rete adattiva.</span><span class="sxs-lookup"><span data-stu-id="25e7f-115">The name of the Adaptive Network Hardening resource.</span></span>

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

### <span data-ttu-id="25e7f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e7f-116">-ResourceGroupName</span></span>
<span data-ttu-id="25e7f-117">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="25e7f-117">Resource group name.</span></span>

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

### <span data-ttu-id="25e7f-118">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="25e7f-118">-ResourceName</span></span>
<span data-ttu-id="25e7f-119">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="25e7f-119">Resource name.</span></span>

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

### <span data-ttu-id="25e7f-120">-ResourceEnne</span><span class="sxs-lookup"><span data-stu-id="25e7f-120">-ResourceNamespace</span></span>
<span data-ttu-id="25e7f-121">Spazio dei nomi della risorsa.</span><span class="sxs-lookup"><span data-stu-id="25e7f-121">The Namespace of the resource.</span></span>

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

### <span data-ttu-id="25e7f-122">-ResourceType</span><span class="sxs-lookup"><span data-stu-id="25e7f-122">-ResourceType</span></span>
<span data-ttu-id="25e7f-123">Tipo della risorsa.</span><span class="sxs-lookup"><span data-stu-id="25e7f-123">The type of the resource.</span></span>

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

### <span data-ttu-id="25e7f-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="25e7f-124">-SubscriptionId</span></span>
<span data-ttu-id="25e7f-125">ID sottoscrizione Azure.</span><span class="sxs-lookup"><span data-stu-id="25e7f-125">Azure subscription ID.</span></span>

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

### <span data-ttu-id="25e7f-126">-Rules</span><span class="sxs-lookup"><span data-stu-id="25e7f-126">-Rules</span></span>
<span data-ttu-id="25e7f-127">Regole da applicare.</span><span class="sxs-lookup"><span data-stu-id="25e7f-127">The rules to enforce.</span></span>

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

### <span data-ttu-id="25e7f-128">-NetworkSecurityGroups</span><span class="sxs-lookup"><span data-stu-id="25e7f-128">-NetworkSecurityGroups</span></span>
<span data-ttu-id="25e7f-129">ID delle risorse di Azure dei gruppi di sicurezza di rete effettivi che verranno aggiornati con le regole di sicurezza create dalle regole di protezione avanzata di rete adattiva.</span><span class="sxs-lookup"><span data-stu-id="25e7f-129">The Azure resource IDs of the effective network security groups that will be updated with the created security rules from the Adaptive Network Hardening rules.</span></span>

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

### <span data-ttu-id="25e7f-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25e7f-130">-PassThru</span></span>
<span data-ttu-id="25e7f-131">Restituisce un valore che indica un'operazione riuscita o non riuscita</span><span class="sxs-lookup"><span data-stu-id="25e7f-131">Return a value indicating success or failure</span></span>

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

### <span data-ttu-id="25e7f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e7f-132">CommonParameters</span></span>
<span data-ttu-id="25e7f-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e7f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e7f-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25e7f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e7f-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="25e7f-135">INPUTS</span></span>

### <span data-ttu-id="25e7f-136">System.String</span><span class="sxs-lookup"><span data-stu-id="25e7f-136">System.String</span></span>

### <span data-ttu-id="25e7f-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span><span class="sxs-lookup"><span data-stu-id="25e7f-137">Microsoft.Azure.Commands.SecurityCenter.Models.AdaptiveNetworkHardenings.PSSecurityAdaptiveNetworkHardeningsRule</span></span>

## <span data-ttu-id="25e7f-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="25e7f-138">OUTPUTS</span></span>

### <span data-ttu-id="25e7f-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25e7f-139">System.Boolean</span></span>

## <span data-ttu-id="25e7f-140">NOTE</span><span class="sxs-lookup"><span data-stu-id="25e7f-140">NOTES</span></span>

## <span data-ttu-id="25e7f-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="25e7f-141">RELATED LINKS</span></span>