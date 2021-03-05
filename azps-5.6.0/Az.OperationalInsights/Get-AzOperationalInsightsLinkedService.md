---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 71a715386a4d5646f1c9015244ad8a096313bb64
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965598"
---
# <span data-ttu-id="9b3f3-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="9b3f3-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="9b3f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b3f3-102">SYNOPSIS</span></span>
<span data-ttu-id="9b3f3-103">Ottenere o elencare un servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="9b3f3-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="9b3f3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9b3f3-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b3f3-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="9b3f3-105">DESCRIPTION</span></span>
<span data-ttu-id="9b3f3-106">Ottenere o elencare il servizio collegato per l'area di lavoro, elenco in cui non è stato fornito "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="9b3f3-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="9b3f3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9b3f3-107">EXAMPLES</span></span>

### <span data-ttu-id="9b3f3-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="9b3f3-108">Example 1</span></span>
```powershell
Get-AzOperationalInsightsLinkedService -ResourceGroupName {rg-name} -WorkspaceName {workspace-name} -LinkedServiceName cluster

Id                    : /subscriptions/{subscription}/resourcegroups/{rg-name}/providers/microsoft.operationalinsights/workspaces/{workspace-name}/linkedservices/cluster
Name                  : {cluster-name}/Cluster
Type                  : Microsoft.OperationalInsights/workspaces/linkedServices
ResourceId            :
WriteAccessResourceId : /subscriptions/{subscription}/resourceGroups/{rg-name}/providers/Microsoft.OperationalInsights/clusters/{cluster-name}
ProvisioningState     : ProvisioningAccount
Tags                  :
```

<span data-ttu-id="9b3f3-109">Ottenere un servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="9b3f3-109">Get linked service for workspace</span></span>

## <span data-ttu-id="9b3f3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9b3f3-110">PARAMETERS</span></span>

### <span data-ttu-id="9b3f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b3f3-111">-DefaultProfile</span></span>
<span data-ttu-id="9b3f3-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9b3f3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b3f3-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="9b3f3-113">-LinkedServiceName</span></span>
<span data-ttu-id="9b3f3-114">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="9b3f3-114">The linked service name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9b3f3-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b3f3-115">-ResourceGroupName</span></span>
<span data-ttu-id="9b3f3-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="9b3f3-116">The resource group name.</span></span>

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

### <span data-ttu-id="9b3f3-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9b3f3-117">-WorkspaceName</span></span>
<span data-ttu-id="9b3f3-118">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="9b3f3-118">The workspace name.</span></span>

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

### <span data-ttu-id="9b3f3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b3f3-119">CommonParameters</span></span>
<span data-ttu-id="9b3f3-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b3f3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b3f3-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9b3f3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b3f3-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="9b3f3-122">INPUTS</span></span>

### <span data-ttu-id="9b3f3-123">System.String</span><span class="sxs-lookup"><span data-stu-id="9b3f3-123">System.String</span></span>

## <span data-ttu-id="9b3f3-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9b3f3-124">OUTPUTS</span></span>

### <span data-ttu-id="9b3f3-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="9b3f3-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="9b3f3-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="9b3f3-126">NOTES</span></span>

## <span data-ttu-id="9b3f3-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9b3f3-127">RELATED LINKS</span></span>
