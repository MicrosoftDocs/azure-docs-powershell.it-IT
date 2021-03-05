---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 295f79f48ffa966024561486745cdcf52ec8e38f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101973326"
---
# <span data-ttu-id="33849-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="33849-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="33849-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33849-102">SYNOPSIS</span></span>
<span data-ttu-id="33849-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="33849-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="33849-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33849-104">SYNTAX</span></span>

### <span data-ttu-id="33849-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33849-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="33849-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="33849-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33849-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="33849-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33849-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="33849-108">ResourceAccessRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33849-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="33849-109">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33849-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="33849-110">ResourceAccessRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="33849-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="33849-111">DESCRIPTION</span></span>
<span data-ttu-id="33849-112">Il cmdlet **Remove-AzStorageAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="33849-112">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="33849-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33849-113">EXAMPLES</span></span>

### <span data-ttu-id="33849-114">Esempio 1: Rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="33849-114">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="33849-115">Questo comando rimuove diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="33849-115">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="33849-116">Esempio 2: Rimuovere un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="33849-116">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="33849-117">Questo comando rimuove un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="33849-117">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="33849-118">Esempio 3: Rimuovere first IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="33849-118">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="33849-119">Questo comando rimuove la prima regola IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="33849-119">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="33849-120">Esempio 4: Rimuovere più RegoleRelavoro VirtualNet con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="33849-120">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="33849-121">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="33849-121">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="33849-122">Esempio 5: Rimuovere una regola di accesso alle risorse con TenantId e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="33849-122">Example 5: Remove a resource access rule with TenantId and ResourceId.</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"  -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="33849-123">Questo comando rimuove una regola di accesso alle risorse con TenantId e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="33849-123">This command removes a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="33849-124">Esempio 6: Rimuovere le prime 3 regole di accesso alle risorse da un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="33849-124">Example 6: Remove the first 3 resource access rules from a storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount").ResourceAccessRules | Select-Object -First 3 | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="33849-125">Questo comando rimuove le prime 3 regole di accesso alle risorse da un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33849-125">This command removes the first 3 resource access rules from a storage account.</span></span>

## <span data-ttu-id="33849-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33849-126">PARAMETERS</span></span>

### <span data-ttu-id="33849-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="33849-127">-AsJob</span></span>
<span data-ttu-id="33849-128">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="33849-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="33849-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33849-129">-DefaultProfile</span></span>
<span data-ttu-id="33849-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="33849-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="33849-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="33849-131">-IPAddressOrRange</span></span>
<span data-ttu-id="33849-132">La matrice di IpAddressOrRange rimuove IpRule con lo stesso IpAddressOrRange dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="33849-132">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: IpRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33849-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="33849-133">-IPRule</span></span>
<span data-ttu-id="33849-134">Matrice di oggetti IpRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="33849-134">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: IpRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33849-135">-Name</span><span class="sxs-lookup"><span data-stu-id="33849-135">-Name</span></span>
<span data-ttu-id="33849-136">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33849-136">Specifies the name of the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33849-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="33849-137">-ResourceAccessRule</span></span>
<span data-ttu-id="33849-138">Account di archiviazione NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="33849-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSResourceAccessRule[]
Parameter Sets: ResourceAccessRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33849-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33849-139">-ResourceGroupName</span></span>
<span data-ttu-id="33849-140">Specifica che il nome del gruppo di risorse contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33849-140">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33849-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="33849-141">-ResourceId</span></span>
<span data-ttu-id="33849-142">ResourceAccessRule ResourceId dell'account di archiviazione nella stringa.</span><span class="sxs-lookup"><span data-stu-id="33849-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33849-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="33849-143">-TenantId</span></span>
<span data-ttu-id="33849-144">ResourceAccessRule TenantId dell'account di archiviazione nella stringa.</span><span class="sxs-lookup"><span data-stu-id="33849-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceAccessRuleString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33849-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="33849-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="33849-146">La matrice VirtualNetworkResourceId rimuove VirtualNetworkRule con lo stesso VirtualNetworkResourceId dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="33849-146">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33849-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="33849-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="33849-148">Matrice di oggetti VirtualNetworkRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="33849-148">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="33849-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="33849-149">-Confirm</span></span>
<span data-ttu-id="33849-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33849-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33849-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33849-151">-WhatIf</span></span>
<span data-ttu-id="33849-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33849-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33849-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="33849-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33849-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33849-154">CommonParameters</span></span>
<span data-ttu-id="33849-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33849-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33849-156">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33849-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33849-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="33849-157">INPUTS</span></span>

### <span data-ttu-id="33849-158">System.String</span><span class="sxs-lookup"><span data-stu-id="33849-158">System.String</span></span>

### <span data-ttu-id="33849-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="33849-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="33849-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="33849-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="33849-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33849-161">OUTPUTS</span></span>

### <span data-ttu-id="33849-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="33849-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="33849-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="33849-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="33849-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="33849-164">NOTES</span></span>

## <span data-ttu-id="33849-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33849-165">RELATED LINKS</span></span>
