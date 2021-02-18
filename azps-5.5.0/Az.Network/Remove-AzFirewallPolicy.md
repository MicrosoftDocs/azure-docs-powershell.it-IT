---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206618"
---
# <span data-ttu-id="cad6d-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cad6d-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="cad6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cad6d-102">SYNOPSIS</span></span>
<span data-ttu-id="cad6d-103">Rimuove un criterio del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="cad6d-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="cad6d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cad6d-104">SYNTAX</span></span>

### <span data-ttu-id="cad6d-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad6d-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad6d-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad6d-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cad6d-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="cad6d-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cad6d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="cad6d-108">DESCRIPTION</span></span>
<span data-ttu-id="cad6d-109">Il cmdlet **Remove-AzFirewallPolicy** rimuove un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="cad6d-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="cad6d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cad6d-110">EXAMPLES</span></span>

### <span data-ttu-id="cad6d-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="cad6d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="cad6d-112">Questo esempio rimuove il criterio del firewall denominato "firewallpolicy" nel gruppo di risorse "TestRg"</span><span class="sxs-lookup"><span data-stu-id="cad6d-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="cad6d-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="cad6d-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="cad6d-114">Questo esempio rimuove i criteri del firewall in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="cad6d-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="cad6d-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="cad6d-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="cad6d-116">Questo esempio rimuove i criteri del firewall $fp</span><span class="sxs-lookup"><span data-stu-id="cad6d-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="cad6d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cad6d-117">PARAMETERS</span></span>

### <span data-ttu-id="cad6d-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cad6d-118">-AsJob</span></span>
<span data-ttu-id="cad6d-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="cad6d-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cad6d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cad6d-120">-DefaultProfile</span></span>
<span data-ttu-id="cad6d-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cad6d-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cad6d-122">-Force</span><span class="sxs-lookup"><span data-stu-id="cad6d-122">-Force</span></span>
<span data-ttu-id="cad6d-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="cad6d-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="cad6d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cad6d-124">-InputObject</span></span>
<span data-ttu-id="cad6d-125">Criteri di AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="cad6d-125">The AzureFirewall Policy</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy
Parameter Sets: RemoveByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cad6d-126">-Name</span><span class="sxs-lookup"><span data-stu-id="cad6d-126">-Name</span></span>
<span data-ttu-id="cad6d-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cad6d-127">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad6d-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cad6d-128">-PassThru</span></span>
<span data-ttu-id="cad6d-129">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="cad6d-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cad6d-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="cad6d-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cad6d-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cad6d-131">-ResourceGroupName</span></span>
<span data-ttu-id="cad6d-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="cad6d-132">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad6d-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cad6d-133">-ResourceId</span></span>
<span data-ttu-id="cad6d-134">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="cad6d-134">The resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cad6d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="cad6d-135">-Confirm</span></span>
<span data-ttu-id="cad6d-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cad6d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cad6d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cad6d-137">-WhatIf</span></span>
<span data-ttu-id="cad6d-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cad6d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cad6d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cad6d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cad6d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cad6d-140">CommonParameters</span></span>
<span data-ttu-id="cad6d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cad6d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cad6d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="cad6d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cad6d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="cad6d-143">INPUTS</span></span>

### <span data-ttu-id="cad6d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="cad6d-144">System.String</span></span>

### <span data-ttu-id="cad6d-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="cad6d-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="cad6d-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cad6d-146">OUTPUTS</span></span>

### <span data-ttu-id="cad6d-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cad6d-147">System.Boolean</span></span>

## <span data-ttu-id="cad6d-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="cad6d-148">NOTES</span></span>

## <span data-ttu-id="cad6d-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cad6d-149">RELATED LINKS</span></span>
