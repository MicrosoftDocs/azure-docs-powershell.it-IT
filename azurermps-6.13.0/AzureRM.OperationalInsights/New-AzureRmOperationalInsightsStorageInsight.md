---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 7660F1A2-604D-4488-93F1-CB7C502F135E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/new-azurermoperationalinsightsstorageinsight
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/New-AzureRmOperationalInsightsStorageInsight.md
ms.openlocfilehash: 1bea5ce9eda22996eb65b6e5d26fb3af19cd1c88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93513556"
---
# <span data-ttu-id="c62eb-101">New-AzureRmOperationalInsightsStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c62eb-101">New-AzureRmOperationalInsightsStorageInsight</span></span>

## <span data-ttu-id="c62eb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c62eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c62eb-103">Crea un'analisi di archiviazione all'interno di un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c62eb-103">Creates a Storage Insight inside a workspace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c62eb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c62eb-104">SYNTAX</span></span>

### <span data-ttu-id="c62eb-105">ByWorkspaceName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c62eb-105">ByWorkspaceName (Default)</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c62eb-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c62eb-106">ByWorkspaceObject</span></span>
```
New-AzureRmOperationalInsightsStorageInsight [-Workspace] <PSWorkspace> [-Name] <String>
 [-StorageAccountResourceId] <String> [-StorageAccountKey] <String> [[-Tables] <String[]>]
 [[-Containers] <String[]>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c62eb-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c62eb-107">DESCRIPTION</span></span>
<span data-ttu-id="c62eb-108">Il cmdlet **New-AzureRmOperationalInsightsStorageInsight** crea una nuova panoramica dello spazio di archiviazione in un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="c62eb-108">The **New-AzureRmOperationalInsightsStorageInsight** cmdlet creates a new Storage Insight in an existing workspace.</span></span>

## <span data-ttu-id="c62eb-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c62eb-109">EXAMPLES</span></span>

### <span data-ttu-id="c62eb-110">Esempio 1: creare una panoramica dello spazio di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="c62eb-110">Example 1: Create a Storage Insight by name</span></span>
```
PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -ResourceGroupName "ContosoResourceGroup" -WorkspaceName "MyWorkspace" -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c62eb-111">Il primo comando usa il cmdlet Get-AzureRmStorageAccount per ottenere l'account di archiviazione denominato ContosoStorage e lo archivia nella variabile $Storage.</span><span class="sxs-lookup"><span data-stu-id="c62eb-111">The first command uses the Get-AzureRmStorageAccount cmdlet to get the storage account named ContosoStorage, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="c62eb-112">Il secondo comando passa l'account di archiviazione in $Storage al cmdlet Get-AzureRmStorageAccountKey usando l'operatore pipeline per ottenere la chiave dell'account di archiviazione specificata e la memorizza nella variabile $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="c62eb-112">The second command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified storage account key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="c62eb-113">Il comando finale crea una panoramica dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro denominata spazio di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c62eb-113">The final command creates a storage insight named MyStorageInsight in the workspace named MyWorkspace.</span></span>
<span data-ttu-id="c62eb-114">Questa panoramica dello spazio di archiviazione utilizza i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="c62eb-114">This storage insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

### <span data-ttu-id="c62eb-115">Esempio 2: creare una panoramica dello spazio di archiviazione utilizzando un oggetto Workspace</span><span class="sxs-lookup"><span data-stu-id="c62eb-115">Example 2: Create a Storage Insight by using a workspace object</span></span>
```
PS C:\>$Workspace = Get-AzureRmOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"

PS C:\>$Storage = Get-AzureRmStorageAccount -ResourceGroupName "ContosoResourceGroup" -Name "ContosoStorage"

PS C:\>$StorageKey = ($Storage | Get-AzureRmStorageAccountKey).Key1

PS C:\>New-AzureRmOperationalInsightsStorageInsight -Workspace $Workspace -Name "MyStorageInsight" -StorageAccountResourceId $Storage.Id -StorageAccountKey $StorageKey -Tables @("WADWindowsEventLogsTable")
```

