---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageAccountNetworkRule.md
ms.openlocfilehash: c0240d18e1e02be9426e2d6aaaca22821458cd25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685798"
---
# <span data-ttu-id="1e4cd-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e4cd-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="1e4cd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e4cd-102">SYNOPSIS</span></span>
<span data-ttu-id="1e4cd-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1e4cd-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e4cd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-104">SYNTAX</span></span>

### <span data-ttu-id="1e4cd-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e4cd-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e4cd-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="1e4cd-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4cd-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="1e4cd-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e4cd-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="1e4cd-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e4cd-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e4cd-109">DESCRIPTION</span></span>
<span data-ttu-id="1e4cd-110">Il cmdlet **Remove-AzureRmStorageAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1e4cd-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="1e4cd-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-111">EXAMPLES</span></span>

### <span data-ttu-id="1e4cd-112">Esempio 1: rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1e4cd-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="1e4cd-113">Questo comando rimuove diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="1e4cd-114">Esempio 2: rimuovere un VirtualNetworkRule con l'input di oggetti VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="1e4cd-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="1e4cd-115">Questo comando rimuove un VirtualNetworkRule con l'input di oggetti VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="1e4cd-116">Esempio 3: rimuovere First IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="1e4cd-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="1e4cd-117">Questo comando rimuove prima IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="1e4cd-118">Esempio 4: rimuovere più VirtualNetworkRules con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="1e4cd-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="1e4cd-119">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="1e4cd-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-120">PARAMETERS</span></span>

### <span data-ttu-id="1e4cd-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e4cd-121">-AsJob</span></span>
<span data-ttu-id="1e4cd-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1e4cd-122">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e4cd-123">-DefaultProfile</span></span>
<span data-ttu-id="1e4cd-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="1e4cd-125">-IPAddressOrRange</span></span>
<span data-ttu-id="1e4cd-126">La matrice di IpAddressOrRange eliminerà IpRule con lo stesso IpAddressOrRange dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: IpRuleString
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="1e4cd-127">-IPRule</span></span>
<span data-ttu-id="1e4cd-128">Matrice di oggetti IpRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: PSIpRule[]
Parameter Sets: IpRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e4cd-129">-Name</span></span>
<span data-ttu-id="1e4cd-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-130">Specifies the name of the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e4cd-131">-ResourceGroupName</span></span>
<span data-ttu-id="1e4cd-132">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-132">Specifies the name of the resource group contains the Storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="1e4cd-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="1e4cd-134">La matrice di VirtualNetworkResourceId eliminerà VirtualNetworkRule con lo stesso VirtualNetworkResourceId dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

```yaml
Type: String[]
Parameter Sets: NetWorkRuleString
Aliases: SubnetId, VirtualNetworkId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e4cd-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="1e4cd-136">Matrice di oggetti VirtualNetworkRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

```yaml
Type: PSVirtualNetworkRule[]
Parameter Sets: NetworkRuleObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e4cd-137">-Confirm</span></span>
<span data-ttu-id="1e4cd-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e4cd-139">-WhatIf</span></span>
<span data-ttu-id="1e4cd-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e4cd-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-141">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e4cd-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e4cd-142">CommonParameters</span></span>
<span data-ttu-id="1e4cd-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e4cd-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e4cd-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e4cd-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e4cd-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-145">INPUTS</span></span>

### <span data-ttu-id="1e4cd-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1e4cd-146">System.String</span></span>
<span data-ttu-id="1e4cd-147">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule [] Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="1e4cd-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[] Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="1e4cd-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e4cd-148">OUTPUTS</span></span>

### <span data-ttu-id="1e4cd-149">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="1e4cd-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>
<span data-ttu-id="1e4cd-150">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="1e4cd-150">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="1e4cd-151">Note</span><span class="sxs-lookup"><span data-stu-id="1e4cd-151">NOTES</span></span>

## <span data-ttu-id="1e4cd-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e4cd-152">RELATED LINKS</span></span>
