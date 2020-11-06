---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.hdinsight/new-azurermhdinsightsqoopjobdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 6f7045773dc1bf5582e2c480fd9e4aed283bf8ac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515731"
---
# <span data-ttu-id="fe4bb-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fe4bb-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="fe4bb-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe4bb-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4bb-103">Crea un oggetto processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe4bb-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe4bb-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fe4bb-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe4bb-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4bb-106">Il cmdlet **New-AzureRmHDInsightSqoopJobDefinition** definisce un oggetto processo Sqoop da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="fe4bb-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe4bb-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4bb-108">Esempio 1: creare una definizione di processo Sqoop</span><span class="sxs-lookup"><span data-stu-id="fe4bb-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="fe4bb-109">Questo comando crea una definizione di processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="fe4bb-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe4bb-110">PARAMETERS</span></span>

### <span data-ttu-id="fe4bb-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="fe4bb-111">-Command</span></span>
<span data-ttu-id="fe4bb-112">Specifica il comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-112">Specifies the Sqoop command.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4bb-113">-DefaultProfile</span></span>
<span data-ttu-id="fe4bb-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="fe4bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe4bb-115">-File</span><span class="sxs-lookup"><span data-stu-id="fe4bb-115">-File</span></span>
<span data-ttu-id="fe4bb-116">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-116">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="fe4bb-117">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-117">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="fe4bb-118">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="fe4bb-118">You can use this parameter instead of the *Query* parameter.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-119">-File</span><span class="sxs-lookup"><span data-stu-id="fe4bb-119">-Files</span></span>
<span data-ttu-id="fe4bb-120">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-120">Specifies a collection of files that are associated with a Hive job.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-121">-LibDir</span><span class="sxs-lookup"><span data-stu-id="fe4bb-121">-LibDir</span></span>
<span data-ttu-id="fe4bb-122">Specifica la directory della raccolta per il processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-122">Specifies the library directory for the Sqoop job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-123">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="fe4bb-123">-StatusFolder</span></span>
<span data-ttu-id="fe4bb-124">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-124">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4bb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4bb-125">CommonParameters</span></span>
<span data-ttu-id="fe4bb-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4bb-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe4bb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4bb-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe4bb-128">INPUTS</span></span>

### <span data-ttu-id="fe4bb-129">Nessuno</span><span class="sxs-lookup"><span data-stu-id="fe4bb-129">None</span></span>
<span data-ttu-id="fe4bb-130">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="fe4bb-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe4bb-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe4bb-131">OUTPUTS</span></span>

### <span data-ttu-id="fe4bb-132">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="fe4bb-132">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="fe4bb-133">Note</span><span class="sxs-lookup"><span data-stu-id="fe4bb-133">NOTES</span></span>

## <span data-ttu-id="fe4bb-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe4bb-134">RELATED LINKS</span></span>

[<span data-ttu-id="fe4bb-135">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="fe4bb-135">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


