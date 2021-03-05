---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchsharedprivatelinkresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchSharedPrivateLinkResource.md
ms.openlocfilehash: 683a6105273bcd2ff2f254352cf6e991491c035d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976398"
---
# <span data-ttu-id="3d27f-101">New-AzSearchSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3d27f-101">New-AzSearchSharedPrivateLinkResource</span></span>

## <span data-ttu-id="3d27f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d27f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d27f-103">Crea una risorsa di collegamento privato condiviso per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d27f-103">Creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3d27f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3d27f-104">SYNTAX</span></span>

```
New-AzSearchSharedPrivateLinkResource [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 [-PrivateLinkResourceId] <String> [-GroupId] <String> [-RequestMessage] <String> [[-ResourceRegion] <String>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d27f-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3d27f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d27f-106">**New-AzSearchSharedPrivateLinkResource** crea una risorsa di collegamento privato condivisa per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d27f-106">The **New-AzSearchSharedPrivateLinkResource** creates a shared private link resource for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3d27f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3d27f-107">EXAMPLES</span></span>

### <span data-ttu-id="3d27f-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="3d27f-108">Example 1</span></span>
```powershell
PS C:\> New-AzSearchSharedPrivateLinkResource -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name blob-pe -PrivateLinkResourceId /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting -GroupId blob -RequestMessage "Please approve" 

Id                    : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/sharedPrivateLinkResources/blob-pe
Type                  : Microsoft.Search/searchServices/sharedPrivateLinkResources
Status                : Pending
Name                  : blob-pe
GroupId               : blob
PrivateLinkResourceId : /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourcegroups/PETesting/providers/Microsoft.Storage/storageAccounts/petesting
ProvisioningState     : Succeeded
RequestMessage        : Please approve
ResourceRegion        :
```

<span data-ttu-id="3d27f-109">Questo esempio crea una risorsa di collegamento privato condiviso al servizio BLOB di un account di archiviazione per il servizio Ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d27f-109">This example creates a shared private link resource to the blob service of a storage account for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="3d27f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3d27f-110">PARAMETERS</span></span>

### <span data-ttu-id="3d27f-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d27f-111">-AsJob</span></span>
<span data-ttu-id="3d27f-112">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="3d27f-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d27f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d27f-113">-DefaultProfile</span></span>
<span data-ttu-id="3d27f-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3d27f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d27f-115">-GroupId</span><span class="sxs-lookup"><span data-stu-id="3d27f-115">-GroupId</span></span>
<span data-ttu-id="3d27f-116">ID gruppo di risorse collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="3d27f-116">Shared private link resource group id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d27f-117">-Name</span><span class="sxs-lookup"><span data-stu-id="3d27f-117">-Name</span></span>
<span data-ttu-id="3d27f-118">Risorsa collegamento privato condiviso di Ricerca cognitiva di Azure</span><span class="sxs-lookup"><span data-stu-id="3d27f-118">Azure Cognitive Search Shared private link resource</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d27f-119">-PrivateLinkResourceId</span><span class="sxs-lookup"><span data-stu-id="3d27f-119">-PrivateLinkResourceId</span></span>
<span data-ttu-id="3d27f-120">ID risorsa di destinazione collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="3d27f-120">Shared private link target resource id</span></span>

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

### <span data-ttu-id="3d27f-121">-RequestMessage</span><span class="sxs-lookup"><span data-stu-id="3d27f-121">-RequestMessage</span></span>
<span data-ttu-id="3d27f-122">Messaggio di richiesta di risorsa collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="3d27f-122">Shared private link resource request message</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d27f-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d27f-123">-ResourceGroupName</span></span>
<span data-ttu-id="3d27f-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="3d27f-124">Resource Group name.</span></span>

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

### <span data-ttu-id="3d27f-125">-ResourceRegion</span><span class="sxs-lookup"><span data-stu-id="3d27f-125">-ResourceRegion</span></span>
<span data-ttu-id="3d27f-126">(Facoltativo) Area risorse collegamento privato condiviso</span><span class="sxs-lookup"><span data-stu-id="3d27f-126">(Optional) Shared private link resource region</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d27f-127">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3d27f-127">-ServiceName</span></span>
<span data-ttu-id="3d27f-128">Nome del servizio di ricerca cognitiva di Azure.</span><span class="sxs-lookup"><span data-stu-id="3d27f-128">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="3d27f-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3d27f-129">-Confirm</span></span>
<span data-ttu-id="3d27f-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d27f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d27f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d27f-131">-WhatIf</span></span>
<span data-ttu-id="3d27f-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d27f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d27f-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3d27f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d27f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d27f-134">CommonParameters</span></span>
<span data-ttu-id="3d27f-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d27f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d27f-136">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3d27f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d27f-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="3d27f-137">INPUTS</span></span>

### <span data-ttu-id="3d27f-138">Nessuno</span><span class="sxs-lookup"><span data-stu-id="3d27f-138">None</span></span>

## <span data-ttu-id="3d27f-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3d27f-139">OUTPUTS</span></span>

### <span data-ttu-id="3d27f-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span><span class="sxs-lookup"><span data-stu-id="3d27f-140">Microsoft.Azure.Commands.Management.Search.Models.PSSharedPrivateLinkResource</span></span>

## <span data-ttu-id="3d27f-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="3d27f-141">NOTES</span></span>

## <span data-ttu-id="3d27f-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3d27f-142">RELATED LINKS</span></span>

[<span data-ttu-id="3d27f-143">Get-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3d27f-143">Get-AzSearchSharedPrivateLinkResource.md</span></span>](./Get-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="3d27f-144">Remove-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3d27f-144">Remove-AzSearchSharedPrivateLinkResource.md</span></span>](./Remove-AzSearchSharedPrivateLinkResource.md)

[<span data-ttu-id="3d27f-145">Set-AzSearchSharedPrivateLinkResource.md</span><span class="sxs-lookup"><span data-stu-id="3d27f-145">Set-AzSearchSharedPrivateLinkResource.md</span></span>](./Set-AzSearchSharedPrivateLinkResource.md)
