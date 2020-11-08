---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFirewallPolicy.md
ms.openlocfilehash: bc869f6bccd2b87927b0cbe3b73cedc1999a261c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032319"
---
# <span data-ttu-id="f7d50-101">Set-AzApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7d50-101">Set-AzApplicationGatewayFirewallPolicy</span></span>

## <span data-ttu-id="f7d50-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7d50-102">SYNOPSIS</span></span>
<span data-ttu-id="f7d50-103">Aggiorna un criterio firewall di Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7d50-103">Updates an application gateway firewall policy.</span></span>

## <span data-ttu-id="f7d50-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7d50-104">SYNTAX</span></span>

### <span data-ttu-id="f7d50-105">ByFactoryObject (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f7d50-105">ByFactoryObject (Default)</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -InputObject <PSApplicationGatewayWebApplicationFirewallPolicy>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d50-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="f7d50-106">ByFactoryName</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -Name <String> -ResourceGroupName <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7d50-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d50-107">ByResourceId</span></span>
```
Set-AzApplicationGatewayFirewallPolicy -ResourceId <String>
 [-CustomRule <PSApplicationGatewayFirewallCustomRule[]>]
 [-PolicySetting <PSApplicationGatewayFirewallPolicySettings>]
 [-ManagedRule <PSApplicationGatewayFirewallPolicyManagedRules>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7d50-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7d50-108">DESCRIPTION</span></span>
<span data-ttu-id="f7d50-109">Il cmdlet **set-AzApplicationGatewayFirewallPolicy** aggiorna un criterio firewall di Azure Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f7d50-109">The **Set-AzApplicationGatewayFirewallPolicy** cmdlet updates an Azure application gateway firewall policy.</span></span>

## <span data-ttu-id="f7d50-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7d50-110">EXAMPLES</span></span>

### <span data-ttu-id="f7d50-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7d50-111">Example 1</span></span>
```powershell
PS C:\> $UpdatedAppGwFirewallPolicy = Set-AzApplicationGatewayFirewallPolicy -ApplicationGateway $AppGwFirewallPolicy
```

<span data-ttu-id="f7d50-112">Questo comando Aggiorna i criteri del firewall del gateway applicazione con le impostazioni nella variabile $AppGwFirewallPolicy e archivia il gateway aggiornato nella variabile $UpdatedAppGwFirewallPolicy.</span><span class="sxs-lookup"><span data-stu-id="f7d50-112">This command updates the application gateway firewall policy with settings in the $AppGwFirewallPolicy variable and stores the updated gateway in the $UpdatedAppGwFirewallPolicy variable.</span></span>

## <span data-ttu-id="f7d50-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7d50-113">PARAMETERS</span></span>

### <span data-ttu-id="f7d50-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f7d50-114">-AsJob</span></span>
<span data-ttu-id="f7d50-115">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f7d50-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f7d50-116">-CustomRule</span><span class="sxs-lookup"><span data-stu-id="f7d50-116">-CustomRule</span></span>
<span data-ttu-id="f7d50-117">Elenco di CustomRules</span><span class="sxs-lookup"><span data-stu-id="f7d50-117">The list of CustomRules</span></span>

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

### <span data-ttu-id="f7d50-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7d50-118">-DefaultProfile</span></span>
<span data-ttu-id="f7d50-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d50-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7d50-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7d50-120">-InputObject</span></span>
<span data-ttu-id="f7d50-121">ApplicationGatewayFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7d50-121">The applicationGatewayFirewallPolicy</span></span>

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

### <span data-ttu-id="f7d50-122">-ManagedRule</span><span class="sxs-lookup"><span data-stu-id="f7d50-122">-ManagedRule</span></span>
<span data-ttu-id="f7d50-123">ManagedRules del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="f7d50-123">ManagedRules of the firewall policy</span></span>

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

### <span data-ttu-id="f7d50-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="f7d50-124">-Name</span></span>
<span data-ttu-id="f7d50-125">Nome del criterio firewall.</span><span class="sxs-lookup"><span data-stu-id="f7d50-125">The Firewall Policy Name.</span></span>

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

### <span data-ttu-id="f7d50-126">-PolicySetting</span><span class="sxs-lookup"><span data-stu-id="f7d50-126">-PolicySetting</span></span>
<span data-ttu-id="f7d50-127">PolicySettings del criterio firewall</span><span class="sxs-lookup"><span data-stu-id="f7d50-127">Policysettings of the firewall policy</span></span>

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

### <span data-ttu-id="f7d50-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7d50-128">-ResourceGroupName</span></span>
<span data-ttu-id="f7d50-129">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7d50-129">The resource group name.</span></span>

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

### <span data-ttu-id="f7d50-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f7d50-130">-ResourceId</span></span>
<span data-ttu-id="f7d50-131">ID risorsa di Azure.</span><span class="sxs-lookup"><span data-stu-id="f7d50-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f7d50-132">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f7d50-132">-Confirm</span></span>
<span data-ttu-id="f7d50-133">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7d50-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7d50-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7d50-134">-WhatIf</span></span>
<span data-ttu-id="f7d50-135">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7d50-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7d50-136">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f7d50-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7d50-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7d50-137">CommonParameters</span></span>
<span data-ttu-id="f7d50-138">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7d50-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7d50-139">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7d50-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7d50-140">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7d50-140">INPUTS</span></span>

### <span data-ttu-id="f7d50-141">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7d50-141">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="f7d50-142">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7d50-142">OUTPUTS</span></span>

### <span data-ttu-id="f7d50-143">Microsoft. Azure. Commands. Network. Models. PSApplicationGatewayWebApplicationFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="f7d50-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallPolicy</span></span>

## <span data-ttu-id="f7d50-144">Note</span><span class="sxs-lookup"><span data-stu-id="f7d50-144">NOTES</span></span>

## <span data-ttu-id="f7d50-145">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7d50-145">RELATED LINKS</span></span>
