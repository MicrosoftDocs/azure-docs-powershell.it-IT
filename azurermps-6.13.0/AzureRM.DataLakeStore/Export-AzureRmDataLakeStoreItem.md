---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/export-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 508a7619374b7e245b8df99c929f161ce1966288
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518720"
---
# <span data-ttu-id="bae87-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="bae87-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bae87-102">SYNOPSIS</span></span>
<span data-ttu-id="bae87-103">Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bae87-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bae87-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bae87-104">SYNTAX</span></span>

### <span data-ttu-id="bae87-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="bae87-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bae87-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="bae87-106">IncludeDiagnosticLogging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bae87-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bae87-107">DESCRIPTION</span></span>
<span data-ttu-id="bae87-108">Il cmdlet **Export-AzureRmDataLakeStoreItem** Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bae87-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="bae87-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bae87-109">EXAMPLES</span></span>

### <span data-ttu-id="bae87-110">Esempio 1: scaricare un elemento da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="bae87-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="bae87-111">Questo comando Scarica il file TestSource.csv da data Lake Store per C:\Test.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="bae87-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="bae87-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bae87-112">PARAMETERS</span></span>

### <span data-ttu-id="bae87-113">-Account</span><span class="sxs-lookup"><span data-stu-id="bae87-113">-Account</span></span>
<span data-ttu-id="bae87-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="bae87-114">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="bae87-115">-Concurrency</span></span>
<span data-ttu-id="bae87-116">Indica il numero di file o blocchi da scaricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="bae87-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="bae87-117">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="bae87-117">Default will be computed as a best effort based on system specifications.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bae87-118">-DefaultProfile</span></span>
<span data-ttu-id="bae87-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="bae87-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bae87-120">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="bae87-120">-Destination</span></span>
<span data-ttu-id="bae87-121">Specifica il percorso del file locale a cui scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="bae87-121">Specifies the local file path to which to download the file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="bae87-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="bae87-123">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="bae87-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="bae87-124">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="bae87-124">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="bae87-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="bae87-126">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="bae87-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-127">-Force</span><span class="sxs-lookup"><span data-stu-id="bae87-127">-Force</span></span>
<span data-ttu-id="bae87-128">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="bae87-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-129">-Path</span><span class="sxs-lookup"><span data-stu-id="bae87-129">-Path</span></span>
<span data-ttu-id="bae87-130">Specifica il percorso dell'elemento da scaricare da data Lake Store, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="bae87-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="bae87-131">-Recurse</span></span>
<span data-ttu-id="bae87-132">Indica che il download di una cartella è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="bae87-132">Indicates that a folder download is recursive.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-133">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="bae87-133">-Resume</span></span>
<span data-ttu-id="bae87-134">Indica che i file da copiare sono la continuazione di un download precedente.</span><span class="sxs-lookup"><span data-stu-id="bae87-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="bae87-135">In questo modo il sistema cercherà di riprendere dall'ultimo file che non è stato completamente scaricato.</span><span class="sxs-lookup"><span data-stu-id="bae87-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bae87-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="bae87-136">-Confirm</span></span>
<span data-ttu-id="bae87-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bae87-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bae87-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bae87-138">-WhatIf</span></span>
<span data-ttu-id="bae87-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bae87-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bae87-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="bae87-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bae87-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bae87-141">CommonParameters</span></span>
<span data-ttu-id="bae87-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bae87-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bae87-143">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bae87-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bae87-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bae87-144">INPUTS</span></span>

### <span data-ttu-id="bae87-145">System. String</span><span class="sxs-lookup"><span data-stu-id="bae87-145">System.String</span></span>

### <span data-ttu-id="bae87-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="bae87-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="bae87-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="bae87-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="bae87-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="bae87-148">System.Int32</span></span>

### <span data-ttu-id="bae87-149">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="bae87-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="bae87-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bae87-150">OUTPUTS</span></span>

### <span data-ttu-id="bae87-151">System. String</span><span class="sxs-lookup"><span data-stu-id="bae87-151">System.String</span></span>
<span data-ttu-id="bae87-152">Percorso in cui è stato scaricato il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="bae87-152">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="bae87-153">Note</span><span class="sxs-lookup"><span data-stu-id="bae87-153">NOTES</span></span>

## <span data-ttu-id="bae87-154">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bae87-154">RELATED LINKS</span></span>

[<span data-ttu-id="bae87-155">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-155">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bae87-156">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bae87-157">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-157">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bae87-158">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-158">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bae87-159">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-159">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bae87-160">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-160">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="bae87-161">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="bae87-161">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


