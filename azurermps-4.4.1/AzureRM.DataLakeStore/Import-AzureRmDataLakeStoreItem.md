---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Import-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: ed10d3ee7c5a35c039a19f44211c7c2fce08aa06
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687207"
---
# <span data-ttu-id="1f6e6-101">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-101">Import-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="1f6e6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1f6e6-102">SYNOPSIS</span></span>
<span data-ttu-id="1f6e6-103">Carica un file o una directory locale in uno Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-103">Uploads a local file or directory to a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1f6e6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1f6e6-104">SYNTAX</span></span>

### <span data-ttu-id="1f6e6-105">Nessuna registrazione diagnostica (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1f6e6-105">No diagnostic logging (Default)</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f6e6-106">Includere la registrazione diagnostica</span><span class="sxs-lookup"><span data-stu-id="1f6e6-106">Include diagnostic logging</span></span>
```
Import-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f6e6-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1f6e6-107">DESCRIPTION</span></span>
<span data-ttu-id="1f6e6-108">Il cmdlet **Import-AzureRmDataLakeStoreItem** carica un file o una directory locale in uno Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-108">The **Import-AzureRmDataLakeStoreItem** cmdlet uploads a local file or directory to a Data Lake Store.</span></span>

## <span data-ttu-id="1f6e6-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1f6e6-109">EXAMPLES</span></span>

### <span data-ttu-id="1f6e6-110">Esempio 1: caricare un file</span><span class="sxs-lookup"><span data-stu-id="1f6e6-110">Example 1: Upload a file</span></span>
```
PS C:\>Import-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv"
```

<span data-ttu-id="1f6e6-111">Questo comando carica il file SrcFile.csv e lo aggiunge alla cartella MyFile nello Store Data Lake come File.csv.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-111">This command uploads the file SrcFile.csv and adds it to the MyFiles folder in the Data Lake Store as File.csv.</span></span>

## <span data-ttu-id="1f6e6-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1f6e6-112">PARAMETERS</span></span>

### <span data-ttu-id="1f6e6-113">-Account</span><span class="sxs-lookup"><span data-stu-id="1f6e6-113">-Account</span></span>
<span data-ttu-id="1f6e6-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="1f6e6-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="1f6e6-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="1f6e6-116">Specificare il numero massimo di file da caricare in parallelo per il caricamento di una cartella.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-116">Specify the maximum number of files to upload in parallel for a folder upload.</span></span>
<span data-ttu-id="1f6e6-117">Il valore predefinito è cinque (5).</span><span class="sxs-lookup"><span data-stu-id="1f6e6-117">The default value is five (5).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6e6-118">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="1f6e6-118">-Destination</span></span>
<span data-ttu-id="1f6e6-119">Specifica il percorso dello Store Data Lake a cui caricare un file o una cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="1f6e6-119">Specifies the Data Lake Store path to which to upload a file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="1f6e6-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="1f6e6-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="1f6e6-121">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="1f6e6-122">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-122">Default is Error.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: Include diagnostic logging
Aliases: 
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6e6-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="1f6e6-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="1f6e6-124">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

```yaml
Type: System.String
Parameter Sets: Include diagnostic logging
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6e6-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1f6e6-125">-Force</span></span>
<span data-ttu-id="1f6e6-126">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="1f6e6-127">-ForceBinary</span><span class="sxs-lookup"><span data-stu-id="1f6e6-127">-ForceBinary</span></span>
<span data-ttu-id="1f6e6-128">Indica che questa operazione carica il file come file binario.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-128">Indicates that this operation uploads the file as a binary file.</span></span>

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

### <span data-ttu-id="1f6e6-129">-Path</span><span class="sxs-lookup"><span data-stu-id="1f6e6-129">-Path</span></span>
<span data-ttu-id="1f6e6-130">Specifica il percorso locale del file o della cartella da caricare.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-130">Specifies the local path of the file or folder to upload.</span></span>

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

### <span data-ttu-id="1f6e6-131">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="1f6e6-131">-PerFileThreadCount</span></span>
<span data-ttu-id="1f6e6-132">Specifica il numero massimo di thread da usare per ogni file.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-132">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="1f6e6-133">Il valore predefinito è Ten (10).</span><span class="sxs-lookup"><span data-stu-id="1f6e6-133">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1f6e6-134">-Recurse</span><span class="sxs-lookup"><span data-stu-id="1f6e6-134">-Recurse</span></span>
<span data-ttu-id="1f6e6-135">Indica che questa operazione deve caricare tutti gli elementi in tutte le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-135">Indicates that this operation should upload all items in all subfolders.</span></span>

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

### <span data-ttu-id="1f6e6-136">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="1f6e6-136">-Resume</span></span>
<span data-ttu-id="1f6e6-137">Indica che questa operazione deve riprendere un caricamento già annullato o non riuscito.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-137">Indicates that this operation should resume a previously canceled or failed upload.</span></span>

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

### <span data-ttu-id="1f6e6-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1f6e6-138">-Confirm</span></span>
<span data-ttu-id="1f6e6-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f6e6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f6e6-140">-WhatIf</span></span>
<span data-ttu-id="1f6e6-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f6e6-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f6e6-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f6e6-143">-DefaultProfile</span></span>
<span data-ttu-id="1f6e6-144">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1f6e6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f6e6-145">CommonParameters</span></span>
<span data-ttu-id="1f6e6-146">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f6e6-147">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f6e6-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f6e6-148">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1f6e6-148">INPUTS</span></span>

## <span data-ttu-id="1f6e6-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1f6e6-149">OUTPUTS</span></span>

### <span data-ttu-id="1f6e6-150">stringa</span><span class="sxs-lookup"><span data-stu-id="1f6e6-150">string</span></span>
<span data-ttu-id="1f6e6-151">Il percorso completo nell'account di data Lake Store per il file o la cartella caricata.</span><span class="sxs-lookup"><span data-stu-id="1f6e6-151">The full path in the Data Lake Store account to the uploaded file or folder.</span></span>

## <span data-ttu-id="1f6e6-152">Note</span><span class="sxs-lookup"><span data-stu-id="1f6e6-152">NOTES</span></span>

## <span data-ttu-id="1f6e6-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1f6e6-153">RELATED LINKS</span></span>

[<span data-ttu-id="1f6e6-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1f6e6-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1f6e6-156">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-156">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1f6e6-157">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-157">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1f6e6-158">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-158">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1f6e6-159">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-159">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="1f6e6-160">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="1f6e6-160">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


