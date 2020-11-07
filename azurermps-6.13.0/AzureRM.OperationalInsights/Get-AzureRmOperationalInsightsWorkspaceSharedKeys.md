---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsworkspacesharedkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsWorkspaceSharedKeys.md
ms.openlocfilehash: 07d0834b89010ff533e1620f29904ea159d3dfea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687591"
---
# <span data-ttu-id="8a915-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span><span class="sxs-lookup"><span data-stu-id="8a915-101">Get-AzureRmOperationalInsightsWorkspaceSharedKeys</span></span>

## <span data-ttu-id="8a915-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8a915-102">SYNOPSIS</span></span>
<span data-ttu-id="8a915-103">Ottiene le chiavi condivise per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8a915-103">Gets the shared keys for a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a915-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8a915-104">SYNTAX</span></span>

```
Get-AzureRmOperationalInsightsWorkspaceSharedKeys [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8a915-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8a915-105">DESCRIPTION</span></span>
<span data-ttu-id="8a915-106">Il cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** elenca le chiavi condivise per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8a915-106">The **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="8a915-107">I tasti vengono usati per connettere gli agenti di Insight operativi all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8a915-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="8a915-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8a915-108">EXAMPLES</span></span>

### <span data-ttu-id="8a915-109">Esempio 1: ottenere le chiavi condivise per nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="8a915-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspaceSharedKeys -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="8a915-110">Questo comando consente di ottenere le chiavi condivise per l'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8a915-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="8a915-111">Esempio 2: ottenere le chiavi condivise tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="8a915-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzureRmOperationalInsightsWorkspaceSharedKeys
```

<span data-ttu-id="8a915-112">Questo comando ottiene l'area di lavoro denominata Workspace usando il cmdlet Get-AzureRmOperationalInsightsWorkspace e quindi passa l'area di lavoro al cmdlet **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** .</span><span class="sxs-lookup"><span data-stu-id="8a915-112">This command gets the workspace named MyWorkspace using the Get-AzureRmOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzureRmOperationalInsightsWorkspaceSharedKeys** cmdlet.</span></span>
<span data-ttu-id="8a915-113">Il comando ottiene le chiavi condivise per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8a915-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="8a915-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8a915-114">PARAMETERS</span></span>

### <span data-ttu-id="8a915-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a915-115">-DefaultProfile</span></span>
<span data-ttu-id="8a915-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="8a915-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8a915-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="8a915-117">-Name</span></span>
<span data-ttu-id="8a915-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="8a915-118">Specifies the workspace name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8a915-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a915-119">-ResourceGroupName</span></span>
<span data-ttu-id="8a915-120">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="8a915-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="8a915-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a915-121">CommonParameters</span></span>
<span data-ttu-id="8a915-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a915-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a915-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a915-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a915-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8a915-124">INPUTS</span></span>

### <span data-ttu-id="8a915-125">System. String</span><span class="sxs-lookup"><span data-stu-id="8a915-125">System.String</span></span>

## <span data-ttu-id="8a915-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8a915-126">OUTPUTS</span></span>

### <span data-ttu-id="8a915-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="8a915-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="8a915-128">Note</span><span class="sxs-lookup"><span data-stu-id="8a915-128">NOTES</span></span>

## <span data-ttu-id="8a915-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8a915-129">RELATED LINKS</span></span>

[<span data-ttu-id="8a915-130">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="8a915-130">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="8a915-131">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="8a915-131">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


