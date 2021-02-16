---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197486"
---
# <span data-ttu-id="d865c-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d865c-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="d865c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d865c-102">SYNOPSIS</span></span>
<span data-ttu-id="d865c-103">Aggiornare la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d865c-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d865c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d865c-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d865c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d865c-105">DESCRIPTION</span></span>
<span data-ttu-id="d865c-106">Il cmdlet **Update-AzStorageAccountNetworkRuleSet** aggiorna la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d865c-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="d865c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d865c-107">EXAMPLES</span></span>

### <span data-ttu-id="d865c-108">Esempio 1: Aggiornare tutte le proprietà di NetworkRule, regole di input con JSON</span><span class="sxs-lookup"><span data-stu-id="d865c-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="d865c-109">Questo comando aggiorna tutte le proprietà di NetworkRule, regole di input con JSON.</span><span class="sxs-lookup"><span data-stu-id="d865c-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="d865c-110">Esempio 2: Proprietà Bypass di aggiornamento di NetworkRule</span><span class="sxs-lookup"><span data-stu-id="d865c-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="d865c-111">Questo comando aggiorna la proprietà Bypass di NetworkRule (le altre proprietà non vengono modificate).</span><span class="sxs-lookup"><span data-stu-id="d865c-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="d865c-112">Esempio 3: Pulire le regole di NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="d865c-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="d865c-113">Questo comando pulisce le regole di NetworkRule di un account di archiviazione (le altre proprietà non vengono modificate).</span><span class="sxs-lookup"><span data-stu-id="d865c-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="d865c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d865c-114">PARAMETERS</span></span>

### <span data-ttu-id="d865c-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d865c-115">-AsJob</span></span>
<span data-ttu-id="d865c-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d865c-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d865c-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="d865c-117">-Bypass</span></span>
<span data-ttu-id="d865c-118">Valore Bypass da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d865c-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="d865c-119">Il valore consentito non è né alcuno né una combinazione di: • Registrazione • Metriche • Azureservices</span><span class="sxs-lookup"><span data-stu-id="d865c-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleBypassEnum
Parameter Sets: (All)
Aliases:
Accepted values: None, Logging, Metrics, AzureServices

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d865c-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="d865c-120">-DefaultAction</span></span>
<span data-ttu-id="d865c-121">Valore DefaultAction da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d865c-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="d865c-122">Opzioni consentite: • Consenti • Nega</span><span class="sxs-lookup"><span data-stu-id="d865c-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Allow, Deny

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d865c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d865c-123">-DefaultProfile</span></span>
<span data-ttu-id="d865c-124">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d865c-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d865c-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="d865c-125">-IPRule</span></span>
<span data-ttu-id="d865c-126">Matrice di oggetti IpRule da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d865c-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d865c-127">-Name</span><span class="sxs-lookup"><span data-stu-id="d865c-127">-Name</span></span>
<span data-ttu-id="d865c-128">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d865c-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="d865c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d865c-129">-ResourceGroupName</span></span>
<span data-ttu-id="d865c-130">Specifica che il nome del gruppo di risorse contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d865c-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="d865c-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="d865c-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="d865c-132">Matrice di oggetti VirtualNetworkRule da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d865c-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d865c-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d865c-133">-Confirm</span></span>
<span data-ttu-id="d865c-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d865c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d865c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d865c-135">-WhatIf</span></span>
<span data-ttu-id="d865c-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d865c-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d865c-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d865c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d865c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d865c-138">CommonParameters</span></span>
<span data-ttu-id="d865c-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d865c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d865c-140">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d865c-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d865c-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="d865c-141">INPUTS</span></span>

### <span data-ttu-id="d865c-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d865c-142">System.String</span></span>

### <span data-ttu-id="d865c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span><span class="sxs-lookup"><span data-stu-id="d865c-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="d865c-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span><span class="sxs-lookup"><span data-stu-id="d865c-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="d865c-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d865c-145">OUTPUTS</span></span>

### <span data-ttu-id="d865c-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d865c-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="d865c-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="d865c-147">NOTES</span></span>

## <span data-ttu-id="d865c-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d865c-148">RELATED LINKS</span></span>
