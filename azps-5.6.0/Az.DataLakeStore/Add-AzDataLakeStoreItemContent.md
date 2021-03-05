---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: aa2fe76f221ce412c0e47f7a43b1dba551131f45
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994390"
---
# <span data-ttu-id="4c69d-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="4c69d-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="4c69d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c69d-102">SYNOPSIS</span></span>
<span data-ttu-id="4c69d-103">Aggiunge contenuto a un elemento in un Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c69d-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="4c69d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c69d-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c69d-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="4c69d-105">DESCRIPTION</span></span>
<span data-ttu-id="4c69d-106">Il cmdlet **Add-AzDataLakeStoreItemContent** aggiunge contenuto a un elemento in un Azure Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c69d-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="4c69d-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c69d-107">EXAMPLES</span></span>

### <span data-ttu-id="4c69d-108">Esempio 1: Aggiungere contenuto a un file</span><span class="sxs-lookup"><span data-stu-id="4c69d-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="4c69d-109">Questo comando aggiunge contenuto al file myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="4c69d-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="4c69d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c69d-110">PARAMETERS</span></span>

### <span data-ttu-id="4c69d-111">-Account</span><span class="sxs-lookup"><span data-stu-id="4c69d-111">-Account</span></span>
<span data-ttu-id="4c69d-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="4c69d-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="4c69d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c69d-113">-DefaultProfile</span></span>
<span data-ttu-id="4c69d-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="4c69d-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c69d-115">-Encoding</span><span class="sxs-lookup"><span data-stu-id="4c69d-115">-Encoding</span></span>
<span data-ttu-id="4c69d-116">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="4c69d-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="4c69d-117">I valori accettabili per questo parametro sono:</span><span class="sxs-lookup"><span data-stu-id="4c69d-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4c69d-118">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="4c69d-118">Unknown</span></span>
- <span data-ttu-id="4c69d-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="4c69d-119">String</span></span>
- <span data-ttu-id="4c69d-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="4c69d-120">Unicode</span></span>
- <span data-ttu-id="4c69d-121">Byte</span><span class="sxs-lookup"><span data-stu-id="4c69d-121">Byte</span></span>
- <span data-ttu-id="4c69d-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="4c69d-122">BigEndianUnicode</span></span>
- <span data-ttu-id="4c69d-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="4c69d-123">UTF8</span></span>
- <span data-ttu-id="4c69d-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="4c69d-124">UTF7</span></span>
- <span data-ttu-id="4c69d-125">Ascii</span><span class="sxs-lookup"><span data-stu-id="4c69d-125">Ascii</span></span>
- <span data-ttu-id="4c69d-126">Impostazione predefinita</span><span class="sxs-lookup"><span data-stu-id="4c69d-126">Default</span></span>
- <span data-ttu-id="4c69d-127">Oem</span><span class="sxs-lookup"><span data-stu-id="4c69d-127">Oem</span></span>
- <span data-ttu-id="4c69d-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="4c69d-128">BigEndianUTF32</span></span>

```yaml
Type: System.Text.Encoding
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c69d-129">-Path</span><span class="sxs-lookup"><span data-stu-id="4c69d-129">-Path</span></span>
<span data-ttu-id="4c69d-130">Specifica il percorso Data Lake Store dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="4c69d-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="4c69d-131">-Value</span><span class="sxs-lookup"><span data-stu-id="4c69d-131">-Value</span></span>
<span data-ttu-id="4c69d-132">Specifica il contenuto da aggiungere all'elemento.</span><span class="sxs-lookup"><span data-stu-id="4c69d-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="4c69d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c69d-133">CommonParameters</span></span>
<span data-ttu-id="4c69d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c69d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c69d-135">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c69d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c69d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="4c69d-136">INPUTS</span></span>

### <span data-ttu-id="4c69d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4c69d-137">System.String</span></span>

### <span data-ttu-id="4c69d-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="4c69d-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="4c69d-139">System.Object</span><span class="sxs-lookup"><span data-stu-id="4c69d-139">System.Object</span></span>

### <span data-ttu-id="4c69d-140">System.Text.Encoding</span><span class="sxs-lookup"><span data-stu-id="4c69d-140">System.Text.Encoding</span></span>

## <span data-ttu-id="4c69d-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c69d-141">OUTPUTS</span></span>

### <span data-ttu-id="4c69d-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c69d-142">System.Boolean</span></span>

## <span data-ttu-id="4c69d-143">NOTE</span><span class="sxs-lookup"><span data-stu-id="4c69d-143">NOTES</span></span>

## <span data-ttu-id="4c69d-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c69d-144">RELATED LINKS</span></span>

[<span data-ttu-id="4c69d-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="4c69d-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


