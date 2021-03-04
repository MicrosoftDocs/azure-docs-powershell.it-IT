---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: 72fcb1ecd78b2682fe678af8b75b36032ff58b32
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957309"
---
# <span data-ttu-id="1e225-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="1e225-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e225-102">SYNOPSIS</span></span>
<span data-ttu-id="1e225-103">Scarica un file da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e225-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="1e225-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e225-104">SYNTAX</span></span>

### <span data-ttu-id="1e225-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e225-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e225-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="1e225-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1e225-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="1e225-107">DESCRIPTION</span></span>
<span data-ttu-id="1e225-108">Il cmdlet **Export-AzDataLakeStoreItem** scarica un file da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e225-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="1e225-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e225-109">EXAMPLES</span></span>

### <span data-ttu-id="1e225-110">Esempio 1: Scaricare un elemento da Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="1e225-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="1e225-111">Questo comando scarica i file TestSource.csv da Data Lake Store C:\Test.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="1e225-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="1e225-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e225-112">PARAMETERS</span></span>

### <span data-ttu-id="1e225-113">-Account</span><span class="sxs-lookup"><span data-stu-id="1e225-113">-Account</span></span>
<span data-ttu-id="1e225-114">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1e225-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1e225-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="1e225-115">-Concurrency</span></span>
<span data-ttu-id="1e225-116">Indica il numero di file o blocchi da scaricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="1e225-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="1e225-117">Il valore predefinito verrà calcolato come lavoro migliore in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="1e225-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="1e225-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e225-118">-DefaultProfile</span></span>
<span data-ttu-id="1e225-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1e225-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1e225-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="1e225-120">-Destination</span></span>
<span data-ttu-id="1e225-121">Specifica il percorso del file locale in cui scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="1e225-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="1e225-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="1e225-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="1e225-123">Facoltativamente, indica il livello di log diagnostico da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="1e225-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="1e225-124">L'impostazione predefinita è Error.</span><span class="sxs-lookup"><span data-stu-id="1e225-124">Default is Error.</span></span>

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

### <span data-ttu-id="1e225-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="1e225-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="1e225-126">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="1e225-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="1e225-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1e225-127">-Force</span></span>
<span data-ttu-id="1e225-128">Indica che questa operazione può sovrascrivere il file di destinazione, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="1e225-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="1e225-129">-Path</span><span class="sxs-lookup"><span data-stu-id="1e225-129">-Path</span></span>
<span data-ttu-id="1e225-130">Specifica il percorso dell'elemento da scaricare da Data Lake Store, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="1e225-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="1e225-131">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="1e225-131">-Recurse</span></span>
<span data-ttu-id="1e225-132">Indica che il download di una cartella è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="1e225-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="1e225-133">-Riprendi</span><span class="sxs-lookup"><span data-stu-id="1e225-133">-Resume</span></span>
<span data-ttu-id="1e225-134">Indica che i file copiati sono una continuazione di un download precedente.</span><span class="sxs-lookup"><span data-stu-id="1e225-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="1e225-135">In questo modo il sistema tenterà di riprendere dall'ultimo file non completamente scaricato.</span><span class="sxs-lookup"><span data-stu-id="1e225-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="1e225-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1e225-136">-Confirm</span></span>
<span data-ttu-id="1e225-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e225-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e225-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e225-138">-WhatIf</span></span>
<span data-ttu-id="1e225-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e225-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e225-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e225-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e225-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e225-141">CommonParameters</span></span>
<span data-ttu-id="1e225-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e225-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e225-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e225-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e225-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="1e225-144">INPUTS</span></span>

### <span data-ttu-id="1e225-145">System.String</span><span class="sxs-lookup"><span data-stu-id="1e225-145">System.String</span></span>

### <span data-ttu-id="1e225-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="1e225-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="1e225-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1e225-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="1e225-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="1e225-148">System.Int32</span></span>

### <span data-ttu-id="1e225-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="1e225-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="1e225-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e225-150">OUTPUTS</span></span>

### <span data-ttu-id="1e225-151">System.String</span><span class="sxs-lookup"><span data-stu-id="1e225-151">System.String</span></span>

## <span data-ttu-id="1e225-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="1e225-152">NOTES</span></span>

## <span data-ttu-id="1e225-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e225-153">RELATED LINKS</span></span>

[<span data-ttu-id="1e225-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e225-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e225-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e225-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e225-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e225-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="1e225-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1e225-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


