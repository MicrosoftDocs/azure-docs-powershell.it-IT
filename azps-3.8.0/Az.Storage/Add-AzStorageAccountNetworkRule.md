---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94021432"
---
# <span data-ttu-id="3f0c3-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f0c3-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="3f0c3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3f0c3-102">SYNOPSIS</span></span>
 <span data-ttu-id="3f0c3-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3f0c3-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3f0c3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3f0c3-104">SYNTAX</span></span>

### <span data-ttu-id="3f0c3-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3f0c3-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3f0c3-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f0c3-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f0c3-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="3f0c3-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3f0c3-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="3f0c3-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3f0c3-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3f0c3-109">DESCRIPTION</span></span>
<span data-ttu-id="3f0c3-110">Il cmdlet **Add-AzStorageAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="3f0c3-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="3f0c3-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3f0c3-111">EXAMPLES</span></span>

### <span data-ttu-id="3f0c3-112">Esempio 1: aggiungere diversi IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3f0c3-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="3f0c3-113">Questo comando aggiunge diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="3f0c3-114">Esempio 2: aggiungere un VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="3f0c3-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="3f0c3-115">Questo comando aggiunge un VirtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="3f0c3-116">Esempio 3: aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="3f0c3-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="3f0c3-117">Questo comando aggiunge VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="3f0c3-118">Esempio 4: aggiungere diversi IpRule con oggetti IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="3f0c3-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="3f0c3-119">Questo comando aggiunge diversi IpRule con oggetti IpRule, input with JSON.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="3f0c3-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3f0c3-120">PARAMETERS</span></span>

### <span data-ttu-id="3f0c3-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3f0c3-121">-AsJob</span></span>
<span data-ttu-id="3f0c3-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3f0c3-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3f0c3-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f0c3-123">-DefaultProfile</span></span>
<span data-ttu-id="3f0c3-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f0c3-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="3f0c3-125">-IPAddressOrRange</span></span>
<span data-ttu-id="3f0c3-126">La matrice di IpAddressOrRange, Aggiungi IpRules con l'input IpAddressOrRange e l'azione predefinita consente di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="3f0c3-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="3f0c3-127">-IPRule</span></span>
<span data-ttu-id="3f0c3-128">Matrice di oggetti IpRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="3f0c3-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="3f0c3-129">-Name</span></span>
<span data-ttu-id="3f0c3-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="3f0c3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f0c3-131">-ResourceGroupName</span></span>
<span data-ttu-id="3f0c3-132">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="3f0c3-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="3f0c3-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="3f0c3-134">La matrice di VirtualNetworkResourceId, aggiungerà VirtualNetworkRule con l'input VirtualNetworkResourceId e l'azione predefinita consentirà di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="3f0c3-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f0c3-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="3f0c3-136">Matrice di oggetti VirtualNetworkRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="3f0c3-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3f0c3-137">-Confirm</span></span>
<span data-ttu-id="3f0c3-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3f0c3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3f0c3-139">-WhatIf</span></span>
<span data-ttu-id="3f0c3-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3f0c3-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3f0c3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f0c3-142">CommonParameters</span></span>
<span data-ttu-id="3f0c3-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f0c3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f0c3-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f0c3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f0c3-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3f0c3-145">INPUTS</span></span>

### <span data-ttu-id="3f0c3-146">System. String</span><span class="sxs-lookup"><span data-stu-id="3f0c3-146">System.String</span></span>

### <span data-ttu-id="3f0c3-147">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="3f0c3-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="3f0c3-148">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="3f0c3-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="3f0c3-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3f0c3-149">OUTPUTS</span></span>

### <span data-ttu-id="3f0c3-150">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="3f0c3-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="3f0c3-151">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="3f0c3-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="3f0c3-152">Note</span><span class="sxs-lookup"><span data-stu-id="3f0c3-152">NOTES</span></span>

## <span data-ttu-id="3f0c3-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3f0c3-153">RELATED LINKS</span></span>
