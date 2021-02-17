---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/export-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Export-AzDataLakeStoreItem.md
ms.openlocfilehash: e0bac2f22249b27442c75da7879f6a6cf85e7da7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198814"
---
# <span data-ttu-id="3cd3a-101">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-101">Export-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="3cd3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cd3a-102">SYNOPSIS</span></span>
<span data-ttu-id="3cd3a-103">Scarica un file da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-103">Downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="3cd3a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3cd3a-104">SYNTAX</span></span>

### <span data-ttu-id="3cd3a-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="3cd3a-105">NoDiagnosticLogging (Default)</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cd3a-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="3cd3a-106">IncludeDiagnosticLogging</span></span>
```
Export-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cd3a-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="3cd3a-107">DESCRIPTION</span></span>
<span data-ttu-id="3cd3a-108">Il cmdlet **Export-AzDataLakeStoreItem** scarica un file da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-108">The **Export-AzDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="3cd3a-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3cd3a-109">EXAMPLES</span></span>

### <span data-ttu-id="3cd3a-110">Esempio 1: Scaricare un elemento da Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="3cd3a-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv" -Concurrency 4
```

<span data-ttu-id="3cd3a-111">Questo comando scarica i file TestSource.csv da Data Lake Store C:\Test.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="3cd3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cd3a-112">PARAMETERS</span></span>

### <span data-ttu-id="3cd3a-113">-Account</span><span class="sxs-lookup"><span data-stu-id="3cd3a-113">-Account</span></span>
<span data-ttu-id="3cd3a-114">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3cd3a-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="3cd3a-115">-Concurrency</span></span>
<span data-ttu-id="3cd3a-116">Indica il numero di file o blocchi da scaricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-116">Indicates the number of files or chunks to download in parallel.</span></span> <span data-ttu-id="3cd3a-117">Il valore predefinito verrà calcolato come lavoro migliore in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="3cd3a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cd3a-118">-DefaultProfile</span></span>
<span data-ttu-id="3cd3a-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3cd3a-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="3cd3a-120">-Destination</span></span>
<span data-ttu-id="3cd3a-121">Specifica il percorso del file locale in cui scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-121">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="3cd3a-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="3cd3a-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="3cd3a-123">Facoltativamente, indica il livello di log diagnostico da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="3cd3a-124">L'impostazione predefinita è Error.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-124">Default is Error.</span></span>

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

### <span data-ttu-id="3cd3a-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="3cd3a-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="3cd3a-126">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="3cd3a-127">-Force</span><span class="sxs-lookup"><span data-stu-id="3cd3a-127">-Force</span></span>
<span data-ttu-id="3cd3a-128">Indica che questa operazione può sovrascrivere il file di destinazione, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="3cd3a-129">-Path</span><span class="sxs-lookup"><span data-stu-id="3cd3a-129">-Path</span></span>
<span data-ttu-id="3cd3a-130">Specifica il percorso dell'elemento da scaricare da Data Lake Store, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="3cd3a-130">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="3cd3a-131">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="3cd3a-131">-Recurse</span></span>
<span data-ttu-id="3cd3a-132">Indica che il download di una cartella è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-132">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="3cd3a-133">-Riprendi</span><span class="sxs-lookup"><span data-stu-id="3cd3a-133">-Resume</span></span>
<span data-ttu-id="3cd3a-134">Indica che i file da copiare sono la continuazione di un download precedente.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-134">Indicates that the file(s) being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="3cd3a-135">In questo modo il sistema tenterà di riprendere dall'ultimo file non completamente scaricato.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-135">This will cause the system to attempt to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="3cd3a-136">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cd3a-136">-Confirm</span></span>
<span data-ttu-id="3cd3a-137">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cd3a-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cd3a-138">-WhatIf</span></span>
<span data-ttu-id="3cd3a-139">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cd3a-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cd3a-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cd3a-141">CommonParameters</span></span>
<span data-ttu-id="3cd3a-142">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cd3a-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cd3a-143">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cd3a-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cd3a-144">INPUT</span><span class="sxs-lookup"><span data-stu-id="3cd3a-144">INPUTS</span></span>

### <span data-ttu-id="3cd3a-145">System.String</span><span class="sxs-lookup"><span data-stu-id="3cd3a-145">System.String</span></span>

### <span data-ttu-id="3cd3a-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3cd3a-146">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="3cd3a-147">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="3cd3a-147">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="3cd3a-148">System.Int32</span><span class="sxs-lookup"><span data-stu-id="3cd3a-148">System.Int32</span></span>

### <span data-ttu-id="3cd3a-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="3cd3a-149">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="3cd3a-150">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3cd3a-150">OUTPUTS</span></span>

### <span data-ttu-id="3cd3a-151">System.String</span><span class="sxs-lookup"><span data-stu-id="3cd3a-151">System.String</span></span>

## <span data-ttu-id="3cd3a-152">NOTE</span><span class="sxs-lookup"><span data-stu-id="3cd3a-152">NOTES</span></span>

## <span data-ttu-id="3cd3a-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3cd3a-153">RELATED LINKS</span></span>

[<span data-ttu-id="3cd3a-154">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-154">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="3cd3a-155">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-155">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="3cd3a-156">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-156">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="3cd3a-157">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-157">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="3cd3a-158">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-158">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="3cd3a-159">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-159">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="3cd3a-160">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3cd3a-160">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


