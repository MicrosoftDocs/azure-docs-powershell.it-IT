---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 75c69c96b82cf71aa71d4ac89bb10c064af1f4f6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189440"
---
# <span data-ttu-id="0923b-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="0923b-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="0923b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0923b-102">SYNOPSIS</span></span>
<span data-ttu-id="0923b-103">Ottiene le chiavi condivise per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0923b-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="0923b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0923b-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0923b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0923b-105">DESCRIPTION</span></span>
<span data-ttu-id="0923b-106">Il cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey** elenca le chiavi condivise per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0923b-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="0923b-107">I tasti vengono usati per connettere gli agenti di Insight operativi all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0923b-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="0923b-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0923b-108">EXAMPLES</span></span>

### <span data-ttu-id="0923b-109">Esempio 1: ottenere le chiavi condivise per nome area di lavoro</span><span class="sxs-lookup"><span data-stu-id="0923b-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="0923b-110">Questo comando consente di ottenere le chiavi condivise per l'area di lavoro denominata area di lavoro nel gruppo risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0923b-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="0923b-111">Esempio 2: ottenere le chiavi condivise tramite la pipeline</span><span class="sxs-lookup"><span data-stu-id="0923b-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="0923b-112">Questo comando ottiene l'area di lavoro denominata Workspace usando il cmdlet Get-AzOperationalInsightsWorkspace e quindi passa l'area di lavoro al cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey** .</span><span class="sxs-lookup"><span data-stu-id="0923b-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="0923b-113">Il comando ottiene le chiavi condivise per l'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0923b-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="0923b-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0923b-114">PARAMETERS</span></span>

### <span data-ttu-id="0923b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0923b-115">-DefaultProfile</span></span>
<span data-ttu-id="0923b-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0923b-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0923b-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="0923b-117">-Name</span></span>
<span data-ttu-id="0923b-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="0923b-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="0923b-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0923b-119">-ResourceGroupName</span></span>
<span data-ttu-id="0923b-120">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="0923b-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="0923b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0923b-121">CommonParameters</span></span>
<span data-ttu-id="0923b-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0923b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0923b-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0923b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0923b-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0923b-124">INPUTS</span></span>

### <span data-ttu-id="0923b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="0923b-125">System.String</span></span>

## <span data-ttu-id="0923b-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0923b-126">OUTPUTS</span></span>

### <span data-ttu-id="0923b-127">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="0923b-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="0923b-128">Note</span><span class="sxs-lookup"><span data-stu-id="0923b-128">NOTES</span></span>

## <span data-ttu-id="0923b-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0923b-129">RELATED LINKS</span></span>

[<span data-ttu-id="0923b-130">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="0923b-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="0923b-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="0923b-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)

