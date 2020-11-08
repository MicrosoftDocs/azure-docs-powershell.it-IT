---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189078"
---
# <span data-ttu-id="8519f-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="8519f-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8519f-102">SYNOPSIS</span></span>
<span data-ttu-id="8519f-103">Crea un nuovo file o una nuova cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8519f-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8519f-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8519f-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8519f-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8519f-105">DESCRIPTION</span></span>
<span data-ttu-id="8519f-106">Il cmdlet **New-AzDataLakeStoreItem** crea un nuovo file o una nuova cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8519f-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8519f-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8519f-107">EXAMPLES</span></span>

### <span data-ttu-id="8519f-108">Esempio 1: creare un nuovo file e una nuova cartella</span><span class="sxs-lookup"><span data-stu-id="8519f-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="8519f-109">Il primo comando crea il file NewFile.txt per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="8519f-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="8519f-110">Il secondo comando crea la cartella NewFolder nella cartella radice.</span><span class="sxs-lookup"><span data-stu-id="8519f-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="8519f-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8519f-111">PARAMETERS</span></span>

### <span data-ttu-id="8519f-112">-Account</span><span class="sxs-lookup"><span data-stu-id="8519f-112">-Account</span></span>
<span data-ttu-id="8519f-113">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8519f-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8519f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8519f-114">-DefaultProfile</span></span>
<span data-ttu-id="8519f-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8519f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8519f-116">-Codifica</span><span class="sxs-lookup"><span data-stu-id="8519f-116">-Encoding</span></span>
<span data-ttu-id="8519f-117">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="8519f-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="8519f-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="8519f-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8519f-119">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="8519f-119">Unknown</span></span>
- <span data-ttu-id="8519f-120">Stringa</span><span class="sxs-lookup"><span data-stu-id="8519f-120">String</span></span>
- <span data-ttu-id="8519f-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="8519f-121">Unicode</span></span>
- <span data-ttu-id="8519f-122">Byte</span><span class="sxs-lookup"><span data-stu-id="8519f-122">Byte</span></span>
- <span data-ttu-id="8519f-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="8519f-123">BigEndianUnicode</span></span>
- <span data-ttu-id="8519f-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="8519f-124">UTF8</span></span>
- <span data-ttu-id="8519f-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="8519f-125">UTF7</span></span>
- <span data-ttu-id="8519f-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="8519f-126">Ascii</span></span>
- <span data-ttu-id="8519f-127">Predefinita</span><span class="sxs-lookup"><span data-stu-id="8519f-127">Default</span></span>
- <span data-ttu-id="8519f-128">OEM</span><span class="sxs-lookup"><span data-stu-id="8519f-128">Oem</span></span>
- <span data-ttu-id="8519f-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="8519f-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="8519f-130">-Cartella</span><span class="sxs-lookup"><span data-stu-id="8519f-130">-Folder</span></span>
<span data-ttu-id="8519f-131">Indica che questa operazione crea una cartella.</span><span class="sxs-lookup"><span data-stu-id="8519f-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="8519f-132">-Force</span><span class="sxs-lookup"><span data-stu-id="8519f-132">-Force</span></span>
<span data-ttu-id="8519f-133">Indica che questa operazione può sovrascrivere l'elemento di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="8519f-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="8519f-134">-Path</span><span class="sxs-lookup"><span data-stu-id="8519f-134">-Path</span></span>
<span data-ttu-id="8519f-135">Specifica il percorso dello Store Data Lake dell'elemento da creare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="8519f-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8519f-136">-Valore</span><span class="sxs-lookup"><span data-stu-id="8519f-136">-Value</span></span>
<span data-ttu-id="8519f-137">Specifica il contenuto da aggiungere all'elemento creato.</span><span class="sxs-lookup"><span data-stu-id="8519f-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="8519f-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="8519f-138">-Confirm</span></span>
<span data-ttu-id="8519f-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8519f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8519f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8519f-140">-WhatIf</span></span>
<span data-ttu-id="8519f-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8519f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8519f-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8519f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8519f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8519f-143">CommonParameters</span></span>
<span data-ttu-id="8519f-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8519f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8519f-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8519f-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8519f-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8519f-146">INPUTS</span></span>

### <span data-ttu-id="8519f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="8519f-147">System.String</span></span>

### <span data-ttu-id="8519f-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8519f-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="8519f-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="8519f-149">System.Object</span></span>

### <span data-ttu-id="8519f-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="8519f-150">System.Text.Encoding</span></span>

### <span data-ttu-id="8519f-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8519f-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8519f-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8519f-152">OUTPUTS</span></span>

### <span data-ttu-id="8519f-153">System. String</span><span class="sxs-lookup"><span data-stu-id="8519f-153">System.String</span></span>

## <span data-ttu-id="8519f-154">Note</span><span class="sxs-lookup"><span data-stu-id="8519f-154">NOTES</span></span>

## <span data-ttu-id="8519f-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8519f-155">RELATED LINKS</span></span>

[<span data-ttu-id="8519f-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="8519f-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="8519f-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="8519f-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="8519f-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="8519f-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8519f-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


