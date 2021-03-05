---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5ae174f31cdbe23a28dd9a21b44b640239e78fdd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976494"
---
# <span data-ttu-id="1d530-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="1d530-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="1d530-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d530-102">SYNOPSIS</span></span>
<span data-ttu-id="1d530-103">Ottenere o elencare un account di archiviazione collegato</span><span class="sxs-lookup"><span data-stu-id="1d530-103">Get or list linked storage account</span></span>

## <span data-ttu-id="1d530-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1d530-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d530-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1d530-105">DESCRIPTION</span></span>
<span data-ttu-id="1d530-106">Ottenere un account di archiviazione collegato, elencare tutti gli account di archiviazione collegati quando non è stato specificato "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="1d530-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="1d530-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1d530-107">EXAMPLES</span></span>

### <span data-ttu-id="1d530-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1d530-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="1d530-109">Elenco dei criteri di archiviazione collegati per l'area di lavoro {workspace-name}</span><span class="sxs-lookup"><span data-stu-id="1d530-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="1d530-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d530-110">PARAMETERS</span></span>

### <span data-ttu-id="1d530-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="1d530-111">-DataSourceType</span></span>
<span data-ttu-id="1d530-112">Il tipo di origine dati deve essere uno dei log personalizzati, "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="1d530-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="1d530-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d530-113">-DefaultProfile</span></span>
<span data-ttu-id="1d530-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1d530-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d530-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d530-115">-ResourceGroupName</span></span>
<span data-ttu-id="1d530-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1d530-116">The resource group name.</span></span>

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

### <span data-ttu-id="1d530-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="1d530-117">-WorkspaceName</span></span>
<span data-ttu-id="1d530-118">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1d530-118">The workspace name.</span></span>

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

### <span data-ttu-id="1d530-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d530-119">CommonParameters</span></span>
<span data-ttu-id="1d530-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d530-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d530-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1d530-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d530-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="1d530-122">INPUTS</span></span>

### <span data-ttu-id="1d530-123">System.String</span><span class="sxs-lookup"><span data-stu-id="1d530-123">System.String</span></span>

## <span data-ttu-id="1d530-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1d530-124">OUTPUTS</span></span>

### <span data-ttu-id="1d530-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="1d530-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="1d530-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="1d530-126">NOTES</span></span>

## <span data-ttu-id="1d530-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1d530-127">RELATED LINKS</span></span>