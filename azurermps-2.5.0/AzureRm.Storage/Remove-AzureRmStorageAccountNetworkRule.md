---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstorageaccountnetworkrule
schema: 2.0.0
ms.openlocfilehash: 6fd79e458c4ac288c6bc8f26add140e8f0a695ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865870"
---
# <span data-ttu-id="9b4bb-101">Remove-AzureRmStorageAccountNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9b4bb-101">Remove-AzureRmStorageAccountNetworkRule</span></span>

## <span data-ttu-id="9b4bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9b4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="9b4bb-103">Rimuovere IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9b4bb-103">Remove IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b4bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b4bb-104">SYNTAX</span></span>

### <span data-ttu-id="9b4bb-105">NetWorkRuleString (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9b4bb-105">NetWorkRuleString (Default)</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkResourceId <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9b4bb-106">IpRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b4bb-106">IpRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String> -IPRule <PSIpRule[]>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b4bb-107">NetworkRuleObject</span><span class="sxs-lookup"><span data-stu-id="9b4bb-107">NetworkRuleObject</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -VirtualNetworkRule <PSVirtualNetworkRule[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9b4bb-108">IpRuleString</span><span class="sxs-lookup"><span data-stu-id="9b4bb-108">IpRuleString</span></span>
```
Remove-AzureRmStorageAccountNetworkRule [-ResourceGroupName] <String> [-Name] <String>
 -IPAddressOrRange <String[]> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9b4bb-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9b4bb-109">DESCRIPTION</span></span>
<span data-ttu-id="9b4bb-110">Il cmdlet **Remove-AzureRmStorageAccountNetworkRule** rimuove IpRules o VirtualNetworkRules dalla proprietà NetWorkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="9b4bb-110">The **Remove-AzureRmStorageAccountNetworkRule** cmdlet removes IpRules or VirtualNetworkRules from the NetWorkRule property of a Storage account</span></span>

## <span data-ttu-id="9b4bb-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b4bb-111">EXAMPLES</span></span>

### <span data-ttu-id="9b4bb-112">Esempio 1: rimuovere più IpRules con IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9b4bb-112">Example 1: Remove several IpRules with IPAddressOrRange</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IPAddressOrRange "10.0.0.0/24,28.1.0.0/16"
```

<span data-ttu-id="9b4bb-113">Questo comando rimuove diversi IpRules con IPAddressOrRange.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-113">This command remove several IpRules with IPAddressOrRange.</span></span>

### <span data-ttu-id="9b4bb-114">Esempio 2: rimuovere un VirtualNetworkRule con l'input di oggetti VirtualNetworkRule con JSON</span><span class="sxs-lookup"><span data-stu-id="9b4bb-114">Example 2: Remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkRules (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"})
```

<span data-ttu-id="9b4bb-115">Questo comando rimuove un VirtualNetworkRule con l'input di oggetti VirtualNetworkRule con JSON.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-115">This command remove a VirtualNetworkRule with VirtualNetworkRule Object input with JSON.</span></span>

### <span data-ttu-id="9b4bb-116">Esempio 3: rimuovere First IpRule con pipeline</span><span class="sxs-lookup"><span data-stu-id="9b4bb-116">Example 3: Remove first IpRule with pipeline</span></span>
```
PS C:\>(Get-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount").IpRules[0] | Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
```

<span data-ttu-id="9b4bb-117">Questo comando rimuove prima IpRule con pipeline.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-117">This command remove first IpRule with pipeline.</span></span>

### <span data-ttu-id="9b4bb-118">Esempio 4: rimuovere più VirtualNetworkRules con VirtualNetworkResourceID</span><span class="sxs-lookup"><span data-stu-id="9b4bb-118">Example 4: Remove several VirtualNetworkRules with VirtualNetworkResourceID</span></span>
```
PS C:\>Remove-AzureRmStorageAccountNetworkRule -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -VirtualNetworkResourceId "/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1","/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet2/subnets/subnet2"
```

<span data-ttu-id="9b4bb-119">Questo comando rimuove diversi VirtualNetworkRules con VirtualNetworkResourceID.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-119">This command remove several VirtualNetworkRules with VirtualNetworkResourceID.</span></span>

## <span data-ttu-id="9b4bb-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9b4bb-120">PARAMETERS</span></span>

### <span data-ttu-id="9b4bb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b4bb-121">-AsJob</span></span>
<span data-ttu-id="9b4bb-122">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="9b4bb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9b4bb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b4bb-123">-DefaultProfile</span></span>
<span data-ttu-id="9b4bb-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b4bb-125">-IPAddressOrRange</span><span class="sxs-lookup"><span data-stu-id="9b4bb-125">-IPAddressOrRange</span></span>
<span data-ttu-id="9b4bb-126">La matrice di IpAddressOrRange eliminerà IpRule con lo stesso IpAddressOrRange dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-126">The Array of IpAddressOrRange, will remove IpRule with same IpAddressOrRange from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9b4bb-127">-IPRule</span><span class="sxs-lookup"><span data-stu-id="9b4bb-127">-IPRule</span></span>
<span data-ttu-id="9b4bb-128">Matrice di oggetti IpRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-128">The Array of IpRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9b4bb-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="9b4bb-129">-Name</span></span>
<span data-ttu-id="9b4bb-130">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-130">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="9b4bb-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b4bb-131">-ResourceGroupName</span></span>
<span data-ttu-id="9b4bb-132">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-132">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="9b4bb-133">-VirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="9b4bb-133">-VirtualNetworkResourceId</span></span>
<span data-ttu-id="9b4bb-134">La matrice di VirtualNetworkResourceId eliminerà VirtualNetworkRule con lo stesso VirtualNetworkResourceId dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-134">The Array of VirtualNetworkResourceId, will remove VirtualNetworkRule with same VirtualNetworkResourceId from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9b4bb-135">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9b4bb-135">-VirtualNetworkRule</span></span>
<span data-ttu-id="9b4bb-136">Matrice di oggetti VirtualNetworkRule da rimuovere dalla proprietà NetWorkRule.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-136">The Array of VirtualNetworkRule objects to remove from the NetWorkRule Property.</span></span>

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

### <span data-ttu-id="9b4bb-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="9b4bb-137">-Confirm</span></span>
<span data-ttu-id="9b4bb-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b4bb-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b4bb-139">-WhatIf</span></span>
<span data-ttu-id="9b4bb-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b4bb-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b4bb-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b4bb-142">CommonParameters</span></span>
<span data-ttu-id="9b4bb-143">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b4bb-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b4bb-144">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b4bb-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b4bb-145">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9b4bb-145">INPUTS</span></span>

### <span data-ttu-id="9b4bb-146">System. String</span><span class="sxs-lookup"><span data-stu-id="9b4bb-146">System.String</span></span>

### <span data-ttu-id="9b4bb-147">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="9b4bb-147">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="9b4bb-148">Parametri: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b4bb-148">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="9b4bb-149">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="9b4bb-149">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="9b4bb-150">Parametri: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b4bb-150">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="9b4bb-151">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b4bb-151">OUTPUTS</span></span>

### <span data-ttu-id="9b4bb-152">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="9b4bb-152">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule</span></span>

### <span data-ttu-id="9b4bb-153">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule</span><span class="sxs-lookup"><span data-stu-id="9b4bb-153">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule</span></span>

## <span data-ttu-id="9b4bb-154">Note</span><span class="sxs-lookup"><span data-stu-id="9b4bb-154">NOTES</span></span>

## <span data-ttu-id="9b4bb-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b4bb-155">RELATED LINKS</span></span>
