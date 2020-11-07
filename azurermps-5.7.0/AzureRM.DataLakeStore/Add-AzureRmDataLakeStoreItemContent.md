---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: f272d7c57a1543f916d828d6324dd23f5780ccad
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686118"
---
# <span data-ttu-id="e02e9-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="e02e9-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="e02e9-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e02e9-102">SYNOPSIS</span></span>
<span data-ttu-id="e02e9-103">Aggiunge contenuto a un elemento in uno Store di data Lake.</span><span class="sxs-lookup"><span data-stu-id="e02e9-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e02e9-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e02e9-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e02e9-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e02e9-105">DESCRIPTION</span></span>
<span data-ttu-id="e02e9-106">Il cmdlet **Add-AzureRmDataLakeStoreItemContent** aggiunge contenuto a un elemento in uno Store di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="e02e9-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="e02e9-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e02e9-107">EXAMPLES</span></span>

### <span data-ttu-id="e02e9-108">Esempio 1: aggiungere contenuto a un file</span><span class="sxs-lookup"><span data-stu-id="e02e9-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="e02e9-109">Questo comando aggiunge contenuto al file myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="e02e9-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="e02e9-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e02e9-110">PARAMETERS</span></span>

### <span data-ttu-id="e02e9-111">-Account</span><span class="sxs-lookup"><span data-stu-id="e02e9-111">-Account</span></span>
<span data-ttu-id="e02e9-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="e02e9-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e02e9-113">-DefaultProfile</span></span>
<span data-ttu-id="e02e9-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e02e9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e02e9-115">-Codifica</span><span class="sxs-lookup"><span data-stu-id="e02e9-115">-Encoding</span></span>
<span data-ttu-id="e02e9-116">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="e02e9-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="e02e9-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="e02e9-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e02e9-118">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="e02e9-118">Unknown</span></span>
- <span data-ttu-id="e02e9-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="e02e9-119">String</span></span>
- <span data-ttu-id="e02e9-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="e02e9-120">Unicode</span></span>
- <span data-ttu-id="e02e9-121">Byte</span><span class="sxs-lookup"><span data-stu-id="e02e9-121">Byte</span></span>
- <span data-ttu-id="e02e9-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="e02e9-122">BigEndianUnicode</span></span>
- <span data-ttu-id="e02e9-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="e02e9-123">UTF8</span></span>
- <span data-ttu-id="e02e9-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="e02e9-124">UTF7</span></span>
- <span data-ttu-id="e02e9-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="e02e9-125">Ascii</span></span>
- <span data-ttu-id="e02e9-126">Predefinita</span><span class="sxs-lookup"><span data-stu-id="e02e9-126">Default</span></span>
- <span data-ttu-id="e02e9-127">OEM</span><span class="sxs-lookup"><span data-stu-id="e02e9-127">Oem</span></span>
- <span data-ttu-id="e02e9-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="e02e9-128">BigEndianUTF32</span></span>

```yaml
Type: FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02e9-129">-Path</span><span class="sxs-lookup"><span data-stu-id="e02e9-129">-Path</span></span>
<span data-ttu-id="e02e9-130">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="e02e9-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e02e9-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="e02e9-131">-Value</span></span>
<span data-ttu-id="e02e9-132">Specifica il contenuto da aggiungere all'elemento.</span><span class="sxs-lookup"><span data-stu-id="e02e9-132">Specifies the content to add to the item.</span></span>

```yaml
Type: Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e02e9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e02e9-133">CommonParameters</span></span>
<span data-ttu-id="e02e9-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e02e9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e02e9-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e02e9-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e02e9-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e02e9-136">INPUTS</span></span>

### <span data-ttu-id="e02e9-137">Oggetto</span><span class="sxs-lookup"><span data-stu-id="e02e9-137">Object</span></span>
<span data-ttu-id="e02e9-138">Il parametro "value" accetta il valore di tipo "Object" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="e02e9-138">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="e02e9-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e02e9-139">OUTPUTS</span></span>

### <span data-ttu-id="e02e9-140">bool</span><span class="sxs-lookup"><span data-stu-id="e02e9-140">bool</span></span>
<span data-ttu-id="e02e9-141">Restituisce vero per successo.</span><span class="sxs-lookup"><span data-stu-id="e02e9-141">Returns true on success.</span></span>

## <span data-ttu-id="e02e9-142">Note</span><span class="sxs-lookup"><span data-stu-id="e02e9-142">NOTES</span></span>

## <span data-ttu-id="e02e9-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e02e9-143">RELATED LINKS</span></span>

[<span data-ttu-id="e02e9-144">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="e02e9-144">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


