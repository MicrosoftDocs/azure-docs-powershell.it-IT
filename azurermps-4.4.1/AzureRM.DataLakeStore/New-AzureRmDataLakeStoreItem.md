---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/New-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a087c2f7cfd4358e137550aa2e916fa2200d2a2e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520108"
---
# <span data-ttu-id="7160c-101">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-101">New-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="7160c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7160c-102">SYNOPSIS</span></span>
<span data-ttu-id="7160c-103">Crea un nuovo file o una nuova cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7160c-103">Creates a new file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7160c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7160c-104">SYNTAX</span></span>

```
New-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <FileSystemCmdletProviderEncoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7160c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7160c-105">DESCRIPTION</span></span>
<span data-ttu-id="7160c-106">Il cmdlet **New-AzureRmDataLakeStoreItem** crea un nuovo file o una nuova cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7160c-106">The **New-AzureRmDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7160c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7160c-107">EXAMPLES</span></span>

### <span data-ttu-id="7160c-108">Esempio 1: creare un nuovo file e una nuova cartella</span><span class="sxs-lookup"><span data-stu-id="7160c-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="7160c-109">Il primo comando crea il file NewFile.txt per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="7160c-109">The first command creates the file NewFile.txt for the specified account.</span></span>

<span data-ttu-id="7160c-110">Il secondo comando crea la cartella NewFolder nella cartella radice.</span><span class="sxs-lookup"><span data-stu-id="7160c-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="7160c-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7160c-111">PARAMETERS</span></span>

### <span data-ttu-id="7160c-112">-Account</span><span class="sxs-lookup"><span data-stu-id="7160c-112">-Account</span></span>
<span data-ttu-id="7160c-113">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7160c-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7160c-114">-Codifica</span><span class="sxs-lookup"><span data-stu-id="7160c-114">-Encoding</span></span>
<span data-ttu-id="7160c-115">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="7160c-115">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="7160c-116">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7160c-116">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7160c-117">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="7160c-117">Unknown</span></span>
- <span data-ttu-id="7160c-118">Stringa</span><span class="sxs-lookup"><span data-stu-id="7160c-118">String</span></span>
- <span data-ttu-id="7160c-119">Unicode</span><span class="sxs-lookup"><span data-stu-id="7160c-119">Unicode</span></span>
- <span data-ttu-id="7160c-120">Byte</span><span class="sxs-lookup"><span data-stu-id="7160c-120">Byte</span></span>
- <span data-ttu-id="7160c-121">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="7160c-121">BigEndianUnicode</span></span>
- <span data-ttu-id="7160c-122">UTF8</span><span class="sxs-lookup"><span data-stu-id="7160c-122">UTF8</span></span>
- <span data-ttu-id="7160c-123">UTF7</span><span class="sxs-lookup"><span data-stu-id="7160c-123">UTF7</span></span>
- <span data-ttu-id="7160c-124">ASCII</span><span class="sxs-lookup"><span data-stu-id="7160c-124">Ascii</span></span>
- <span data-ttu-id="7160c-125">Predefinita</span><span class="sxs-lookup"><span data-stu-id="7160c-125">Default</span></span>
- <span data-ttu-id="7160c-126">OEM</span><span class="sxs-lookup"><span data-stu-id="7160c-126">Oem</span></span>
- <span data-ttu-id="7160c-127">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="7160c-127">BigEndianUTF32</span></span>

```yaml
Type: Microsoft.PowerShell.Commands.FileSystemCmdletProviderEncoding
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7160c-128">-Cartella</span><span class="sxs-lookup"><span data-stu-id="7160c-128">-Folder</span></span>
<span data-ttu-id="7160c-129">Indica che questa operazione crea una cartella.</span><span class="sxs-lookup"><span data-stu-id="7160c-129">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="7160c-130">-Force</span><span class="sxs-lookup"><span data-stu-id="7160c-130">-Force</span></span>
<span data-ttu-id="7160c-131">Indica che questa operazione può sovrascrivere l'elemento di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="7160c-131">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="7160c-132">-Path</span><span class="sxs-lookup"><span data-stu-id="7160c-132">-Path</span></span>
<span data-ttu-id="7160c-133">Specifica il percorso dello Store Data Lake dell'elemento da creare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="7160c-133">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7160c-134">-Valore</span><span class="sxs-lookup"><span data-stu-id="7160c-134">-Value</span></span>
<span data-ttu-id="7160c-135">Specifica il contenuto da aggiungere all'elemento creato.</span><span class="sxs-lookup"><span data-stu-id="7160c-135">Specifies the content to add to the item you create.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7160c-136">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7160c-136">-Confirm</span></span>
<span data-ttu-id="7160c-137">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7160c-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7160c-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7160c-138">-WhatIf</span></span>
<span data-ttu-id="7160c-139">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7160c-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7160c-140">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7160c-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7160c-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7160c-141">-DefaultProfile</span></span>
<span data-ttu-id="7160c-142">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7160c-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7160c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7160c-143">CommonParameters</span></span>
<span data-ttu-id="7160c-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7160c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7160c-145">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7160c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7160c-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7160c-146">INPUTS</span></span>

### <span data-ttu-id="7160c-147">Oggetto</span><span class="sxs-lookup"><span data-stu-id="7160c-147">Object</span></span>
<span data-ttu-id="7160c-148">Il parametro "value" accetta il valore di tipo "Object" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="7160c-148">Parameter 'Value' accepts value of type 'Object' from the pipeline</span></span>

## <span data-ttu-id="7160c-149">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7160c-149">OUTPUTS</span></span>

### <span data-ttu-id="7160c-150">stringa</span><span class="sxs-lookup"><span data-stu-id="7160c-150">string</span></span>
<span data-ttu-id="7160c-151">Percorso completo per il file o la cartella creata.</span><span class="sxs-lookup"><span data-stu-id="7160c-151">The full path to the created file or folder.</span></span>

## <span data-ttu-id="7160c-152">Note</span><span class="sxs-lookup"><span data-stu-id="7160c-152">NOTES</span></span>

## <span data-ttu-id="7160c-153">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7160c-153">RELATED LINKS</span></span>

[<span data-ttu-id="7160c-154">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-154">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7160c-155">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-155">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7160c-156">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-156">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7160c-157">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-157">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7160c-158">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-158">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="7160c-159">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7160c-159">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


