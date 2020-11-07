---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 3C6DCC81-82F7-4044-AFBC-4EE1BCC306F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/invoke-azhdinsighthivejob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/Invoke-AzHDInsightHiveJob.md
ms.openlocfilehash: f51545cc28a11984c55fa05b6760b71a055de7a7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674310"
---
# <span data-ttu-id="c2f85-101">Invoke-AzHDInsightHiveJob</span><span class="sxs-lookup"><span data-stu-id="c2f85-101">Invoke-AzHDInsightHiveJob</span></span>

## <span data-ttu-id="c2f85-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c2f85-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f85-103">Invia una query hive a un cluster HDInsight e recupera i risultati della query in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="c2f85-103">Submits a Hive query to an HDInsight cluster and retrieves query results in one operation.</span></span>

## <span data-ttu-id="c2f85-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c2f85-104">SYNTAX</span></span>

```
Invoke-AzHDInsightHiveJob [-Arguments <String[]>] [-Files <String[]>] [-StatusFolder <String>]
 [-Defines <Hashtable>] [-File <String>] [-JobName <String>] [-Query <String>] [-RunAsFileJob]
 [-DefaultContainer <String>] [-DefaultStorageAccountName <String>] [-DefaultStorageAccountKey <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2f85-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c2f85-105">DESCRIPTION</span></span>
<span data-ttu-id="c2f85-106">Il cmdlet **Invoke-AzHDInsightHiveJob** invia una query hive a un cluster HDInsight di Azure e recupera i risultati di una query in un'unica operazione.</span><span class="sxs-lookup"><span data-stu-id="c2f85-106">The **Invoke-AzHDInsightHiveJob** cmdlet submits a Hive query to an Azure HDInsight cluster and retrieves query results in one operation.</span></span>
<span data-ttu-id="c2f85-107">Usa il cmdlet Use-AzHDInsightCluster prima di chiamare **Invoke-AzHDInsightHiveJob** per specificare quale cluster verrà usato per la query.</span><span class="sxs-lookup"><span data-stu-id="c2f85-107">Use the Use-AzHDInsightCluster cmdlet before calling **Invoke-AzHDInsightHiveJob** to specify which cluster will be used for the query.</span></span>

## <span data-ttu-id="c2f85-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c2f85-108">EXAMPLES</span></span>

### <span data-ttu-id="c2f85-109">Esempio 1: inviare una query hive a un cluster di Azure HDInsight</span><span class="sxs-lookup"><span data-stu-id="c2f85-109">Example 1: Submit a Hive query to an Azure HDInsight cluster</span></span>
```
PS C:\># Primary storage account info
PS C:\> $storageAccountResourceGroupName = "Group"
PS C:\> $storageAccountName = "yourstorageacct001"
PS C:\> $storageAccountKey = (Get-AzStorageAccountKey -ResourceGroupName $storageAccountResourceGroupName -Name $storageAccountName)[0].value


PS C:\> $storageContainer = "container001"

# Cluster info
PS C:\> $clusterName = "your-hadoop-001"
PS C:\> $clusterCreds = Get-Credential

# Hive job details
PS C:\> $statusFolder = "tempStatusFolder/"
PS C:\> $query = "SHOW TABLES"

PS C:\> Use-AzHDInsightCluster `
            -ClusterCredential $clusterCreds `
            -ClusterName $clusterName

PS C:\> Invoke-AzHDInsightHiveJob -StatusFolder $statusFolder `
            -Query $query `
            -DefaultContainer $storageAccountContainer `
            -DefaultStorageAccountName "$storageAccountName.blob.core.windows.net" `
            -DefaultStorageAccountKey $storageAccountKey
