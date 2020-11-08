---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192121"
---
# <span data-ttu-id="6794d-101">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-101">Import-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="6794d-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6794d-102">SYNOPSIS</span></span>
<span data-ttu-id="6794d-103">Carica un file o una directory locale in uno Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6794d-103">Uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="6794d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6794d-104">SYNTAX</span></span>

### <span data-ttu-id="6794d-105">NoDiagnosticLogging (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6794d-105">NoDiagnosticLogging (Default)</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6794d-106">IncludeDiagnosticLogging</span><span class="sxs-lookup"><span data-stu-id="6794d-106">IncludeDiagnosticLogging</span></span>
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6794d-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6794d-107">DESCRIPTION</span></span>
<span data-ttu-id="6794d-108">Il cmdlet **Import-AzDataLakeStoreItem** carica un file o una directory locale in uno Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="6794d-108">The **Import-AzDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="6794d-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6794d-109">EXAMPLES</span></span>

### <span data-ttu-id="6794d-110">Esempio 1: caricare un file</span><span class="sxs-lookup"><span data-stu-id="6794d-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

<span data-ttu-id="6794d-111">Questo comando carica il file SrcFile.csv e lo aggiunge alla cartella MyFile nello Store Data Lake come File.csv con una concorrenza di 4.</span><span class="sxs-lookup"><span data-stu-id="6794d-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv with a concurrency of 4.</span></span>

## <span data-ttu-id="6794d-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6794d-112">PARAMETERS</span></span>

### <span data-ttu-id="6794d-113">-Account</span><span class="sxs-lookup"><span data-stu-id="6794d-113">-Account</span></span>
<span data-ttu-id="6794d-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6794d-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6794d-115">-Concorrenza</span><span class="sxs-lookup"><span data-stu-id="6794d-115">-Concurrency</span></span>
<span data-ttu-id="6794d-116">Indica il numero di file o blocchi da caricare in parallelo.</span><span class="sxs-lookup"><span data-stu-id="6794d-116">Indicates the number of files or chunks to upload in parallel.</span></span> <span data-ttu-id="6794d-117">L'impostazione predefinita verrà calcolata come uno sforzo ottimale in base alle specifiche di sistema.</span><span class="sxs-lookup"><span data-stu-id="6794d-117">Default will be computed as a best effort based on system specifications.</span></span>

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

### <span data-ttu-id="6794d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6794d-118">-DefaultProfile</span></span>
<span data-ttu-id="6794d-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6794d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6794d-120">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="6794d-120">-Destination</span></span>
<span data-ttu-id="6794d-121">Specifica il percorso dello Store Data Lake a cui caricare un file o una cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="6794d-121">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6794d-122">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="6794d-122">-DiagnosticLogLevel</span></span>
<span data-ttu-id="6794d-123">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="6794d-123">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="6794d-124">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="6794d-124">Default is Error.</span></span>

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

### <span data-ttu-id="6794d-125">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="6794d-125">-DiagnosticLogPath</span></span>
<span data-ttu-id="6794d-126">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="6794d-126">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="6794d-127">-Force</span><span class="sxs-lookup"><span data-stu-id="6794d-127">-Force</span></span>
<span data-ttu-id="6794d-128">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="6794d-128">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6794d-129">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="6794d-129">-ForceBinary</span></span>
<span data-ttu-id="6794d-130">Indica che i file da copiare devono essere copiati senza alcuna preoccupazione per la conservazione delle nuove linee tra le aggiunte.</span><span class="sxs-lookup"><span data-stu-id="6794d-130">Indicates that the file(s) being copied should be copied with no concern for new line preservation across appends.</span></span>

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

### <span data-ttu-id="6794d-131">-Path</span><span class="sxs-lookup"><span data-stu-id="6794d-131">-Path</span></span>
<span data-ttu-id="6794d-132">Specifica il percorso locale del file o della cartella da caricare.</span><span class="sxs-lookup"><span data-stu-id="6794d-132">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="6794d-133">-Recurse</span><span class="sxs-lookup"><span data-stu-id="6794d-133">-Recurse</span></span>
<span data-ttu-id="6794d-134">Indica che questa operazione deve caricare tutti gli elementi in tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="6794d-134">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="6794d-135">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="6794d-135">-Resume</span></span>
<span data-ttu-id="6794d-136">Indica che i file da copiare sono la continuazione di un caricamento precedente.</span><span class="sxs-lookup"><span data-stu-id="6794d-136">Indicates that the file(s) being copied are a continuation of a previous upload.</span></span> <span data-ttu-id="6794d-137">In questo modo il sistema cercherà di riprendere dall'ultimo file che non è stato completamente caricato.</span><span class="sxs-lookup"><span data-stu-id="6794d-137">This will cause the system to attempt to resume from the last file that was not fully uploaded.</span></span>

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

### <span data-ttu-id="6794d-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6794d-138">-Confirm</span></span>
<span data-ttu-id="6794d-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6794d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6794d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6794d-140">-WhatIf</span></span>
<span data-ttu-id="6794d-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6794d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6794d-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6794d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6794d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6794d-143">CommonParameters</span></span>
<span data-ttu-id="6794d-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6794d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6794d-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6794d-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6794d-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6794d-146">INPUTS</span></span>

### <span data-ttu-id="6794d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="6794d-147">System.String</span></span>

### <span data-ttu-id="6794d-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6794d-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6794d-149">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6794d-149">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6794d-150">System. Int32</span><span class="sxs-lookup"><span data-stu-id="6794d-150">System.Int32</span></span>

### <span data-ttu-id="6794d-151">Microsoft. Azure. Commands. DataLakeStore. Models. LogLevel</span><span class="sxs-lookup"><span data-stu-id="6794d-151">Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel</span></span>

## <span data-ttu-id="6794d-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6794d-152">OUTPUTS</span></span>

### <span data-ttu-id="6794d-153">System. String</span><span class="sxs-lookup"><span data-stu-id="6794d-153">System.String</span></span>

## <span data-ttu-id="6794d-154">Note</span><span class="sxs-lookup"><span data-stu-id="6794d-154">NOTES</span></span>

## <span data-ttu-id="6794d-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6794d-155">RELATED LINKS</span></span>

[<span data-ttu-id="6794d-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="6794d-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="6794d-158">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-158">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="6794d-159">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-159">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="6794d-160">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-160">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="6794d-161">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-161">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="6794d-162">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6794d-162">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


