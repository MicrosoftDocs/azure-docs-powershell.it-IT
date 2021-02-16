---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186767"
---
# <span data-ttu-id="ee638-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee638-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="ee638-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee638-102">SYNOPSIS</span></span>
<span data-ttu-id="ee638-103">Creare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ee638-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="ee638-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ee638-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee638-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ee638-105">DESCRIPTION</span></span>
<span data-ttu-id="ee638-106">Creare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ee638-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="ee638-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ee638-107">EXAMPLES</span></span>

### <span data-ttu-id="ee638-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ee638-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="ee638-109">Aggiungere spazio di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ee638-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="ee638-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ee638-110">PARAMETERS</span></span>

### <span data-ttu-id="ee638-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="ee638-111">-DataSourceType</span></span>
<span data-ttu-id="ee638-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="ee638-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:
Accepted values: CustomLogs, AzureWatson

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee638-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee638-113">-DefaultProfile</span></span>
<span data-ttu-id="ee638-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ee638-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee638-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ee638-115">-Force</span></span>
<span data-ttu-id="ee638-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ee638-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ee638-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee638-117">-ResourceGroupName</span></span>
<span data-ttu-id="ee638-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ee638-118">The resource group name.</span></span>

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

### <span data-ttu-id="ee638-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="ee638-119">-StorageAccountIds</span></span>
<span data-ttu-id="ee638-120">elenco di ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ee638-120">list of storage account Id.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ee638-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ee638-121">-WorkspaceName</span></span>
<span data-ttu-id="ee638-122">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ee638-122">The workspace name.</span></span>

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

### <span data-ttu-id="ee638-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ee638-123">-Confirm</span></span>
<span data-ttu-id="ee638-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee638-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee638-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee638-125">-WhatIf</span></span>
<span data-ttu-id="ee638-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee638-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ee638-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ee638-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee638-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee638-128">CommonParameters</span></span>
<span data-ttu-id="ee638-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee638-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee638-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ee638-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee638-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ee638-131">INPUTS</span></span>

### <span data-ttu-id="ee638-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ee638-132">System.String</span></span>

## <span data-ttu-id="ee638-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ee638-133">OUTPUTS</span></span>

### <span data-ttu-id="ee638-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="ee638-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="ee638-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ee638-135">NOTES</span></span>

## <span data-ttu-id="ee638-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ee638-136">RELATED LINKS</span></span>
