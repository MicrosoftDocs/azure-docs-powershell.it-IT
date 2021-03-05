---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: 69d9e49c83b2f1231be4fe2b1ffc3cba25c2cf2c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993773"
---
# <span data-ttu-id="04993-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="04993-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="04993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04993-102">SYNOPSIS</span></span>
<span data-ttu-id="04993-103">Rimuove un criterio del firewall di Azure</span><span class="sxs-lookup"><span data-stu-id="04993-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="04993-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="04993-104">SYNTAX</span></span>

### <span data-ttu-id="04993-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="04993-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04993-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="04993-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="04993-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="04993-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="04993-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="04993-108">DESCRIPTION</span></span>
<span data-ttu-id="04993-109">Il cmdlet **Remove-AzFirewallPolicy** rimuove un criterio del firewall di Azure.</span><span class="sxs-lookup"><span data-stu-id="04993-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="04993-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="04993-110">EXAMPLES</span></span>

### <span data-ttu-id="04993-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="04993-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="04993-112">Questo esempio rimuove il criterio del firewall denominato "firewallpolicy" nel gruppo di risorse "TestRg"</span><span class="sxs-lookup"><span data-stu-id="04993-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="04993-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="04993-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="04993-114">Questo esempio rimuove i criteri del firewall in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="04993-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="04993-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="04993-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="04993-116">Questo esempio rimuove i criteri del firewall $fp</span><span class="sxs-lookup"><span data-stu-id="04993-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="04993-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="04993-117">PARAMETERS</span></span>

### <span data-ttu-id="04993-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="04993-118">-AsJob</span></span>
<span data-ttu-id="04993-119">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="04993-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="04993-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04993-120">-DefaultProfile</span></span>
<span data-ttu-id="04993-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="04993-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="04993-122">-Force</span><span class="sxs-lookup"><span data-stu-id="04993-122">-Force</span></span>
<span data-ttu-id="04993-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="04993-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="04993-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="04993-124">-InputObject</span></span>
<span data-ttu-id="04993-125">Criteri di AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="04993-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="04993-126">-Name</span><span class="sxs-lookup"><span data-stu-id="04993-126">-Name</span></span>
<span data-ttu-id="04993-127">Nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="04993-127">The resource name.</span></span>

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

### <span data-ttu-id="04993-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="04993-128">-PassThru</span></span>
<span data-ttu-id="04993-129">Restituisce un oggetto che rappresenta l'elemento su cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="04993-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="04993-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="04993-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="04993-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04993-131">-ResourceGroupName</span></span>
<span data-ttu-id="04993-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="04993-132">The resource group name.</span></span>

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

### <span data-ttu-id="04993-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="04993-133">-ResourceId</span></span>
<span data-ttu-id="04993-134">ID della risorsa.</span><span class="sxs-lookup"><span data-stu-id="04993-134">The resource Id.</span></span>

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

### <span data-ttu-id="04993-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="04993-135">-Confirm</span></span>
<span data-ttu-id="04993-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="04993-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="04993-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="04993-137">-WhatIf</span></span>
<span data-ttu-id="04993-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04993-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="04993-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="04993-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="04993-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04993-140">CommonParameters</span></span>
<span data-ttu-id="04993-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04993-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04993-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="04993-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04993-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="04993-143">INPUTS</span></span>

### <span data-ttu-id="04993-144">System.String</span><span class="sxs-lookup"><span data-stu-id="04993-144">System.String</span></span>

### <span data-ttu-id="04993-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="04993-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="04993-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="04993-146">OUTPUTS</span></span>

### <span data-ttu-id="04993-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="04993-147">System.Boolean</span></span>

## <span data-ttu-id="04993-148">NOTE</span><span class="sxs-lookup"><span data-stu-id="04993-148">NOTES</span></span>

## <span data-ttu-id="04993-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="04993-149">RELATED LINKS</span></span>
