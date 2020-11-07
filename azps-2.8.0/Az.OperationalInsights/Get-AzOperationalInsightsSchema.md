---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 077272f15d37645de86f144424fddd7e5f026908
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93865570"
---
# <span data-ttu-id="42d4f-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="42d4f-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="42d4f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="42d4f-102">SYNOPSIS</span></span>
<span data-ttu-id="42d4f-103">Restituisce lo schema associato a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="42d4f-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="42d4f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="42d4f-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42d4f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="42d4f-105">DESCRIPTION</span></span>
<span data-ttu-id="42d4f-106">Il cmdlet **Get-AzOperationalInsightsSchema** restituisce lo schema associato all'area di lavoro specificata all'interno di tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="42d4f-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="42d4f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="42d4f-107">EXAMPLES</span></span>

### <span data-ttu-id="42d4f-108">Esempio 1: ottenere gli schemi per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="42d4f-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="42d4f-109">Questo comando consente di ottenere gli schemi associati a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="42d4f-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="42d4f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="42d4f-110">PARAMETERS</span></span>

### <span data-ttu-id="42d4f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42d4f-111">-DefaultProfile</span></span>
<span data-ttu-id="42d4f-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="42d4f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42d4f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42d4f-113">-ResourceGroupName</span></span>
<span data-ttu-id="42d4f-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="42d4f-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d4f-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="42d4f-115">-WorkspaceName</span></span>
<span data-ttu-id="42d4f-116">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="42d4f-116">Specifies a workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42d4f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42d4f-117">CommonParameters</span></span>
<span data-ttu-id="42d4f-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42d4f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42d4f-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42d4f-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42d4f-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="42d4f-120">INPUTS</span></span>

### <span data-ttu-id="42d4f-121">System. String</span><span class="sxs-lookup"><span data-stu-id="42d4f-121">System.String</span></span>

## <span data-ttu-id="42d4f-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="42d4f-122">OUTPUTS</span></span>

### <span data-ttu-id="42d4f-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="42d4f-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="42d4f-124">Note</span><span class="sxs-lookup"><span data-stu-id="42d4f-124">NOTES</span></span>

## <span data-ttu-id="42d4f-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="42d4f-125">RELATED LINKS</span></span>

[<span data-ttu-id="42d4f-126">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="42d4f-126">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


