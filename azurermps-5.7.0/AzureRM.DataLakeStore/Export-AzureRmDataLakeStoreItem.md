---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 907e4e92b511349011b27cb8aaf7588b8e495220
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685836"
---
# <span data-ttu-id="e6377-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="e6377-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6377-102">SYNOPSIS</span></span>
<span data-ttu-id="e6377-103">Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6377-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e6377-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6377-104">SYNTAX</span></span>

### <span data-ttu-id="e6377-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6377-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e6377-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="e6377-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [[-Concurrency] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6377-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6377-107">DESCRIPTION</span></span>
<span data-ttu-id="e6377-108">Il cmdlet **Export-AzureRmDataLakeStoreItem** Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6377-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="e6377-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6377-109">EXAMPLES</span></span>

### <span data-ttu-id="e6377-110">Esempio 1: scaricare un elemento da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e6377-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="e6377-111">Questo comando Scarica il file TestSource.csv da data Lake Store per C:\Test.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="e6377-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="e6377-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6377-112">PARAMETERS</span></span>

### <span data-ttu-id="e6377-113">-Account</span><span class="sxs-lookup"><span data-stu-id="e6377-113">-Account</span></span>
<span data-ttu-id="e6377-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e6377-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="e6377-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="e6377-115">-Concurrency</span></span>
<span data-ttu-id="e6377-116">Indica il numero di file o blocchi da scaricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="e6377-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="e6377-117">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="e6377-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-118">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="e6377-118">-ConcurrentFileCount</span></span>
<span data-ttu-id="e6377-119">Indica il numero massimo di file da scaricare in parallelo per il download di una cartella.</span><span class="sxs-lookup"><span data-stu-id="e6377-119">Indicates the maximum number of files to download in parallel for a folder download.</span></span>  <span data-ttu-id="e6377-120">Il calcolo predefinito verrà calcolato come uno sforzo ottimale in base alle dimensioni della cartella e del file</span><span class="sxs-lookup"><span data-stu-id="e6377-120">Default will be computed as a best effort based on folder and file size</span></span>

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

### <span data-ttu-id="e6377-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6377-121">-DefaultProfile</span></span>
<span data-ttu-id="e6377-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6377-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6377-123">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="e6377-123">-Destination</span></span>
<span data-ttu-id="e6377-124">Specifica il percorso del file locale a cui scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="e6377-124">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-125">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="e6377-125">-DiagnosticLogLevel</span></span>
<span data-ttu-id="e6377-126">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="e6377-126">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="e6377-127">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="e6377-127">Default is Error.</span></span>

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

### <span data-ttu-id="e6377-128">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="e6377-128">-DiagnosticLogPath</span></span>
<span data-ttu-id="e6377-129">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="e6377-129">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="e6377-130">-Force</span><span class="sxs-lookup"><span data-stu-id="e6377-130">-Force</span></span>
<span data-ttu-id="e6377-131">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="e6377-131">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-132">-Path</span><span class="sxs-lookup"><span data-stu-id="e6377-132">-Path</span></span>
<span data-ttu-id="e6377-133">Specifica il percorso dell'elemento da scaricare da data Lake Store, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="e6377-133">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-134">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="e6377-134">-PerFileThreadCount</span></span>
<span data-ttu-id="e6377-135">Indica il numero massimo di thread da usare per ogni file.</span><span class="sxs-lookup"><span data-stu-id="e6377-135">Indicates the maximum number of threads to use per file.</span></span>  <span data-ttu-id="e6377-136">Il calcolo predefinito verrà calcolato come uno sforzo ottimale in base alle dimensioni della cartella e del file</span><span class="sxs-lookup"><span data-stu-id="e6377-136">Default will be computed as a best effort based on folder and file size</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e6377-137">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e6377-137">-Recurse</span></span>
<span data-ttu-id="e6377-138">Indica che il download di una cartella è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="e6377-138">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="e6377-139">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="e6377-139">-Resume</span></span>
<span data-ttu-id="e6377-140">Indica che i file da copiare sono la continuazione di un download precedente.</span><span class="sxs-lookup"><span data-stu-id="e6377-140">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="e6377-141">In questo modo il sistema cercherà di riprendere dall'ultimo file che non è stato completamente scaricato.</span><span class="sxs-lookup"><span data-stu-id="e6377-141">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="e6377-142">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6377-142">-Confirm</span></span>
<span data-ttu-id="e6377-143">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6377-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6377-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6377-144">-WhatIf</span></span>
<span data-ttu-id="e6377-145">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6377-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6377-146">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6377-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6377-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6377-147">CommonParameters</span></span>
<span data-ttu-id="e6377-148">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6377-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6377-149">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e6377-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6377-150">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6377-150">INPUTS</span></span>

### <span data-ttu-id="e6377-151">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6377-151">None</span></span>
<span data-ttu-id="e6377-152">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="e6377-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e6377-153">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6377-153">OUTPUTS</span></span>

### <span data-ttu-id="e6377-154">stringa</span><span class="sxs-lookup"><span data-stu-id="e6377-154">string</span></span>
<span data-ttu-id="e6377-155">Percorso in cui è stato scaricato il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="e6377-155">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="e6377-156">Note</span><span class="sxs-lookup"><span data-stu-id="e6377-156">NOTES</span></span>

## <span data-ttu-id="e6377-157">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6377-157">RELATED LINKS</span></span>

[<span data-ttu-id="e6377-158">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-158">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e6377-159">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-159">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e6377-160">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-160">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e6377-161">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-161">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e6377-162">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-162">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e6377-163">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-163">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="e6377-164">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="e6377-164">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


