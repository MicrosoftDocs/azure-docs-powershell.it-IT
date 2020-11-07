---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 29ABCC1B-8590-4243-A629-709F207927B4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/get-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Get-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: e51325a18f8a880131e9037473a60e8a56ea488f
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "93688679"
---
# <span data-ttu-id="88771-101">Get-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="88771-101">Get-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="88771-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88771-102">SYNOPSIS</span></span>
<span data-ttu-id="88771-103">Ottiene informazioni su un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88771-103">Gets information about a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88771-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88771-104">SYNTAX</span></span>

### <span data-ttu-id="88771-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88771-105">ByWorkspaceName (Default)</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88771-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="88771-106">ByWorkspaceObject</span></span>
```
Get-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88771-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88771-107">DESCRIPTION</span></span>
<span data-ttu-id="88771-108">Il cmdlet **Get-AzureRmOperationalInsightsStorageInsight** ottiene informazioni su un'analisi dello spazio di archiviazione esistente.</span><span class="sxs-lookup"><span data-stu-id="88771-108">The **Get-AzureRmOperationalInsightsStorageInsight** cmdlet gets information about an existing Storage Insight.</span></span>
<span data-ttu-id="88771-109">Se si specifica un nome di Insight di archiviazione, questo cmdlet ottiene le informazioni relative all'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88771-109">If a Storage Insight name is specified, this cmdlet gets information about that Storage Insight.</span></span>
<span data-ttu-id="88771-110">Se non specifichi un nome, questo cmdlet riceverà informazioni su tutti gli approfondimenti di archiviazione in un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="88771-110">If you do not specify a name, this cmdlet gets information about all storage insights in a workspace.</span></span>

## <span data-ttu-id="88771-111">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88771-111">EXAMPLES</span></span>

### <span data-ttu-id="88771-112">Esempio 1: ottenere una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="88771-112">Example 1: Get a Storage Insight by name</span></span>
```
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Name "MyStorageInsight" -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "ContosoWorkspace"
```

<span data-ttu-id="88771-113">Questo comando consente di ottenere la panoramica dello spazio di archiviazione denominata MyStorageInsight dall'area di lavoro denominata ContosoWorkspace.</span><span class="sxs-lookup"><span data-stu-id="88771-113">This command gets the storage insight named MyStorageInsight from the workspace named ContosoWorkspace.</span></span>

### <span data-ttu-id="88771-114">Esempio 2: ottenere una panoramica dello spazio di archiviazione utilizzando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="88771-114">Example 2: Get a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
PS C:\>Get-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight"
```

<span data-ttu-id="88771-115">Il primo comando usa il cmdlet **Get-AzureRmOperationalInsightsWorkspace** per ottenere un'area di lavoro Insights operativa e lo archivia nella variabile $Workspace.</span><span class="sxs-lookup"><span data-stu-id="88771-115">The first command uses the **Get-AzureRmOperationalInsightsWorkspace** cmdlet to get an Operational Insights workspace, and then stores it in the $Workspace variable.</span></span>

<span data-ttu-id="88771-116">Il secondo comando consente di ottenere l'Insight di archiviazione denominato MyStorageInsight per l'area di lavoro in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="88771-116">The second command gets the storage insight named MyStorageInsight for the workspace in $Workspace.</span></span>

## <span data-ttu-id="88771-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88771-117">PARAMETERS</span></span>

### <span data-ttu-id="88771-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88771-118">-DefaultProfile</span></span>
<span data-ttu-id="88771-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="88771-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88771-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="88771-120">-Name</span></span>
<span data-ttu-id="88771-121">Specifica il nome della panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88771-121">Specifies the Storage Insight name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88771-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88771-122">-ResourceGroupName</span></span>
<span data-ttu-id="88771-123">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="88771-123">Specifies the name of an Azure resource group.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88771-124">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="88771-124">-Workspace</span></span>
<span data-ttu-id="88771-125">Specifica l'area di lavoro che contiene gli approfondimenti dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88771-125">Specifies the workspace that contains the Storage Insights.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88771-126">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="88771-126">-WorkspaceName</span></span>
<span data-ttu-id="88771-127">Specifica il nome dell'area di lavoro che contiene gli approfondimenti dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="88771-127">Specifies the name of the workspace that contains the Storage Insights.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88771-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88771-128">CommonParameters</span></span>
<span data-ttu-id="88771-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88771-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88771-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88771-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88771-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88771-131">INPUTS</span></span>

### <span data-ttu-id="88771-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="88771-132">PSWorkspace</span></span>
<span data-ttu-id="88771-133">Il parametro ' Workspace ' accetta il valore di tipo ' PSWorkspace ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="88771-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="88771-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88771-134">OUTPUTS</span></span>

### <span data-ttu-id="88771-135">System. Collections. Generic. list ' 1 [Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight]</span><span class="sxs-lookup"><span data-stu-id="88771-135">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight]</span></span>

### <span data-ttu-id="88771-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="88771-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="88771-137">Note</span><span class="sxs-lookup"><span data-stu-id="88771-137">NOTES</span></span>

## <span data-ttu-id="88771-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88771-138">RELATED LINKS</span></span>

[<span data-ttu-id="88771-139">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="88771-139">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)


