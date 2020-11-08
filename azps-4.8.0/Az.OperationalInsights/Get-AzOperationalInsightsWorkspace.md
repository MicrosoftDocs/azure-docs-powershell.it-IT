---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 1a0d36c2e871bd0495216bce18d84dff60e1044d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94032266"
---
# <span data-ttu-id="1b106-101">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b106-101">Get-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="1b106-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b106-102">SYNOPSIS</span></span>
<span data-ttu-id="1b106-103">Ottiene informazioni su un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1b106-103">Gets information about a workspace.</span></span>

## <span data-ttu-id="1b106-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b106-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b106-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b106-105">DESCRIPTION</span></span>
<span data-ttu-id="1b106-106">Il cmdlet **Get-AzOperationalInsightsWorkspace** ottiene le informazioni su un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="1b106-106">The **Get-AzOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="1b106-107">Se specifichi un nome per l'area di lavoro, questo cmdlet ottiene informazioni sull'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1b106-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="1b106-108">Se non si specifica un nome, questo cmdlet otterrà informazioni su tutte le aree di lavoro in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1b106-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="1b106-109">Se non specifichi un nome e un gruppo di risorse, questo cmdlet riceverà informazioni su tutte le aree di lavoro in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="1b106-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="1b106-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b106-110">EXAMPLES</span></span>

### <span data-ttu-id="1b106-111">Esempio 1: ottenere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="1b106-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="1b106-112">Questo comando consente di ottenere un'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b106-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="1b106-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b106-113">PARAMETERS</span></span>

### <span data-ttu-id="1b106-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b106-114">-DefaultProfile</span></span>
<span data-ttu-id="1b106-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1b106-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b106-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="1b106-116">-Name</span></span>
<span data-ttu-id="1b106-117">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="1b106-117">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b106-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b106-118">-ResourceGroupName</span></span>
<span data-ttu-id="1b106-119">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="1b106-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b106-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b106-120">CommonParameters</span></span>
<span data-ttu-id="1b106-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b106-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b106-122">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b106-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b106-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b106-123">INPUTS</span></span>

### <span data-ttu-id="1b106-124">System. String</span><span class="sxs-lookup"><span data-stu-id="1b106-124">System.String</span></span>

## <span data-ttu-id="1b106-125">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b106-125">OUTPUTS</span></span>

### <span data-ttu-id="1b106-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="1b106-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="1b106-127">Note</span><span class="sxs-lookup"><span data-stu-id="1b106-127">NOTES</span></span>

## <span data-ttu-id="1b106-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b106-128">RELATED LINKS</span></span>

[<span data-ttu-id="1b106-129">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="1b106-129">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


