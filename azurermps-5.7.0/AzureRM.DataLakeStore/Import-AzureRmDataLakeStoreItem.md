---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/import-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 54969735bad877592abd17327c53e22a765b69fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519027"
---
# <span data-ttu-id="e486a-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e486a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e486a-102">SYNOPSIS</span></span>
<span data-ttu-id="e486a-103">Carica un file o una directory locale in uno Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e486a-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e486a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e486a-104">SYNTAX</span></span>

### <span data-ttu-id="e486a-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e486a-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e486a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="e486a-106">IncludeDiagnosticLogging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e486a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e486a-107">DESCRIPTION</span></span>
<span data-ttu-id="e486a-108">Il cmdlet **Import-AzureRmDataLakeStoreItem** carica un file o una directory locale in uno Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e486a-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="e486a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e486a-109">EXAMPLES</span></span>

### <span data-ttu-id="e486a-110">Esempio 1: caricare un file</span><span class="sxs-lookup"><span data-stu-id="e486a-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="e486a-111">Questo comando carica il file SrcFile.csv e lo aggiunge alla cartella MyFile nello Store Data Lake come File.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="e486a-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="e486a-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e486a-112">PARAMETERS</span></span>

### <span data-ttu-id="e486a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e486a-113">-Account</span></span>
<span data-ttu-id="e486a-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e486a-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="e486a-115">-Concurrency</span></span>
<span data-ttu-id="e486a-116">Indica il numero di file o blocchi da caricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="e486a-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="e486a-117">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="e486a-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="e486a-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="e486a-119">Indica il numero massimo di file da caricare in parallelo per il caricamento di una cartella.</span><span class="sxs-lookup"><span data-stu-id="e486a-119">Indicates the maximum number of files to upload in parallel for a folder upload.</span></span>  <span data-ttu-id="e486a-120">Il calcolo predefinito verrà calcolato come uno sforzo ottimale in base alle dimensioni della cartella e del file</span><span class="sxs-lookup"><span data-stu-id="e486a-120">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e486a-121">-DefaultProfile</span></span>
<span data-ttu-id="e486a-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e486a-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e486a-123">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="e486a-123">-Destination</span></span>
<span data-ttu-id="e486a-124">Specifica il percorso dello Store Data Lake a cui caricare un file o una cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="e486a-124">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="e486a-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="e486a-126">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="e486a-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="e486a-127">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="e486a-127">Default is Error.</span></span>

```yaml
Type: LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="e486a-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="e486a-129">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="e486a-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: String
Parameter Sets: IncludeDiagnosticLogging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e486a-130">-Force</span></span>
<span data-ttu-id="e486a-131">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="e486a-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-132">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="e486a-132">-ForceBinary</span></span>
<span data-ttu-id="e486a-133">Indica che i file da copiare devono essere copiati senza alcuna preoccupazione per la conservazione delle nuove linee tra le aggiunte.</span><span class="sxs-lookup"><span data-stu-id="e486a-133">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-134">-Path</span><span class="sxs-lookup"><span data-stu-id="e486a-134">-Path</span></span>
<span data-ttu-id="e486a-135">Specifica il percorso locale del file o della cartella da caricare.</span><span class="sxs-lookup"><span data-stu-id="e486a-135">Specifies the local path of the file or folder to upload.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-136">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="e486a-136">-PerFileThreadCount</span></span>
<span data-ttu-id="e486a-137">Indica il numero massimo di thread da usare per ogni file.</span><span class="sxs-lookup"><span data-stu-id="e486a-137">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="e486a-138">Il calcolo predefinito verrà calcolato come uno sforzo ottimale in base alle dimensioni della cartella e del file</span><span class="sxs-lookup"><span data-stu-id="e486a-138">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-139">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e486a-139">-Recurse</span></span>
<span data-ttu-id="e486a-140">Indica che questa operazione deve caricare tutti gli elementi in tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="e486a-140">Indicates that this operation should upload all items in all subfolders.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-141">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="e486a-141">-Resume</span></span>
<span data-ttu-id="e486a-142">Indica che i file da copiare sono la continuazione di un caricamento precedente.</span><span class="sxs-lookup"><span data-stu-id="e486a-142">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="e486a-143">In questo modo il sistema cercherà di riprendere dall'ultimo file che non è stato completamente caricato.</span><span class="sxs-lookup"><span data-stu-id="e486a-143">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-144">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e486a-144">-Confirm</span></span>
<span data-ttu-id="e486a-145">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e486a-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e486a-146">-WhatIf</span></span>
<span data-ttu-id="e486a-147">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e486a-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e486a-148">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e486a-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e486a-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e486a-149">CommonParameters</span></span>
<span data-ttu-id="e486a-150">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e486a-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e486a-151">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e486a-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e486a-152">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e486a-152">INPUTS</span></span>

### <span data-ttu-id="e486a-153">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e486a-153">None</span></span>
<span data-ttu-id="e486a-154">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e486a-154">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e486a-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e486a-155">OUTPUTS</span></span>

### <span data-ttu-id="e486a-156">stringa</span><span class="sxs-lookup"><span data-stu-id="e486a-156">string</span></span>
<span data-ttu-id="e486a-157">Il percorso completo nell'account di data Lake Store per il file o la cartella caricata.</span><span class="sxs-lookup"><span data-stu-id="e486a-157">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="e486a-158">Note</span><span class="sxs-lookup"><span data-stu-id="e486a-158">NOTES</span></span>

## <span data-ttu-id="e486a-159">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e486a-159">RELATED LINKS</span></span>

[<span data-ttu-id="e486a-160">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-160">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e486a-161">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-161">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e486a-162">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-162">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e486a-163">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-163">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e486a-164">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-164">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e486a-165">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-165">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e486a-166">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e486a-166">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


