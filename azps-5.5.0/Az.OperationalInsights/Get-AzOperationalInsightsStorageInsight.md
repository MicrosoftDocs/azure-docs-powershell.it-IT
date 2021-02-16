---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: a89b4210fcd498aca3a25451e6f691df20d5510e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179230"
---
# <span data-ttu-id="7864a-101">Get-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="7864a-101">Get-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="7864a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7864a-102">SYNOPSIS</span></span>
<span data-ttu-id="7864a-103">Ottiene informazioni su informazioni sull'archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7864a-103">Gets information about a Storage Insight.</span></span>

## <span data-ttu-id="7864a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7864a-104">SYNTAX</span></span>

### <span data-ttu-id="7864a-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7864a-105">ByWorkspaceName (Default)</span></span>
```
Get-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7864a-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7864a-106">ByWorkspaceObject</span></span>
```
Get-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7864a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7864a-107">DESCRIPTION</span></span>
<span data-ttu-id="7864a-108">Il cmdlet **Get-AzOperationalInsightsStorageInsight** ottiene informazioni su un approfondimento di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="7864a-108">The **Get-AzOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="7864a-109">Se si specifica un nome di Informazioni dettagliate di archiviazione, questo cmdlet ottiene informazioni su tale informazione.</span><span class="sxs-lookup"><span data-stu-id="7864a-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="7864a-110">Se non si specifica un nome, questo cmdlet riceve informazioni su tutte le informazioni di archiviazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="7864a-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="7864a-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7864a-111">EXAMPLES</span></span>

### <span data-ttu-id="7864a-112">Esempio 1: Ottenere informazioni dettagliate sull'archiviazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="7864a-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="7864a-113">Questo comando recupera le informazioni di archiviazione denominate MyStorageInsight dall'area di lavoro ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="7864a-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="7864a-114">Esempio 2: Ottenere informazioni dettagliate sull'archiviazione usando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7864a-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="7864a-115">Il primo comando usa il cmdlet **Get-AzOperationalInsightsWorkspace** per ottenere un'area di lavoro di Operational Insights e quindi la archivia nella variabile $Workspace lavoro.</span><span class="sxs-lookup"><span data-stu-id="7864a-115">The first command uses the **Get-AzOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="7864a-116">Il secondo comando ottiene le informazioni di archiviazione denominate MyStorageInsight per l'area di lavoro di $Workspace.</span><span class="sxs-lookup"><span data-stu-id="7864a-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="7864a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7864a-117">PARAMETERS</span></span>

### <span data-ttu-id="7864a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7864a-118">-DefaultProfile</span></span>
<span data-ttu-id="7864a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="7864a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7864a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7864a-120">-Name</span></span>
<span data-ttu-id="7864a-121">Specifica il nome di Informazioni dettagliate di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7864a-121">Specifies the Storage Insight name.</span></span>

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

### <span data-ttu-id="7864a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7864a-122">-ResourceGroupName</span></span>
<span data-ttu-id="7864a-123">Specifica il nome di un gruppo di risorse di Azure.</span><span class="sxs-lookup"><span data-stu-id="7864a-123">Specifies the name of an Azure resource group.</span></span>

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

### <span data-ttu-id="7864a-124">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="7864a-124">-Workspace</span></span>
<span data-ttu-id="7864a-125">Specifica l'area di lavoro che contiene gli Approfondimenti archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7864a-125">Specifies the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="7864a-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7864a-126">-WorkspaceName</span></span>
<span data-ttu-id="7864a-127">Specifica il nome dell'area di lavoro che contiene i dati di Archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7864a-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

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

### <span data-ttu-id="7864a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7864a-128">CommonParameters</span></span>
<span data-ttu-id="7864a-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7864a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7864a-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7864a-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7864a-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="7864a-131">INPUTS</span></span>

### <span data-ttu-id="7864a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7864a-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7864a-133">System.String</span><span class="sxs-lookup"><span data-stu-id="7864a-133">System.String</span></span>

## <span data-ttu-id="7864a-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7864a-134">OUTPUTS</span></span>

### <span data-ttu-id="7864a-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="7864a-135">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="7864a-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="7864a-136">NOTES</span></span>

## <span data-ttu-id="7864a-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7864a-137">RELATED LINKS</span></span>

[<span data-ttu-id="7864a-138">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="7864a-138">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)


