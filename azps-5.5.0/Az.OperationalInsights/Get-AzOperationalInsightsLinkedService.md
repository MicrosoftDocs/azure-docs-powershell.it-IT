---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184111"
---
# <span data-ttu-id="93f8c-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="93f8c-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="93f8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93f8c-102">SYNOPSIS</span></span>
<span data-ttu-id="93f8c-103">Ottenere o elencare un servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="93f8c-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="93f8c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="93f8c-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93f8c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="93f8c-105">DESCRIPTION</span></span>
<span data-ttu-id="93f8c-106">Ottenere o elencare il servizio collegato per l'area di lavoro, elenco in cui non è stato fornito "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="93f8c-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="93f8c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="93f8c-107">EXAMPLES</span></span>

### <span data-ttu-id="93f8c-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="93f8c-108">Example 1</span></span>
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

<span data-ttu-id="93f8c-109">Ottieni servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="93f8c-109">Get linked service for workspace</span></span>

## <span data-ttu-id="93f8c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93f8c-110">PARAMETERS</span></span>

### <span data-ttu-id="93f8c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93f8c-111">-DefaultProfile</span></span>
<span data-ttu-id="93f8c-112">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="93f8c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93f8c-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="93f8c-113">-LinkedServiceName</span></span>
<span data-ttu-id="93f8c-114">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="93f8c-114">The linked service name.</span></span>

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

### <span data-ttu-id="93f8c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93f8c-115">-ResourceGroupName</span></span>
<span data-ttu-id="93f8c-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="93f8c-116">The resource group name.</span></span>

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

### <span data-ttu-id="93f8c-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="93f8c-117">-WorkspaceName</span></span>
<span data-ttu-id="93f8c-118">Il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="93f8c-118">The workspace name.</span></span>

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

### <span data-ttu-id="93f8c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93f8c-119">CommonParameters</span></span>
<span data-ttu-id="93f8c-120">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93f8c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93f8c-121">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93f8c-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93f8c-122">INPUT</span><span class="sxs-lookup"><span data-stu-id="93f8c-122">INPUTS</span></span>

### <span data-ttu-id="93f8c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="93f8c-123">System.String</span></span>

## <span data-ttu-id="93f8c-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="93f8c-124">OUTPUTS</span></span>

### <span data-ttu-id="93f8c-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="93f8c-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="93f8c-126">NOTE</span><span class="sxs-lookup"><span data-stu-id="93f8c-126">NOTES</span></span>

## <span data-ttu-id="93f8c-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="93f8c-127">RELATED LINKS</span></span>
