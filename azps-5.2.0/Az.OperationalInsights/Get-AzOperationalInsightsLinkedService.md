---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightslinkedservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsLinkedService.md
ms.openlocfilehash: 14f1f96dd533492aedd1c4ed187e380c021a1b5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370257"
---
# <span data-ttu-id="db4ca-101">Get-AzOperationalInsightsLinkedService</span><span class="sxs-lookup"><span data-stu-id="db4ca-101">Get-AzOperationalInsightsLinkedService</span></span>

## <span data-ttu-id="db4ca-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="db4ca-102">SYNOPSIS</span></span>
<span data-ttu-id="db4ca-103">Ottenere o elencare il servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="db4ca-103">Get or list linked service for workspace</span></span>

## <span data-ttu-id="db4ca-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="db4ca-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsLinkedService [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-LinkedServiceName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="db4ca-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="db4ca-105">DESCRIPTION</span></span>
<span data-ttu-id="db4ca-106">Ottenere o elencare il servizio collegato per l'area di lavoro, elenco quando non è stato fornito "-LinkedServiceName"</span><span class="sxs-lookup"><span data-stu-id="db4ca-106">Get or list linked service for workspace, list when "-LinkedServiceName" was not provided</span></span>

## <span data-ttu-id="db4ca-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="db4ca-107">EXAMPLES</span></span>

### <span data-ttu-id="db4ca-108">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="db4ca-108">Example 1</span></span>
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

<span data-ttu-id="db4ca-109">Ottenere il servizio collegato per l'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="db4ca-109">Get linked service for workspace</span></span>

## <span data-ttu-id="db4ca-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="db4ca-110">PARAMETERS</span></span>

### <span data-ttu-id="db4ca-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db4ca-111">-DefaultProfile</span></span>
<span data-ttu-id="db4ca-112">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="db4ca-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="db4ca-113">-LinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="db4ca-113">-LinkedServiceName</span></span>
<span data-ttu-id="db4ca-114">Nome del servizio collegato.</span><span class="sxs-lookup"><span data-stu-id="db4ca-114">The linked service name.</span></span>

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

### <span data-ttu-id="db4ca-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db4ca-115">-ResourceGroupName</span></span>
<span data-ttu-id="db4ca-116">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="db4ca-116">The resource group name.</span></span>

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

### <span data-ttu-id="db4ca-117">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="db4ca-117">-WorkspaceName</span></span>
<span data-ttu-id="db4ca-118">Nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="db4ca-118">The workspace name.</span></span>

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

### <span data-ttu-id="db4ca-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db4ca-119">CommonParameters</span></span>
<span data-ttu-id="db4ca-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db4ca-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db4ca-121">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="db4ca-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db4ca-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="db4ca-122">INPUTS</span></span>

### <span data-ttu-id="db4ca-123">System. String</span><span class="sxs-lookup"><span data-stu-id="db4ca-123">System.String</span></span>

## <span data-ttu-id="db4ca-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="db4ca-124">OUTPUTS</span></span>

### <span data-ttu-id="db4ca-125">Microsoft. Azure. Commands. OperationalInsights. Models. PSLinkedService</span><span class="sxs-lookup"><span data-stu-id="db4ca-125">Microsoft.Azure.Commands.OperationalInsights.Models.PSLinkedService</span></span>

## <span data-ttu-id="db4ca-126">Note</span><span class="sxs-lookup"><span data-stu-id="db4ca-126">NOTES</span></span>

## <span data-ttu-id="db4ca-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="db4ca-127">RELATED LINKS</span></span>
