---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchService.md
ms.openlocfilehash: 60969665c2989e026af3334e38e1d3035467b25b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178671"
---
# <span data-ttu-id="27b95-101">Set-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="27b95-101">Set-AzSearchService</span></span>

## <span data-ttu-id="27b95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27b95-102">SYNOPSIS</span></span>
<span data-ttu-id="27b95-103">Aggiornare un servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="27b95-103">Update an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="27b95-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27b95-104">SYNTAX</span></span>

### <span data-ttu-id="27b95-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27b95-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchService [-ResourceGroupName] <String> [-Name] <String> [-PartitionCount <Int32>]
 [-ReplicaCount <Int32>] [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>]
 [-IPRuleList <PSIpRule[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27b95-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b95-106">InputObjectParameterSet</span></span>
```
Set-AzSearchService [-InputObject] <PSSearchService> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27b95-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27b95-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchService [-ResourceId] <String> [-PartitionCount <Int32>] [-ReplicaCount <Int32>]
 [-PublicNetworkAccess <PSPublicNetworkAccess>] [-IdentityType <PSIdentityType>] [-IPRuleList <PSIpRule[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27b95-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="27b95-108">DESCRIPTION</span></span>
<span data-ttu-id="27b95-109">Il cmdlet **Set-AzSearchService** modifica un servizio di Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="27b95-109">The **Set-AzSearchService** cmdlet modifies an Azure Cognitive Search service.</span></span>

## <span data-ttu-id="27b95-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27b95-110">EXAMPLES</span></span>

### <span data-ttu-id="27b95-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="27b95-111">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchService -ResourceGroupName "TestAzureSearchPsGroup" -Name "pstestazuresearch01" -PartitionCount 2 -ReplicaCount 2


ResourceGroupName : TestAzureSearchPsGroup
Name              : pstestazuresearch01
Id                : /subscriptions/f9b96b36-1f5e-4021-8959-51527e26e6d3/resourceGroups/TestAzureSearchPsGroup/providers/Microsoft.Search/searchServices/pstestazuresearch01
Location          : West US
Sku               : Standard
ReplicaCount      : 2
PartitionCount    : 2
HostingMode       : Default
Tags              :
```

<span data-ttu-id="27b95-112">L'esempio modifica il numero di partizioni e il numero di replica del servizio Ricerca cognitiva di Azure in 2.</span><span class="sxs-lookup"><span data-stu-id="27b95-112">The example changes partition count and replica count of the Azure Cognitive Search service to 2.</span></span>

## <span data-ttu-id="27b95-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="27b95-113">PARAMETERS</span></span>

### <span data-ttu-id="27b95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27b95-114">-DefaultProfile</span></span>
<span data-ttu-id="27b95-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="27b95-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27b95-116">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="27b95-116">-IdentityType</span></span>
<span data-ttu-id="27b95-117">(Facoltativo) Identità del servizio Ricerca cognitiva di Azure (nessuna/SystemAssigned)</span><span class="sxs-lookup"><span data-stu-id="27b95-117">(Optional) Azure Cognitive Search Service Identity (None/SystemAssigned)</span></span>

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

### <span data-ttu-id="27b95-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="27b95-118">-InputObject</span></span>
<span data-ttu-id="27b95-119">Oggetto di input del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="27b95-119">Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="27b95-120">-IPRuleList</span><span class="sxs-lookup"><span data-stu-id="27b95-120">-IPRuleList</span></span>
<span data-ttu-id="27b95-121">(Facoltativo) Regole IP del servizio Ricerca cognitiva di Azure</span><span class="sxs-lookup"><span data-stu-id="27b95-121">(Optional) Azure Cognitive Search Service IP rules</span></span>

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

### <span data-ttu-id="27b95-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27b95-122">-Name</span></span>
<span data-ttu-id="27b95-123">Nome del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="27b95-123">Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b95-124">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="27b95-124">-PartitionCount</span></span>
<span data-ttu-id="27b95-125">Numero di partizioni del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="27b95-125">Search Service partition count.</span></span>

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

### <span data-ttu-id="27b95-126">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="27b95-126">-PublicNetworkAccess</span></span>
<span data-ttu-id="27b95-127">(Facoltativo) Accesso alla rete pubblica del servizio Cognitivo di Azure (abilitato/disabilitato)</span><span class="sxs-lookup"><span data-stu-id="27b95-127">(Optional) Azure Cognitive Search Service public network access (Enabled/Disabled)</span></span>

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

### <span data-ttu-id="27b95-128">-ReplicaCount</span><span class="sxs-lookup"><span data-stu-id="27b95-128">-ReplicaCount</span></span>
<span data-ttu-id="27b95-129">Numero di replica del servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="27b95-129">Search Service replica count.</span></span>

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

### <span data-ttu-id="27b95-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27b95-130">-ResourceGroupName</span></span>
<span data-ttu-id="27b95-131">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27b95-131">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="27b95-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27b95-132">-ResourceId</span></span>
<span data-ttu-id="27b95-133">ID risorsa servizio di ricerca.</span><span class="sxs-lookup"><span data-stu-id="27b95-133">Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="27b95-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="27b95-134">-Confirm</span></span>
<span data-ttu-id="27b95-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27b95-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27b95-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27b95-136">-WhatIf</span></span>
<span data-ttu-id="27b95-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27b95-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27b95-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27b95-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27b95-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27b95-139">CommonParameters</span></span>
<span data-ttu-id="27b95-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27b95-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27b95-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="27b95-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27b95-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="27b95-142">INPUTS</span></span>

### <span data-ttu-id="27b95-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="27b95-143">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="27b95-144">System.String</span><span class="sxs-lookup"><span data-stu-id="27b95-144">System.String</span></span>

## <span data-ttu-id="27b95-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27b95-145">OUTPUTS</span></span>

### <span data-ttu-id="27b95-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="27b95-146">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

## <span data-ttu-id="27b95-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="27b95-147">NOTES</span></span>

## <span data-ttu-id="27b95-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27b95-148">RELATED LINKS</span></span>

[<span data-ttu-id="27b95-149">New-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="27b95-149">New-AzSearchService</span></span>](./New-AzSearchService.md)

[<span data-ttu-id="27b95-150">Get-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="27b95-150">Get-AzSearchService</span></span>](./Get-AzSearchService.md)

[<span data-ttu-id="27b95-151">Remove-AzSearchService</span><span class="sxs-lookup"><span data-stu-id="27b95-151">Remove-AzSearchService</span></span>](./Remove-AzSearchService.md)