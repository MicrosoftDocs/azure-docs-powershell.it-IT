---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/add-azurermdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Add-AzureRmDataLakeStoreItemContent.md
ms.openlocfilehash: ed931444940b86c04e027eb88da9266c7af20206
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93518735"
---
# <span data-ttu-id="7382f-101">Add-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="7382f-101">Add-AzureRmDataLakeStoreItemContent</span></span>

## <span data-ttu-id="7382f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7382f-102">SYNOPSIS</span></span>
<span data-ttu-id="7382f-103">Aggiunge contenuto a un elemento in uno Store di data Lake.</span><span class="sxs-lookup"><span data-stu-id="7382f-103">Adds content to an item in a Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7382f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7382f-104">SYNTAX</span></span>

```
Add-AzureRmDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7382f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7382f-105">DESCRIPTION</span></span>
<span data-ttu-id="7382f-106">Il cmdlet **Add-AzureRmDataLakeStoreItemContent** aggiunge contenuto a un elemento in uno Store di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="7382f-106">The **Add-AzureRmDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="7382f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7382f-107">EXAMPLES</span></span>

### <span data-ttu-id="7382f-108">Esempio 1: aggiungere contenuto a un file</span><span class="sxs-lookup"><span data-stu-id="7382f-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzureRmDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="7382f-109">Questo comando aggiunge contenuto al file myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="7382f-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="7382f-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7382f-110">PARAMETERS</span></span>

### <span data-ttu-id="7382f-111">-Account</span><span class="sxs-lookup"><span data-stu-id="7382f-111">-Account</span></span>
<span data-ttu-id="7382f-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7382f-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7382f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7382f-113">-DefaultProfile</span></span>
<span data-ttu-id="7382f-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="7382f-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7382f-115">-Codifica</span><span class="sxs-lookup"><span data-stu-id="7382f-115">-Encoding</span></span>
<span data-ttu-id="7382f-116">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="7382f-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="7382f-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7382f-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7382f-118">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="7382f-118">Unknown</span></span>
- <span data-ttu-id="7382f-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="7382f-119">String</span></span>
- <span data-ttu-id="7382f-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="7382f-120">Unicode</span></span>
- <span data-ttu-id="7382f-121">Byte</span><span class="sxs-lookup"><span data-stu-id="7382f-121">Byte</span></span>
- <span data-ttu-id="7382f-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="7382f-122">BigEndianUnicode</span></span>
- <span data-ttu-id="7382f-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="7382f-123">UTF8</span></span>
- <span data-ttu-id="7382f-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="7382f-124">UTF7</span></span>
- <span data-ttu-id="7382f-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="7382f-125">Ascii</span></span>
- <span data-ttu-id="7382f-126">Predefinita</span><span class="sxs-lookup"><span data-stu-id="7382f-126">Default</span></span>
- <span data-ttu-id="7382f-127">OEM</span><span class="sxs-lookup"><span data-stu-id="7382f-127">Oem</span></span>
- <span data-ttu-id="7382f-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="7382f-128">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, String, Unicode, Byte, BigEndianUnicode, UTF8, UTF7, UTF32, Ascii, Default, Oem, BigEndianUTF32

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7382f-129">-Path</span><span class="sxs-lookup"><span data-stu-id="7382f-129">-Path</span></span>
<span data-ttu-id="7382f-130">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="7382f-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7382f-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="7382f-131">-Value</span></span>
<span data-ttu-id="7382f-132">Specifica il contenuto da aggiungere all'elemento.</span><span class="sxs-lookup"><span data-stu-id="7382f-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="7382f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7382f-133">CommonParameters</span></span>
<span data-ttu-id="7382f-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7382f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7382f-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7382f-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7382f-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7382f-136">INPUTS</span></span>

### <span data-ttu-id="7382f-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7382f-137">System.String</span></span>

### <span data-ttu-id="7382f-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7382f-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7382f-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="7382f-139">System.Object</span></span>

### <span data-ttu-id="7382f-140">Microsoft. Azure. Commands. DataLakeStore. Models. FileSystemCmdletProviderEncoding</span><span class="sxs-lookup"><span data-stu-id="7382f-140">Microsoft.Azure.Commands.DataLakeStore.Models.FileSystemCmdletProviderEncoding</span></span>

## <span data-ttu-id="7382f-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7382f-141">OUTPUTS</span></span>

### <span data-ttu-id="7382f-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7382f-142">System.Boolean</span></span>

## <span data-ttu-id="7382f-143">Note</span><span class="sxs-lookup"><span data-stu-id="7382f-143">NOTES</span></span>

## <span data-ttu-id="7382f-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7382f-144">RELATED LINKS</span></span>

[<span data-ttu-id="7382f-145">Get-AzureRmDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="7382f-145">Get-AzureRmDataLakeStoreItemContent</span></span>](./Get-AzureRmDataLakeStoreItemContent.md)


