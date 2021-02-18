---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountNetworkRule.md
ms.openlocfilehash: 1eeaf3a7c9d0c4b5715bc5b75e42e53a8fa98c5e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190758"
---
# <span data-ttu-id="52f09-101">Remove-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52f09-101">Remove-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="52f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52f09-102">SYNOPSIS</span></span>
<span data-ttu-id="52f09-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52f09-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="52f09-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="52f09-104">SYNTAX</span></span>

### <span data-ttu-id="52f09-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="52f09-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52f09-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="52f09-106">IpRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f09-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="52f09-107">NetworkRuleObject</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52f09-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="52f09-108">IpRuleString</span></span>
```
Remove-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52f09-109">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="52f09-109">DESCRIPTION</span></span>
<span data-ttu-id="52f09-110">Il cmdlet **Remove-AzStorageAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="52f09-110">The **Remove-AzStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="52f09-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="52f09-111">EXAMPLES</span></span>

### <span data-ttu-id="52f09-112">Esempio 1: Rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="52f09-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="52f09-113">Questo comando rimuove diverse IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="52f09-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="52f09-114">Esempio 2: Rimuovere un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="52f09-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="52f09-115">Questo comando rimuove un valore VirtualNetworkRule con l'input dell'oggetto VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="52f09-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="52f09-116">Esempio 3: Rimuovere la prima regola IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="52f09-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="52f09-117">Questo comando rimuove la prima regola IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="52f09-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="52f09-118">Esempio 4: Rimuovere più RegoleRelavoro VirtualNet con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="52f09-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="52f09-119">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="52f09-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="52f09-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52f09-120">PARAMETERS</span></span>

### <span data-ttu-id="52f09-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52f09-121">-AsJob</span></span>
<span data-ttu-id="52f09-122">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="52f09-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52f09-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52f09-123">-DefaultProfile</span></span>
<span data-ttu-id="52f09-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="52f09-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52f09-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="52f09-125">-IPAddressOrRange</span></span>
<span data-ttu-id="52f09-126">La matrice di IpAddressOrRange rimuove IpRule con lo stesso IpAddressOrRange dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="52f09-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="52f09-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="52f09-127">-IPRule</span></span>
<span data-ttu-id="52f09-128">Matrice di oggetti IpRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="52f09-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="52f09-129">-Name</span><span class="sxs-lookup"><span data-stu-id="52f09-129">-Name</span></span>
<span data-ttu-id="52f09-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52f09-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="52f09-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52f09-131">-ResourceGroupName</span></span>
<span data-ttu-id="52f09-132">Specifica che il nome del gruppo di risorse contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="52f09-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="52f09-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="52f09-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="52f09-134">La matrice VirtualNetworkResourceId rimuove VirtualNetworkRule con lo stesso VirtualNetworkResourceId dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="52f09-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="52f09-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52f09-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="52f09-136">Matrice di oggetti VirtualNetworkRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="52f09-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="52f09-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="52f09-137">-Confirm</span></span>
<span data-ttu-id="52f09-138">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52f09-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52f09-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52f09-139">-WhatIf</span></span>
<span data-ttu-id="52f09-140">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52f09-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52f09-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="52f09-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52f09-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52f09-142">CommonParameters</span></span>
<span data-ttu-id="52f09-143">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52f09-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52f09-144">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52f09-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52f09-145">INPUT</span><span class="sxs-lookup"><span data-stu-id="52f09-145">INPUTS</span></span>

### <span data-ttu-id="52f09-146">System.String</span><span class="sxs-lookup"><span data-stu-id="52f09-146">System.String</span></span>

### <span data-ttu-id="52f09-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="52f09-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="52f09-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="52f09-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="52f09-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="52f09-149">OUTPUTS</span></span>

### <span data-ttu-id="52f09-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="52f09-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="52f09-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span><span class="sxs-lookup"><span data-stu-id="52f09-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="52f09-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="52f09-152">NOTES</span></span>

## <span data-ttu-id="52f09-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="52f09-153">RELATED LINKS</span></span>
