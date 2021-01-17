---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/new-azoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/New-AzOperationalInsightsStorageInsight.md
ms.openlocfilehash: 6d936e267c734ddd9df12e0feec22b2d6f6c4b65
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327177"
---
# <span data-ttu-id="6a391-101">New-AzOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6a391-101">New-AzOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="6a391-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6a391-102">SYNOPSIS</span></span>
<span data-ttu-id="6a391-103">Crea un'analisi di archiviazione all'interno di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6a391-103">Creates a Storage Insight inside a workspace.</span></span>

## <span data-ttu-id="6a391-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6a391-104">SYNTAX</span></span>

### <span data-ttu-id="6a391-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6a391-105">ByWorkspaceName (Default)</span></span>
```
New-AzOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6a391-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="6a391-106">ByWorkspaceObject</span></span>
```
New-AzOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6a391-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6a391-107">DESCRIPTION</span></span>
<span data-ttu-id="6a391-108">Il cmdlet **New-AzOperationalInsightsStorageInsight** crea una nuova panoramica dello spazio di archiviazione in un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="6a391-108">The **New-AzOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="6a391-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6a391-109">EXAMPLES</span></span>

### <span data-ttu-id="6a391-110">Esempio 1: creare una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="6a391-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="6a391-111">Il primo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione denominato ContosoStorage e lo archivia nella variabile $Storage.</span><span class="sxs-lookup"><span data-stu-id="6a391-111">The first command uses the Get-AzStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="6a391-112">Il secondo comando passa l'account di archiviazione in $Storage al cmdlet Get-AzStorageAccountKey usando l'operatore pipeline per ottenere la chiave dell'account di archiviazione specificata e la memorizza nella variabile $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="6a391-112">The second command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="6a391-113">Questo esempio recupera la prima chiave.</span><span class="sxs-lookup"><span data-stu-id="6a391-113">This example retrieves the first key.</span></span> <span data-ttu-id="6a391-114">Per recuperare l'altro, USA Value [1] invece di value [0].</span><span class="sxs-lookup"><span data-stu-id="6a391-114">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="6a391-115">Il comando finale crea una panoramica dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro denominata spazio di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6a391-115">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="6a391-116">Questa panoramica dello spazio di archiviazione utilizza i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="6a391-116">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="6a391-117">Esempio 2: creare una panoramica dello spazio di archiviazione utilizzando un oggetto Workspace</span><span class="sxs-lookup"><span data-stu-id="6a391-117">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzStorageAccountKey).Value[0]

PS C:\>New-AzOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="6a391-118">Il primo comando usa il cmdlet Get-AzOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo archivia nella variabile $Workspace.</span><span class="sxs-lookup"><span data-stu-id="6a391-118">The first command uses the Get-AzOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="6a391-119">Il secondo comando usa il cmdlet Get-AzStorageAccount per ottenere l'account di archiviazione specificato e lo archivia nella variabile $Storage.</span><span class="sxs-lookup"><span data-stu-id="6a391-119">The second command uses the Get-AzStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="6a391-120">Il terzo comando passa l'account di archiviazione in $Storage al cmdlet Get-AzStorageAccountKey usando l'operatore pipeline per ottenere la chiave specificata e quindi la archivia nella variabile $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="6a391-120">The third command passes the storage account in $Storage to the Get-AzStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span> <span data-ttu-id="6a391-121">Questo esempio recupera la prima chiave.</span><span class="sxs-lookup"><span data-stu-id="6a391-121">This example retrieves the first key.</span></span> <span data-ttu-id="6a391-122">Per recuperare l'altro, USA Value [1] invece di value [0].</span><span class="sxs-lookup"><span data-stu-id="6a391-122">To retrieve the other one, use Value[1] instead of Value[0].</span></span>
<span data-ttu-id="6a391-123">Il comando finale crea una panoramica dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro definita in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="6a391-123">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="6a391-124">La panoramica dello spazio di archiviazione utilizza i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="6a391-124">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="6a391-125">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6a391-125">PARAMETERS</span></span>

### <span data-ttu-id="6a391-126">-Contenitori</span><span class="sxs-lookup"><span data-stu-id="6a391-126">-Containers</span></span>
<span data-ttu-id="6a391-127">Specifica l'elenco di contenitori che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="6a391-127">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="6a391-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a391-128">-DefaultProfile</span></span>
<span data-ttu-id="6a391-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="6a391-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6a391-130">-Force</span><span class="sxs-lookup"><span data-stu-id="6a391-130">-Force</span></span>
<span data-ttu-id="6a391-131">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6a391-131">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6a391-132">-Nome</span><span class="sxs-lookup"><span data-stu-id="6a391-132">-Name</span></span>
<span data-ttu-id="6a391-133">Specifica il nome dell'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a391-133">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="6a391-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6a391-134">-ResourceGroupName</span></span>
<span data-ttu-id="6a391-135">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="6a391-135">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="6a391-136">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="6a391-136">-StorageAccountKey</span></span>
<span data-ttu-id="6a391-137">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a391-137">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="6a391-138">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="6a391-138">-StorageAccountResourceId</span></span>
<span data-ttu-id="6a391-139">Specifica la risorsa Azure di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a391-139">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="6a391-140">Questa operazione può essere recuperata eseguendo il cmdlet Get-AzStorageAccount e accedendo al parametro *ID* del risultato.</span><span class="sxs-lookup"><span data-stu-id="6a391-140">This can be retrieved by executing the Get-AzStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="6a391-141">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="6a391-141">-Tables</span></span>
<span data-ttu-id="6a391-142">Specifica l'elenco delle tabelle che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="6a391-142">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="6a391-143">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="6a391-143">-Workspace</span></span>
<span data-ttu-id="6a391-144">Specifica l'area di lavoro per la nuova panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6a391-144">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="6a391-145">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="6a391-145">-WorkspaceName</span></span>
<span data-ttu-id="6a391-146">Specifica il nome di un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="6a391-146">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="6a391-147">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6a391-147">-Confirm</span></span>
<span data-ttu-id="6a391-148">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a391-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a391-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a391-149">-WhatIf</span></span>
<span data-ttu-id="6a391-150">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a391-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6a391-151">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6a391-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a391-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a391-152">CommonParameters</span></span>
<span data-ttu-id="6a391-153">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a391-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a391-154">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a391-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a391-155">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6a391-155">INPUTS</span></span>

### <span data-ttu-id="6a391-156">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a391-156">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="6a391-157">System. String</span><span class="sxs-lookup"><span data-stu-id="6a391-157">System.String</span></span>

### <span data-ttu-id="6a391-158">System. String []</span><span class="sxs-lookup"><span data-stu-id="6a391-158">System.String[]</span></span>

## <span data-ttu-id="6a391-159">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6a391-159">OUTPUTS</span></span>

### <span data-ttu-id="6a391-160">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="6a391-160">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="6a391-161">Note</span><span class="sxs-lookup"><span data-stu-id="6a391-161">NOTES</span></span>

## <span data-ttu-id="6a391-162">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6a391-162">RELATED LINKS</span></span>

[<span data-ttu-id="6a391-163">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="6a391-163">Azure Operational Insights Cmdlets</span></span>](./Az.OperationalInsights.md)

[<span data-ttu-id="6a391-164">Get-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="6a391-164">Get-AzOperationalInsightsWorkspace</span></span>](./Get-AzOperationalInsightsWorkspace.md)


