---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstorageaccountnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageAccountNetworkRuleSet.md
ms.openlocfilehash: d167061692e3d5cccfd54a3f990af8312446ac67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517291"
---
# <span data-ttu-id="32b87-101">Update-AzureRmStorageAccountNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="32b87-101">Update-AzureRmStorageAccountNetworkRuleSet</span></span>

## <span data-ttu-id="32b87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="32b87-102">SYNOPSIS</span></span>
<span data-ttu-id="32b87-103">Aggiornare la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="32b87-103">Update the NetworkRule property of a Storage account</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32b87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="32b87-104">SYNTAX</span></span>

```
Update-AzureRmStorageAccountNetworkRuleSet [-ResourceGroupName] <String> [-Name] <String>
 [-Bypass <PSNetWorkRuleBypassEnum>] [-DefaultAction <PSNetWorkRuleDefaultActionEnum>] [-IPRule <PSIpRule[]>]
 [-VirtualNetworkRule <PSVirtualNetworkRule[]>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="32b87-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="32b87-105">DESCRIPTION</span></span>
<span data-ttu-id="32b87-106">Il cmdlet **Update-AzureRmStorageAccountNetworkRuleSet** aggiorna la proprietà NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="32b87-106">The **Update-AzureRmStorageAccountNetworkRuleSet** cmdlet updates the NetworkRule property of a Storage account</span></span>

## <span data-ttu-id="32b87-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="32b87-107">EXAMPLES</span></span>

### <span data-ttu-id="32b87-108">Esempio 1: aggiornare tutte le proprietà di NetworkRule, regole di input con JSON</span><span class="sxs-lookup"><span data-stu-id="32b87-108">Example 1: Update all properties of NetworkRule, input Rules with JSON</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass Logging,Metrics -DefaultAction Allow -IpRule (@{IPAddressOrRange="10.0.0.0/24";Action="allow"},@{IPAddressOrRange="28.2.0.0/16";Action="allow"})
    -VirtualNetworkRule (@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualNetworks/vnet1/subnets/subnet1";Action="allow"},@{VirtualNetworkReourceId="/subscriptions/s1/resourceGroups/g1/providers/Microsoft.Network/virtualN
    etworks/vnet2/subnets/subnet2";Action="allow"})
```

<span data-ttu-id="32b87-109">Questo comando Aggiorna tutte le proprietà di NetworkRule, regole di input con JSON.</span><span class="sxs-lookup"><span data-stu-id="32b87-109">This command update all properties of NetworkRule, input Rules with JSON.</span></span>

