---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: b6e57494daf556c3b824ee06735711042d3851b9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206331"
---
# <span data-ttu-id="dbaff-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="dbaff-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="dbaff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbaff-102">SYNOPSIS</span></span>
<span data-ttu-id="dbaff-103">Impostare l'account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dbaff-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="dbaff-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="dbaff-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbaff-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="dbaff-105">DESCRIPTION</span></span>
<span data-ttu-id="dbaff-106">Impostare l'account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dbaff-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="dbaff-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="dbaff-107">EXAMPLES</span></span>

### <span data-ttu-id="dbaff-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="dbaff-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="dbaff-109">Impostare lo spazio di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="dbaff-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="dbaff-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dbaff-110">PARAMETERS</span></span>

### <span data-ttu-id="dbaff-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="dbaff-111">-DataSourceType</span></span>
<span data-ttu-id="dbaff-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="dbaff-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="dbaff-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbaff-113">-DefaultProfile</span></span>
<span data-ttu-id="dbaff-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="dbaff-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbaff-115">-Force</span><span class="sxs-lookup"><span data-stu-id="dbaff-115">-Force</span></span>
<span data-ttu-id="dbaff-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="dbaff-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dbaff-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbaff-117">-ResourceGroupName</span></span>
<span data-ttu-id="dbaff-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="dbaff-118">The resource group name.</span></span>

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

### <span data-ttu-id="dbaff-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="dbaff-119">-StorageAccountIds</span></span>
<span data-ttu-id="dbaff-120">elenco di ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="dbaff-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="dbaff-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dbaff-121">-WorkspaceName</span></span>
<span data-ttu-id="dbaff-122">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="dbaff-122">The workspace name.</span></span>

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

### <span data-ttu-id="dbaff-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dbaff-123">-Confirm</span></span>
<span data-ttu-id="dbaff-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dbaff-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbaff-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbaff-125">-WhatIf</span></span>
<span data-ttu-id="dbaff-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbaff-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbaff-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="dbaff-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbaff-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbaff-128">CommonParameters</span></span>
<span data-ttu-id="dbaff-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbaff-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbaff-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dbaff-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbaff-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="dbaff-131">INPUTS</span></span>

### <span data-ttu-id="dbaff-132">System.String</span><span class="sxs-lookup"><span data-stu-id="dbaff-132">System.String</span></span>

## <span data-ttu-id="dbaff-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="dbaff-133">OUTPUTS</span></span>

### <span data-ttu-id="dbaff-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="dbaff-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="dbaff-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="dbaff-135">NOTES</span></span>

## <span data-ttu-id="dbaff-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="dbaff-136">RELATED LINKS</span></span>
