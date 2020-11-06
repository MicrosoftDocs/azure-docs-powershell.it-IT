---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 15DFF66F-3D78-422B-BA40-71058DE66BA2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 7a757ca4b310176a71a7b2fe7e5c301137998ff9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520640"
---
# <span data-ttu-id="71eba-101">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="71eba-101">Get-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="71eba-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="71eba-102">SYNOPSIS</span></span>
<span data-ttu-id="71eba-103">Ottiene il contenuto di un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71eba-103">Gets the contents of a file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71eba-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="71eba-104">SYNTAX</span></span>

### <span data-ttu-id="71eba-105">PreviewFileContent (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="71eba-105">PreviewFileContent (Default)</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Offset] <Int64>]
 [[-Length] <Int64>] [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71eba-106">PreviewFileRowsFromHead</span><span class="sxs-lookup"><span data-stu-id="71eba-106">PreviewFileRowsFromHead</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Head] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="71eba-107">PreviewFileRowsFromTail</span><span class="sxs-lookup"><span data-stu-id="71eba-107">PreviewFileRowsFromTail</span></span>
```
Get-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Tail] <Int32>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="71eba-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="71eba-108">DESCRIPTION</span></span>
<span data-ttu-id="71eba-109">Il cmdlet **Get-AzureRmDataLakeStoreItemContent** ottiene il contenuto di un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71eba-109">The **Get-AzureRmDataLakeStoreItemContent** cmdlet gets the contents of a file in Data Lake Store.</span></span>

## <span data-ttu-id="71eba-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="71eba-110">EXAMPLES</span></span>

### <span data-ttu-id="71eba-111">Esempio 1: recuperare il contenuto di un file</span><span class="sxs-lookup"><span data-stu-id="71eba-111">Example 1: Get the contents of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt"
```

<span data-ttu-id="71eba-112">Questo comando consente di ottenere il contenuto del file MyFile.txt nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="71eba-112">This command gets the contents of the file MyFile.txt in the ContosoADL account.</span></span>

### <span data-ttu-id="71eba-113">Esempio 2: ottenere le prime due righe di un file</span><span class="sxs-lookup"><span data-stu-id="71eba-113">Example 2: Get the first two rows of a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemContent -AccountName "ContosoADL" -Path "/MyFile.txt" -Head 2
```

<span data-ttu-id="71eba-114">Questo comando consente di ottenere le prime due righe separate della nuova riga nel MyFile.txt file nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="71eba-114">This command gets the first two new line separated rows in the file MyFile.txt in the ContosoADL account.</span></span>

## <span data-ttu-id="71eba-115">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="71eba-115">PARAMETERS</span></span>

### <span data-ttu-id="71eba-116">-Account</span><span class="sxs-lookup"><span data-stu-id="71eba-116">-Account</span></span>
<span data-ttu-id="71eba-117">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="71eba-117">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="71eba-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="71eba-118">-DefaultProfile</span></span>
<span data-ttu-id="71eba-119">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="71eba-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="71eba-120">-Codifica</span><span class="sxs-lookup"><span data-stu-id="71eba-120">-Encoding</span></span>
<span data-ttu-id="71eba-121">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="71eba-121">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="71eba-122">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="71eba-122">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="71eba-123">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="71eba-123">Unknown</span></span>
- <span data-ttu-id="71eba-124">Stringa</span><span class="sxs-lookup"><span data-stu-id="71eba-124">String</span></span>
- <span data-ttu-id="71eba-125">Unicode</span><span class="sxs-lookup"><span data-stu-id="71eba-125">Unicode</span></span>
- <span data-ttu-id="71eba-126">Byte</span><span class="sxs-lookup"><span data-stu-id="71eba-126">Byte</span></span>
- <span data-ttu-id="71eba-127">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="71eba-127">BigEndianUnicode</span></span>
- <span data-ttu-id="71eba-128">UTF8</span><span class="sxs-lookup"><span data-stu-id="71eba-128">UTF8</span></span>
- <span data-ttu-id="71eba-129">UTF7</span><span class="sxs-lookup"><span data-stu-id="71eba-129">UTF7</span></span>
- <span data-ttu-id="71eba-130">ASCII</span><span class="sxs-lookup"><span data-stu-id="71eba-130">Ascii</span></span>
- <span data-ttu-id="71eba-131">Predefinita</span><span class="sxs-lookup"><span data-stu-id="71eba-131">Default</span></span>
- <span data-ttu-id="71eba-132">OEM</span><span class="sxs-lookup"><span data-stu-id="71eba-132">Oem</span></span>
- <span data-ttu-id="71eba-133">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="71eba-133">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71eba-134">-Force</span><span class="sxs-lookup"><span data-stu-id="71eba-134">-Force</span></span>
<span data-ttu-id="71eba-135">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="71eba-135">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71eba-136">-Head</span><span class="sxs-lookup"><span data-stu-id="71eba-136">-Head</span></span>
<span data-ttu-id="71eba-137">Numero di righe (nuova riga delimitato) dall'inizio del file in anteprima.</span><span class="sxs-lookup"><span data-stu-id="71eba-137">The number of rows (new line delimited) from the beginning of the file to preview.</span></span> <span data-ttu-id="71eba-138">Se non viene rilevata una nuova riga nei primi 4 MB di dati, verranno restituiti solo i dati.</span><span class="sxs-lookup"><span data-stu-id="71eba-138">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromHead
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71eba-139">-Lunghezza</span><span class="sxs-lookup"><span data-stu-id="71eba-139">-Length</span></span>
<span data-ttu-id="71eba-140">Specifica la lunghezza, in byte, del contenuto da ottenere.</span><span class="sxs-lookup"><span data-stu-id="71eba-140">Specifies the length, in bytes, of the content to get.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71eba-141">-Offset</span><span class="sxs-lookup"><span data-stu-id="71eba-141">-Offset</span></span>
<span data-ttu-id="71eba-142">Specifica il numero di byte da ignorare in un file prima di ottenere contenuto.</span><span class="sxs-lookup"><span data-stu-id="71eba-142">Specifies the number of bytes to skip in a file before getting content.</span></span>

```yaml
Type: System.Int64
Parameter Sets: PreviewFileContent
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71eba-143">-Path</span><span class="sxs-lookup"><span data-stu-id="71eba-143">-Path</span></span>
<span data-ttu-id="71eba-144">Specifica il percorso di data Lake Store di un file, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="71eba-144">Specifies the Data Lake Store path of a file, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="71eba-145">-Coda</span><span class="sxs-lookup"><span data-stu-id="71eba-145">-Tail</span></span>
<span data-ttu-id="71eba-146">Numero di righe (nuova riga delimitato) dalla fine del file in anteprima.</span><span class="sxs-lookup"><span data-stu-id="71eba-146">The number of rows (new line delimited) from the end of the file to preview.</span></span> <span data-ttu-id="71eba-147">Se non viene rilevata una nuova riga nei primi 4 MB di dati, verranno restituiti solo i dati.</span><span class="sxs-lookup"><span data-stu-id="71eba-147">If no new line is encountered in the first 4mb of data, only that data will be returned.</span></span>

```yaml
Type: System.Int32
Parameter Sets: PreviewFileRowsFromTail
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="71eba-148">-Confermare</span><span class="sxs-lookup"><span data-stu-id="71eba-148">-Confirm</span></span>
<span data-ttu-id="71eba-149">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="71eba-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="71eba-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="71eba-150">-WhatIf</span></span>
<span data-ttu-id="71eba-151">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71eba-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="71eba-152">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="71eba-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="71eba-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71eba-153">CommonParameters</span></span>
<span data-ttu-id="71eba-154">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="71eba-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71eba-155">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71eba-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71eba-156">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="71eba-156">INPUTS</span></span>

### <span data-ttu-id="71eba-157">System. String</span><span class="sxs-lookup"><span data-stu-id="71eba-157">System.String</span></span>

### <span data-ttu-id="71eba-158">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="71eba-158">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="71eba-159">System. Int32</span><span class="sxs-lookup"><span data-stu-id="71eba-159">System.Int32</span></span>

### <span data-ttu-id="71eba-160">System. Int64</span><span class="sxs-lookup"><span data-stu-id="71eba-160">System.Int64</span></span>

### <span data-ttu-id="71eba-161">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="71eba-161">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

### <span data-ttu-id="71eba-162">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="71eba-162">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="71eba-163">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="71eba-163">OUTPUTS</span></span>

### <span data-ttu-id="71eba-164">System. byte</span><span class="sxs-lookup"><span data-stu-id="71eba-164">System.Byte</span></span>
<span data-ttu-id="71eba-165">Rappresentazione del flusso di byte del contenuto del file recuperato.</span><span class="sxs-lookup"><span data-stu-id="71eba-165">The byte stream representation of the file contents retrieved.</span></span>

### <span data-ttu-id="71eba-166">System. String</span><span class="sxs-lookup"><span data-stu-id="71eba-166">System.String</span></span>
<span data-ttu-id="71eba-167">Rappresentazione di stringa (nella codifica specificata) del contenuto del file recuperato.</span><span class="sxs-lookup"><span data-stu-id="71eba-167">The string representation (in the specified encoding) of the file contents retrieved.</span></span>

## <span data-ttu-id="71eba-168">Note</span><span class="sxs-lookup"><span data-stu-id="71eba-168">NOTES</span></span>

## <span data-ttu-id="71eba-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="71eba-169">RELATED LINKS</span></span>
