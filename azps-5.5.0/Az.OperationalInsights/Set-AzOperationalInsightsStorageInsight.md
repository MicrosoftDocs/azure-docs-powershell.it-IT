---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 53482eade80e1fdc3d719160185941741e447258
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186695"
---
# <span data-ttu-id="ef54b-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ef54b-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="ef54b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef54b-102">SYNOPSIS</span></span>
<span data-ttu-id="ef54b-103">Aggiorna un approfondimento di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ef54b-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="ef54b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ef54b-104">SYNTAX</span></span>

### <span data-ttu-id="ef54b-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ef54b-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ef54b-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="ef54b-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ef54b-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="ef54b-107">DESCRIPTION</span></span>
<span data-ttu-id="ef54b-108">Il cmdlet **Set-AzOperationalInsightsStorageInsight** cambia la configurazione di un elemento Storage Insight.</span><span class="sxs-lookup"><span data-stu-id="ef54b-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="ef54b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ef54b-109">EXAMPLES</span></span>

### <span data-ttu-id="ef54b-110">Esempio 1: Modificare un approfondimento di archiviazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="ef54b-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="ef54b-111">Questo comando modifica le tabelle da cui vengono lette le informazioni di archiviazione denominate MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="ef54b-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="ef54b-112">Esempio 2: Modificare un approfondimento di archiviazione usando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ef54b-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="ef54b-113">Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkspace e quindi la archivia nella $Workspace variabile.</span><span class="sxs-lookup"><span data-stu-id="ef54b-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="ef54b-114">Il secondo comando modifica i contenitori da cui vengono letti i dati di Archiviazione denominati MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="ef54b-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="ef54b-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef54b-115">PARAMETERS</span></span>

### <span data-ttu-id="ef54b-116">-Containers</span><span class="sxs-lookup"><span data-stu-id="ef54b-116">-Containers</span></span>
<span data-ttu-id="ef54b-117">Specifica l'elenco di contenitori che forniscono i dati.</span><span class="sxs-lookup"><span data-stu-id="ef54b-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="ef54b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef54b-118">-DefaultProfile</span></span>
<span data-ttu-id="ef54b-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="ef54b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef54b-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ef54b-120">-Name</span></span>
<span data-ttu-id="ef54b-121">Specifica il nome di un approfondimento di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ef54b-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="ef54b-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef54b-122">-ResourceGroupName</span></span>
<span data-ttu-id="ef54b-123">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ef54b-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="ef54b-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="ef54b-124">-StorageAccountKey</span></span>
<span data-ttu-id="ef54b-125">Specifica la chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ef54b-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="ef54b-126">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="ef54b-126">-Tables</span></span>
<span data-ttu-id="ef54b-127">Specifica l'elenco di tabelle che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="ef54b-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="ef54b-128">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="ef54b-128">-Workspace</span></span>
<span data-ttu-id="ef54b-129">Specifica l'area di lavoro che contiene i dati di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ef54b-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="ef54b-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="ef54b-130">-WorkspaceName</span></span>
<span data-ttu-id="ef54b-131">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="ef54b-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="ef54b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef54b-132">CommonParameters</span></span>
<span data-ttu-id="ef54b-133">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef54b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef54b-134">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef54b-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef54b-135">INPUT</span><span class="sxs-lookup"><span data-stu-id="ef54b-135">INPUTS</span></span>

### <span data-ttu-id="ef54b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef54b-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="ef54b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="ef54b-137">System.String</span></span>

### <span data-ttu-id="ef54b-138">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ef54b-138">System.String[]</span></span>

## <span data-ttu-id="ef54b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ef54b-139">OUTPUTS</span></span>

### <span data-ttu-id="ef54b-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="ef54b-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="ef54b-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="ef54b-141">NOTES</span></span>

## <span data-ttu-id="ef54b-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ef54b-142">RELATED LINKS</span></span>

[<span data-ttu-id="ef54b-143">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="ef54b-143">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="ef54b-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="ef54b-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


