---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 1293a2d045da5da1856052495516e9311e42e5f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94201543"
---
# <span data-ttu-id="76a38-101">New-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="76a38-101">New-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="76a38-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="76a38-102">SYNOPSIS</span></span>
<span data-ttu-id="76a38-103">Creare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="76a38-103">Create linked storage account for workspace</span></span>

## <span data-ttu-id="76a38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="76a38-104">SYNTAX</span></span>

```
New-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DataSourceType] <String> [-StorageAccountIds] <String[]> [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76a38-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="76a38-105">DESCRIPTION</span></span>
<span data-ttu-id="76a38-106">Creare un account di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="76a38-106">Create linked storage account for workspace</span></span>

## <span data-ttu-id="76a38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="76a38-107">EXAMPLES</span></span>

### <span data-ttu-id="76a38-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="76a38-108">Example 1</span></span>
```powershell
$account = Get-AzStorageAccount -ResourceGroupName {rg-name} -Name {account-name}

New-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -DataSourceType CustomLogs -StorageAccountIds $account.Id

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/CustomLogs
Name              : customlogs
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{storage-account}}
```

<span data-ttu-id="76a38-109">Aggiungere spazio di archiviazione collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="76a38-109">Add linked storage for workspace</span></span>

## <span data-ttu-id="76a38-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="76a38-110">PARAMETERS</span></span>

### <span data-ttu-id="76a38-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="76a38-111">-DataSourceType</span></span>
<span data-ttu-id="76a38-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="76a38-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="76a38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76a38-113">-DefaultProfile</span></span>
<span data-ttu-id="76a38-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="76a38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76a38-115">-Force</span><span class="sxs-lookup"><span data-stu-id="76a38-115">-Force</span></span>
<span data-ttu-id="76a38-116">Non chiedere conferma.</span><span class="sxs-lookup"><span data-stu-id="76a38-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76a38-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76a38-117">-ResourceGroupName</span></span>
<span data-ttu-id="76a38-118">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="76a38-118">The resource group name.</span></span>

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

### <span data-ttu-id="76a38-119">-StorageAccountIds</span><span class="sxs-lookup"><span data-stu-id="76a38-119">-StorageAccountIds</span></span>
<span data-ttu-id="76a38-120">elenco di ID account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="76a38-120">list of storage account Id.</span></span>

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

### <span data-ttu-id="76a38-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="76a38-121">-WorkspaceName</span></span>
<span data-ttu-id="76a38-122">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="76a38-122">The workspace name.</span></span>

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

### <span data-ttu-id="76a38-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="76a38-123">-Confirm</span></span>
<span data-ttu-id="76a38-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76a38-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76a38-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76a38-125">-WhatIf</span></span>
<span data-ttu-id="76a38-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76a38-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76a38-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="76a38-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76a38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76a38-128">CommonParameters</span></span>
<span data-ttu-id="76a38-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76a38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76a38-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76a38-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76a38-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="76a38-131">INPUTS</span></span>

### <span data-ttu-id="76a38-132">System. String</span><span class="sxs-lookup"><span data-stu-id="76a38-132">System.String</span></span>

## <span data-ttu-id="76a38-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="76a38-133">OUTPUTS</span></span>

### <span data-ttu-id="76a38-134">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="76a38-134">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="76a38-135">Note</span><span class="sxs-lookup"><span data-stu-id="76a38-135">NOTES</span></span>

## <span data-ttu-id="76a38-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="76a38-136">RELATED LINKS</span></span>
