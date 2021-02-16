---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204362"
---
# <span data-ttu-id="a32c5-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="a32c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a32c5-102">SYNOPSIS</span></span>
<span data-ttu-id="a32c5-103">Carica un file o una directory locale in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a32c5-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="a32c5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a32c5-104">SYNTAX</span></span>

### <span data-ttu-id="a32c5-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a32c5-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a32c5-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="a32c5-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a32c5-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="a32c5-107">DESCRIPTION</span></span>
<span data-ttu-id="a32c5-108">Il cmdlet **Import-AzDataLakeStoreItem** carica un file o una directory locale in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a32c5-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="a32c5-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a32c5-109">EXAMPLES</span></span>

### <span data-ttu-id="a32c5-110">Esempio 1: Caricare un file</span><span class="sxs-lookup"><span data-stu-id="a32c5-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="a32c5-111">Questo comando carica il file SrcFile.csv e lo aggiunge alla cartella MyFiles in Data Lake Store File.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="a32c5-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="a32c5-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a32c5-112">PARAMETERS</span></span>

### <span data-ttu-id="a32c5-113">-Account</span><span class="sxs-lookup"><span data-stu-id="a32c5-113">-Account</span></span>
<span data-ttu-id="a32c5-114">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a32c5-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a32c5-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="a32c5-115">-Concurrency</span></span>
<span data-ttu-id="a32c5-116">Indica il numero di file o blocchi da caricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="a32c5-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="a32c5-117">L'impostazione predefinita verrà calcolata nel miglior modo possibile in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="a32c5-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="a32c5-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a32c5-118">-DefaultProfile</span></span>
<span data-ttu-id="a32c5-119">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a32c5-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a32c5-120">-Destination</span><span class="sxs-lookup"><span data-stu-id="a32c5-120">-Destination</span></span>
<span data-ttu-id="a32c5-121">Specifica il percorso di Data Lake Store in cui caricare un file o una cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="a32c5-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32c5-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="a32c5-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="a32c5-123">Facoltativamente, indica il livello di log diagnostico da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="a32c5-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="a32c5-124">L'impostazione predefinita è Error.</span><span class="sxs-lookup"><span data-stu-id="a32c5-124">Default is Error.</span></span>

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

### <span data-ttu-id="a32c5-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="a32c5-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="a32c5-126">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="a32c5-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="a32c5-127">-Force</span><span class="sxs-lookup"><span data-stu-id="a32c5-127">-Force</span></span>
<span data-ttu-id="a32c5-128">Indica che questa operazione può sovrascrivere il file di destinazione, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="a32c5-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32c5-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="a32c5-129">-ForceBinary</span></span>
<span data-ttu-id="a32c5-130">Indica che il file o i file da copiare devono essere copiati senza alcuna preoccupazione per la conservazione delle nuove righe tra le aggiunte.</span><span class="sxs-lookup"><span data-stu-id="a32c5-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a32c5-131">-Path</span><span class="sxs-lookup"><span data-stu-id="a32c5-131">-Path</span></span>
<span data-ttu-id="a32c5-132">Specifica il percorso locale del file o della cartella da caricare.</span><span class="sxs-lookup"><span data-stu-id="a32c5-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="a32c5-133">-Ricorrenza</span><span class="sxs-lookup"><span data-stu-id="a32c5-133">-Recurse</span></span>
<span data-ttu-id="a32c5-134">Indica che questa operazione deve caricare tutti gli elementi in tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="a32c5-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="a32c5-135">-Riprendi</span><span class="sxs-lookup"><span data-stu-id="a32c5-135">-Resume</span></span>
<span data-ttu-id="a32c5-136">Indica che i file copiati sono una continuazione di un caricamento precedente.</span><span class="sxs-lookup"><span data-stu-id="a32c5-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="a32c5-137">In questo modo il sistema tenterà di riprendere dall'ultimo file non completamente caricato.</span><span class="sxs-lookup"><span data-stu-id="a32c5-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="a32c5-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a32c5-138">-Confirm</span></span>
<span data-ttu-id="a32c5-139">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a32c5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a32c5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a32c5-140">-WhatIf</span></span>
<span data-ttu-id="a32c5-141">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a32c5-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a32c5-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a32c5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a32c5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a32c5-143">CommonParameters</span></span>
<span data-ttu-id="a32c5-144">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a32c5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a32c5-145">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a32c5-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a32c5-146">INPUT</span><span class="sxs-lookup"><span data-stu-id="a32c5-146">INPUTS</span></span>

### <span data-ttu-id="a32c5-147">System.String</span><span class="sxs-lookup"><span data-stu-id="a32c5-147">System.String</span></span>

### <span data-ttu-id="a32c5-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a32c5-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a32c5-149">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a32c5-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="a32c5-150">System.Int32</span><span class="sxs-lookup"><span data-stu-id="a32c5-150">System.Int32</span></span>

### <span data-ttu-id="a32c5-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span><span class="sxs-lookup"><span data-stu-id="a32c5-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="a32c5-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a32c5-152">OUTPUTS</span></span>

### <span data-ttu-id="a32c5-153">System.String</span><span class="sxs-lookup"><span data-stu-id="a32c5-153">System.String</span></span>

## <span data-ttu-id="a32c5-154">NOTE</span><span class="sxs-lookup"><span data-stu-id="a32c5-154">NOTES</span></span>

## <span data-ttu-id="a32c5-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a32c5-155">RELATED LINKS</span></span>

[<span data-ttu-id="a32c5-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="a32c5-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="a32c5-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="a32c5-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="a32c5-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="a32c5-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="a32c5-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a32c5-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


