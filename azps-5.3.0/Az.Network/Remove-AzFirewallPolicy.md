---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azfirewallpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzFirewallPolicy.md
ms.openlocfilehash: a6539d1569d3dc4f0d12190b6b1d0670b036c30a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98475882"
---
# <span data-ttu-id="9a32a-101">Remove-AzFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9a32a-101">Remove-AzFirewallPolicy</span></span>

## <span data-ttu-id="9a32a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9a32a-102">SYNOPSIS</span></span>
<span data-ttu-id="9a32a-103">Rimuove un criterio di Azure firewall</span><span class="sxs-lookup"><span data-stu-id="9a32a-103">Removes an Azure Firewall Policy</span></span>

## <span data-ttu-id="9a32a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9a32a-104">SYNTAX</span></span>

### <span data-ttu-id="9a32a-105">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a32a-105">RemoveByNameParameterSet</span></span>
```
Remove-AzFirewallPolicy -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a32a-106">RemoveByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a32a-106">RemoveByResourceIdParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a32a-107">RemoveByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a32a-107">RemoveByInputObjectParameterSet</span></span>
```
Remove-AzFirewallPolicy [-Force] [-PassThru] [-AsJob] -InputObject <PSAzureFirewallPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a32a-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9a32a-108">DESCRIPTION</span></span>
<span data-ttu-id="9a32a-109">Il cmdlet **Remove-AzFirewallPolicy** rimuove un criterio di Azure firewall.</span><span class="sxs-lookup"><span data-stu-id="9a32a-109">The **Remove-AzFirewallPolicy** cmdlet removes an Azure Firewall Policy.</span></span>

## <span data-ttu-id="9a32a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9a32a-110">EXAMPLES</span></span>

### <span data-ttu-id="9a32a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9a32a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceGroupName TestRg
```

<span data-ttu-id="9a32a-112">In questo esempio vengono rimossi i criteri del firewall denominati "firewallpolicy" nel ResourceGroup "TestRg"</span><span class="sxs-lookup"><span data-stu-id="9a32a-112">This example removes the firewall policy named "firewallpolicy" in the resourcegroup "TestRg"</span></span>

### <span data-ttu-id="9a32a-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="9a32a-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -Name firewallpolicy -ResourceId "/subscriptions/12345/resourceGroups/TestRg/providers/Microsoft.Network/firewallpolicies/firewallPolicy1"
```

<span data-ttu-id="9a32a-114">Questo esempio rimuove i criteri del firewall in base all'ID.</span><span class="sxs-lookup"><span data-stu-id="9a32a-114">This example removes the firewall policy by the Id.</span></span>

### <span data-ttu-id="9a32a-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="9a32a-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzFirewallPolicy -InputObject $fp
```

<span data-ttu-id="9a32a-116">Questo esempio rimuove il criterio firewall $fp</span><span class="sxs-lookup"><span data-stu-id="9a32a-116">This example removes the firewall policy $fp</span></span>

## <span data-ttu-id="9a32a-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9a32a-117">PARAMETERS</span></span>

### <span data-ttu-id="9a32a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a32a-118">-AsJob</span></span>
<span data-ttu-id="9a32a-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9a32a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a32a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a32a-120">-DefaultProfile</span></span>
<span data-ttu-id="9a32a-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9a32a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a32a-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9a32a-122">-Force</span></span>
<span data-ttu-id="9a32a-123">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="9a32a-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9a32a-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a32a-124">-InputObject</span></span>
<span data-ttu-id="9a32a-125">Criteri AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="9a32a-125">The AzureFirewall Policy</span></span>

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

### <span data-ttu-id="9a32a-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a32a-126">-Name</span></span>
<span data-ttu-id="9a32a-127">Il nome della risorsa.</span><span class="sxs-lookup"><span data-stu-id="9a32a-127">The resource name.</span></span>

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

### <span data-ttu-id="9a32a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a32a-128">-PassThru</span></span>
<span data-ttu-id="9a32a-129">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="9a32a-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a32a-130">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="9a32a-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a32a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a32a-131">-ResourceGroupName</span></span>
<span data-ttu-id="9a32a-132">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9a32a-132">The resource group name.</span></span>

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

### <span data-ttu-id="9a32a-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a32a-133">-ResourceId</span></span>
<span data-ttu-id="9a32a-134">ID risorsa.</span><span class="sxs-lookup"><span data-stu-id="9a32a-134">The resource Id.</span></span>

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

### <span data-ttu-id="9a32a-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9a32a-135">-Confirm</span></span>
<span data-ttu-id="9a32a-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a32a-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a32a-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a32a-137">-WhatIf</span></span>
<span data-ttu-id="9a32a-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a32a-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a32a-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9a32a-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a32a-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a32a-140">CommonParameters</span></span>
<span data-ttu-id="9a32a-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a32a-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a32a-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a32a-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a32a-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9a32a-143">INPUTS</span></span>

### <span data-ttu-id="9a32a-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9a32a-144">System.String</span></span>

### <span data-ttu-id="9a32a-145">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallPolicy</span><span class="sxs-lookup"><span data-stu-id="9a32a-145">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallPolicy</span></span>

## <span data-ttu-id="9a32a-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9a32a-146">OUTPUTS</span></span>

### <span data-ttu-id="9a32a-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a32a-147">System.Boolean</span></span>

## <span data-ttu-id="9a32a-148">Note</span><span class="sxs-lookup"><span data-stu-id="9a32a-148">NOTES</span></span>

## <span data-ttu-id="9a32a-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9a32a-149">RELATED LINKS</span></span>
