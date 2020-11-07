---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 010328F9-C878-4F16-AFD7-2135465A1968
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/set-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Set-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: b81d7e7d87e8db7658db425f889630a3897d1ecd
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/13/2020
ms.locfileid: "93685278"
---
# <span data-ttu-id="b7257-101">Set-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b7257-101">Set-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="b7257-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="b7257-102">SYNOPSIS</span></span>
<span data-ttu-id="b7257-103">Aggiorna un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b7257-103">Updates a Storage Insight.</span></span>

## <span data-ttu-id="b7257-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="b7257-104">SYNTAX</span></span>

### <span data-ttu-id="b7257-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="b7257-105">ByWorkspaceName (Default)</span></span>
```
Set-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7257-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="b7257-106">ByWorkspaceObject</span></span>
```
Set-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [[-StorageAccountKey] <String>] [[-Tables] <String[]>] [[-Containers] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7257-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="b7257-107">DESCRIPTION</span></span>
<span data-ttu-id="b7257-108">Il cmdlet **set-AzOperationalInsightsStorageInsight** modifica la configurazione di un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b7257-108">The **Set-AzOperationalInsightsStorageInsight** cmdlet changes the configuration of a Storage Insight.</span></span>

## <span data-ttu-id="b7257-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="b7257-109">EXAMPLES</span></span>

### <span data-ttu-id="b7257-110">Esempio 1: modificare una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="b7257-110">Example 1: Modify a Storage Insight by name</span></span>
```
PS C:\>Set-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="b7257-111">Questo comando modifica le tabelle da cui viene letta l'analisi dello spazio di archiviazione denominata MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="b7257-111">This command modifies the tables from which the Storage Insight named MyStorageInsight reads.</span></span>

### <span data-ttu-id="b7257-112">Esempio 2: modificare un'analisi dello spazio di archiviazione usando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b7257-112">Example 2: Modify a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>Set-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -Containers @("wad-iis-logfiles")
```

<span data-ttu-id="b7257-113">Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo archivia nella variabile $Workspace.</span><span class="sxs-lookup"><span data-stu-id="b7257-113">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="b7257-114">Il secondo comando consente di modificare i contenitori da cui si legge l'Insight di archiviazione denominato MyStorageInsight.</span><span class="sxs-lookup"><span data-stu-id="b7257-114">The second command modifies the containers from which the Storage Insight named MyStorageInsight reads.</span></span>

## <span data-ttu-id="b7257-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="b7257-115">PARAMETERS</span></span>

### <span data-ttu-id="b7257-116">-Contenitori</span><span class="sxs-lookup"><span data-stu-id="b7257-116">-Containers</span></span>
<span data-ttu-id="b7257-117">Specifica l'elenco di contenitori che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="b7257-117">Specifies the list of containers that provide the data.</span></span>

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

### <span data-ttu-id="b7257-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7257-118">-DefaultProfile</span></span>
<span data-ttu-id="b7257-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="b7257-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7257-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="b7257-120">-Name</span></span>
<span data-ttu-id="b7257-121">Specifica il nome di un'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b7257-121">Specifies the name of a Storage Insight.</span></span>

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

### <span data-ttu-id="b7257-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7257-122">-ResourceGroupName</span></span>
<span data-ttu-id="b7257-123">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b7257-123">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="b7257-124">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="b7257-124">-StorageAccountKey</span></span>
<span data-ttu-id="b7257-125">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b7257-125">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="b7257-126">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="b7257-126">-Tables</span></span>
<span data-ttu-id="b7257-127">Specifica l'elenco delle tabelle che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="b7257-127">Specifies the list of tables that contain the data.</span></span>

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

### <span data-ttu-id="b7257-128">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="b7257-128">-Workspace</span></span>
<span data-ttu-id="b7257-129">Specifica l'area di lavoro che contiene la panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="b7257-129">Specifies the workspace that contains the Storage Insight.</span></span>

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

### <span data-ttu-id="b7257-130">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="b7257-130">-WorkspaceName</span></span>
<span data-ttu-id="b7257-131">Specifica il nome di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="b7257-131">Specifies the name of a workspace.</span></span>

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

### <span data-ttu-id="b7257-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7257-132">CommonParameters</span></span>
<span data-ttu-id="b7257-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7257-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7257-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7257-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7257-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="b7257-135">INPUTS</span></span>

### <span data-ttu-id="b7257-136">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="b7257-136">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="b7257-137">System. String</span><span class="sxs-lookup"><span data-stu-id="b7257-137">System.String</span></span>

### <span data-ttu-id="b7257-138">System. String []</span><span class="sxs-lookup"><span data-stu-id="b7257-138">System.String[]</span></span>

## <span data-ttu-id="b7257-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="b7257-139">OUTPUTS</span></span>

### <span data-ttu-id="b7257-140">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="b7257-140">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="b7257-141">Note</span><span class="sxs-lookup"><span data-stu-id="b7257-141">NOTES</span></span>

## <span data-ttu-id="b7257-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="b7257-142">RELATED LINKS</span></span>

[<span data-ttu-id="b7257-143">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="b7257-143">Azure Operational Insights Cmdlets</span></span>](/powershell/module/az.operationalinsights)

[<span data-ttu-id="b7257-144">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="b7257-144">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