### <span data-ttu-id="32b87-110">Esempio 2: Proprietà Update bypass di NetworkRule</span><span class="sxs-lookup"><span data-stu-id="32b87-110">Example 2: Update Bypass property of NetworkRule</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -Bypass AzureServices,Metrics
```

<span data-ttu-id="32b87-111">Questa proprietà di aggiornamento dei comandi di NetworkRule (altre proprietà non cambieranno).</span><span class="sxs-lookup"><span data-stu-id="32b87-111">This command update Bypass property of NetworkRule (other properties won't change).</span></span>

### <span data-ttu-id="32b87-112">Esempio 3: pulire le regole di NetworkRule di un account di archiviazione</span><span class="sxs-lookup"><span data-stu-id="32b87-112">Example 3: Clean up rules of NetworkRule of a Storage account</span></span>
```
PS C:\> Update-AzureRmStorageAccountNetworkRuleSet -ResourceGroupName "myResourceGroup" -AccountName "mystorageaccount" -IpRule @() -VirtualNetworkRule @()
```

<span data-ttu-id="32b87-113">Questo comando pulisce le regole di NetworkRule di un account di archiviazione (altre proprietà non cambiano).</span><span class="sxs-lookup"><span data-stu-id="32b87-113">This command clean up rules of NetworkRule of a Storage account (other properties not change).</span></span>

## <span data-ttu-id="32b87-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="32b87-114">PARAMETERS</span></span>

### <span data-ttu-id="32b87-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="32b87-115">-AsJob</span></span>
<span data-ttu-id="32b87-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="32b87-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="32b87-117">-Bypass</span><span class="sxs-lookup"><span data-stu-id="32b87-117">-Bypass</span></span>
<span data-ttu-id="32b87-118">Il valore di bypass da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32b87-118">The Bypass value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="32b87-119">Il valore consentito è None o qualsiasi combinazione di: • registrazione • metriche • Azureservices</span><span class="sxs-lookup"><span data-stu-id="32b87-119">The allowed value are none or any combination of: • Logging • Metrics • Azureservices</span></span>

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

### <span data-ttu-id="32b87-120">-DefaultAction</span><span class="sxs-lookup"><span data-stu-id="32b87-120">-DefaultAction</span></span>
<span data-ttu-id="32b87-121">Valore DefaultAction da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32b87-121">The DefaultAction value to update to the NetworkRule property of a Storage account.</span></span>
<span data-ttu-id="32b87-122">Opzioni consentite: • Consenti • Nega</span><span class="sxs-lookup"><span data-stu-id="32b87-122">The allowed Options: • Allow • Deny</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSNetWorkRuleDefaultActionEnum
Parameter Sets: (All)
Aliases:
Accepted values: Deny, Allow

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32b87-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32b87-123">-DefaultProfile</span></span>
<span data-ttu-id="32b87-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="32b87-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32b87-125">-IPRule</span><span class="sxs-lookup"><span data-stu-id="32b87-125">-IPRule</span></span>
<span data-ttu-id="32b87-126">Matrice di oggetti IpRule da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32b87-126">The Array of IpRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="32b87-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="32b87-127">-Name</span></span>
<span data-ttu-id="32b87-128">Specifica il nome dell'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32b87-128">Specifies the name of the Storage account.</span></span>

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

### <span data-ttu-id="32b87-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32b87-129">-ResourceGroupName</span></span>
<span data-ttu-id="32b87-130">Specifica il nome del gruppo di risorse che contiene l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32b87-130">Specifies the name of the resource group contains the Storage account.</span></span>

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

### <span data-ttu-id="32b87-131">-VirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="32b87-131">-VirtualNetworkRule</span></span>
<span data-ttu-id="32b87-132">Matrice di oggetti VirtualNetworkRule da aggiornare alla proprietà NetworkRule di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="32b87-132">The Array of VirtualNetworkRule objects to update to the NetworkRule Property of a Storage account.</span></span>

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

### <span data-ttu-id="32b87-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="32b87-133">-Confirm</span></span>
<span data-ttu-id="32b87-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32b87-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32b87-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32b87-135">-WhatIf</span></span>
<span data-ttu-id="32b87-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32b87-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32b87-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="32b87-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32b87-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32b87-138">CommonParameters</span></span>
<span data-ttu-id="32b87-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32b87-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32b87-140">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32b87-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32b87-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="32b87-141">INPUTS</span></span>

### <span data-ttu-id="32b87-142">System. String</span><span class="sxs-lookup"><span data-stu-id="32b87-142">System.String</span></span>

### <span data-ttu-id="32b87-143">Microsoft. Azure. Commands. Management. storage. Models. PSIpRule []</span><span class="sxs-lookup"><span data-stu-id="32b87-143">Microsoft.Azure.Commands.Management.Storage.Models.PSIpRule[]</span></span>
<span data-ttu-id="32b87-144">Parametri: IPRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32b87-144">Parameters: IPRule (ByValue)</span></span>

### <span data-ttu-id="32b87-145">Microsoft. Azure. Commands. Management. storage. Models. PSVirtualNetworkRule []</span><span class="sxs-lookup"><span data-stu-id="32b87-145">Microsoft.Azure.Commands.Management.Storage.Models.PSVirtualNetworkRule[]</span></span>
<span data-ttu-id="32b87-146">Parametri: VirtualNetworkRule (ByValue)</span><span class="sxs-lookup"><span data-stu-id="32b87-146">Parameters: VirtualNetworkRule (ByValue)</span></span>

## <span data-ttu-id="32b87-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="32b87-147">OUTPUTS</span></span>

### <span data-ttu-id="32b87-148">Microsoft. Azure. Commands. Management. storage. Models. PSNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="32b87-148">Microsoft.Azure.Commands.Management.Storage.Models.PSNetworkRuleSet</span></span>

## <span data-ttu-id="32b87-149">Note</span><span class="sxs-lookup"><span data-stu-id="32b87-149">NOTES</span></span>

## <span data-ttu-id="32b87-150">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="32b87-150">RELATED LINKS</span></span>
