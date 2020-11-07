---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: F94415DA-1A4A-4D37-A626-1EDF5D1EFE74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspace.md
ms.openlocfilehash: 042597d8d300f57600680282dadb16e8ec221e59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687128"
---
# <span data-ttu-id="7e2c5-101">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e2c5-101">Get-AzureRmOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="7e2c5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7e2c5-102">SYNOPSIS</span></span>
<span data-ttu-id="7e2c5-103">Ottiene informazioni su un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-103">Gets information about a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7e2c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7e2c5-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7e2c5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7e2c5-105">DESCRIPTION</span></span>
<span data-ttu-id="7e2c5-106">Il cmdlet **Get-AzureRmOperationalInsightsWorkspace** ottiene le informazioni su un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-106">The **Get-AzureRmOperationalInsightsWorkspace** cmdlet gets information about an existing workspace.</span></span>
<span data-ttu-id="7e2c5-107">Se specifichi un nome per l'area di lavoro, questo cmdlet ottiene informazioni sull'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-107">If you specify a workspace name, this cmdlet gets information about that workspace.</span></span>
<span data-ttu-id="7e2c5-108">Se non si specifica un nome, questo cmdlet otterrà informazioni su tutte le aree di lavoro in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-108">If you do not specify a name, this cmdlet gets information about all workspaces in a resource group.</span></span>
<span data-ttu-id="7e2c5-109">Se non specifichi un nome e un gruppo di risorse, questo cmdlet riceverà informazioni su tutte le aree di lavoro in un abbonamento.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-109">If you do not specify a name and resource group, this cmdlet gets information about all workspaces in a subscription.</span></span>

## <span data-ttu-id="7e2c5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7e2c5-110">EXAMPLES</span></span>

### <span data-ttu-id="7e2c5-111">Esempio 1: ottenere un'area di lavoro in base al nome</span><span class="sxs-lookup"><span data-stu-id="7e2c5-111">Example 1: Get a workspace by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -Name "MyWorkspace" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="7e2c5-112">Questo comando consente di ottenere un'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-112">This command gets a workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="7e2c5-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7e2c5-113">PARAMETERS</span></span>

### <span data-ttu-id="7e2c5-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="7e2c5-114">-Name</span></span>
<span data-ttu-id="7e2c5-115">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-115">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="7e2c5-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e2c5-116">-ResourceGroupName</span></span>
<span data-ttu-id="7e2c5-117">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-117">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="7e2c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e2c5-118">-DefaultProfile</span></span>
<span data-ttu-id="7e2c5-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e2c5-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e2c5-120">CommonParameters</span></span>
<span data-ttu-id="7e2c5-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e2c5-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e2c5-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e2c5-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e2c5-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7e2c5-123">INPUTS</span></span>

## <span data-ttu-id="7e2c5-124">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7e2c5-124">OUTPUTS</span></span>

### <span data-ttu-id="7e2c5-125">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace]</span><span class="sxs-lookup"><span data-stu-id="7e2c5-125">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace]</span></span>

### <span data-ttu-id="7e2c5-126">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7e2c5-126">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="7e2c5-127">Note</span><span class="sxs-lookup"><span data-stu-id="7e2c5-127">NOTES</span></span>

## <span data-ttu-id="7e2c5-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7e2c5-128">RELATED LINKS</span></span>

[<span data-ttu-id="7e2c5-129">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="7e2c5-129">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

