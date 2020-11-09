---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: e1517801c964c4794c21ada6b7d64152c6e58178
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310567"
---
# <span data-ttu-id="bdb57-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bdb57-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="bdb57-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bdb57-102">SYNOPSIS</span></span>
 <span data-ttu-id="bdb57-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="bdb57-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="bdb57-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bdb57-104">SYNTAX</span></span>

### <span data-ttu-id="bdb57-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bdb57-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdb57-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="bdb57-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb57-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="bdb57-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdb57-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="bdb57-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPAddressOrRange <String[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdb57-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bdb57-109">DESCRIPTION</span></span>
<span data-ttu-id="bdb57-110">Il cmdlet **Add-AzStorageAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="bdb57-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="bdb57-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bdb57-111">EXAMPLES</span></span>

### <span data-ttu-id="bdb57-112">Esempio 1: aggiungere diversi IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bdb57-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="bdb57-113">Questo comando aggiunge diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="bdb57-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="bdb57-114">Esempio 2: aggiungere un VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="bdb57-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="bdb57-115">Questo comando aggiunge un VirtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="bdb57-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="bdb57-116">Esempio 3: aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="bdb57-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="bdb57-117">Questo comando aggiunge VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="bdb57-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="bdb57-118">Esempio 4: aggiungere diversi IpRule con oggetti IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="bdb57-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="bdb57-119">Questo comando aggiunge diversi IpRule con oggetti IpRule, input with JSON.</span><span class="sxs-lookup"><span data-stu-id="bdb57-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="bdb57-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bdb57-120">PARAMETERS</span></span>

### <span data-ttu-id="bdb57-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bdb57-121">-AsJob</span></span>
<span data-ttu-id="bdb57-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="bdb57-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bdb57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdb57-123">-DefaultProfile</span></span>
<span data-ttu-id="bdb57-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bdb57-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdb57-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="bdb57-125">-IPAddressOrRange</span></span>
<span data-ttu-id="bdb57-126">La matrice di IpAddressOrRange, Aggiungi IpRules con l'input IpAddressOrRange e l'azione predefinita consente di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdb57-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="bdb57-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="bdb57-127">-IPRule</span></span>
<span data-ttu-id="bdb57-128">Matrice di oggetti IpRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="bdb57-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="bdb57-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="bdb57-129">-Name</span></span>
<span data-ttu-id="bdb57-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bdb57-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="bdb57-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdb57-131">-ResourceGroupName</span></span>
<span data-ttu-id="bdb57-132">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="bdb57-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="bdb57-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="bdb57-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="bdb57-134">La matrice di VirtualNetworkResourceId, aggiungerà VirtualNetworkRule con l'input VirtualNetworkResourceId e l'azione predefinita consentirà di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="bdb57-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="bdb57-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bdb57-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="bdb57-136">Matrice di oggetti VirtualNetworkRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="bdb57-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="bdb57-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bdb57-137">-Confirm</span></span>
<span data-ttu-id="bdb57-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdb57-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdb57-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdb57-139">-WhatIf</span></span>
<span data-ttu-id="bdb57-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdb57-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdb57-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bdb57-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdb57-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdb57-142">CommonParameters</span></span>
<span data-ttu-id="bdb57-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdb57-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdb57-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdb57-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdb57-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bdb57-145">INPUTS</span></span>

### <span data-ttu-id="bdb57-146">System. String</span><span class="sxs-lookup"><span data-stu-id="bdb57-146">System.String</span></span>

### <span data-ttu-id="bdb57-147">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="bdb57-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="bdb57-148">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="bdb57-148">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="bdb57-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bdb57-149">OUTPUTS</span></span>

### <span data-ttu-id="bdb57-150">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="bdb57-150">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="bdb57-151">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="bdb57-151">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="bdb57-152">Note</span><span class="sxs-lookup"><span data-stu-id="bdb57-152">NOTES</span></span>

## <span data-ttu-id="bdb57-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bdb57-153">RELATED LINKS</span></span>
