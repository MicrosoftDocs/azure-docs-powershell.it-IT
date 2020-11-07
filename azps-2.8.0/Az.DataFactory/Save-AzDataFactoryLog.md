---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: 976f00f62cfda991e7d1aff349a0b04807dbbe1a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674941"
---
# <span data-ttu-id="28ff1-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="28ff1-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="28ff1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="28ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="28ff1-103">Scarica i file di log dall'elaborazione di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="28ff1-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="28ff1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="28ff1-104">SYNTAX</span></span>

### <span data-ttu-id="28ff1-105">ByFactoryName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="28ff1-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="28ff1-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="28ff1-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ff1-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="28ff1-107">DESCRIPTION</span></span>
<span data-ttu-id="28ff1-108">Il cmdlet **Save-AzDataFactoryLog** Scarica i file di log associati all'elaborazione di Azure HDInsight di progetti di suini o hive o per attività personalizzate nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="28ff1-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="28ff1-109">Viene eseguito prima di tutto il cmdlet Get-AzDataFactoryRun per ottenere un ID per un'attività eseguita per una fetta di dati e quindi usare tale ID per recuperare i file di log dall'archiviazione BLOB (Binary Large Object) associata al cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="28ff1-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="28ff1-110">Se non specifichi il parametro *DownloadLogs* , il cmdlet restituisce semplicemente la posizione dei file di log.</span><span class="sxs-lookup"><span data-stu-id="28ff1-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="28ff1-111">Se specifichi *DownloadLogs* senza specificare una directory di output (parametro di *output* ), i file di log vengono scaricati nella cartella documenti predefiniti.</span><span class="sxs-lookup"><span data-stu-id="28ff1-111">If you specify *DownloadLogs* without specifying an output directory ( *Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="28ff1-112">Se specifichi *DownloadLogs* insieme a una cartella di output ( *output* ), i file di log vengono scaricati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="28ff1-112">If you specify *DownloadLogs* along with an output folder ( *Output* ), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="28ff1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="28ff1-113">EXAMPLES</span></span>

### <span data-ttu-id="28ff1-114">Esempio 1: salvare i file di log in una cartella specifica</span><span class="sxs-lookup"><span data-stu-id="28ff1-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="28ff1-115">Questo comando Salva i file di log per l'attività eseguita con l'ID di 841b77c9-d56c-48D1-99A3-8c16c3e77d39 in cui l'attività appartiene a una pipeline nella Factory di dati denominata LogProcessingFactory nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="28ff1-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="28ff1-116">I file di log vengono salvati nella cartella C:\Test.</span><span class="sxs-lookup"><span data-stu-id="28ff1-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="28ff1-117">Esempio 2: salvare i file di log nella cartella documenti predefiniti</span><span class="sxs-lookup"><span data-stu-id="28ff1-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="28ff1-118">Questo comando Salva i file di log nella cartella documenti (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="28ff1-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="28ff1-119">Esempio 3: ottenere la posizione dei file di log</span><span class="sxs-lookup"><span data-stu-id="28ff1-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="28ff1-120">Questo comando restituisce la posizione dei file di log.</span><span class="sxs-lookup"><span data-stu-id="28ff1-120">This command returns the location of log files.</span></span>
<span data-ttu-id="28ff1-121">Tieni presente che *DownloadLogs* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="28ff1-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="28ff1-122">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="28ff1-122">PARAMETERS</span></span>

### <span data-ttu-id="28ff1-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="28ff1-123">-DataFactory</span></span>
<span data-ttu-id="28ff1-124">Specifica un oggetto **PSDataFactory** .</span><span class="sxs-lookup"><span data-stu-id="28ff1-124">Specifies a **PSDataFactory** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ff1-125">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="28ff1-125">-DataFactoryName</span></span>
<span data-ttu-id="28ff1-126">Specifica il nome di una data factory.</span><span class="sxs-lookup"><span data-stu-id="28ff1-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="28ff1-127">Questo cmdlet Scarica i file di log per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="28ff1-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ff1-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ff1-128">-DefaultProfile</span></span>
<span data-ttu-id="28ff1-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="28ff1-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28ff1-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="28ff1-130">-DownloadLogs</span></span>
<span data-ttu-id="28ff1-131">Indica che questo cmdlet Scarica i file di log nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="28ff1-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="28ff1-132">Se la cartella di *output* non è specificata, i file vengono salvati nella cartella documenti in una sottocartella.</span><span class="sxs-lookup"><span data-stu-id="28ff1-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="28ff1-133">-ID</span><span class="sxs-lookup"><span data-stu-id="28ff1-133">-Id</span></span>
<span data-ttu-id="28ff1-134">Specifica l'ID dell'esecuzione dell'attività per la sezione dati.</span><span class="sxs-lookup"><span data-stu-id="28ff1-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="28ff1-135">Usa il cmdlet Get-AzDataFactoryRun per ottenere un ID.</span><span class="sxs-lookup"><span data-stu-id="28ff1-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ff1-136">-Output</span><span class="sxs-lookup"><span data-stu-id="28ff1-136">-Output</span></span>
<span data-ttu-id="28ff1-137">Specifica la cartella di output in cui vengono salvati i file di log scaricati.</span><span class="sxs-lookup"><span data-stu-id="28ff1-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28ff1-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28ff1-138">-ResourceGroupName</span></span>
<span data-ttu-id="28ff1-139">Specifica il nome di un gruppo di risorse Azure.</span><span class="sxs-lookup"><span data-stu-id="28ff1-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="28ff1-140">Questo cmdlet crea una factory di dati che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="28ff1-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="28ff1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ff1-141">CommonParameters</span></span>
<span data-ttu-id="28ff1-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ff1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ff1-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ff1-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ff1-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="28ff1-144">INPUTS</span></span>

### <span data-ttu-id="28ff1-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="28ff1-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="28ff1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="28ff1-146">System.String</span></span>

## <span data-ttu-id="28ff1-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="28ff1-147">OUTPUTS</span></span>

### <span data-ttu-id="28ff1-148">Microsoft. Azure. Commands. datafactories. Models. PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="28ff1-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="28ff1-149">Note</span><span class="sxs-lookup"><span data-stu-id="28ff1-149">NOTES</span></span>
* <span data-ttu-id="28ff1-150">Parole chiave: Azure, azurerm, ARM, Resource, Management, Manager, data, Factory</span><span class="sxs-lookup"><span data-stu-id="28ff1-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="28ff1-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="28ff1-151">RELATED LINKS</span></span>

[<span data-ttu-id="28ff1-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="28ff1-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="28ff1-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="28ff1-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="28ff1-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="28ff1-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="28ff1-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="28ff1-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="28ff1-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="28ff1-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="28ff1-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="28ff1-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


