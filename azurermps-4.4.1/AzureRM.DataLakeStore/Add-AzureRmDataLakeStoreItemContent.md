---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: 4ce79044793bbecc76d72fab015166ccc3d8fba6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93510652"
---
# <span data-ttu-id="5f31b-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5f31b-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="5f31b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5f31b-102">SYNOPSIS</span></span>
<span data-ttu-id="5f31b-103">Aggiunge contenuto a un elemento in uno Store di data Lake.</span><span class="sxs-lookup"><span data-stu-id="5f31b-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f31b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5f31b-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5f31b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5f31b-105">DESCRIPTION</span></span>
<span data-ttu-id="5f31b-106">Il cmdlet **Add-AzureRmDataLakeStoreItemContent** aggiunge contenuto a un elemento in uno Store di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="5f31b-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="5f31b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5f31b-107">EXAMPLES</span></span>

### <span data-ttu-id="5f31b-108">Esempio 1: aggiungere contenuto a un file</span><span class="sxs-lookup"><span data-stu-id="5f31b-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="5f31b-109">Questo comando aggiunge contenuto al file myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="5f31b-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="5f31b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5f31b-110">PARAMETERS</span></span>

### <span data-ttu-id="5f31b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="5f31b-111">-Account</span></span>
<span data-ttu-id="5f31b-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="5f31b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="5f31b-113">-Codifica</span><span class="sxs-lookup"><span data-stu-id="5f31b-113">-Encoding</span></span>
<span data-ttu-id="5f31b-114">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="5f31b-114">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="5f31b-115">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="5f31b-115">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5f31b-116">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="5f31b-116">Unknown</span></span>
- <span data-ttu-id="5f31b-117">Stringa</span><span class="sxs-lookup"><span data-stu-id="5f31b-117">String</span></span>
- <span data-ttu-id="5f31b-118">Unicode</span><span class="sxs-lookup"><span data-stu-id="5f31b-118">Unicode</span></span>
- <span data-ttu-id="5f31b-119">Byte</span><span class="sxs-lookup"><span data-stu-id="5f31b-119">Byte</span></span>
- <span data-ttu-id="5f31b-120">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="5f31b-120">BigEndianUnicode</span></span>
- <span data-ttu-id="5f31b-121">UTF8</span><span class="sxs-lookup"><span data-stu-id="5f31b-121">UTF8</span></span>
- <span data-ttu-id="5f31b-122">UTF7</span><span class="sxs-lookup"><span data-stu-id="5f31b-122">UTF7</span></span>
- <span data-ttu-id="5f31b-123">ASCII</span><span class="sxs-lookup"><span data-stu-id="5f31b-123">Ascii</span></span>
- <span data-ttu-id="5f31b-124">Predefinita</span><span class="sxs-lookup"><span data-stu-id="5f31b-124">Default</span></span>
- <span data-ttu-id="5f31b-125">OEM</span><span class="sxs-lookup"><span data-stu-id="5f31b-125">Oem</span></span>
- <span data-ttu-id="5f31b-126">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="5f31b-126">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f31b-127">-Path</span><span class="sxs-lookup"><span data-stu-id="5f31b-127">-Path</span></span>
<span data-ttu-id="5f31b-128">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="5f31b-128">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="5f31b-129">-Valore</span><span class="sxs-lookup"><span data-stu-id="5f31b-129">-Value</span></span>
<span data-ttu-id="5f31b-130">Specifica il contenuto da aggiungere all'elemento.</span><span class="sxs-lookup"><span data-stu-id="5f31b-130">Specifies the content to add to the item.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5f31b-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f31b-131">-DefaultProfile</span></span>
<span data-ttu-id="5f31b-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="5f31b-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f31b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f31b-133">CommonParameters</span></span>
<span data-ttu-id="5f31b-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f31b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f31b-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f31b-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f31b-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5f31b-136">INPUTS</span></span>

### <span data-ttu-id="5f31b-137">Oggetto</span><span class="sxs-lookup"><span data-stu-id="5f31b-137">Object</span></span>
<span data-ttu-id="5f31b-138">Il parametro "value" accetta il valore di tipo "Object" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5f31b-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="5f31b-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5f31b-139">OUTPUTS</span></span>

### <span data-ttu-id="5f31b-140">bool</span><span class="sxs-lookup"><span data-stu-id="5f31b-140">bool</span></span>
<span data-ttu-id="5f31b-141">Restituisce vero per successo.</span><span class="sxs-lookup"><span data-stu-id="5f31b-141">Returns true on success.</span></span>

## <span data-ttu-id="5f31b-142">Note</span><span class="sxs-lookup"><span data-stu-id="5f31b-142">NOTES</span></span>

## <span data-ttu-id="5f31b-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5f31b-143">RELATED LINKS</span></span>

[<span data-ttu-id="5f31b-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="5f31b-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


