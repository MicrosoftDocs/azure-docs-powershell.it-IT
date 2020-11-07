---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 1e1e56a4cf0e31af3d64377df05b6057354dd534
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685824"
---
# <span data-ttu-id="ce4c6-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="ce4c6-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="ce4c6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ce4c6-102">SYNOPSIS</span></span>
<span data-ttu-id="ce4c6-103">Restituisce lo schema associato a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce4c6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ce4c6-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ce4c6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ce4c6-105">DESCRIPTION</span></span>
<span data-ttu-id="ce4c6-106">Il cmdlet **Get-AzureRmOperationalInsightsSchema** restituisce lo schema associato all'area di lavoro specificata all'interno di tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="ce4c6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ce4c6-107">EXAMPLES</span></span>

### <span data-ttu-id="ce4c6-108">Esempio 1: ottenere gli schemi per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ce4c6-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="ce4c6-109">Questo comando consente di ottenere gli schemi associati a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="ce4c6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ce4c6-110">PARAMETERS</span></span>

### <span data-ttu-id="ce4c6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce4c6-111">-DefaultProfile</span></span>
<span data-ttu-id="ce4c6-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ce4c6-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce4c6-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce4c6-113">-ResourceGroupName</span></span>
<span data-ttu-id="ce4c6-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c6-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ce4c6-115">-WorkspaceName</span></span>
<span data-ttu-id="ce4c6-116">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-116">Specifies a workspace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce4c6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce4c6-117">CommonParameters</span></span>
<span data-ttu-id="ce4c6-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce4c6-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce4c6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce4c6-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ce4c6-120">INPUTS</span></span>

### <span data-ttu-id="ce4c6-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="ce4c6-121">None</span></span>
<span data-ttu-id="ce4c6-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="ce4c6-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ce4c6-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ce4c6-123">OUTPUTS</span></span>

### <span data-ttu-id="ce4c6-124">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="ce4c6-124">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="ce4c6-125">Note</span><span class="sxs-lookup"><span data-stu-id="ce4c6-125">NOTES</span></span>

## <span data-ttu-id="ce4c6-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ce4c6-126">RELATED LINKS</span></span>

[<span data-ttu-id="ce4c6-127">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="ce4c6-127">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


