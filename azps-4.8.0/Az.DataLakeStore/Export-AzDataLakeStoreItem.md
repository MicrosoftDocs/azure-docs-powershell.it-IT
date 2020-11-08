---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189092"
---
# <span data-ttu-id="7c37f-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="7c37f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7c37f-102">SYNOPSIS</span></span>
<span data-ttu-id="7c37f-103">Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c37f-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="7c37f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7c37f-104">SYNTAX</span></span>

### <span data-ttu-id="7c37f-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7c37f-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c37f-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="7c37f-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7c37f-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7c37f-107">DESCRIPTION</span></span>
<span data-ttu-id="7c37f-108">Il cmdlet **Export-AzDataLakeStoreItem** Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c37f-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="7c37f-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7c37f-109">EXAMPLES</span></span>

### <span data-ttu-id="7c37f-110">Esempio 1: scaricare un elemento da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="7c37f-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="7c37f-111">Questo comando Scarica il file TestSource.csv da data Lake Store per C:\Test.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="7c37f-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="7c37f-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7c37f-112">PARAMETERS</span></span>

### <span data-ttu-id="7c37f-113">-Account</span><span class="sxs-lookup"><span data-stu-id="7c37f-113">-Account</span></span>
<span data-ttu-id="7c37f-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7c37f-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7c37f-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="7c37f-115">-Concurrency</span></span>
<span data-ttu-id="7c37f-116">Indica il numero di file o blocchi da scaricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="7c37f-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="7c37f-117">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="7c37f-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="7c37f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c37f-118">-DefaultProfile</span></span>
<span data-ttu-id="7c37f-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7c37f-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c37f-120">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="7c37f-120">-Destination</span></span>
<span data-ttu-id="7c37f-121">Specifica il percorso del file locale a cui scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="7c37f-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="7c37f-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="7c37f-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="7c37f-123">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="7c37f-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="7c37f-124">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="7c37f-124">Default is Error.</span></span>

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

### <span data-ttu-id="7c37f-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="7c37f-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="7c37f-126">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="7c37f-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="7c37f-127">-Force</span><span class="sxs-lookup"><span data-stu-id="7c37f-127">-Force</span></span>
<span data-ttu-id="7c37f-128">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="7c37f-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="7c37f-129">-Path</span><span class="sxs-lookup"><span data-stu-id="7c37f-129">-Path</span></span>
<span data-ttu-id="7c37f-130">Specifica il percorso dell'elemento da scaricare da data Lake Store, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="7c37f-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="7c37f-131">-Recurse</span><span class="sxs-lookup"><span data-stu-id="7c37f-131">-Recurse</span></span>
<span data-ttu-id="7c37f-132">Indica che il download di una cartella è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="7c37f-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="7c37f-133">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="7c37f-133">-Resume</span></span>
<span data-ttu-id="7c37f-134">Indica che i file da copiare sono la continuazione di un download precedente.</span><span class="sxs-lookup"><span data-stu-id="7c37f-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="7c37f-135">In questo modo il sistema cercherà di riprendere dall'ultimo file che non è stato completamente scaricato.</span><span class="sxs-lookup"><span data-stu-id="7c37f-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="7c37f-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7c37f-136">-Confirm</span></span>
<span data-ttu-id="7c37f-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c37f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c37f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c37f-138">-WhatIf</span></span>
<span data-ttu-id="7c37f-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c37f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c37f-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7c37f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c37f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c37f-141">CommonParameters</span></span>
<span data-ttu-id="7c37f-142">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c37f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c37f-143">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c37f-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c37f-144">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7c37f-144">INPUTS</span></span>

### <span data-ttu-id="7c37f-145">System. String</span><span class="sxs-lookup"><span data-stu-id="7c37f-145">System.String</span></span>

### <span data-ttu-id="7c37f-146">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7c37f-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7c37f-147">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7c37f-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7c37f-148">System. Int32</span><span class="sxs-lookup"><span data-stu-id="7c37f-148">System.Int32</span></span>

### <span data-ttu-id="7c37f-149">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="7c37f-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="7c37f-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7c37f-150">OUTPUTS</span></span>

### <span data-ttu-id="7c37f-151">System. String</span><span class="sxs-lookup"><span data-stu-id="7c37f-151">System.String</span></span>

## <span data-ttu-id="7c37f-152">Note</span><span class="sxs-lookup"><span data-stu-id="7c37f-152">NOTES</span></span>

## <span data-ttu-id="7c37f-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7c37f-153">RELATED LINKS</span></span>

[<span data-ttu-id="7c37f-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="7c37f-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="7c37f-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="7c37f-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="7c37f-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="7c37f-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="7c37f-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7c37f-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