<span data-ttu-id="c62eb-116">Il primo comando usa il cmdlet Get-AzureRmOperationalInsightsWorkspace per ottenere l'area di lavoro denominata Workspace e lo archivia nella variabile $Workspace.</span><span class="sxs-lookup"><span data-stu-id="c62eb-116">The first command uses the Get-AzureRmOperationalInsightsWorkspace cmdlet to get the workspace named MyWorkspace, and then stores it in the $Workspace variable.</span></span>
<span data-ttu-id="c62eb-117">Il secondo comando usa il cmdlet Get-AzureRmStorageAccount per ottenere l'account di archiviazione specificato e lo archivia nella variabile $Storage.</span><span class="sxs-lookup"><span data-stu-id="c62eb-117">The second command uses the Get-AzureRmStorageAccount cmdlet to get the specified storage account, and then stores it in the $Storage variable.</span></span>
<span data-ttu-id="c62eb-118">Il terzo comando passa l'account di archiviazione in $Storage al cmdlet Get-AzureRmStorageAccountKey usando l'operatore pipeline per ottenere la chiave specificata e quindi la archivia nella variabile $StorageKey.</span><span class="sxs-lookup"><span data-stu-id="c62eb-118">The third command passes the storage account in $Storage to the Get-AzureRmStorageAccountKey cmdlet by using the pipeline operator to get the specified key, and then stores it in the $StorageKey variable.</span></span>
<span data-ttu-id="c62eb-119">Il comando finale crea una panoramica dello spazio di archiviazione denominata MyStorageInsight nell'area di lavoro definita in $Workspace.</span><span class="sxs-lookup"><span data-stu-id="c62eb-119">The final command creates a storage insight named MyStorageInsight in the workspace defined in $Workspace.</span></span>
<span data-ttu-id="c62eb-120">La panoramica dello spazio di archiviazione utilizza i dati della tabella WADWindowsEventLogsTable nella risorsa dell'account di archiviazione specificata.</span><span class="sxs-lookup"><span data-stu-id="c62eb-120">The Storage Insight consumes data from the WADWindowsEventLogsTable table in the specified storage account resource.</span></span>

## <span data-ttu-id="c62eb-121">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c62eb-121">PARAMETERS</span></span>

### <span data-ttu-id="c62eb-122">-Contenitori</span><span class="sxs-lookup"><span data-stu-id="c62eb-122">-Containers</span></span>
<span data-ttu-id="c62eb-123">Specifica l'elenco di contenitori che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="c62eb-123">Specifies the list of containers that contain the data.</span></span>

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

### <span data-ttu-id="c62eb-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c62eb-124">-DefaultProfile</span></span>
<span data-ttu-id="c62eb-125">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c62eb-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c62eb-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c62eb-126">-Force</span></span>
<span data-ttu-id="c62eb-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c62eb-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c62eb-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="c62eb-128">-Name</span></span>
<span data-ttu-id="c62eb-129">Specifica il nome dell'analisi dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c62eb-129">Specifies the name of the Storage Insight.</span></span>

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

### <span data-ttu-id="c62eb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c62eb-130">-ResourceGroupName</span></span>
<span data-ttu-id="c62eb-131">Specifica il nome di un gruppo di risorse Azure che contiene un'area di lavoro.</span><span class="sxs-lookup"><span data-stu-id="c62eb-131">Specifies the name of an Azure resource group that contains a workspace.</span></span>

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

### <span data-ttu-id="c62eb-132">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c62eb-132">-StorageAccountKey</span></span>
<span data-ttu-id="c62eb-133">Specifica il tasto di scelta per l'account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c62eb-133">Specifies the access key for the storage account.</span></span>

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

