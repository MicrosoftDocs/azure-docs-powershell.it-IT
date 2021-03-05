---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-AzSearchPrivateLinkResource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateLinkResource.md
ms.openlocfilehash: a04af740a320d2550eb3fb4668689328bbe60857
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101963726"
---
# <span data-ttu-id="a7b01-101">Get-AzSearchPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a7b01-101">Get-AzSearchPrivateLinkResource</span></span>

## <span data-ttu-id="a7b01-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7b01-102">SYNOPSIS</span></span>
<span data-ttu-id="a7b01-103">Recupera i dettagli delle risorse del collegamento privato per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-103">Gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a7b01-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a7b01-104">SYNTAX</span></span>

### <span data-ttu-id="a7b01-105">ResourceNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a7b01-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7b01-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7b01-106">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7b01-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7b01-107">InputObjectParameterSet</span></span>
```
Get-AzSearchPrivateLinkResource [-InputObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7b01-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a7b01-108">DESCRIPTION</span></span>
<span data-ttu-id="a7b01-109">Il cmdlet **Get-AzSearchPrivateLinkResource** ottiene i dettagli delle risorse del collegamento privato per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-109">The **Get-AzSearchPrivateLinkResource** cmdlet gets private link resource details for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a7b01-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a7b01-110">EXAMPLES</span></span>

### <span data-ttu-id="a7b01-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a7b01-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateLinkResource -ResourceGroupName arjagann -Name arjagann-test-cuseuap | ConvertTo-Json

  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateLinkResources/searchService",
  "Type": "Microsoft.Search/searchServices/privateLinkResources",
  "GroupId": "searchService",
  "RequiredMembers": [
    "searchService"
  ],
  "RequiredZoneNames": [
    "privatelink.search-dogfood.windows-int.net"
  ],
  "ShareablePrivateLinkResourceTypes": [
    {
      "Name": "blob",
      "Description": "Azure Cognitive Search indexers can connect to blobs in Azure Storage for reading data (data source), for writing intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "blob"
    },
    {
      "Name": "table",
      "Description": "Azure Cognitive Search indexers can connect to tables in Azure Storage for reading data (data source), for writing book-keeping information about intermediate results of indexer execution (annotation cache, preview) or for storing any knowledge store projections (preview)",
      "Type": "Microsoft.Storage/storageAccounts",
      "GroupId": "table"
    },
    {
      "Name": "Sql",
      "Description": "Azure Cognitive Search indexers can connect to CosmosDB using the SQL head for reading data (data source).",
      "Type": "Microsoft.DocumentDB/databaseAccounts",
      "GroupId": "Sql"
    },
    {
      "Name": "plr",
      "Description": "Azure Cognitive Search indexers can connect to AzureSQL databases in a SQL server for reading data (data source).",
      "Type": "Microsoft.Sql/servers",
      "GroupId": "sqlServer"
    },
    {
      "Name": "vault",
      "Description": "Azure Cognitive Search can access keys in Azure Key Vault to encrypt search index and synonym map data",
      "Type": "Microsoft.KeyVault/vaults",
      "GroupId": "vault"
    }
  ]
}
```

<span data-ttu-id="a7b01-112">L'esempio mostra come ottenere i dettagli delle risorse del collegamento privato in formato JSON per praticità per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-112">The example shows how to get the private link resource details (in JSON form for convenience) for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a7b01-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a7b01-113">PARAMETERS</span></span>

### <span data-ttu-id="a7b01-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7b01-114">-DefaultProfile</span></span>
<span data-ttu-id="a7b01-115">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7b01-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a7b01-116">-InputObject</span></span>
<span data-ttu-id="a7b01-117">Oggetto di input del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="a7b01-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a7b01-118">-Name</span></span>
<span data-ttu-id="a7b01-119">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-119">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="a7b01-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7b01-120">-ResourceGroupName</span></span>
<span data-ttu-id="a7b01-121">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a7b01-121">Resource Group name.</span></span>

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

### <span data-ttu-id="a7b01-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7b01-122">-ResourceId</span></span>
<span data-ttu-id="a7b01-123">ID risorsa del servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="a7b01-123">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7b01-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a7b01-124">-Confirm</span></span>
<span data-ttu-id="a7b01-125">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a7b01-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7b01-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7b01-126">-WhatIf</span></span>
<span data-ttu-id="a7b01-127">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7b01-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7b01-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a7b01-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7b01-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7b01-129">CommonParameters</span></span>
<span data-ttu-id="a7b01-130">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7b01-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7b01-131">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a7b01-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7b01-132">INPUT</span><span class="sxs-lookup"><span data-stu-id="a7b01-132">INPUTS</span></span>

### <span data-ttu-id="a7b01-133">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a7b01-133">None</span></span>

## <span data-ttu-id="a7b01-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a7b01-134">OUTPUTS</span></span>

### <span data-ttu-id="a7b01-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="a7b01-135">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="a7b01-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="a7b01-136">NOTES</span></span>

## <span data-ttu-id="a7b01-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a7b01-137">RELATED LINKS</span></span>

[<span data-ttu-id="a7b01-138">New-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a7b01-138">New-AzSearchSharedPrivateLinkResource.md</span></span>](./New-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="a7b01-139">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a7b01-139">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="a7b01-140">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a7b01-140">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="a7b01-141">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="a7b01-141">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)