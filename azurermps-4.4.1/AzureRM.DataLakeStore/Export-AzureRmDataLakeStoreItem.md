---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B10B1F5D-5566-4129-9D42-05A6D3B72C9E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Export-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: febcec4d309e849e3b259fc2d80b3129ca7b65f6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520115"
---
# <span data-ttu-id="aec16-101">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-101">Export-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="aec16-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="aec16-102">SYNOPSIS</span></span>
<span data-ttu-id="aec16-103">Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aec16-103">Downloads a file from Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="aec16-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aec16-104">SYNTAX</span></span>

### <span data-ttu-id="aec16-105">Nessuna registrazione diagnostica (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="aec16-105">No diagnostic logging (Default)</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aec16-106">Includere la registrazione diagnostica</span><span class="sxs-lookup"><span data-stu-id="aec16-106">Include diagnostic logging</span></span>
```
Export-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Destination] <String>
 [-Recurse] [-Resume] [[-PerFileThreadCount] <Int32>] [[-ConcurrentFileCount] <Int32>] [-Force]
 [-DiagnosticLogLevel <LogLevel>] -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aec16-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="aec16-107">DESCRIPTION</span></span>
<span data-ttu-id="aec16-108">Il cmdlet **Export-AzureRmDataLakeStoreItem** Scarica un file da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aec16-108">The **Export-AzureRmDataLakeStoreItem** cmdlet downloads a file from Data Lake Store.</span></span>

## <span data-ttu-id="aec16-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aec16-109">EXAMPLES</span></span>

### <span data-ttu-id="aec16-110">Esempio 1: scaricare un elemento da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="aec16-110">Example 1: Download an item from the Data Lake Store</span></span>
```
PS C:\>Export-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path /myFiles/TestSource.csv -Destination "C:\Test.csv"
```

<span data-ttu-id="aec16-111">Questo comando Scarica il file TestSource.csv da data Lake Store in C:\Test.csv.</span><span class="sxs-lookup"><span data-stu-id="aec16-111">This command downloads the file TestSource.csv from the Data Lake Store to C:\Test.csv.</span></span>

## <span data-ttu-id="aec16-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="aec16-112">PARAMETERS</span></span>

### <span data-ttu-id="aec16-113">-Account</span><span class="sxs-lookup"><span data-stu-id="aec16-113">-Account</span></span>
<span data-ttu-id="aec16-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aec16-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="aec16-115">-ConcurrentFileCount</span><span class="sxs-lookup"><span data-stu-id="aec16-115">-ConcurrentFileCount</span></span>
<span data-ttu-id="aec16-116">Specifica il numero massimo di file da scaricare in parallelo per il download di una cartella.</span><span class="sxs-lookup"><span data-stu-id="aec16-116">Specifies the maximum number of files to download in parallel for a folder download.</span></span>
<span data-ttu-id="aec16-117">Il valore predefinito è cinque (5).</span><span class="sxs-lookup"><span data-stu-id="aec16-117">The default value is five (5).</span></span>

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

### <span data-ttu-id="aec16-118">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="aec16-118">-Destination</span></span>
<span data-ttu-id="aec16-119">Specifica il percorso del file locale a cui scaricare il file.</span><span class="sxs-lookup"><span data-stu-id="aec16-119">Specifies the local file path to which to download the file.</span></span>

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

### <span data-ttu-id="aec16-120">-DiagnosticLogLevel</span><span class="sxs-lookup"><span data-stu-id="aec16-120">-DiagnosticLogLevel</span></span>
<span data-ttu-id="aec16-121">Facoltativamente, indica il livello del log di diagnostica da usare per registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="aec16-121">Optionally indicates the diagnostic log level to use to record events during the file or folder import.</span></span> <span data-ttu-id="aec16-122">Il valore predefinito è Error.</span><span class="sxs-lookup"><span data-stu-id="aec16-122">Default is Error.</span></span>

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

### <span data-ttu-id="aec16-123">-DiagnosticLogPath</span><span class="sxs-lookup"><span data-stu-id="aec16-123">-DiagnosticLogPath</span></span>
<span data-ttu-id="aec16-124">Specifica il percorso del log di diagnostica in cui registrare gli eventi durante l'importazione di file o cartelle.</span><span class="sxs-lookup"><span data-stu-id="aec16-124">Specifies the path for the diagnostic log to record events to during the file or folder import.</span></span>

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

### <span data-ttu-id="aec16-125">-Force</span><span class="sxs-lookup"><span data-stu-id="aec16-125">-Force</span></span>
<span data-ttu-id="aec16-126">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="aec16-126">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="aec16-127">-Path</span><span class="sxs-lookup"><span data-stu-id="aec16-127">-Path</span></span>
<span data-ttu-id="aec16-128">Specifica il percorso dell'elemento da scaricare da data Lake Store, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="aec16-128">Specifies the path of the item to download from the Data Lake Store, starting from the root directory (/).</span></span>

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

### <span data-ttu-id="aec16-129">-PerFileThreadCount</span><span class="sxs-lookup"><span data-stu-id="aec16-129">-PerFileThreadCount</span></span>
<span data-ttu-id="aec16-130">Specifica il numero massimo di thread da usare per ogni file.</span><span class="sxs-lookup"><span data-stu-id="aec16-130">Specifies the maximum number of threads to use per file.</span></span>
<span data-ttu-id="aec16-131">Il valore predefinito è Ten (10).</span><span class="sxs-lookup"><span data-stu-id="aec16-131">The default value is ten (10).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="aec16-132">-Recurse</span><span class="sxs-lookup"><span data-stu-id="aec16-132">-Recurse</span></span>
<span data-ttu-id="aec16-133">Indica che il download di una cartella è ricorsivo.</span><span class="sxs-lookup"><span data-stu-id="aec16-133">Indicates that a folder download is recursive.</span></span>

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

### <span data-ttu-id="aec16-134">-Curriculum vitae</span><span class="sxs-lookup"><span data-stu-id="aec16-134">-Resume</span></span>
<span data-ttu-id="aec16-135">Indica che il file o i file da copiare sono la continuazione di un download precedente.</span><span class="sxs-lookup"><span data-stu-id="aec16-135">Indicates that the file or files being copied are a continuation of a previous download.</span></span>
<span data-ttu-id="aec16-136">Il download tenta di riprendere dall'ultimo file che non è stato completamente scaricato.</span><span class="sxs-lookup"><span data-stu-id="aec16-136">The download attempts to resume from the last file that was not fully downloaded.</span></span>

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

### <span data-ttu-id="aec16-137">-Confermare</span><span class="sxs-lookup"><span data-stu-id="aec16-137">-Confirm</span></span>
<span data-ttu-id="aec16-138">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aec16-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aec16-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aec16-139">-WhatIf</span></span>
<span data-ttu-id="aec16-140">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aec16-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aec16-141">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="aec16-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aec16-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aec16-142">-DefaultProfile</span></span>
<span data-ttu-id="aec16-143">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aec16-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aec16-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aec16-144">CommonParameters</span></span>
<span data-ttu-id="aec16-145">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aec16-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aec16-146">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aec16-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aec16-147">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="aec16-147">INPUTS</span></span>

## <span data-ttu-id="aec16-148">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aec16-148">OUTPUTS</span></span>

### <span data-ttu-id="aec16-149">stringa</span><span class="sxs-lookup"><span data-stu-id="aec16-149">string</span></span>
<span data-ttu-id="aec16-150">Percorso in cui è stato scaricato il file o la cartella.</span><span class="sxs-lookup"><span data-stu-id="aec16-150">The path where the file or folder was downloaded to.</span></span>

## <span data-ttu-id="aec16-151">Note</span><span class="sxs-lookup"><span data-stu-id="aec16-151">NOTES</span></span>

## <span data-ttu-id="aec16-152">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aec16-152">RELATED LINKS</span></span>

[<span data-ttu-id="aec16-153">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-153">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="aec16-154">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-154">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="aec16-155">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-155">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="aec16-156">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-156">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="aec16-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="aec16-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="aec16-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aec16-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