### <span data-ttu-id="c62eb-134">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="c62eb-134">-StorageAccountResourceId</span></span>
<span data-ttu-id="c62eb-135">Specifica la risorsa Azure di un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c62eb-135">Specifies the Azure resource of a storage account.</span></span>
<span data-ttu-id="c62eb-136">Questa operazione può essere recuperata eseguendo il cmdlet Get-AzureRmStorageAccount e accedendo al parametro *ID* del risultato.</span><span class="sxs-lookup"><span data-stu-id="c62eb-136">This can be retrieved by executing the Get-AzureRmStorageAccount cmdlet and accessing the *Id* parameter of the result.</span></span>

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

### <span data-ttu-id="c62eb-137">-Tabelle</span><span class="sxs-lookup"><span data-stu-id="c62eb-137">-Tables</span></span>
<span data-ttu-id="c62eb-138">Specifica l'elenco delle tabelle che contengono i dati.</span><span class="sxs-lookup"><span data-stu-id="c62eb-138">Specifies the list of tables that provide the data.</span></span>

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

### <span data-ttu-id="c62eb-139">-Area di lavoro</span><span class="sxs-lookup"><span data-stu-id="c62eb-139">-Workspace</span></span>
<span data-ttu-id="c62eb-140">Specifica l'area di lavoro per la nuova panoramica dello spazio di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c62eb-140">Specifies the workspace for the new Storage Insight.</span></span>

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

### <span data-ttu-id="c62eb-141">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c62eb-141">-WorkspaceName</span></span>
<span data-ttu-id="c62eb-142">Specifica il nome di un'area di lavoro esistente.</span><span class="sxs-lookup"><span data-stu-id="c62eb-142">Specifies the name of an existing workspace.</span></span>

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

### <span data-ttu-id="c62eb-143">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c62eb-143">-Confirm</span></span>
<span data-ttu-id="c62eb-144">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c62eb-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c62eb-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c62eb-145">-WhatIf</span></span>
<span data-ttu-id="c62eb-146">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c62eb-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c62eb-147">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c62eb-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c62eb-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c62eb-148">CommonParameters</span></span>
<span data-ttu-id="c62eb-149">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c62eb-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c62eb-150">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c62eb-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c62eb-151">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c62eb-151">INPUTS</span></span>

### <span data-ttu-id="c62eb-152">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="c62eb-152">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>
<span data-ttu-id="c62eb-153">Parametri: area di lavoro (ByValue)</span><span class="sxs-lookup"><span data-stu-id="c62eb-153">Parameters: Workspace (ByValue)</span></span>

### <span data-ttu-id="c62eb-154">System. String</span><span class="sxs-lookup"><span data-stu-id="c62eb-154">System.String</span></span>

### <span data-ttu-id="c62eb-155">System. String []</span><span class="sxs-lookup"><span data-stu-id="c62eb-155">System.String[]</span></span>

## <span data-ttu-id="c62eb-156">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c62eb-156">OUTPUTS</span></span>

### <span data-ttu-id="c62eb-157">Microsoft. Azure. Commands. OperationalInsights. Models. PSStorageInsight</span><span class="sxs-lookup"><span data-stu-id="c62eb-157">Microsoft.Azure.Commands.OperationalInsights.Models.PSStorageInsight</span></span>

## <span data-ttu-id="c62eb-158">Note</span><span class="sxs-lookup"><span data-stu-id="c62eb-158">NOTES</span></span>

## <span data-ttu-id="c62eb-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c62eb-159">RELATED LINKS</span></span>

[<span data-ttu-id="c62eb-160">Cmdlet di Insight operativi di Azure</span><span class="sxs-lookup"><span data-stu-id="c62eb-160">Azure Operational Insights Cmdlets</span></span>](./AzureRM.OperationalInsights.md)

[<span data-ttu-id="c62eb-161">Get-AzureRmOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="c62eb-161">Get-AzureRmOperationalInsightsWorkspace</span></span>](./Get-AzureRmOperationalInsightsWorkspace.md)


