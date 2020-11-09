---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301416"
---
# <span data-ttu-id="d37f6-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d37f6-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="d37f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d37f6-102">SYNOPSIS</span></span>
<span data-ttu-id="d37f6-103">Aggiorna un criterio firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d37f6-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="d37f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d37f6-104">SYNTAX</span></span>

### <span data-ttu-id="d37f6-105">ByFactoryObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d37f6-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37f6-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="d37f6-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d37f6-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d37f6-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d37f6-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d37f6-108">DESCRIPTION</span></span>
<span data-ttu-id="d37f6-109">Il cmdlet **set-AzApplicationGatewayFirewallPolicy** aggiorna un criterio firewall di Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="d37f6-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="d37f6-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d37f6-110">EXAMPLES</span></span>

### <span data-ttu-id="d37f6-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d37f6-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="d37f6-112">Questo comando Aggiorna i criteri del firewall del gateway applicazione con le impostazioni nella variabile $AppGwFirewallPolicy e archivia il gateway aggiornato nella variabile $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="d37f6-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="d37f6-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d37f6-113">PARAMETERS</span></span>

### <span data-ttu-id="d37f6-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d37f6-114">-AsJob</span></span>
<span data-ttu-id="d37f6-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d37f6-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d37f6-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="d37f6-116">-CustomRule</span></span>
<span data-ttu-id="d37f6-117">Elenco di CustomRules</span><span class="sxs-lookup"><span data-stu-id="d37f6-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="d37f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d37f6-118">-DefaultProfile</span></span>
<span data-ttu-id="d37f6-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d37f6-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d37f6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d37f6-120">-InputObject</span></span>
<span data-ttu-id="d37f6-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d37f6-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="d37f6-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="d37f6-122">-ManagedRule</span></span>
<span data-ttu-id="d37f6-123">ManagedRules del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="d37f6-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="d37f6-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="d37f6-124">-Name</span></span>
<span data-ttu-id="d37f6-125">Nome del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="d37f6-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="d37f6-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="d37f6-126">-PolicySetting</span></span>
<span data-ttu-id="d37f6-127">PolicySettings del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="d37f6-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="d37f6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d37f6-128">-ResourceGroupName</span></span>
<span data-ttu-id="d37f6-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d37f6-129">The resource group name.</span></span>

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

### <span data-ttu-id="d37f6-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d37f6-130">-ResourceId</span></span>
<span data-ttu-id="d37f6-131">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="d37f6-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d37f6-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d37f6-132">-Confirm</span></span>
<span data-ttu-id="d37f6-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d37f6-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d37f6-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d37f6-134">-WhatIf</span></span>
<span data-ttu-id="d37f6-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d37f6-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d37f6-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d37f6-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d37f6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d37f6-137">CommonParameters</span></span>
<span data-ttu-id="d37f6-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d37f6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d37f6-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d37f6-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d37f6-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d37f6-140">INPUTS</span></span>

### <span data-ttu-id="d37f6-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d37f6-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="d37f6-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d37f6-142">OUTPUTS</span></span>

### <span data-ttu-id="d37f6-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="d37f6-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="d37f6-144">Note</span><span class="sxs-lookup"><span data-stu-id="d37f6-144">NOTES</span></span>

## <span data-ttu-id="d37f6-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d37f6-145">RELATED LINKS</span></span>
