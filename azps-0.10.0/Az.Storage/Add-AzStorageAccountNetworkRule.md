---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/add-azstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Add-AzStorageAccountNetworkRule.md
ms.openlocfilehash: fb8df6e3444a650cc5f3c249545a43b4033689bd
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862293"
---
# <span data-ttu-id="034ff-101">Add-AzStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="034ff-101">Add-AzStorageAccountNetworkRule</span></span>

## <span data-ttu-id="034ff-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="034ff-102">SYNOPSIS</span></span>
 <span data-ttu-id="034ff-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="034ff-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="034ff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="034ff-104">SYNTAX</span></span>

### <span data-ttu-id="034ff-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="034ff-105">NetWorkRuleString (Default)</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="034ff-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="034ff-106">IpRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="034ff-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="034ff-107">NetworkRuleObject</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="034ff-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="034ff-108">IpRuleString</span></span>
```
Add-AzStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="034ff-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="034ff-109">DESCRIPTION</span></span>
<span data-ttu-id="034ff-110">Il cmdlet **Add-AzStorageAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="034ff-110">The **Add-AzStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="034ff-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="034ff-111">EXAMPLES</span></span>

### <span data-ttu-id="034ff-112">Esempio 1: aggiungere diversi IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="034ff-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="034ff-113">Questo comando aggiunge diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="034ff-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="034ff-114">Esempio 2: aggiungere un VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="034ff-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzVirtualNetworkSubnetConfig
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="034ff-115">Questo comando aggiunge un VirtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="034ff-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="034ff-116">Esempio 3: aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="034ff-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="034ff-117">Questo comando aggiunge VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="034ff-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="034ff-118">Esempio 4: aggiungere diversi IpRule con oggetti IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="034ff-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="034ff-119">Questo comando aggiunge diversi IpRule con oggetti IpRule, input with JSON.</span><span class="sxs-lookup"><span data-stu-id="034ff-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="034ff-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="034ff-120">PARAMETERS</span></span>

### <span data-ttu-id="034ff-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="034ff-121">-AsJob</span></span>
<span data-ttu-id="034ff-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="034ff-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="034ff-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="034ff-123">-DefaultProfile</span></span>
<span data-ttu-id="034ff-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="034ff-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="034ff-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="034ff-125">-IPAddressOrRange</span></span>
<span data-ttu-id="034ff-126">La matrice di IpAddressOrRange, Aggiungi IpRules con l'input IpAddressOrRange e l'azione predefinita consente di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="034ff-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="034ff-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="034ff-127">-IPRule</span></span>
<span data-ttu-id="034ff-128">Matrice di oggetti IpRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="034ff-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="034ff-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="034ff-129">-Name</span></span>
<span data-ttu-id="034ff-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="034ff-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="034ff-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="034ff-131">-ResourceGroupName</span></span>
<span data-ttu-id="034ff-132">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="034ff-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="034ff-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="034ff-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="034ff-134">La matrice di VirtualNetworkResourceId, aggiungerà VirtualNetworkRule con l'input VirtualNetworkResourceId e l'azione predefinita consentirà di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="034ff-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="034ff-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="034ff-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="034ff-136">Matrice di oggetti VirtualNetworkRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="034ff-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="034ff-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="034ff-137">-Confirm</span></span>
<span data-ttu-id="034ff-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="034ff-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="034ff-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="034ff-139">-WhatIf</span></span>
<span data-ttu-id="034ff-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="034ff-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="034ff-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="034ff-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="034ff-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="034ff-142">CommonParameters</span></span>
<span data-ttu-id="034ff-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="034ff-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="034ff-144">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="034ff-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="034ff-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="034ff-145">INPUTS</span></span>

### <span data-ttu-id="034ff-146">System. String</span><span class="sxs-lookup"><span data-stu-id="034ff-146">System.String</span></span>

### <span data-ttu-id="034ff-147">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="034ff-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="034ff-148">Parametri: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="034ff-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="034ff-149">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="034ff-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="034ff-150">Parametri: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="034ff-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="034ff-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="034ff-151">OUTPUTS</span></span>

### <span data-ttu-id="034ff-152">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="034ff-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="034ff-153">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="034ff-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="034ff-154">Note</span><span class="sxs-lookup"><span data-stu-id="034ff-154">NOTES</span></span>

## <span data-ttu-id="034ff-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="034ff-155">RELATED LINKS</span></span>
