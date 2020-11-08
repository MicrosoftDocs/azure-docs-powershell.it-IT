---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: 03e03de70f61672d1246ffeb8469efe0c04b3ea4
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032939"
---
# <span data-ttu-id="07f5a-101">New-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="07f5a-101">New-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="07f5a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="07f5a-102">SYNOPSIS</span></span>
<span data-ttu-id="07f5a-103">Crea un criterio firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="07f5a-103">Creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="07f5a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="07f5a-104">SYNTAX</span></span>

```
New-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String> -Location <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07f5a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="07f5a-105">DESCRIPTION</span></span>
<span data-ttu-id="07f5a-106">Il cmdlet **New-AzApplicationGatewayFirewallPolicy** crea un criterio del firewall di gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="07f5a-106">The **New-AzApplicationGatewayFirewallPolicy** cmdlet creates a application gateway firewall policy.</span></span>

## <span data-ttu-id="07f5a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="07f5a-107">EXAMPLES</span></span>

### <span data-ttu-id="07f5a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="07f5a-108">Example 1</span></span>
```powershell
PS C:\> $firewallPolicy = New-AzApplicationGatewayFirewallPolicy -Name wafResource1 -ResourceGroupName "rg1"  -Location  "westus" -CustomRule $customRule
```

<span data-ttu-id="07f5a-109">Questo comando crea un nuovo criterio firewall di gateway di applicazioni di Azure denominato "wafResource1" nel gruppo di risorse "RG1" in location "westus" con le regole personalizzate definite nella variabile $customRule</span><span class="sxs-lookup"><span data-stu-id="07f5a-109">This command creates a new Azure application gateway firewall policy named "wafResource1" in resource group "rg1" in location "westus" with custom rules defined in the $customRule variable</span></span>

## <span data-ttu-id="07f5a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="07f5a-110">PARAMETERS</span></span>

### <span data-ttu-id="07f5a-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07f5a-111">-AsJob</span></span>
<span data-ttu-id="07f5a-112">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="07f5a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07f5a-113">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="07f5a-113">-CustomRule</span></span>
<span data-ttu-id="07f5a-114">Elenco di CustomRules</span><span class="sxs-lookup"><span data-stu-id="07f5a-114">The list of CustomRules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07f5a-115">-DefaultProfile</span></span>
<span data-ttu-id="07f5a-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="07f5a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07f5a-117">-Force</span><span class="sxs-lookup"><span data-stu-id="07f5a-117">-Force</span></span>
<span data-ttu-id="07f5a-118">Non chiedere conferma se si vuole sovrascrivere una risorsa</span><span class="sxs-lookup"><span data-stu-id="07f5a-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="07f5a-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="07f5a-119">-Location</span></span>
<span data-ttu-id="07f5a-120">posizione.</span><span class="sxs-lookup"><span data-stu-id="07f5a-120">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-121">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="07f5a-121">-ManagedRule</span></span>
<span data-ttu-id="07f5a-122">Impostazione di regole gestite</span><span class="sxs-lookup"><span data-stu-id="07f5a-122">Managed Rule Setting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="07f5a-123">-Name</span></span>
<span data-ttu-id="07f5a-124">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="07f5a-124">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-125">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="07f5a-125">-PolicySetting</span></span>
<span data-ttu-id="07f5a-126">Impostazioni dei criteri per il firewall delle applicazioni Web</span><span class="sxs-lookup"><span data-stu-id="07f5a-126">Policy Settings for Web Application Firewall</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07f5a-127">-ResourceGroupName</span></span>
<span data-ttu-id="07f5a-128">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="07f5a-128">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="07f5a-129">-Tag</span></span>
<span data-ttu-id="07f5a-130">Hashtable che rappresenta i tag delle risorse.</span><span class="sxs-lookup"><span data-stu-id="07f5a-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07f5a-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="07f5a-131">-Confirm</span></span>
<span data-ttu-id="07f5a-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07f5a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07f5a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07f5a-133">-WhatIf</span></span>
<span data-ttu-id="07f5a-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07f5a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07f5a-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="07f5a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07f5a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07f5a-136">CommonParameters</span></span>
<span data-ttu-id="07f5a-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07f5a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07f5a-138">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="07f5a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07f5a-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="07f5a-139">INPUTS</span></span>

### <span data-ttu-id="07f5a-140">System. String</span><span class="sxs-lookup"><span data-stu-id="07f5a-140">System.String</span></span>

### <span data-ttu-id="07f5a-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallCustomRule []</span><span class="sxs-lookup"><span data-stu-id="07f5a-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallCustomRule[]</span></span>

### <span data-ttu-id="07f5a-142">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicySettings</span><span class="sxs-lookup"><span data-stu-id="07f5a-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicySettings</span></span>

### <span data-ttu-id="07f5a-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayFirewallPolicyManagedRules</span><span class="sxs-lookup"><span data-stu-id="07f5a-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFirewallPolicyManagedRules</span></span>

### <span data-ttu-id="07f5a-144">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="07f5a-144">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07f5a-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="07f5a-145">OUTPUTS</span></span>

### <span data-ttu-id="07f5a-146">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="07f5a-146">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="07f5a-147">Note</span><span class="sxs-lookup"><span data-stu-id="07f5a-147">NOTES</span></span>

## <span data-ttu-id="07f5a-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="07f5a-148">RELATED LINKS</span></span>
