---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/set-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Set-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 460a1585c8c6c556f0044b9cd0673a3be750ffe2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685924"
---
# <span data-ttu-id="33c1e-101">Set-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="33c1e-101">Set-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="33c1e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="33c1e-102">SYNOPSIS</span></span>
<span data-ttu-id="33c1e-103">Aggiorna un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33c1e-103">Updates a Storage Insight.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="33c1e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="33c1e-104">SYNTAX</span></span>

### <span data-ttu-id="33c1e-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="33c1e-105">ByWorkspaceName (Default)</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="33c1e-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="33c1e-106">ByWorkspaceObject</span></span>
```
Set-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="33c1e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="33c1e-107">DESCRIPTION</span></span>
<span data-ttu-id="33c1e-108">Il cmdlet **set-AzureRmOperationalInsightsStorageInsight** modifica la configurazione di un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33c1e-108">The **Set-AzureRmOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="33c1e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="33c1e-109">EXAMPLES</span></span>

### <span data-ttu-id="33c1e-110">Esempio 1: modificare una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="33c1e-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="33c1e-111">Questo comando modifica le tabelle da cui viene letta l'analisi dello spazio di archiviazione denominata MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="33c1e-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="33c1e-112">Esempio 2: modificare un'analisi dello spazio di archiviazione usando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="33c1e-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="33c1e-113">Il primo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo archivia nella variabile $Workspace.</span><span class="sxs-lookup"><span data-stu-id="33c1e-113">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="33c1e-114">Il secondo comando consente di modificare i contenitori da cui si legge l'Insight di archiviazione denominato MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="33c1e-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="33c1e-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="33c1e-115">PARAMETERS</span></span>

### <span data-ttu-id="33c1e-116">-Contenitori</span><span class="sxs-lookup"><span data-stu-id="33c1e-116">-Containers</span></span>
<span data-ttu-id="33c1e-117">Specifica l'elenco di contenitori che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="33c1e-117">Specifies the list of containers that provide the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c1e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c1e-118">-DefaultProfile</span></span>
<span data-ttu-id="33c1e-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="33c1e-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33c1e-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="33c1e-120">-Name</span></span>
<span data-ttu-id="33c1e-121">Specifica il nome di un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33c1e-121">Specifies the name of a Storage Insight.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c1e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c1e-122">-ResourceGroupName</span></span>
<span data-ttu-id="33c1e-123">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="33c1e-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="33c1e-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="33c1e-124">-StorageAccountKey</span></span>
<span data-ttu-id="33c1e-125">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33c1e-125">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c1e-126">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="33c1e-126">-Tables</span></span>
<span data-ttu-id="33c1e-127">Specifica l'elenco delle tabelle che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="33c1e-127">Specifies the list of tables that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="33c1e-128">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="33c1e-128">-Workspace</span></span>
<span data-ttu-id="33c1e-129">Specifica l'area di lavoro che contiene la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="33c1e-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="33c1e-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="33c1e-130">-WorkspaceName</span></span>
<span data-ttu-id="33c1e-131">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="33c1e-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="33c1e-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c1e-132">CommonParameters</span></span>
<span data-ttu-id="33c1e-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c1e-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c1e-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33c1e-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c1e-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="33c1e-135">INPUTS</span></span>

### <span data-ttu-id="33c1e-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="33c1e-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="33c1e-137">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="33c1e-137">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="33c1e-138">System. String</span><span class="sxs-lookup"><span data-stu-id="33c1e-138">System.String</span></span>

### <span data-ttu-id="33c1e-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="33c1e-139">System.String[]</span></span>

## <span data-ttu-id="33c1e-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="33c1e-140">OUTPUTS</span></span>

### <span data-ttu-id="33c1e-141">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="33c1e-141">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="33c1e-142">Note</span><span class="sxs-lookup"><span data-stu-id="33c1e-142">NOTES</span></span>

## <span data-ttu-id="33c1e-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="33c1e-143">RELATED LINKS</span></span>

[<span data-ttu-id="33c1e-144">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="33c1e-144">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="33c1e-145">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="33c1e-145">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


