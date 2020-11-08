---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/update-azstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Update-AzStorageAccountNetworkRuleSet.md
ms.openlocfilehash: 04611df4dd315c972d9e32b280d635a6ecd0ed21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94188718"
---
# <span data-ttu-id="f3fb0-101">Update-AzStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3fb0-101">Update-AzStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="f3fb0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f3fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fb0-103">Aggiornare la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f3fb0-103">Update the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f3fb0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-104">SYNTAX</span></span>

```
Update-AzStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3fb0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f3fb0-105">DESCRIPTION</span></span>
<span data-ttu-id="f3fb0-106">Il cmdlet **Update-AzStorageAccountNetworkRuleSet** aggiorna la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f3fb0-106">The **Update-AzStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="f3fb0-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-107">EXAMPLES</span></span>

### <span data-ttu-id="f3fb0-108">Esempio 1: aggiornare tutte le proprietà di NetworkRule, regole di input con JSON</span><span class="sxs-lookup"><span data-stu-id="f3fb0-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkResourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="f3fb0-109">Questo comando Aggiorna tutte le proprietà di NetworkRule, regole di input con JSON.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="f3fb0-110">Esempio 2: Proprietà Update bypass di NetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3fb0-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="f3fb0-111">Questa proprietà di aggiornamento dei comandi di NetworkRule (altre proprietà non cambieranno).</span><span class="sxs-lookup"><span data-stu-id="f3fb0-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="f3fb0-112">Esempio 3: pulire le regole di NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f3fb0-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="f3fb0-113">Questo comando pulisce le regole di NetworkRule di un account di archiviazione (altre proprietà non cambiano).</span><span class="sxs-lookup"><span data-stu-id="f3fb0-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="f3fb0-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-114">PARAMETERS</span></span>

### <span data-ttu-id="f3fb0-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3fb0-115">-AsJob</span></span>
<span data-ttu-id="f3fb0-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="f3fb0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3fb0-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="f3fb0-117">-Bypass</span></span>
<span data-ttu-id="f3fb0-118">Il valore di bypass da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="f3fb0-119">Il valore consentito è None o qualsiasi combinazione di: • registrazione • metriche • Azureservices</span><span class="sxs-lookup"><span data-stu-id="f3fb0-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="f3fb0-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="f3fb0-120">-DefaultAction</span></span>
<span data-ttu-id="f3fb0-121">Valore DefaultAction da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="f3fb0-122">Opzioni consentite: • Consenti • Nega</span><span class="sxs-lookup"><span data-stu-id="f3fb0-122">The allowed Options: • Allow • Deny</span></span>

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

### <span data-ttu-id="f3fb0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fb0-123">-DefaultProfile</span></span>
<span data-ttu-id="f3fb0-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3fb0-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="f3fb0-125">-IPRule</span></span>
<span data-ttu-id="f3fb0-126">Matrice di oggetti IpRule da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="f3fb0-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="f3fb0-127">-Name</span></span>
<span data-ttu-id="f3fb0-128">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="f3fb0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3fb0-129">-ResourceGroupName</span></span>
<span data-ttu-id="f3fb0-130">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="f3fb0-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="f3fb0-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="f3fb0-132">Matrice di oggetti VirtualNetworkRule da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="f3fb0-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f3fb0-133">-Confirm</span></span>
<span data-ttu-id="f3fb0-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3fb0-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3fb0-135">-WhatIf</span></span>
<span data-ttu-id="f3fb0-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3fb0-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3fb0-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fb0-138">CommonParameters</span></span>
<span data-ttu-id="f3fb0-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3fb0-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fb0-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3fb0-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fb0-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-141">INPUTS</span></span>

### <span data-ttu-id="f3fb0-142">System. String</span><span class="sxs-lookup"><span data-stu-id="f3fb0-142">System.String</span></span>

### <span data-ttu-id="f3fb0-143">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="f3fb0-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>

### <span data-ttu-id="f3fb0-144">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="f3fb0-144">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>

## <span data-ttu-id="f3fb0-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f3fb0-145">OUTPUTS</span></span>

### <span data-ttu-id="f3fb0-146">Microsoft. Azure. Commands. Management. storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="f3fb0-146">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="f3fb0-147">Note</span><span class="sxs-lookup"><span data-stu-id="f3fb0-147">NOTES</span></span>

## <span data-ttu-id="f3fb0-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f3fb0-148">RELATED LINKS</span></span>
