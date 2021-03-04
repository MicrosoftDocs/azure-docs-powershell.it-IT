---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: e6b9c873110118392e9380418276bfa0f4d938a8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981709"
---
# <span data-ttu-id="203c8-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="203c8-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="203c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="203c8-102">SYNOPSIS</span></span>
<span data-ttu-id="203c8-103">Aggiorna i criteri firewall del gateway applicazione.</span><span class="sxs-lookup"><span data-stu-id="203c8-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="203c8-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="203c8-104">SYNTAX</span></span>

### <span data-ttu-id="203c8-105">ByFactoryObject (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="203c8-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="203c8-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="203c8-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="203c8-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="203c8-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="203c8-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="203c8-108">DESCRIPTION</span></span>
<span data-ttu-id="203c8-109">Il cmdlet **Set-AzApplicationGatewayFirewallPolicy** aggiorna i criteri firewall del gateway applicazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="203c8-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="203c8-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="203c8-110">EXAMPLES</span></span>

### <span data-ttu-id="203c8-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="203c8-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="203c8-112">Questo comando aggiorna i criteri firewall del gateway applicazione con le impostazioni nella variabile $AppGwFirewallPolicy e archivia il gateway aggiornato nella variabile $UpdatedAppGwFirewallPolicy variabile.</span><span class="sxs-lookup"><span data-stu-id="203c8-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="203c8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="203c8-113">PARAMETERS</span></span>

### <span data-ttu-id="203c8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="203c8-114">-AsJob</span></span>
<span data-ttu-id="203c8-115">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="203c8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="203c8-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="203c8-116">-CustomRule</span></span>
<span data-ttu-id="203c8-117">Elenco Delle Regole Personalizzate</span><span class="sxs-lookup"><span data-stu-id="203c8-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="203c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="203c8-118">-DefaultProfile</span></span>
<span data-ttu-id="203c8-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="203c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="203c8-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="203c8-120">-InputObject</span></span>
<span data-ttu-id="203c8-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="203c8-121">The applicationGatewayFirewallPolicy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="203c8-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="203c8-122">-ManagedRule</span></span>
<span data-ttu-id="203c8-123">ManagedRules dei criteri del firewall</span><span class="sxs-lookup"><span data-stu-id="203c8-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="203c8-124">-Name</span><span class="sxs-lookup"><span data-stu-id="203c8-124">-Name</span></span>
<span data-ttu-id="203c8-125">Nome del criterio del firewall.</span><span class="sxs-lookup"><span data-stu-id="203c8-125">The Firewall Policy Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203c8-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="203c8-126">-PolicySetting</span></span>
<span data-ttu-id="203c8-127">Policysettings del criterio del firewall</span><span class="sxs-lookup"><span data-stu-id="203c8-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="203c8-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="203c8-128">-ResourceGroupName</span></span>
<span data-ttu-id="203c8-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="203c8-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="203c8-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="203c8-130">-ResourceId</span></span>
<span data-ttu-id="203c8-131">ID della risorsa Azure.</span><span class="sxs-lookup"><span data-stu-id="203c8-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="203c8-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="203c8-132">-Confirm</span></span>
<span data-ttu-id="203c8-133">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="203c8-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="203c8-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="203c8-134">-WhatIf</span></span>
<span data-ttu-id="203c8-135">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="203c8-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="203c8-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="203c8-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="203c8-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="203c8-137">CommonParameters</span></span>
<span data-ttu-id="203c8-138">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="203c8-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="203c8-139">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="203c8-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="203c8-140">INPUT</span><span class="sxs-lookup"><span data-stu-id="203c8-140">INPUTS</span></span>

### <span data-ttu-id="203c8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="203c8-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="203c8-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="203c8-142">OUTPUTS</span></span>

### <span data-ttu-id="203c8-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="203c8-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="203c8-144">NOTE</span><span class="sxs-lookup"><span data-stu-id="203c8-144">NOTES</span></span>

## <span data-ttu-id="203c8-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="203c8-145">RELATED LINKS</span></span>
