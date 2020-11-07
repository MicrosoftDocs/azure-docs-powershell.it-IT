---
external help file: Microsoft.Azure.Commands.HDInsight.dll-Help.xml
Module Name: AzureRM.HDInsight
ms.assetid: 4ED47646-542B-4983-B46B-B603BE33D499
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/HDInsight/Commands.HDInsight/help/New-AzureRmHDInsightSqoopJobDefinition.md
ms.openlocfilehash: 769406d0eb47672fcaaea8acfb3b3fdccd6810d0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688023"
---
# <span data-ttu-id="5dc84-101">New-AzureRmHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5dc84-101">New-AzureRmHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="5dc84-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5dc84-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc84-103">Crea un oggetto processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="5dc84-103">Creates a Sqoop job object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dc84-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5dc84-104">SYNTAX</span></span>

```
New-AzureRmHDInsightSqoopJobDefinition [-Files <String[]>] [-StatusFolder <String>] [-File <String>]
 [-Command <String>] [-LibDir <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5dc84-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5dc84-105">DESCRIPTION</span></span>
<span data-ttu-id="5dc84-106">Il cmdlet **New-AzureRmHDInsightSqoopJobDefinition** definisce un oggetto processo Sqoop da usare con un cluster di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="5dc84-106">The **New-AzureRmHDInsightSqoopJobDefinition** cmdlet defines a Sqoop job object for use with an Azure HDInsight cluster.</span></span>

## <span data-ttu-id="5dc84-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5dc84-107">EXAMPLES</span></span>

### <span data-ttu-id="5dc84-108">Esempio 1: creare una definizione di processo Sqoop</span><span class="sxs-lookup"><span data-stu-id="5dc84-108">Example 1: Create a Sqoop job definition</span></span>
```
PS C:\># Cluster info
PS C:\>$clusterName = "your-hadoop-001"
PS C:\>$clusterCreds = Get-Credential

PS C:\>New-AzureRmHDInsightSqoopJobDefinition -StatusFolder $statusFolder `
            -Command $sqoopCommand `
        | Start-AzureRmHDInsightJob -ClusterName $clusterName `
            -ClusterCredential $clusterCreds
```

<span data-ttu-id="5dc84-109">Questo comando crea una definizione di processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="5dc84-109">This command creates a Sqoop job definition.</span></span>

## <span data-ttu-id="5dc84-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5dc84-110">PARAMETERS</span></span>

### <span data-ttu-id="5dc84-111">-Comando</span><span class="sxs-lookup"><span data-stu-id="5dc84-111">-Command</span></span>
<span data-ttu-id="5dc84-112">Specifica il comando Sqoop.</span><span class="sxs-lookup"><span data-stu-id="5dc84-112">Specifies the Sqoop command.</span></span>

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

### <span data-ttu-id="5dc84-113">-File</span><span class="sxs-lookup"><span data-stu-id="5dc84-113">-File</span></span>
<span data-ttu-id="5dc84-114">Specifica il percorso di un file che contiene la query da eseguire.</span><span class="sxs-lookup"><span data-stu-id="5dc84-114">Specifies the path to a file that contains the query to run.</span></span>
<span data-ttu-id="5dc84-115">Il file deve essere disponibile nell'account di archiviazione associato al cluster.</span><span class="sxs-lookup"><span data-stu-id="5dc84-115">The file must be available on the Storage account associated with the cluster.</span></span>
<span data-ttu-id="5dc84-116">Puoi usare questo parametro invece del parametro di *query* .</span><span class="sxs-lookup"><span data-stu-id="5dc84-116">You can use this parameter instead of the *Query* parameter.</span></span>

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

### <span data-ttu-id="5dc84-117">-File</span><span class="sxs-lookup"><span data-stu-id="5dc84-117">-Files</span></span>
<span data-ttu-id="5dc84-118">Specifica una raccolta di file associati a un processo hive.</span><span class="sxs-lookup"><span data-stu-id="5dc84-118">Specifies a collection of files that are associated with a Hive job.</span></span>

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

### <span data-ttu-id="5dc84-119">-LibDir</span><span class="sxs-lookup"><span data-stu-id="5dc84-119">-LibDir</span></span>
<span data-ttu-id="5dc84-120">Specifica la directory della raccolta per il processo Sqoop.</span><span class="sxs-lookup"><span data-stu-id="5dc84-120">Specifies the library directory for the Sqoop job.</span></span>

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

### <span data-ttu-id="5dc84-121">-StatusFolder</span><span class="sxs-lookup"><span data-stu-id="5dc84-121">-StatusFolder</span></span>
<span data-ttu-id="5dc84-122">Specifica la posizione della cartella che contiene gli output standard e gli output degli errori per un processo.</span><span class="sxs-lookup"><span data-stu-id="5dc84-122">Specifies the location of the folder that contains standard outputs and error outputs for a job.</span></span>

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

### <span data-ttu-id="5dc84-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc84-123">-DefaultProfile</span></span>
<span data-ttu-id="5dc84-124">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5dc84-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5dc84-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc84-125">CommonParameters</span></span>
<span data-ttu-id="5dc84-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dc84-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dc84-127">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc84-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc84-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5dc84-128">INPUTS</span></span>

## <span data-ttu-id="5dc84-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5dc84-129">OUTPUTS</span></span>

### <span data-ttu-id="5dc84-130">Microsoft. Azure. Commands. HDInsight. Models. AzureHDInsightSqoopJobDefinition</span><span class="sxs-lookup"><span data-stu-id="5dc84-130">Microsoft.Azure.Commands.HDInsight.Models.AzureHDInsightSqoopJobDefinition</span></span>

## <span data-ttu-id="5dc84-131">Note</span><span class="sxs-lookup"><span data-stu-id="5dc84-131">NOTES</span></span>

## <span data-ttu-id="5dc84-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5dc84-132">RELATED LINKS</span></span>

[<span data-ttu-id="5dc84-133">Start-AzureRmHDInsightJob</span><span class="sxs-lookup"><span data-stu-id="5dc84-133">Start-AzureRmHDInsightJob</span></span>](./Start-AzureRmHDInsightJob.md)


