---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: b2bd8855d9c8b125b4bef72f42f0bd4a63071adb
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93522186"
---
# <span data-ttu-id="c9d9a-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9d9a-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="c9d9a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d9a-103">Ottiene informazioni su un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d9a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9d9a-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9d9a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d9a-106">Il cmdlet **Get-AzureRmOperationalInsightsWorkspace** ottiene le informazioni su un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="c9d9a-107">Se specifichi un nome per l'area di lavoro, questo cmdlet ottiene informazioni sull'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="c9d9a-108">Se non si specifica un nome, questo cmdlet otterrà informazioni su tutte le aree di lavoro in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="c9d9a-109">Se non specifichi un nome e un gruppo di risorse, questo cmdlet riceverà informazioni su tutte le aree di lavoro in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="c9d9a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9d9a-110">EXAMPLES</span></span>

### <span data-ttu-id="c9d9a-111">Esempio 1: ottenere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="c9d9a-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="c9d9a-112">Questo comando consente di ottenere un'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c9d9a-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9d9a-113">PARAMETERS</span></span>

### <span data-ttu-id="c9d9a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9d9a-114">-DefaultProfile</span></span>
<span data-ttu-id="c9d9a-115">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c9d9a-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9d9a-116">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9d9a-116">-Name</span></span>
<span data-ttu-id="c9d9a-117">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-117">Specifies the workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d9a-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9d9a-118">-ResourceGroupName</span></span>
<span data-ttu-id="c9d9a-119">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-119">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9d9a-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d9a-120">CommonParameters</span></span>
<span data-ttu-id="c9d9a-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d9a-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d9a-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d9a-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9d9a-123">INPUTS</span></span>

### <span data-ttu-id="c9d9a-124">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c9d9a-124">None</span></span>
<span data-ttu-id="c9d9a-125">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="c9d9a-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9d9a-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9d9a-126">OUTPUTS</span></span>

### <span data-ttu-id="c9d9a-127">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="c9d9a-127">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="c9d9a-128">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c9d9a-128">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="c9d9a-129">Note</span><span class="sxs-lookup"><span data-stu-id="c9d9a-129">NOTES</span></span>

## <span data-ttu-id="c9d9a-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9d9a-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9d9a-131">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="c9d9a-131">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


