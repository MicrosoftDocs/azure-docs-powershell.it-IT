---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: 5490BB24-127E-4C21-B85F-B70D817B659A
online version: https://docs.microsoft.com/powershell/module/az.datafactory/save-azdatafactorylog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Save-AzDataFactoryLog.md
ms.openlocfilehash: eb2e3c9acd93e8b20c7bdf6f4ee04ef2910a3cbb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006973"
---
# <span data-ttu-id="de882-101">Save-AzDataFactoryLog</span><span class="sxs-lookup"><span data-stu-id="de882-101">Save-AzDataFactoryLog</span></span>

## <span data-ttu-id="de882-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="de882-102">SYNOPSIS</span></span>
<span data-ttu-id="de882-103">Scarica i file di log dall'elaborazione di Azure HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de882-103">Downloads log files from Azure HDInsight processing.</span></span>

## <span data-ttu-id="de882-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="de882-104">SYNTAX</span></span>

### <span data-ttu-id="de882-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="de882-105">ByFactoryName (Default)</span></span>
```
Save-AzDataFactoryLog [-DataFactoryName] <String> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de882-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="de882-106">ByFactoryObject</span></span>
```
Save-AzDataFactoryLog [-DataFactory] <PSDataFactory> [-Id] <String> [-DownloadLogs] [[-Output] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de882-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="de882-107">DESCRIPTION</span></span>
<span data-ttu-id="de882-108">Il cmdlet **Save-AzDataFactoryLog** scarica i file di log associati all'elaborazione di Azure HDInsight dei progetti Mai o Hive o per le attività personalizzate nel disco rigido locale.</span><span class="sxs-lookup"><span data-stu-id="de882-108">The **Save-AzDataFactoryLog** cmdlet downloads log files associated with Azure HDInsight processing of Pig or Hive projects or for custom activities to your local hard drive.</span></span>
<span data-ttu-id="de882-109">Eseguire prima il cmdlet Get-AzDataFactoryRun per ottenere un ID per un'attività eseguita per una sezione di dati, quindi usare tale ID per recuperare i file di log dall'archiviazione BLOB (Binary Large Object) associata al cluster HDInsight.</span><span class="sxs-lookup"><span data-stu-id="de882-109">You first run the Get-AzDataFactoryRun cmdlet to get an ID for an activity run for a data slice, and then use that ID to retrieve log files from the binary large object (BLOB) storage associated with the HDInsight cluster.</span></span>
<span data-ttu-id="de882-110">Se non si specifica il *parametro DownloadLogs,* il cmdlet restituisce semplicemente il percorso dei file di log.</span><span class="sxs-lookup"><span data-stu-id="de882-110">If you do not specify the *DownloadLogs* parameter, the cmdlet just returns the location of log files.</span></span>
<span data-ttu-id="de882-111">Se si specifica *DownloadLogs* senza specificare una directory di output (parametro *di output),* i file di log vengono scaricati nella cartella Documenti predefinita.</span><span class="sxs-lookup"><span data-stu-id="de882-111">If you specify *DownloadLogs* without specifying an output directory (*Output* parameter), the log files are downloaded to the default Documents folder.</span></span>
<span data-ttu-id="de882-112">Se si specifica *DownloadLogs* insieme a una cartella di output *(Output),* i file di log vengono scaricati nella cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="de882-112">If you specify *DownloadLogs* along with an output folder (*Output*), the log files are downloaded to the specified folder.</span></span>

## <span data-ttu-id="de882-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="de882-113">EXAMPLES</span></span>

### <span data-ttu-id="de882-114">Esempio 1: Salvare i file di log in una cartella specifica</span><span class="sxs-lookup"><span data-stu-id="de882-114">Example 1: Save log files to a specific folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs -Output "C:\Test"
```

<span data-ttu-id="de882-115">Questo comando salva i file di log per l'attività eseguita con l'ID 841b77c9-d56c-48d1-99a3-8c16c3e77d39, dove l'attività appartiene a una pipeline nel data factory denominato LogProcessingFactory nel gruppo di risorse denominato ADF.</span><span class="sxs-lookup"><span data-stu-id="de882-115">This command saves log files for the activity run with the ID of 841b77c9-d56c-48d1-99a3-8c16c3e77d39 where the activity belongs to a pipeline in the data factory named LogProcessingFactory in the resource group named ADF.</span></span>
<span data-ttu-id="de882-116">I file di log vengono salvati nella cartella C:\Test.</span><span class="sxs-lookup"><span data-stu-id="de882-116">The log files are saved to the C:\Test folder.</span></span>

### <span data-ttu-id="de882-117">Esempio 2: Salvare i file di log nella cartella Documenti predefinita</span><span class="sxs-lookup"><span data-stu-id="de882-117">Example 2: Save log files to default Documents folder</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39" -DownloadLogs
```

<span data-ttu-id="de882-118">Questo comando salva i file di log nella cartella Documenti (impostazione predefinita).</span><span class="sxs-lookup"><span data-stu-id="de882-118">This command saves log files to Documents folder (default).</span></span>

### <span data-ttu-id="de882-119">Esempio 3: Ottenere il percorso dei file di log</span><span class="sxs-lookup"><span data-stu-id="de882-119">Example 3: Get the location of log files</span></span>
```
PS C:\>Save-AzDataFactoryLog -ResourceGroupName "ADF" -DataFactoryName "LogProcessingFactory" -Id "841b77c9-d56c-48d1-99a3-8c16c3e77d39"
```

<span data-ttu-id="de882-120">Questo comando restituisce il percorso dei file di log.</span><span class="sxs-lookup"><span data-stu-id="de882-120">This command returns the location of log files.</span></span>
<span data-ttu-id="de882-121">Si noti *che downloadLogs* non è specificato.</span><span class="sxs-lookup"><span data-stu-id="de882-121">Note that *DownloadLogs* is not specified.</span></span>

## <span data-ttu-id="de882-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="de882-122">PARAMETERS</span></span>

### <span data-ttu-id="de882-123">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="de882-123">-DataFactory</span></span>
<span data-ttu-id="de882-124">Specifica un **oggetto PSDataFactory.**</span><span class="sxs-lookup"><span data-stu-id="de882-124">Specifies a **PSDataFactory** object.</span></span>

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

### <span data-ttu-id="de882-125">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="de882-125">-DataFactoryName</span></span>
<span data-ttu-id="de882-126">Specifica il nome di un data factory.</span><span class="sxs-lookup"><span data-stu-id="de882-126">Specifies the name of a data factory.</span></span>
<span data-ttu-id="de882-127">Questo cmdlet scarica i file di log per il data factory specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="de882-127">This cmdlet downloads log files for the data factory that this parameter specifies.</span></span>

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

### <span data-ttu-id="de882-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de882-128">-DefaultProfile</span></span>
<span data-ttu-id="de882-129">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="de882-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="de882-130">-DownloadLogs</span><span class="sxs-lookup"><span data-stu-id="de882-130">-DownloadLogs</span></span>
<span data-ttu-id="de882-131">Indica che questo cmdlet scarica i file di log nel computer locale.</span><span class="sxs-lookup"><span data-stu-id="de882-131">Indicates that this cmdlet downloads log files to your local computer.</span></span>
<span data-ttu-id="de882-132">Se *non* si specifica la cartella Output, i file vengono salvati nella cartella Documenti in una sottocartella.</span><span class="sxs-lookup"><span data-stu-id="de882-132">If *Output* folder is not specified, files are saved to Documents folder under a subfolder.</span></span>

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

### <span data-ttu-id="de882-133">-Id</span><span class="sxs-lookup"><span data-stu-id="de882-133">-Id</span></span>
<span data-ttu-id="de882-134">Specifica l'ID dell'attività eseguita per la sezione di dati.</span><span class="sxs-lookup"><span data-stu-id="de882-134">Specifies the ID of the activity run for the data slice.</span></span>
<span data-ttu-id="de882-135">Usare il cmdlet Get-AzDataFactoryRun per ottenere un ID.</span><span class="sxs-lookup"><span data-stu-id="de882-135">Use the Get-AzDataFactoryRun cmdlet to get an ID.</span></span>

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

### <span data-ttu-id="de882-136">-Output</span><span class="sxs-lookup"><span data-stu-id="de882-136">-Output</span></span>
<span data-ttu-id="de882-137">Specifica la cartella di output in cui vengono salvati i file di log scaricati.</span><span class="sxs-lookup"><span data-stu-id="de882-137">Specifies the output folder in which the downloaded log files are saved.</span></span>

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

### <span data-ttu-id="de882-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de882-138">-ResourceGroupName</span></span>
<span data-ttu-id="de882-139">Specifica il nome di un gruppo di risorse azure.</span><span class="sxs-lookup"><span data-stu-id="de882-139">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="de882-140">Questo cmdlet crea un data factory che appartiene al gruppo specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="de882-140">This cmdlet creates a data factory that belongs to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="de882-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de882-141">CommonParameters</span></span>
<span data-ttu-id="de882-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de882-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de882-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de882-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de882-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="de882-144">INPUTS</span></span>

### <span data-ttu-id="de882-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="de882-145">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

### <span data-ttu-id="de882-146">System.String</span><span class="sxs-lookup"><span data-stu-id="de882-146">System.String</span></span>

## <span data-ttu-id="de882-147">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="de882-147">OUTPUTS</span></span>

### <span data-ttu-id="de882-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span><span class="sxs-lookup"><span data-stu-id="de882-148">Microsoft.Azure.Commands.DataFactories.Models.PSRunLogInfo</span></span>

## <span data-ttu-id="de882-149">NOTE</span><span class="sxs-lookup"><span data-stu-id="de882-149">NOTES</span></span>
* <span data-ttu-id="de882-150">Parole chiave: azure, azurerm, arm, risorsa, gestione, manager, dati, fattori</span><span class="sxs-lookup"><span data-stu-id="de882-150">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="de882-151">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="de882-151">RELATED LINKS</span></span>

[<span data-ttu-id="de882-152">Get-AzDataFactoryRun</span><span class="sxs-lookup"><span data-stu-id="de882-152">Get-AzDataFactoryRun</span></span>](./Get-AzDataFactoryRun.md)

[<span data-ttu-id="de882-153">Get-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="de882-153">Get-AzDataFactoryPipeline</span></span>](./Get-AzDataFactoryPipeline.md)

[<span data-ttu-id="de882-154">New-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="de882-154">New-AzDataFactoryPipeline</span></span>](./New-AzDataFactoryPipeline.md)

[<span data-ttu-id="de882-155">Remove-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="de882-155">Remove-AzDataFactoryPipeline</span></span>](./Remove-AzDataFactoryPipeline.md)

[<span data-ttu-id="de882-156">Set-AzDataFactoryPipelineActivePeriod</span><span class="sxs-lookup"><span data-stu-id="de882-156">Set-AzDataFactoryPipelineActivePeriod</span></span>](./Set-AzDataFactoryPipelineActivePeriod.md)

[<span data-ttu-id="de882-157">Suspend-AzDataFactoryPipeline</span><span class="sxs-lookup"><span data-stu-id="de882-157">Suspend-AzDataFactoryPipeline</span></span>](./Suspend-AzDataFactoryPipeline.md)


