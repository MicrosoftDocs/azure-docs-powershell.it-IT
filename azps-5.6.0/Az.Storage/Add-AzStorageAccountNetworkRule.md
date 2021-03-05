---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 0104c64bf65acc945609f4e2e0ae78ff288b142d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976174"
---
# <span data-ttu-id="96d4b-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="96d4b-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="96d4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96d4b-102">SYNOPSIS</span></span>
 <span data-ttu-id="96d4b-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="96d4b-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="96d4b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="96d4b-104">SYNTAX</span></span>

### <span data-ttu-id="96d4b-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="96d4b-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="96d4b-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="96d4b-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d4b-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="96d4b-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d4b-108">ResourceAccessRuleObject</span><span class="sxs-lookup"><span data-stu-id="96d4b-108">ResourceAccessRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -ResourceAccessRule <PSResourceAccessRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d4b-109">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="96d4b-109">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96d4b-110">ResourceAccessRuleString</span><span class="sxs-lookup"><span data-stu-id="96d4b-110">ResourceAccessRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -TenantId <String>
 -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96d4b-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="96d4b-111">DESCRIPTION</span></span>
<span data-ttu-id="96d4b-112">Il cmdlet **Add-AzStorageAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="96d4b-112">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="96d4b-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="96d4b-113">EXAMPLES</span></span>

### <span data-ttu-id="96d4b-114">Esempio 1: Aggiungere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="96d4b-114">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="96d4b-115">Questo comando aggiunge più IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="96d4b-115">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="96d4b-116">Esempio 2: Aggiungere una regola VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="96d4b-116">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="96d4b-117">Questo comando aggiunge virtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="96d4b-117">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="96d4b-118">Esempio 3: Aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="96d4b-118">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="96d4b-119">Questo comando aggiunge VirtualNetworkRules con gli oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="96d4b-119">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="96d4b-120">Esempio 4: Aggiungere diversi oggetti IpRule con oggetti IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="96d4b-120">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="96d4b-121">Questo comando aggiunge diversi oggetti IpRule con oggetti IpRule, input con JSON.</span><span class="sxs-lookup"><span data-stu-id="96d4b-121">This command add several IpRule with IpRule objects, input with JSON.</span></span>

### <span data-ttu-id="96d4b-122">Esempio 5: Aggiungere una regola di accesso alle risorse</span><span class="sxs-lookup"><span data-stu-id="96d4b-122">Example 5: Add a resource access rule</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -TenantId $tenantId -ResourceId $ResourceId
```

<span data-ttu-id="96d4b-123">Questo comando aggiunge una regola di accesso alle risorse con TenantId e ResourceId.</span><span class="sxs-lookup"><span data-stu-id="96d4b-123">This command adds a resource access rule with TenantId and ResourceId.</span></span>

### <span data-ttu-id="96d4b-124">Esempio 6: Aggiungere tutte le regole di accesso alle risorse di un account di archiviazione a un altro account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="96d4b-124">Example 6: Add all resource access rules of one storage account to another storage account</span></span>
```
PS C:\> (Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1").ResourceAccessRules | Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2"
```

<span data-ttu-id="96d4b-125">Questo comando recupera tutte le regole di accesso alle risorse da un account di archiviazione e le aggiunge a un altro account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="96d4b-125">This command gets all resource access rules from one storage account, and adds them to another storage account.</span></span>

## <span data-ttu-id="96d4b-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96d4b-126">PARAMETERS</span></span>

### <span data-ttu-id="96d4b-127">-AsJob</span><span class="sxs-lookup"><span data-stu-id="96d4b-127">-AsJob</span></span>
<span data-ttu-id="96d4b-128">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="96d4b-128">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="96d4b-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96d4b-129">-DefaultProfile</span></span>
<span data-ttu-id="96d4b-130">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="96d4b-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96d4b-131">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="96d4b-131">-IPAddressOrRange</span></span>
<span data-ttu-id="96d4b-132">Matrice di IpAddressOrRange, aggiungere IpRules con l'input IpAddressOrRange e la proprietà default Action Allow to NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="96d4b-132">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="96d4b-133">-IPRule</span><span class="sxs-lookup"><span data-stu-id="96d4b-133">-IPRule</span></span>
<span data-ttu-id="96d4b-134">Matrice di oggetti IpRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="96d4b-134">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="96d4b-135">-Name</span><span class="sxs-lookup"><span data-stu-id="96d4b-135">-Name</span></span>
<span data-ttu-id="96d4b-136">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="96d4b-136">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="96d4b-137">-ResourceAccessRule</span><span class="sxs-lookup"><span data-stu-id="96d4b-137">-ResourceAccessRule</span></span>
<span data-ttu-id="96d4b-138">Account di archiviazione NetworkRule ResourceAccessRules.</span><span class="sxs-lookup"><span data-stu-id="96d4b-138">Storage Account NetworkRule ResourceAccessRules.</span></span>

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

### <span data-ttu-id="96d4b-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96d4b-139">-ResourceGroupName</span></span>
<span data-ttu-id="96d4b-140">Specifica che il nome del gruppo di risorse contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="96d4b-140">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="96d4b-141">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96d4b-141">-ResourceId</span></span>
<span data-ttu-id="96d4b-142">ResourceAccessRule ResourceId dell'account di archiviazione nella stringa.</span><span class="sxs-lookup"><span data-stu-id="96d4b-142">Storage Account ResourceAccessRule ResourceId  in string.</span></span>

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

### <span data-ttu-id="96d4b-143">-TenantId</span><span class="sxs-lookup"><span data-stu-id="96d4b-143">-TenantId</span></span>
<span data-ttu-id="96d4b-144">ResourceAccessRule TenantId dell'account di archiviazione nella stringa.</span><span class="sxs-lookup"><span data-stu-id="96d4b-144">Storage Account ResourceAccessRule TenantId  in string.</span></span>

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

### <span data-ttu-id="96d4b-145">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="96d4b-145">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="96d4b-146">La matrice virtualNetworkResourceId aggiunge VirtualNetworkRule con l'input VirtualNetworkResourceId e la proprietà predefinita Action Allow to NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="96d4b-146">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="96d4b-147">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="96d4b-147">-VirtualNetworkRule</span></span>
<span data-ttu-id="96d4b-148">Matrice di oggetti VirtualNetworkRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="96d4b-148">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="96d4b-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96d4b-149">-Confirm</span></span>
<span data-ttu-id="96d4b-150">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="96d4b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96d4b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96d4b-151">-WhatIf</span></span>
<span data-ttu-id="96d4b-152">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96d4b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="96d4b-153">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="96d4b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96d4b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96d4b-154">CommonParameters</span></span>
<span data-ttu-id="96d4b-155">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="96d4b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96d4b-156">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="96d4b-156">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96d4b-157">INPUT</span><span class="sxs-lookup"><span data-stu-id="96d4b-157">INPUTS</span></span>

### <span data-ttu-id="96d4b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="96d4b-158">System.String</span></span>

### <span data-ttu-id="96d4b-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="96d4b-159">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="96d4b-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="96d4b-160">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="96d4b-161">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="96d4b-161">OUTPUTS</span></span>

### <span data-ttu-id="96d4b-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="96d4b-162">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="96d4b-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="96d4b-163">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="96d4b-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="96d4b-164">NOTES</span></span>

## <span data-ttu-id="96d4b-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="96d4b-165">RELATED LINKS</span></span>
