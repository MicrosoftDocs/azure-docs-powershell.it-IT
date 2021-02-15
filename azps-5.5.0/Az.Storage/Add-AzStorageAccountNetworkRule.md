---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100195830"
---
# <span data-ttu-id="9c4da-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9c4da-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="9c4da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c4da-102">SYNOPSIS</span></span>
 <span data-ttu-id="9c4da-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9c4da-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9c4da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9c4da-104">SYNTAX</span></span>

### <span data-ttu-id="9c4da-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9c4da-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c4da-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="9c4da-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c4da-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9c4da-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c4da-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="9c4da-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c4da-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9c4da-109">DESCRIPTION</span></span>
<span data-ttu-id="9c4da-110">Il cmdlet **Add-AzStorageAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9c4da-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="9c4da-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9c4da-111">EXAMPLES</span></span>

### <span data-ttu-id="9c4da-112">Esempio 1: Aggiungere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9c4da-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="9c4da-113">Questo comando aggiunge più IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="9c4da-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="9c4da-114">Esempio 2: Aggiungere una regola VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="9c4da-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="9c4da-115">Questo comando aggiunge virtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="9c4da-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="9c4da-116">Esempio 3: Aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="9c4da-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="9c4da-117">Questo comando aggiunge VirtualNetworkRules con gli oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="9c4da-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="9c4da-118">Esempio 4: Aggiungere più oggetti IpRule con IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="9c4da-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="9c4da-119">Questo comando aggiunge diversi oggetti IpRule con oggetti IpRule, input con JSON.</span><span class="sxs-lookup"><span data-stu-id="9c4da-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="9c4da-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c4da-120">PARAMETERS</span></span>

### <span data-ttu-id="9c4da-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c4da-121">-AsJob</span></span>
<span data-ttu-id="9c4da-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9c4da-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c4da-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c4da-123">-DefaultProfile</span></span>
<span data-ttu-id="9c4da-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9c4da-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9c4da-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9c4da-125">-IPAddressOrRange</span></span>
<span data-ttu-id="9c4da-126">Matrice di IpAddressOrRange, aggiungere IpRules con l'input IpAddressOrRange e la proprietà default Action Allow to NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9c4da-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="9c4da-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9c4da-127">-IPRule</span></span>
<span data-ttu-id="9c4da-128">Matrice di oggetti IpRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9c4da-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="9c4da-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9c4da-129">-Name</span></span>
<span data-ttu-id="9c4da-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9c4da-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9c4da-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c4da-131">-ResourceGroupName</span></span>
<span data-ttu-id="9c4da-132">Specifica che il nome del gruppo di risorse contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9c4da-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9c4da-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9c4da-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9c4da-134">La matrice di VirtualNetworkResourceId aggiunge VirtualNetworkRule con l'input VirtualNetworkResourceId e la proprietà predefinita Action Allow to NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9c4da-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="9c4da-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9c4da-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="9c4da-136">Matrice di oggetti VirtualNetworkRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="9c4da-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="9c4da-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c4da-137">-Confirm</span></span>
<span data-ttu-id="9c4da-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c4da-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c4da-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c4da-139">-WhatIf</span></span>
<span data-ttu-id="9c4da-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c4da-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c4da-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9c4da-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c4da-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c4da-142">CommonParameters</span></span>
<span data-ttu-id="9c4da-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c4da-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c4da-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c4da-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c4da-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="9c4da-145">INPUTS</span></span>

### <span data-ttu-id="9c4da-146">System.String</span><span class="sxs-lookup"><span data-stu-id="9c4da-146">System.String</span></span>

### <span data-ttu-id="9c4da-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="9c4da-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="9c4da-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="9c4da-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="9c4da-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9c4da-149">OUTPUTS</span></span>

### <span data-ttu-id="9c4da-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9c4da-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="9c4da-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="9c4da-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="9c4da-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="9c4da-152">NOTES</span></span>

## <span data-ttu-id="9c4da-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9c4da-153">RELATED LINKS</span></span>
