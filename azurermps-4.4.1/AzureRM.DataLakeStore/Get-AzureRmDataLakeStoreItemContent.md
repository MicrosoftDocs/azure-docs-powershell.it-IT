---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 3da97a14049671f8fff8bc03f7f32609f9b86984
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687216"
---
# <span data-ttu-id="ca168-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="ca168-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="ca168-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ca168-102">SYNOPSIS</span></span>
<span data-ttu-id="ca168-103">Ottiene il contenuto di un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ca168-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca168-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ca168-104">SYNTAX</span></span>

### <span data-ttu-id="ca168-105">Anteprima del contenuto del file (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ca168-105">Preview file content (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca168-106">Visualizzare in anteprima le righe del file dalla testa del file</span><span class="sxs-lookup"><span data-stu-id="ca168-106">Preview file rows from the head of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ca168-107">Visualizzare in anteprima le righe del file dalla coda del file</span><span class="sxs-lookup"><span data-stu-id="ca168-107">Preview file rows from the tail of the file</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ca168-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ca168-108">DESCRIPTION</span></span>
<span data-ttu-id="ca168-109">Il cmdlet **Get-AzureRmDataLakeStoreItemContent** ottiene il contenuto di un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ca168-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="ca168-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ca168-110">EXAMPLES</span></span>

### <span data-ttu-id="ca168-111">Esempio 1: recuperare il contenuto di un file</span><span class="sxs-lookup"><span data-stu-id="ca168-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="ca168-112">Questo comando consente di ottenere il contenuto del file MyFile.txt nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ca168-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="ca168-113">Esempio 2: ottenere le prime due righe di un file</span><span class="sxs-lookup"><span data-stu-id="ca168-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="ca168-114">Questo comando consente di ottenere le prime due righe separate della nuova riga nel MyFile.txt file nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="ca168-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="ca168-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ca168-115">PARAMETERS</span></span>

### <span data-ttu-id="ca168-116">-Account</span><span class="sxs-lookup"><span data-stu-id="ca168-116">-Account</span></span>
<span data-ttu-id="ca168-117">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="ca168-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="ca168-118">-Codifica</span><span class="sxs-lookup"><span data-stu-id="ca168-118">-Encoding</span></span>
<span data-ttu-id="ca168-119">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="ca168-119">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="ca168-120">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="ca168-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ca168-121">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="ca168-121">Unknown</span></span>
- <span data-ttu-id="ca168-122">Stringa</span><span class="sxs-lookup"><span data-stu-id="ca168-122">String</span></span>
- <span data-ttu-id="ca168-123">Unicode</span><span class="sxs-lookup"><span data-stu-id="ca168-123">Unicode</span></span>
- <span data-ttu-id="ca168-124">Byte</span><span class="sxs-lookup"><span data-stu-id="ca168-124">Byte</span></span>
- <span data-ttu-id="ca168-125">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="ca168-125">BigEndianUnicode</span></span>
- <span data-ttu-id="ca168-126">UTF8</span><span class="sxs-lookup"><span data-stu-id="ca168-126">UTF8</span></span>
- <span data-ttu-id="ca168-127">UTF7</span><span class="sxs-lookup"><span data-stu-id="ca168-127">UTF7</span></span>
- <span data-ttu-id="ca168-128">ASCII</span><span class="sxs-lookup"><span data-stu-id="ca168-128">Ascii</span></span>
- <span data-ttu-id="ca168-129">Predefinita</span><span class="sxs-lookup"><span data-stu-id="ca168-129">Default</span></span>
- <span data-ttu-id="ca168-130">OEM</span><span class="sxs-lookup"><span data-stu-id="ca168-130">Oem</span></span>
- <span data-ttu-id="ca168-131">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="ca168-131">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca168-132">-Force</span><span class="sxs-lookup"><span data-stu-id="ca168-132">-Force</span></span>
<span data-ttu-id="ca168-133">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ca168-133">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca168-134">-Head</span><span class="sxs-lookup"><span data-stu-id="ca168-134">-Head</span></span>
<span data-ttu-id="ca168-135">Numero di righe (nuova riga delimitato) dall'inizio del file in anteprima.</span><span class="sxs-lookup"><span data-stu-id="ca168-135">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="ca168-136">Se non viene rilevata una nuova riga nei primi 4 MB di dati, verranno restituiti solo i dati.</span><span class="sxs-lookup"><span data-stu-id="ca168-136">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the head of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca168-137">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="ca168-137">-Length</span></span>
<span data-ttu-id="ca168-138">Specifica la lunghezza, in byte, del contenuto da ottenere.</span><span class="sxs-lookup"><span data-stu-id="ca168-138">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca168-139">-Offset</span><span class="sxs-lookup"><span data-stu-id="ca168-139">-Offset</span></span>
<span data-ttu-id="ca168-140">Specifica il numero di byte da ignorare in un file prima di ottenere contenuto.</span><span class="sxs-lookup"><span data-stu-id="ca168-140">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: Preview file content
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca168-141">-Path</span><span class="sxs-lookup"><span data-stu-id="ca168-141">-Path</span></span>
<span data-ttu-id="ca168-142">Specifica il percorso di data Lake Store di un file, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="ca168-142">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="ca168-143">-Coda</span><span class="sxs-lookup"><span data-stu-id="ca168-143">-Tail</span></span>
<span data-ttu-id="ca168-144">Numero di righe (nuova riga delimitato) dalla fine del file in anteprima.</span><span class="sxs-lookup"><span data-stu-id="ca168-144">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="ca168-145">Se non viene rilevata una nuova riga nei primi 4 MB di dati, verranno restituiti solo i dati.</span><span class="sxs-lookup"><span data-stu-id="ca168-145">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: Preview file rows from the tail of the file
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ca168-146">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ca168-146">-Confirm</span></span>
<span data-ttu-id="ca168-147">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ca168-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ca168-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ca168-148">-WhatIf</span></span>
<span data-ttu-id="ca168-149">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca168-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ca168-150">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ca168-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ca168-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca168-151">-DefaultProfile</span></span>
<span data-ttu-id="ca168-152">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ca168-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca168-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca168-153">CommonParameters</span></span>
<span data-ttu-id="ca168-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca168-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca168-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca168-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca168-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ca168-156">INPUTS</span></span>

## <span data-ttu-id="ca168-157">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ca168-157">OUTPUTS</span></span>

### <span data-ttu-id="ca168-158">byte []</span><span class="sxs-lookup"><span data-stu-id="ca168-158">byte[]</span></span>
<span data-ttu-id="ca168-159">Rappresentazione del flusso di byte del contenuto del file recuperato.</span><span class="sxs-lookup"><span data-stu-id="ca168-159">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="ca168-160">stringa</span><span class="sxs-lookup"><span data-stu-id="ca168-160">string</span></span>
<span data-ttu-id="ca168-161">Rappresentazione di stringa (nella codifica specificata) del contenuto del file recuperato.</span><span class="sxs-lookup"><span data-stu-id="ca168-161">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="ca168-162">Note</span><span class="sxs-lookup"><span data-stu-id="ca168-162">NOTES</span></span>

## <span data-ttu-id="ca168-163">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ca168-163">RELATED LINKS</span></span>

