---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 6A834F26-C3D1-46DA-A4A6-1BB5B69291D0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsSchema.md
ms.openlocfilehash: 0dcac3fac32094cf2d9a0e42abcffd6222783e78
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93517391"
---
# <span data-ttu-id="d41e4-101">Get-AzureRmOperationalInsightsSchema</span><span class="sxs-lookup"><span data-stu-id="d41e4-101">Get-AzureRmOperationalInsightsSchema</span></span>

## <span data-ttu-id="d41e4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d41e4-102">SYNOPSIS</span></span>
<span data-ttu-id="d41e4-103">Restituisce lo schema associato a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d41e4-103">Returns the schema associated with a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d41e4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d41e4-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsSchema [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d41e4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d41e4-105">DESCRIPTION</span></span>
<span data-ttu-id="d41e4-106">Il cmdlet **Get-AzureRmOperationalInsightsSchema** restituisce lo schema associato all'area di lavoro specificata all'interno di tale gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d41e4-106">The **Get-AzureRmOperationalInsightsSchema** cmdlet returns the schema associated with the specified workspace within that resource group.</span></span>

## <span data-ttu-id="d41e4-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d41e4-107">EXAMPLES</span></span>

### <span data-ttu-id="d41e4-108">Esempio 1: ottenere gli schemi per un'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="d41e4-108">Example 1: Get the schemas for a workspace</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsSchema -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="d41e4-109">Questo comando consente di ottenere gli schemi associati a un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d41e4-109">This command gets the schemas associated with a workspace.</span></span>

## <span data-ttu-id="d41e4-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d41e4-110">PARAMETERS</span></span>

### <span data-ttu-id="d41e4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d41e4-111">-DefaultProfile</span></span>
<span data-ttu-id="d41e4-112">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="d41e4-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d41e4-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d41e4-113">-ResourceGroupName</span></span>
<span data-ttu-id="d41e4-114">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d41e4-114">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="d41e4-115">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="d41e4-115">-WorkspaceName</span></span>
<span data-ttu-id="d41e4-116">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="d41e4-116">Specifies a workspace name.</span></span>

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

### <span data-ttu-id="d41e4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d41e4-117">CommonParameters</span></span>
<span data-ttu-id="d41e4-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d41e4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d41e4-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d41e4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d41e4-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d41e4-120">INPUTS</span></span>

### <span data-ttu-id="d41e4-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d41e4-121">System.String</span></span>

## <span data-ttu-id="d41e4-122">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d41e4-122">OUTPUTS</span></span>

### <span data-ttu-id="d41e4-123">Microsoft. Azure. Commands. OperationalInsights. Models. PSSearchGetSchemaResponse</span><span class="sxs-lookup"><span data-stu-id="d41e4-123">Microsoft.Azure.Commands.OperationalInsights.Models.PSSearchGetSchemaResponse</span></span>

## <span data-ttu-id="d41e4-124">Note</span><span class="sxs-lookup"><span data-stu-id="d41e4-124">NOTES</span></span>

## <span data-ttu-id="d41e4-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d41e4-125">RELATED LINKS</span></span>

[<span data-ttu-id="d41e4-126">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="d41e4-126">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


