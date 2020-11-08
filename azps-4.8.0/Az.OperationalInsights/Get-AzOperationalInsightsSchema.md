---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsSchema.md
ms.openlocfilehash: 12c3e54725abfd5addf33a3d31edcb8f8016e9dd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192693"
---
# <span data-ttu-id="bfaf1-101">Get-AzOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="bfaf1-101">Get-AzOperationalInsightsSchema</span></span>

## <span data-ttu-id="bfaf1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bfaf1-102">SYNOPSIS</span></span>
<span data-ttu-id="bfaf1-103">Restituisce lo schema associato a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-103">Returns the schema associated with a workspace.</span></span>

## <span data-ttu-id="bfaf1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bfaf1-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bfaf1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bfaf1-105">DESCRIPTION</span></span>
<span data-ttu-id="bfaf1-106">Il cmdlet **Get-AzOperationalInsightsSchema** restituisce lo schema associato all'area di lavoro specificata all'interno di tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-106">The **Get-AzOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="bfaf1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bfaf1-107">EXAMPLES</span></span>

### <span data-ttu-id="bfaf1-108">Esempio 1: ottenere gli schemi per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="bfaf1-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="bfaf1-109">Questo comando consente di ottenere gli schemi associati a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="bfaf1-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bfaf1-110">PARAMETERS</span></span>

### <span data-ttu-id="bfaf1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfaf1-111">-DefaultProfile</span></span>
<span data-ttu-id="bfaf1-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="bfaf1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bfaf1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfaf1-113">-ResourceGroupName</span></span>
<span data-ttu-id="bfaf1-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="bfaf1-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bfaf1-115">-WorkspaceName</span></span>
<span data-ttu-id="bfaf1-116">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="bfaf1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfaf1-117">CommonParameters</span></span>
<span data-ttu-id="bfaf1-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfaf1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfaf1-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bfaf1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfaf1-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bfaf1-120">INPUTS</span></span>

### <span data-ttu-id="bfaf1-121">System. String</span><span class="sxs-lookup"><span data-stu-id="bfaf1-121">System.String</span></span>

## <span data-ttu-id="bfaf1-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bfaf1-122">OUTPUTS</span></span>

### <span data-ttu-id="bfaf1-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="bfaf1-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="bfaf1-124">Note</span><span class="sxs-lookup"><span data-stu-id="bfaf1-124">NOTES</span></span>

## <span data-ttu-id="bfaf1-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bfaf1-125">RELATED LINKS</span></span>

[<span data-ttu-id="bfaf1-126">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="bfaf1-126">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

