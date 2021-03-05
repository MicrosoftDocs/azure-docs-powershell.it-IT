---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: f3ab3c381e36c766e6d4bdb24476f6bd1cd69df3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101989896"
---
# <span data-ttu-id="4d3af-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="4d3af-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="4d3af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d3af-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3af-103">Crea un approfondimento di archiviazione all'interno di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4d3af-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="4d3af-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4d3af-104">SYNTAX</span></span>

### <span data-ttu-id="4d3af-105">ByWorkspaceName (Impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4d3af-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4d3af-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="4d3af-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4d3af-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4d3af-107">DESCRIPTION</span></span>
<span data-ttu-id="4d3af-108">Il cmdlet **New-AzOperationalInsightsStorageInsight** crea una nuova istanza di Storage Insight in un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="4d3af-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="4d3af-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4d3af-109">EXAMPLES</span></span>

### <span data-ttu-id="4d3af-110">Esempio 1: Creare un approfondimento di archiviazione in base al nome</span><span class="sxs-lookup"><span data-stu-id="4d3af-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="4d3af-111">Il primo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione denominato ContosoStorage e quindi lo archivia nella $Storage variabile.</span><span class="sxs-lookup"><span data-stu-id="4d3af-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="4d3af-112">Il secondo comando passa l'account di archiviazione di $Storage al cmdlet Get-AzStorageAccountKey usando l'operatore della pipeline per ottenere la chiave dell'account di archiviazione specificata e quindi la archivia nella variabile $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="4d3af-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="4d3af-113">Questo esempio recupera la prima chiave.</span><span class="sxs-lookup"><span data-stu-id="4d3af-113">This example retrieves the first key.</span></span> <span data-ttu-id="4d3af-114">Per recuperare l'altro, usare Valore[1] invece di Valore[0].</span><span class="sxs-lookup"><span data-stu-id="4d3af-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="4d3af-115">Il comando finale crea un'analisi dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro denominata MyWorkspace.</span><span class="sxs-lookup"><span data-stu-id="4d3af-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="4d3af-116">Queste informazioni di archiviazione utilizzano i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="4d3af-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="4d3af-117">Esempio 2: Creare un approfondimento di archiviazione usando un oggetto area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4d3af-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="4d3af-118">Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata MyWorkspace e quindi la archivia nella $Workspace variabile.</span><span class="sxs-lookup"><span data-stu-id="4d3af-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="4d3af-119">Il secondo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione specificato e quindi lo archivia nella $Storage variabile.</span><span class="sxs-lookup"><span data-stu-id="4d3af-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="4d3af-120">Il terzo comando passa l'account di archiviazione di $Storage al cmdlet Get-AzStorageAccountKey usando l'operatore della pipeline per ottenere la chiave specificata e quindi lo archivia nella variabile $StorageKey variabile.</span><span class="sxs-lookup"><span data-stu-id="4d3af-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="4d3af-121">Questo esempio recupera la prima chiave.</span><span class="sxs-lookup"><span data-stu-id="4d3af-121">This example retrieves the first key.</span></span> <span data-ttu-id="4d3af-122">Per recuperare l'altro, usare Valore[1] invece di Valore[0].</span><span class="sxs-lookup"><span data-stu-id="4d3af-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="4d3af-123">Il comando finale crea un'analisi dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro definita in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="4d3af-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="4d3af-124">Informazioni dettagliate di archiviazione utilizza i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="4d3af-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="4d3af-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d3af-125">PARAMETERS</span></span>

### <span data-ttu-id="4d3af-126">-Containers</span><span class="sxs-lookup"><span data-stu-id="4d3af-126">-Containers</span></span>
<span data-ttu-id="4d3af-127">Specifica l'elenco di contenitori che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="4d3af-127">Specifies the list of containers that contain the data.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3af-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3af-128">-DefaultProfile</span></span>
<span data-ttu-id="4d3af-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4d3af-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d3af-130">-Force</span><span class="sxs-lookup"><span data-stu-id="4d3af-130">-Force</span></span>
<span data-ttu-id="4d3af-131">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="4d3af-131">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3af-132">-Name</span><span class="sxs-lookup"><span data-stu-id="4d3af-132">-Name</span></span>
<span data-ttu-id="4d3af-133">Specifica il nome dell'approfondimento di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4d3af-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="4d3af-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d3af-134">-ResourceGroupName</span></span>
<span data-ttu-id="4d3af-135">Specifica il nome di un gruppo di risorse di Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="4d3af-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="4d3af-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="4d3af-136">-StorageAccountKey</span></span>
<span data-ttu-id="4d3af-137">Specifica la chiave di accesso per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4d3af-137">Specifies the access key for the storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3af-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="4d3af-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="4d3af-139">Specifica la risorsa Azure di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4d3af-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="4d3af-140">Può essere recuperata eseguendo il cmdlet Get-AzStorageAccount e accedendo al *parametro ID* del risultato.</span><span class="sxs-lookup"><span data-stu-id="4d3af-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d3af-141">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="4d3af-141">-Tables</span></span>
<span data-ttu-id="4d3af-142">Specifica l'elenco di tabelle che forniscono i dati.</span><span class="sxs-lookup"><span data-stu-id="4d3af-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="4d3af-143">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="4d3af-143">-Workspace</span></span>
<span data-ttu-id="4d3af-144">Specifica l'area di lavoro per il nuovo approfondimento archiviazione.</span><span class="sxs-lookup"><span data-stu-id="4d3af-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="4d3af-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="4d3af-145">-WorkspaceName</span></span>
<span data-ttu-id="4d3af-146">Specifica il nome di un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="4d3af-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="4d3af-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d3af-147">-Confirm</span></span>
<span data-ttu-id="4d3af-148">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3af-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3af-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3af-149">-WhatIf</span></span>
<span data-ttu-id="4d3af-150">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d3af-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3af-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4d3af-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d3af-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3af-152">CommonParameters</span></span>
<span data-ttu-id="4d3af-153">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3af-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3af-154">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d3af-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3af-155">INPUT</span><span class="sxs-lookup"><span data-stu-id="4d3af-155">INPUTS</span></span>

### <span data-ttu-id="4d3af-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d3af-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="4d3af-157">System.String</span><span class="sxs-lookup"><span data-stu-id="4d3af-157">System.String</span></span>

### <span data-ttu-id="4d3af-158">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4d3af-158">System.String[]</span></span>

## <span data-ttu-id="4d3af-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4d3af-159">OUTPUTS</span></span>

### <span data-ttu-id="4d3af-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="4d3af-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="4d3af-161">NOTE</span><span class="sxs-lookup"><span data-stu-id="4d3af-161">NOTES</span></span>

## <span data-ttu-id="4d3af-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4d3af-162">RELATED LINKS</span></span>

[<span data-ttu-id="4d3af-163">Cmdlet di Azure Operational Insights</span><span class="sxs-lookup"><span data-stu-id="4d3af-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="4d3af-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="4d3af-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


