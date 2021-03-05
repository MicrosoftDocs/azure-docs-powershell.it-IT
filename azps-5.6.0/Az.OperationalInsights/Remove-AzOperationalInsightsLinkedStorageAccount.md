---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/remove-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 8e4dd13b93a0aadf8c69325bc6d79a2a1b3e1359
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989784"
---
# <span data-ttu-id="988a3-101">Remove-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="988a3-101">Remove-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="988a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="988a3-102">SYNOPSIS</span></span>
<span data-ttu-id="988a3-103">Eliminare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="988a3-103">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="988a3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="988a3-104">SYNTAX</span></span>

```
Remove-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="988a3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="988a3-105">DESCRIPTION</span></span>
<span data-ttu-id="988a3-106">Eliminare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="988a3-106">Delete linked storage account for workspace</span></span>

## <span data-ttu-id="988a3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="988a3-107">EXAMPLES</span></span>

### <span data-ttu-id="988a3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="988a3-108">Example 1</span></span>
```powershell
Remove-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs
True
```

<span data-ttu-id="988a3-109">Eliminare l'account di archiviazione collegato con il tipo "CustomLogs" per {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="988a3-109">Delete linked storage account with type "CustomLogs" for {workspace-name}</span></span>

## <span data-ttu-id="988a3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="988a3-110">PARAMETERS</span></span>

### <span data-ttu-id="988a3-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="988a3-111">-DataSourceType</span></span>
<span data-ttu-id="988a3-112">Il tipo di origine dati deve essere uno dei log personalizzati, "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="988a3-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="988a3-113">-DefaultProfile</span></span>
<span data-ttu-id="988a3-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="988a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="988a3-115">-Force</span></span>
<span data-ttu-id="988a3-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="988a3-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="988a3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="988a3-117">-ResourceGroupName</span></span>
<span data-ttu-id="988a3-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="988a3-118">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a3-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="988a3-119">-WorkspaceName</span></span>
<span data-ttu-id="988a3-120">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="988a3-120">The workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="988a3-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="988a3-121">-Confirm</span></span>
<span data-ttu-id="988a3-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="988a3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="988a3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="988a3-123">-WhatIf</span></span>
<span data-ttu-id="988a3-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="988a3-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="988a3-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="988a3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="988a3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="988a3-126">CommonParameters</span></span>
<span data-ttu-id="988a3-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="988a3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="988a3-128">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="988a3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="988a3-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="988a3-129">INPUTS</span></span>

### <span data-ttu-id="988a3-130">System.String</span><span class="sxs-lookup"><span data-stu-id="988a3-130">System.String</span></span>

## <span data-ttu-id="988a3-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="988a3-131">OUTPUTS</span></span>

### <span data-ttu-id="988a3-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="988a3-132">System.Boolean</span></span>

## <span data-ttu-id="988a3-133">NOTE</span><span class="sxs-lookup"><span data-stu-id="988a3-133">NOTES</span></span>

## <span data-ttu-id="988a3-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="988a3-134">RELATED LINKS</span></span>
