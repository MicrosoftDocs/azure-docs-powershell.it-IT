---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HDInsight.dll-Help.xml
Module Name: Az.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/az.hdinsight/new-azhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HDInsight/HDInsight/help/New-AzHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 2cc5acb2017a9db2bf5ed1f80ccfd1069bc1a465
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865443"
---
# <span data-ttu-id="85799-101">New-AzHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85799-101">New-AzHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="85799-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="85799-102">SYNOPSIS</span></span>
<span data-ttu-id="85799-103">Crea un oggetto processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="85799-103">Creates a Sqoop job object.</span></span>

## <span data-ttu-id="85799-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="85799-104">SYNTAX</span></span>

```
New-AzHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="85799-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="85799-105">DESCRIPTION</span></span>
<span data-ttu-id="85799-106">Il cmdlet **New-AzHDInsightSqoopJobDefinition** definisce un oggetto processo Sqoop da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="85799-106">The **New-AzHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="85799-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="85799-107">EXAMPLES</span></span>

### <span data-ttu-id="85799-108">Esempio 1: creare una definizione di processo Sqoop</span><span class="sxs-lookup"><span data-stu-id="85799-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="85799-109">Questo comando crea una definizione di processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="85799-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="85799-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="85799-110">PARAMETERS</span></span>

### <span data-ttu-id="85799-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="85799-111">-Command</span></span>
<span data-ttu-id="85799-112">Specifica il comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="85799-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="85799-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85799-113">-DefaultProfile</span></span>
<span data-ttu-id="85799-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="85799-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85799-115">-File</span><span class="sxs-lookup"><span data-stu-id="85799-115">-File</span></span>
<span data-ttu-id="85799-116">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="85799-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="85799-117">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="85799-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="85799-118">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="85799-118">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="85799-119">-File</span><span class="sxs-lookup"><span data-stu-id="85799-119">-Files</span></span>
<span data-ttu-id="85799-120">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="85799-120">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="85799-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="85799-121">-LibDir</span></span>
<span data-ttu-id="85799-122">Specifica la directory della raccolta per il processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="85799-122">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="85799-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="85799-123">-StatusFolder</span></span>
<span data-ttu-id="85799-124">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="85799-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="85799-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85799-125">CommonParameters</span></span>
<span data-ttu-id="85799-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="85799-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85799-127">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="85799-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85799-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="85799-128">INPUTS</span></span>

### <span data-ttu-id="85799-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="85799-129">None</span></span>

## <span data-ttu-id="85799-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="85799-130">OUTPUTS</span></span>

### <span data-ttu-id="85799-131">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="85799-131">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="85799-132">Note</span><span class="sxs-lookup"><span data-stu-id="85799-132">NOTES</span></span>

## <span data-ttu-id="85799-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="85799-133">RELATED LINKS</span></span>

[<span data-ttu-id="85799-134">Start-AzHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="85799-134">Start-AzHDInsightJob</span></span>](./Start-AzHDInsightJob.md)


