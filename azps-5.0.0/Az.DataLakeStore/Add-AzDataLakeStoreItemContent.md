---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: B008028D-27FC-4469-BE71-54F7218C068B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/add-azdatalakestoreitemcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Add-AzDataLakeStoreItemContent.md
ms.openlocfilehash: 3cf411e75e2a3ec430f13354015d5b6e271c840c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297942"
---
# <span data-ttu-id="56f77-101">Add-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="56f77-101">Add-AzDataLakeStoreItemContent</span></span>

## <span data-ttu-id="56f77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56f77-102">SYNOPSIS</span></span>
<span data-ttu-id="56f77-103">Aggiunge contenuto a un elemento in uno Store di data Lake.</span><span class="sxs-lookup"><span data-stu-id="56f77-103">Adds content to an item in a Data Lake Store.</span></span>

## <span data-ttu-id="56f77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56f77-104">SYNTAX</span></span>

```
Add-AzDataLakeStoreItemContent [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Value] <Object>
 [[-Encoding] <Encoding>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56f77-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56f77-105">DESCRIPTION</span></span>
<span data-ttu-id="56f77-106">Il cmdlet **Add-AzDataLakeStoreItemContent** aggiunge contenuto a un elemento in uno Store di Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="56f77-106">The **Add-AzDataLakeStoreItemContent** cmdlet adds content to an item in an Azure Data Lake Store.</span></span>

## <span data-ttu-id="56f77-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56f77-107">EXAMPLES</span></span>

### <span data-ttu-id="56f77-108">Esempio 1: aggiungere contenuto a un file</span><span class="sxs-lookup"><span data-stu-id="56f77-108">Example 1: Add content to a file</span></span>
```
PS C:\>Add-AzDataLakeStoreItemContent -AccountName "ContosoADLS" -Path /abc/myFile.txt -Value "My content here"
```

<span data-ttu-id="56f77-109">Questo comando aggiunge contenuto al file myFile.txt.</span><span class="sxs-lookup"><span data-stu-id="56f77-109">This command adds content to the file myFile.txt.</span></span>

## <span data-ttu-id="56f77-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56f77-110">PARAMETERS</span></span>

### <span data-ttu-id="56f77-111">-Account</span><span class="sxs-lookup"><span data-stu-id="56f77-111">-Account</span></span>
<span data-ttu-id="56f77-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="56f77-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="56f77-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56f77-113">-DefaultProfile</span></span>
<span data-ttu-id="56f77-114">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="56f77-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="56f77-115">-Codifica</span><span class="sxs-lookup"><span data-stu-id="56f77-115">-Encoding</span></span>
<span data-ttu-id="56f77-116">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="56f77-116">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="56f77-117">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="56f77-117">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="56f77-118">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="56f77-118">Unknown</span></span>
- <span data-ttu-id="56f77-119">Stringa</span><span class="sxs-lookup"><span data-stu-id="56f77-119">String</span></span>
- <span data-ttu-id="56f77-120">Unicode</span><span class="sxs-lookup"><span data-stu-id="56f77-120">Unicode</span></span>
- <span data-ttu-id="56f77-121">Byte</span><span class="sxs-lookup"><span data-stu-id="56f77-121">Byte</span></span>
- <span data-ttu-id="56f77-122">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="56f77-122">BigEndianUnicode</span></span>
- <span data-ttu-id="56f77-123">UTF8</span><span class="sxs-lookup"><span data-stu-id="56f77-123">UTF8</span></span>
- <span data-ttu-id="56f77-124">UTF7</span><span class="sxs-lookup"><span data-stu-id="56f77-124">UTF7</span></span>
- <span data-ttu-id="56f77-125">ASCII</span><span class="sxs-lookup"><span data-stu-id="56f77-125">Ascii</span></span>
- <span data-ttu-id="56f77-126">Predefinita</span><span class="sxs-lookup"><span data-stu-id="56f77-126">Default</span></span>
- <span data-ttu-id="56f77-127">OEM</span><span class="sxs-lookup"><span data-stu-id="56f77-127">Oem</span></span>
- <span data-ttu-id="56f77-128">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="56f77-128">BigEndianUTF32</span></span>

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

### <span data-ttu-id="56f77-129">-Path</span><span class="sxs-lookup"><span data-stu-id="56f77-129">-Path</span></span>
<span data-ttu-id="56f77-130">Specifica il percorso dello Store Data Lake dell'elemento da modificare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="56f77-130">Specifies the Data Lake Store path of the item to modify, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="56f77-131">-Valore</span><span class="sxs-lookup"><span data-stu-id="56f77-131">-Value</span></span>
<span data-ttu-id="56f77-132">Specifica il contenuto da aggiungere all'elemento.</span><span class="sxs-lookup"><span data-stu-id="56f77-132">Specifies the content to add to the item.</span></span>

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

### <span data-ttu-id="56f77-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56f77-133">CommonParameters</span></span>
<span data-ttu-id="56f77-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56f77-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56f77-135">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56f77-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56f77-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56f77-136">INPUTS</span></span>

### <span data-ttu-id="56f77-137">System. String</span><span class="sxs-lookup"><span data-stu-id="56f77-137">System.String</span></span>

### <span data-ttu-id="56f77-138">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="56f77-138">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="56f77-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="56f77-139">System.Object</span></span>

### <span data-ttu-id="56f77-140">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="56f77-140">System.Text.Encoding</span></span>

## <span data-ttu-id="56f77-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56f77-141">OUTPUTS</span></span>

### <span data-ttu-id="56f77-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="56f77-142">System.Boolean</span></span>

## <span data-ttu-id="56f77-143">Note</span><span class="sxs-lookup"><span data-stu-id="56f77-143">NOTES</span></span>

## <span data-ttu-id="56f77-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56f77-144">RELATED LINKS</span></span>

[<span data-ttu-id="56f77-145">Get-AzDataLakeStoreItemContent</span><span class="sxs-lookup"><span data-stu-id="56f77-145">Get-AzDataLakeStoreItemContent</span></span>](./Get-AzDataLakeStoreItemContent.md)


