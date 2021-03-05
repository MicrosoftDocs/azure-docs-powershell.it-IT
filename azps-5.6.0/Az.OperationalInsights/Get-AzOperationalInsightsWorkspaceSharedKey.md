---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 112D5C69-3F4F-4BB6-9DA4-52757146B0EF
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacesharedkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceSharedKey.md
ms.openlocfilehash: 2cf7f548db74a7c7393fcd52bb7183c54f5f4e60
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001005"
---
# <span data-ttu-id="03122-101">Get-AzOperationalInsightsWorkspaceSharedKey</span><span class="sxs-lookup"><span data-stu-id="03122-101">Get-AzOperationalInsightsWorkspaceSharedKey</span></span>

## <span data-ttu-id="03122-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03122-102">SYNOPSIS</span></span>
<span data-ttu-id="03122-103">Ottiene le chiavi condivise per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03122-103">Gets the shared keys for a workspace.</span></span>

## <span data-ttu-id="03122-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03122-104">SYNTAX</span></span>

```
Get-AzOperationalInsightsWorkspaceSharedKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03122-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03122-105">DESCRIPTION</span></span>
<span data-ttu-id="03122-106">Il cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey** elenca le chiavi condivise per un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03122-106">The **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet lists the shared keys for a workspace.</span></span>
<span data-ttu-id="03122-107">Le chiavi vengono usate per connettere gli agenti di Analisi operativa all'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03122-107">The keys are used to connect Operational Insights agents to the workspace.</span></span>

## <span data-ttu-id="03122-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03122-108">EXAMPLES</span></span>

### <span data-ttu-id="03122-109">Esempio 1: Ottenere chiavi condivise in base al nome dell'area di lavoro</span><span class="sxs-lookup"><span data-stu-id="03122-109">Example 1: Get shared keys by workspace name</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspaceSharedKey -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

<span data-ttu-id="03122-110">Questo comando recupera le chiavi condivise per l'area di lavoro denominata MyWorkspace nel gruppo di risorse denominato ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="03122-110">This command gets the shared keys for the workspace named MyWorkspace in the resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="03122-111">Esempio 2: Ottenere chiavi condivise usando la pipeline</span><span class="sxs-lookup"><span data-stu-id="03122-111">Example 2: Get shared keys by using the pipeline</span></span>
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceSharedKey
```

<span data-ttu-id="03122-112">Questo comando recupera l'area di lavoro denominata MyWorkspace con il cmdlet Get-AzOperationalInsightsWorkspace e quindi passa l'area di lavoro al cmdlet **Get-AzOperationalInsightsWorkspaceSharedKey.**</span><span class="sxs-lookup"><span data-stu-id="03122-112">This command gets the workspace named MyWorkspace using the Get-AzOperationalInsightsWorkspace cmdlet, and then passes the workspace to the **Get-AzOperationalInsightsWorkspaceSharedKey** cmdlet.</span></span>
<span data-ttu-id="03122-113">Il comando ottiene le chiavi condivise per quell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03122-113">The command gets the shared keys for that workspace.</span></span>

## <span data-ttu-id="03122-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03122-114">PARAMETERS</span></span>

### <span data-ttu-id="03122-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03122-115">-DefaultProfile</span></span>
<span data-ttu-id="03122-116">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="03122-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="03122-117">-Name</span><span class="sxs-lookup"><span data-stu-id="03122-117">-Name</span></span>
<span data-ttu-id="03122-118">Specifica il nome dell'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="03122-118">Specifies the workspace name.</span></span>

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

### <span data-ttu-id="03122-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03122-119">-ResourceGroupName</span></span>
<span data-ttu-id="03122-120">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="03122-120">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="03122-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03122-121">CommonParameters</span></span>
<span data-ttu-id="03122-122">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03122-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03122-123">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03122-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03122-124">INPUT</span><span class="sxs-lookup"><span data-stu-id="03122-124">INPUTS</span></span>

### <span data-ttu-id="03122-125">System.String</span><span class="sxs-lookup"><span data-stu-id="03122-125">System.String</span></span>

## <span data-ttu-id="03122-126">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03122-126">OUTPUTS</span></span>

### <span data-ttu-id="03122-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span><span class="sxs-lookup"><span data-stu-id="03122-127">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspaceKeys</span></span>

## <span data-ttu-id="03122-128">NOTE</span><span class="sxs-lookup"><span data-stu-id="03122-128">NOTES</span></span>

## <span data-ttu-id="03122-129">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03122-129">RELATED LINKS</span></span>

[<span data-ttu-id="03122-130">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="03122-130">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="03122-131">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="03122-131">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