```

<span data-ttu-id="c2f85-110">Questo comando Invia la query SHOW Tables al cluster denominato your-Hadoop-001.</span><span class="sxs-lookup"><span data-stu-id="c2f85-110">This command submits the query SHOW TABLES to the cluster named your-hadoop-001.</span></span>

## <span data-ttu-id="c2f85-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c2f85-111">PARAMETERS</span></span>

### <span data-ttu-id="c2f85-112">-Argomenti</span><span class="sxs-lookup"><span data-stu-id="c2f85-112">-Arguments</span></span>
<span data-ttu-id="c2f85-113">Specifica una matrice di argomenti per il processo.</span><span class="sxs-lookup"><span data-stu-id="c2f85-113">Specifies an array of arguments for the job.</span></span>
<span data-ttu-id="c2f85-114">Gli argomenti vengono passati come argomenti della riga di comando per ogni attività.</span><span class="sxs-lookup"><span data-stu-id="c2f85-114">The arguments are passed as command-line arguments to each task.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-115">-DefaultContainer</span><span class="sxs-lookup"><span data-stu-id="c2f85-115">-DefaultContainer</span></span>
<span data-ttu-id="c2f85-116">Specifica il nome del contenitore predefinito nell'account di archiviazione di Azure predefinito usato da un cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2f85-116">Specifies the name of the default container in the default Azure Storage account that an HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f85-117">-DefaultProfile</span></span>
<span data-ttu-id="c2f85-118">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="c2f85-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2f85-119">-DefaultStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c2f85-119">-DefaultStorageAccountKey</span></span>
<span data-ttu-id="c2f85-120">Specifica la chiave dell'account per l'account di archiviazione predefinito usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2f85-120">Specifies the account key for the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-121">-DefaultStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="c2f85-121">-DefaultStorageAccountName</span></span>
<span data-ttu-id="c2f85-122">Specifica il nome dell'account di archiviazione predefinito usato dal cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="c2f85-122">Specifies the name of the default storage account that the HDInsight cluster uses.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-123">-Definisce</span><span class="sxs-lookup"><span data-stu-id="c2f85-123">-Defines</span></span>
<span data-ttu-id="c2f85-124">Specifica i valori di configurazione di Hadoop da impostare quando viene eseguito un processo.</span><span class="sxs-lookup"><span data-stu-id="c2f85-124">Specifies Hadoop configuration values to set when a job runs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-125">-File</span><span class="sxs-lookup"><span data-stu-id="c2f85-125">-File</span></span>
<span data-ttu-id="c2f85-126">Specifica il percorso di un file in Azure storage che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c2f85-126">Specifies the path to a file in Azure Storage that contains the query to run.</span></span>
<span data-ttu-id="c2f85-127">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="c2f85-127">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-128">-File</span><span class="sxs-lookup"><span data-stu-id="c2f85-128">-Files</span></span>
<span data-ttu-id="c2f85-129">Specifica una raccolta di file necessari per un processo hive.</span><span class="sxs-lookup"><span data-stu-id="c2f85-129">Specifies a collection of files that are required for a Hive job.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-130">-JobName</span><span class="sxs-lookup"><span data-stu-id="c2f85-130">-JobName</span></span>
<span data-ttu-id="c2f85-131">Specifica il nome di un processo hive.</span><span class="sxs-lookup"><span data-stu-id="c2f85-131">Specifies the name of a Hive job.</span></span>
<span data-ttu-id="c2f85-132">Se non specifichi questo parametro, questo cmdlet usa il valore predefinito: "hive: \< first 100 characters of query \> ".</span><span class="sxs-lookup"><span data-stu-id="c2f85-132">If you do not specify this parameter, this cmdlet uses the default value: "Hive: \<first 100 characters of Query\>".</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-133">-Query</span><span class="sxs-lookup"><span data-stu-id="c2f85-133">-Query</span></span>
<span data-ttu-id="c2f85-134">Specifica la query hive.</span><span class="sxs-lookup"><span data-stu-id="c2f85-134">Specifies the Hive query.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-135">-RunAsFileJob</span><span class="sxs-lookup"><span data-stu-id="c2f85-135">-RunAsFileJob</span></span>
<span data-ttu-id="c2f85-136">Indica che questo cmdlet crea un file nell'account di archiviazione di Azure predefinito in cui archiviare una query.</span><span class="sxs-lookup"><span data-stu-id="c2f85-136">Indicates that this cmdlet creates a file in the default Azure storage account in which to store a query.</span></span>
<span data-ttu-id="c2f85-137">Questo cmdlet invia il processo che fa riferimento a questo file come script da eseguire.</span><span class="sxs-lookup"><span data-stu-id="c2f85-137">This cmdlet submits the job that references this file as a script to run.</span></span>
<span data-ttu-id="c2f85-138">Puoi usare questa funzionalità per gestire caratteri speciali come il segno di percentuale (%) l'invio di un processo non viene eseguito tramite Templeton, perché Templeton interpreta una query con un segno di percentuale come parametro URL.</span><span class="sxs-lookup"><span data-stu-id="c2f85-138">You can use this functionality to handle special characters such as percent sign (%) that would fail on a job submission through Templeton, because Templeton interprets a query with a percent sign as a URL parameter.</span></span>

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

### <span data-ttu-id="c2f85-139">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="c2f85-139">-StatusFolder</span></span>
<span data-ttu-id="c2f85-140">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="c2f85-140">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2f85-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f85-141">CommonParameters</span></span>
<span data-ttu-id="c2f85-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f85-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f85-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f85-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f85-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c2f85-144">INPUTS</span></span>

### <span data-ttu-id="c2f85-145">Nessuno</span><span class="sxs-lookup"><span data-stu-id="c2f85-145">None</span></span>

## <span data-ttu-id="c2f85-146">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c2f85-146">OUTPUTS</span></span>

### <span data-ttu-id="c2f85-147">System. String</span><span class="sxs-lookup"><span data-stu-id="c2f85-147">System.String</span></span>

## <span data-ttu-id="c2f85-148">Note</span><span class="sxs-lookup"><span data-stu-id="c2f85-148">NOTES</span></span>

## <span data-ttu-id="c2f85-149">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c2f85-149">RELATED LINKS</span></span>

[<span data-ttu-id="c2f85-150">Usare-AzHDInsightCluster</span><span class="sxs-lookup"><span data-stu-id="c2f85-150">Use-AzHDInsightCluster</span></span>](./Use-AzHDInsightCluster.md)


