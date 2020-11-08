---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedStorageAccount.md
ms.openlocfilehash: 5095a3d9f989a6600776140239b9207ba3293d53
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192694"
---
# <span data-ttu-id="f7bcf-101">Get-AzOperationalInsightsLinkedStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f7bcf-101">Get-AzOperationalInsightsLinkedStorageAccount</span></span>

## <span data-ttu-id="f7bcf-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f7bcf-102">SYNOPSIS</span></span>
<span data-ttu-id="f7bcf-103">Account di archiviazione collegato Get o List</span><span class="sxs-lookup"><span data-stu-id="f7bcf-103">Get or list linked storage account</span></span>

## <span data-ttu-id="f7bcf-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f7bcf-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedStorageAccount [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-DataSourceType] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f7bcf-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f7bcf-105">DESCRIPTION</span></span>
<span data-ttu-id="f7bcf-106">Ottieni account di archiviazione collegato, elenca tutti gli account di archiviazione collegati quando non è stato specificato "-DataSourceType"</span><span class="sxs-lookup"><span data-stu-id="f7bcf-106">Get linked storage account, list all linked storage accounts when "-DataSourceType" was not specified</span></span>

## <span data-ttu-id="f7bcf-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f7bcf-107">EXAMPLES</span></span>

### <span data-ttu-id="f7bcf-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="f7bcf-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedStorageAccount -ResourceGroupName {rg-name} -WorkspaceName {workspace-name}

Id                : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/workspaces/{workspace-name}/linkedStorageAccounts/customlogs
Name              :
Type              : Microsoft.OperationalInsights/workspaces/linkedStorageAccounts
DataSourceType    : CustomLogs
StorageAccountIds : {/subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.Storage/storageAccounts/{account}}
```

<span data-ttu-id="f7bcf-109">elenco di archiviazione collegato accoounts per l'area di lavoro {Workspace-Name}</span><span class="sxs-lookup"><span data-stu-id="f7bcf-109">list linked storage accoounts for workspace {workspace-name}</span></span>

## <span data-ttu-id="f7bcf-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f7bcf-110">PARAMETERS</span></span>

### <span data-ttu-id="f7bcf-111">-DataSourceType</span><span class="sxs-lookup"><span data-stu-id="f7bcf-111">-DataSourceType</span></span>
<span data-ttu-id="f7bcf-112">Il tipo di origine dati deve essere uno di "CustomLogs", "AzureWatson".</span><span class="sxs-lookup"><span data-stu-id="f7bcf-112">Data Source Type should be one of 'CustomLogs', 'AzureWatson'.</span></span>

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

### <span data-ttu-id="f7bcf-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7bcf-113">-DefaultProfile</span></span>
<span data-ttu-id="f7bcf-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f7bcf-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7bcf-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7bcf-115">-ResourceGroupName</span></span>
<span data-ttu-id="f7bcf-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f7bcf-116">The resource group name.</span></span>

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

### <span data-ttu-id="f7bcf-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f7bcf-117">-WorkspaceName</span></span>
<span data-ttu-id="f7bcf-118">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="f7bcf-118">The workspace name.</span></span>

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

### <span data-ttu-id="f7bcf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7bcf-119">CommonParameters</span></span>
<span data-ttu-id="f7bcf-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7bcf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7bcf-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7bcf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7bcf-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f7bcf-122">INPUTS</span></span>

### <span data-ttu-id="f7bcf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="f7bcf-123">System.String</span></span>

## <span data-ttu-id="f7bcf-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f7bcf-124">OUTPUTS</span></span>

### <span data-ttu-id="f7bcf-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedStorageAccountsResource</span><span class="sxs-lookup"><span data-stu-id="f7bcf-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedStorageAccountsResource</span></span>

## <span data-ttu-id="f7bcf-126">Note</span><span class="sxs-lookup"><span data-stu-id="f7bcf-126">NOTES</span></span>

## <span data-ttu-id="f7bcf-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f7bcf-127">RELATED LINKS</span></span>