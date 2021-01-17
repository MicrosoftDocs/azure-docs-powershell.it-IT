---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98488808"
---
# <span data-ttu-id="2b17c-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="2b17c-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="2b17c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2b17c-102">SYNOPSIS</span></span>
<span data-ttu-id="2b17c-103">Creare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="2b17c-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="2b17c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2b17c-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2b17c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b17c-105">DESCRIPTION</span></span>
<span data-ttu-id="2b17c-106">Creare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="2b17c-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="2b17c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2b17c-107">EXAMPLES</span></span>

### <span data-ttu-id="2b17c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="2b17c-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="2b17c-109">Aggiungere spazio di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="2b17c-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="2b17c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2b17c-110">PARAMETERS</span></span>

### <span data-ttu-id="2b17c-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="2b17c-111">-DataSourceType</span></span>
<span data-ttu-id="2b17c-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="2b17c-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="2b17c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b17c-113">-DefaultProfile</span></span>
<span data-ttu-id="2b17c-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2b17c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b17c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="2b17c-115">-Force</span></span>
<span data-ttu-id="2b17c-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="2b17c-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2b17c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b17c-117">-ResourceGroupName</span></span>
<span data-ttu-id="2b17c-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="2b17c-118">The resource group name.</span></span>

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

### <span data-ttu-id="2b17c-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="2b17c-119">-StorageAccountIds</span></span>
<span data-ttu-id="2b17c-120">elenco di ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2b17c-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="2b17c-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="2b17c-121">-WorkspaceName</span></span>
<span data-ttu-id="2b17c-122">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="2b17c-122">The workspace name.</span></span>

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

### <span data-ttu-id="2b17c-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2b17c-123">-Confirm</span></span>
<span data-ttu-id="2b17c-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2b17c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2b17c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2b17c-125">-WhatIf</span></span>
<span data-ttu-id="2b17c-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b17c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2b17c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2b17c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2b17c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b17c-128">CommonParameters</span></span>
<span data-ttu-id="2b17c-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b17c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b17c-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2b17c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b17c-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2b17c-131">INPUTS</span></span>

### <span data-ttu-id="2b17c-132">System. String</span><span class="sxs-lookup"><span data-stu-id="2b17c-132">System.String</span></span>

## <span data-ttu-id="2b17c-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2b17c-133">OUTPUTS</span></span>

### <span data-ttu-id="2b17c-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="2b17c-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="2b17c-135">Note</span><span class="sxs-lookup"><span data-stu-id="2b17c-135">NOTES</span></span>

## <span data-ttu-id="2b17c-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2b17c-136">RELATED LINKS</span></span>
