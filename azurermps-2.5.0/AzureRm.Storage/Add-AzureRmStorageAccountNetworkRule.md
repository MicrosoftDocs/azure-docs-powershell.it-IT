---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/add-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 0b1d497bbd7e976d942bdc3f99c6bea2d4c2c1cb
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866190"
---
# <span data-ttu-id="aa06f-101">Add-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa06f-101">Add-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="aa06f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aa06f-102">SYNOPSIS</span></span>
 <span data-ttu-id="aa06f-103">Aggiungere IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa06f-103">Add IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aa06f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aa06f-104">SYNTAX</span></span>

### <span data-ttu-id="aa06f-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aa06f-105">NetWorkRuleString (Default)</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="aa06f-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="aa06f-106">IpRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa06f-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="aa06f-107">NetworkRuleObject</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa06f-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="aa06f-108">IpRuleString</span></span>
```
Add-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="aa06f-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aa06f-109">DESCRIPTION</span></span>
<span data-ttu-id="aa06f-110">Il cmdlet **Add-AzureRmStorageAccountNetworkRule** aggiunge IpRules o VirtualNetworkRules alla proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="aa06f-110">The **Add-AzureRmStorageAccountNetworkRule** cmdlet adds IpRules or VirtualNetworkRules to the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="aa06f-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aa06f-111">EXAMPLES</span></span>

### <span data-ttu-id="aa06f-112">Esempio 1: aggiungere diversi IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="aa06f-112">Example 1: Add several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPAddressOrRange "10.0.0.0/24","28.2.0.0/16"
```

<span data-ttu-id="aa06f-113">Questo comando aggiunge diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="aa06f-113">This command add several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="aa06f-114">Esempio 2: aggiungere un VirtualNetworkRule con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="aa06f-114">Example 2: Add a VirtualNetworkRule with VirtualNetworkResourceID</span></span>
```
PS C:\>$subnet = Get-AzureRmVirtualNetwork -ResourceGroupName "myResourceGroup" -Name "myvirtualnetwork" | Get-AzureRmVirtualNetworkSubnetConfig
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -VirtualNetworkResourceId $subnet[0].Id
```

<span data-ttu-id="aa06f-115">Questo comando aggiunge un VirtualNetworkRule con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="aa06f-115">This command add a VirtualNetworkRule with VirtualNetworkResourceID.</span></span>

### <span data-ttu-id="aa06f-116">Esempio 3: aggiungere VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account</span><span class="sxs-lookup"><span data-stu-id="aa06f-116">Example 3: Add VirtualNetworkRules with VirtualNetworkRule Objects from another account</span></span>
```
PS C:\> $networkrule = Get-AzureRMStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -Name "mystorageaccount1"
PS C:\> Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount2" -VirtualNetworkRule $networkrule.VirtualNetworkRules
```

<span data-ttu-id="aa06f-117">Questo comando aggiunge VirtualNetworkRules con oggetti VirtualNetworkRule da un altro account.</span><span class="sxs-lookup"><span data-stu-id="aa06f-117">This command add VirtualNetworkRules with VirtualNetworkRule Objects from another account.</span></span>

### <span data-ttu-id="aa06f-118">Esempio 4: aggiungere diversi IpRule con oggetti IpRule, input con JSON</span><span class="sxs-lookup"><span data-stu-id="aa06f-118">Example 4: Add several IpRule with IpRule objects, input with JSON</span></span>
```
PS C:\>Add-AzureRMStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -Name "mystorageaccount" -IPRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
```

<span data-ttu-id="aa06f-119">Questo comando aggiunge diversi IpRule con oggetti IpRule, input with JSON.</span><span class="sxs-lookup"><span data-stu-id="aa06f-119">This command add several IpRule with IpRule objects, input with JSON.</span></span>

## <span data-ttu-id="aa06f-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aa06f-120">PARAMETERS</span></span>

### <span data-ttu-id="aa06f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="aa06f-121">-AsJob</span></span>
<span data-ttu-id="aa06f-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="aa06f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="aa06f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa06f-123">-DefaultProfile</span></span>
<span data-ttu-id="aa06f-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aa06f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa06f-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="aa06f-125">-IPAddressOrRange</span></span>
<span data-ttu-id="aa06f-126">La matrice di IpAddressOrRange, Aggiungi IpRules con l'input IpAddressOrRange e l'azione predefinita consente di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="aa06f-126">The Array of IpAddressOrRange, add IpRules with the input IpAddressOrRange and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="aa06f-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="aa06f-127">-IPRule</span></span>
<span data-ttu-id="aa06f-128">Matrice di oggetti IpRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="aa06f-128">The Array of IpRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="aa06f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="aa06f-129">-Name</span></span>
<span data-ttu-id="aa06f-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa06f-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="aa06f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aa06f-131">-ResourceGroupName</span></span>
<span data-ttu-id="aa06f-132">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="aa06f-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="aa06f-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="aa06f-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="aa06f-134">La matrice di VirtualNetworkResourceId, aggiungerà VirtualNetworkRule con l'input VirtualNetworkResourceId e l'azione predefinita consentirà di NetworkRule proprietà.</span><span class="sxs-lookup"><span data-stu-id="aa06f-134">The Array of VirtualNetworkResourceId, will add VirtualNetworkRule with input VirtualNetworkResourceId and default Action Allow to NetworkRule Property.</span></span>

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

### <span data-ttu-id="aa06f-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa06f-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="aa06f-136">Matrice di oggetti VirtualNetworkRule da aggiungere alla proprietà NetworkRule.</span><span class="sxs-lookup"><span data-stu-id="aa06f-136">The Array of VirtualNetworkRule objects to add to the NetworkRule Property.</span></span>

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

### <span data-ttu-id="aa06f-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aa06f-137">-Confirm</span></span>
<span data-ttu-id="aa06f-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa06f-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa06f-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa06f-139">-WhatIf</span></span>
<span data-ttu-id="aa06f-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa06f-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa06f-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aa06f-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa06f-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa06f-142">CommonParameters</span></span>
<span data-ttu-id="aa06f-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa06f-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa06f-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aa06f-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa06f-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aa06f-145">INPUTS</span></span>

### <span data-ttu-id="aa06f-146">System. String</span><span class="sxs-lookup"><span data-stu-id="aa06f-146">System.String</span></span>

### <span data-ttu-id="aa06f-147">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="aa06f-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="aa06f-148">Parametri: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa06f-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="aa06f-149">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="aa06f-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="aa06f-150">Parametri: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="aa06f-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="aa06f-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aa06f-151">OUTPUTS</span></span>

### <span data-ttu-id="aa06f-152">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="aa06f-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="aa06f-153">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="aa06f-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="aa06f-154">Note</span><span class="sxs-lookup"><span data-stu-id="aa06f-154">NOTES</span></span>

## <span data-ttu-id="aa06f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aa06f-155">RELATED LINKS</span></span>
