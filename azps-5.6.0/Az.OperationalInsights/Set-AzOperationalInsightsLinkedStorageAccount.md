---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/set-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1392e77ef6497265dde8bcf0a05a86529253f539
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989727"
---
# <span data-ttu-id="ecdbd-101">Set-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ecdbd-101">Set-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="ecdbd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ecdbd-102">SYNOPSIS</span></span>
<span data-ttu-id="ecdbd-103">Impostare l'account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ecdbd-103">Set linked storage account for workspace</span></span>

## <span data-ttu-id="ecdbd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ecdbd-104">SYNTAX</span></span>

```
Set-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ecdbd-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ecdbd-105">DESCRIPTION</span></span>
<span data-ttu-id="ecdbd-106">Impostare l'account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ecdbd-106">Set linked storage account for workspace</span></span>

## <span data-ttu-id="ecdbd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ecdbd-107">EXAMPLES</span></span>

### <span data-ttu-id="ecdbd-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ecdbd-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

Set-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="ecdbd-109">Impostare lo spazio di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ecdbd-109">Set linked storage for workspace</span></span>

## <span data-ttu-id="ecdbd-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ecdbd-110">PARAMETERS</span></span>

### <span data-ttu-id="ecdbd-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="ecdbd-111">-DataSourceType</span></span>
<span data-ttu-id="ecdbd-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="ecdbd-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="ecdbd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ecdbd-113">-DefaultProfile</span></span>
<span data-ttu-id="ecdbd-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ecdbd-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ecdbd-115">-Force</span></span>
<span data-ttu-id="ecdbd-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="ecdbd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ecdbd-117">-ResourceGroupName</span></span>
<span data-ttu-id="ecdbd-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-118">The resource group name.</span></span>

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

### <span data-ttu-id="ecdbd-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="ecdbd-119">-StorageAccountIds</span></span>
<span data-ttu-id="ecdbd-120">elenco di ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="ecdbd-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ecdbd-121">-WorkspaceName</span></span>
<span data-ttu-id="ecdbd-122">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-122">The workspace name.</span></span>

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

### <span data-ttu-id="ecdbd-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ecdbd-123">-Confirm</span></span>
<span data-ttu-id="ecdbd-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ecdbd-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ecdbd-125">-WhatIf</span></span>
<span data-ttu-id="ecdbd-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ecdbd-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ecdbd-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ecdbd-128">CommonParameters</span></span>
<span data-ttu-id="ecdbd-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ecdbd-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ecdbd-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ecdbd-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="ecdbd-131">INPUTS</span></span>

### <span data-ttu-id="ecdbd-132">System.String</span><span class="sxs-lookup"><span data-stu-id="ecdbd-132">System.String</span></span>

## <span data-ttu-id="ecdbd-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ecdbd-133">OUTPUTS</span></span>

### <span data-ttu-id="ecdbd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="ecdbd-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="ecdbd-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="ecdbd-135">NOTES</span></span>

## <span data-ttu-id="ecdbd-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ecdbd-136">RELATED LINKS</span></span>
