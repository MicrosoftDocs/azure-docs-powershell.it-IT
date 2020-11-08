---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94190920"
---
# <span data-ttu-id="415ef-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="415ef-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="415ef-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="415ef-102">SYNOPSIS</span></span>
<span data-ttu-id="415ef-103">Ottenere o elencare il servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="415ef-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="415ef-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="415ef-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="415ef-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="415ef-105">DESCRIPTION</span></span>
<span data-ttu-id="415ef-106">Ottenere o elencare il servizio collegato per l'area di lavoro, elenco quando non è stato fornito "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="415ef-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="415ef-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="415ef-107">EXAMPLES</span></span>

### <span data-ttu-id="415ef-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="415ef-108">Example 1</span></span>
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

<span data-ttu-id="415ef-109">Ottenere il servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="415ef-109">Get linked service for workspace</span></span>

## <span data-ttu-id="415ef-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="415ef-110">PARAMETERS</span></span>

### <span data-ttu-id="415ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="415ef-111">-DefaultProfile</span></span>
<span data-ttu-id="415ef-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="415ef-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="415ef-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="415ef-113">-LinkedServiceName</span></span>
<span data-ttu-id="415ef-114">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="415ef-114">The linked service name.</span></span>

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

### <span data-ttu-id="415ef-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="415ef-115">-ResourceGroupName</span></span>
<span data-ttu-id="415ef-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="415ef-116">The resource group name.</span></span>

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

### <span data-ttu-id="415ef-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="415ef-117">-WorkspaceName</span></span>
<span data-ttu-id="415ef-118">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="415ef-118">The workspace name.</span></span>

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

### <span data-ttu-id="415ef-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="415ef-119">CommonParameters</span></span>
<span data-ttu-id="415ef-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="415ef-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="415ef-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="415ef-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="415ef-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="415ef-122">INPUTS</span></span>

### <span data-ttu-id="415ef-123">System. String</span><span class="sxs-lookup"><span data-stu-id="415ef-123">System.String</span></span>

## <span data-ttu-id="415ef-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="415ef-124">OUTPUTS</span></span>

### <span data-ttu-id="415ef-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="415ef-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="415ef-126">Note</span><span class="sxs-lookup"><span data-stu-id="415ef-126">NOTES</span></span>

## <span data-ttu-id="415ef-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="415ef-127">RELATED LINKS</span></span>