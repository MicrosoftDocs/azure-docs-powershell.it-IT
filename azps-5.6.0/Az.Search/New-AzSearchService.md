---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchService.md
ms.openlocfilehash: 61101242b100ca4b477910a0dfa339ef7f9ea81b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957998"
---
# <span data-ttu-id="e993a-101">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e993a-101">New-AzSearchService</span></span>

## <span data-ttu-id="e993a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e993a-102">SYNOPSIS</span></span>
<span data-ttu-id="e993a-103">Crea un servizio Di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-103">Creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e993a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e993a-104">SYNTAX</span></span>

```
New-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-Sku] <PSSkuName> [-Location] <String>
 [-PartitionCount <Int32>] [-ReplicaCount <Int32>] [-HostingMode <PSHostingMode>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e993a-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e993a-105">DESCRIPTION</span></span>
<span data-ttu-id="e993a-106">Il cmdlet **New-AzSearchService** crea un servizio di Ricerca cognitiva di Azure con parametri specificati.</span><span class="sxs-lookup"><span data-stu-id="e993a-106">The **New-AzSearchService** cmdlet creates an Azure Cognitive Search service with specified parameters.</span></span>

## <span data-ttu-id="e993a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e993a-107">EXAMPLES</span></span>

### <span data-ttu-id="e993a-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e993a-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -Sku "Standard" -Location "West US" -PartitionCount 1 -ReplicaCount 1 -HostingMode Default -Force


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 1
PartitionCount    : 1
HostingMode       : Default
Tags              :
```

<span data-ttu-id="e993a-109">Il comando crea un servizio di Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-109">The command creates an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="e993a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e993a-110">PARAMETERS</span></span>

### <span data-ttu-id="e993a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e993a-111">-DefaultProfile</span></span>
<span data-ttu-id="e993a-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e993a-113">-HostingMode</span><span class="sxs-lookup"><span data-stu-id="e993a-113">-HostingMode</span></span>
<span data-ttu-id="e993a-114">Modalità di hosting del servizio Cognitivo di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-114">Azure Cognitive Search Service hosting mode.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSHostingMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, HighDensity

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-115">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="e993a-115">-IdentityType</span></span>
<span data-ttu-id="e993a-116">(Facoltativo) Identità del servizio Ricerca cognitiva di Azure (nessuna/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="e993a-116">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSIdentityType]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-117">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="e993a-117">-IPRuleList</span></span>
<span data-ttu-id="e993a-118">(Facoltativo) Regole IP del servizio ricerca cognitiva di Azure</span><span class="sxs-lookup"><span data-stu-id="e993a-118">(Optional) Azure Cognitive Search Service IP rules</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSIpRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-119">-Location</span><span class="sxs-lookup"><span data-stu-id="e993a-119">-Location</span></span>
<span data-ttu-id="e993a-120">Percorso del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-120">Azure Cognitive Search Service location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="e993a-121">-Name</span></span>
<span data-ttu-id="e993a-122">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-122">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-123">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="e993a-123">-PartitionCount</span></span>
<span data-ttu-id="e993a-124">Numero di partizioni del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-124">Azure Cognitive Search Service partition count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="e993a-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="e993a-126">(Facoltativo) Accesso alla rete pubblica del servizio Cognitivo di Azure (abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="e993a-126">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Management.Search.Models.PSPublicNetworkAccess]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-127">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="e993a-127">-ReplicaCount</span></span>
<span data-ttu-id="e993a-128">Numero di replica del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-128">Azure Cognitive Search Service replica count.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e993a-129">-ResourceGroupName</span></span>
<span data-ttu-id="e993a-130">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e993a-130">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="e993a-131">-Sku</span></span>
<span data-ttu-id="e993a-132">SKU del servizio ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="e993a-132">Azure Cognitive Search Service Sku.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSkuName
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard, Standard2, Standard3

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e993a-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e993a-133">-Confirm</span></span>
<span data-ttu-id="e993a-134">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e993a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e993a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e993a-135">-WhatIf</span></span>
<span data-ttu-id="e993a-136">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e993a-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e993a-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e993a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e993a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e993a-138">CommonParameters</span></span>
<span data-ttu-id="e993a-139">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e993a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e993a-140">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e993a-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e993a-141">INPUT</span><span class="sxs-lookup"><span data-stu-id="e993a-141">INPUTS</span></span>

### <span data-ttu-id="e993a-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e993a-142">None</span></span>

## <span data-ttu-id="e993a-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e993a-143">OUTPUTS</span></span>

### <span data-ttu-id="e993a-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="e993a-144">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="e993a-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="e993a-145">NOTES</span></span>

## <span data-ttu-id="e993a-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e993a-146">RELATED LINKS</span></span>

[<span data-ttu-id="e993a-147">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e993a-147">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="e993a-148">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e993a-148">Set-AzSearchService</span></span>](./Set-AzSearchService.md)

[<span data-ttu-id="e993a-149">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="e993a-149">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)