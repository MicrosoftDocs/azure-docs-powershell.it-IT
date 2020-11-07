---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 589b6012a1819eac638f6197d0569972e4727fba
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685397"
---
# <span data-ttu-id="18653-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="18653-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="18653-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18653-102">SYNOPSIS</span></span>
<span data-ttu-id="18653-103">Ottiene informazioni su un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18653-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="18653-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18653-104">SYNTAX</span></span>

### <span data-ttu-id="18653-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="18653-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="18653-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="18653-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18653-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18653-107">DESCRIPTION</span></span>
<span data-ttu-id="18653-108">Il cmdlet **Get-AzOperationalInsightsStorageInsight** ottiene informazioni su un'analisi dello spazio di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="18653-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="18653-109">Se si specifica un nome di Insight di archiviazione, questo cmdlet ottiene le informazioni relative all'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18653-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="18653-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti gli approfondimenti di archiviazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="18653-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="18653-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18653-111">EXAMPLES</span></span>

### <span data-ttu-id="18653-112">Esempio 1: ottenere una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="18653-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="18653-113">Questo comando consente di ottenere la panoramica dello spazio di archiviazione denominata MyStorageInsight dall'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="18653-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="18653-114">Esempio 2: ottenere una panoramica dello spazio di archiviazione utilizzando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="18653-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="18653-115">Il primo comando usa il cmdlet **Get-AzOperationalInsightsWorkspace** per ottenere un'area di lavoro Insights operativa e lo archivia nella variabile $Workspace.</span><span class="sxs-lookup"><span data-stu-id="18653-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="18653-116">Il secondo comando consente di ottenere l'Insight di archiviazione denominato MyStorageInsight per l'area di lavoro in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="18653-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="18653-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18653-117">PARAMETERS</span></span>

### <span data-ttu-id="18653-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18653-118">-DefaultProfile</span></span>
<span data-ttu-id="18653-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="18653-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18653-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="18653-120">-Name</span></span>
<span data-ttu-id="18653-121">Specifica il nome della panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18653-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18653-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="18653-122">-ResourceGroupName</span></span>
<span data-ttu-id="18653-123">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="18653-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18653-124">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="18653-124">-Workspace</span></span>
<span data-ttu-id="18653-125">Specifica l'area di lavoro che contiene gli approfondimenti dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18653-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18653-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="18653-126">-WorkspaceName</span></span>
<span data-ttu-id="18653-127">Specifica il nome dell'area di lavoro che contiene gli approfondimenti dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18653-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18653-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18653-128">CommonParameters</span></span>
<span data-ttu-id="18653-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18653-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18653-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18653-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18653-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18653-131">INPUTS</span></span>

### <span data-ttu-id="18653-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="18653-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="18653-133">System. String</span><span class="sxs-lookup"><span data-stu-id="18653-133">System.String</span></span>

## <span data-ttu-id="18653-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18653-134">OUTPUTS</span></span>

### <span data-ttu-id="18653-135">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="18653-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="18653-136">Note</span><span class="sxs-lookup"><span data-stu-id="18653-136">NOTES</span></span>

## <span data-ttu-id="18653-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18653-137">RELATED LINKS</span></span>

[<span data-ttu-id="18653-138">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="18653-138">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)


