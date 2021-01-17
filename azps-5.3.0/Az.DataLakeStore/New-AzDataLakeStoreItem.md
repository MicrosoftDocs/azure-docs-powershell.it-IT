---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: A8222AB8-0003-4AC6-8114-294ABE8054CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/new-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/New-AzDataLakeStoreItem.md
ms.openlocfilehash: ab752ec2201c9b64a9656153f29a947b7a722819
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473571"
---
# <span data-ttu-id="7f833-101">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-101">New-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="7f833-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7f833-102">SYNOPSIS</span></span>
<span data-ttu-id="7f833-103">Crea un nuovo file o una nuova cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f833-103">Creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7f833-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7f833-104">SYNTAX</span></span>

```
New-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-Value] <Object>]
 [[-Encoding] <Encoding>] [-Folder] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7f833-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7f833-105">DESCRIPTION</span></span>
<span data-ttu-id="7f833-106">Il cmdlet **New-AzDataLakeStoreItem** crea un nuovo file o una nuova cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f833-106">The **New-AzDataLakeStoreItem** cmdlet creates a new file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="7f833-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7f833-107">EXAMPLES</span></span>

### <span data-ttu-id="7f833-108">Esempio 1: creare un nuovo file e una nuova cartella</span><span class="sxs-lookup"><span data-stu-id="7f833-108">Example 1: Create a new file and a new folder</span></span>
```
PS C:\>New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFile.txt"
PS C:\> New-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/NewFolder" -Folder
```

<span data-ttu-id="7f833-109">Il primo comando crea il file NewFile.txt per l'account specificato.</span><span class="sxs-lookup"><span data-stu-id="7f833-109">The first command creates the file NewFile.txt for the specified account.</span></span>
<span data-ttu-id="7f833-110">Il secondo comando crea la cartella NewFolder nella cartella radice.</span><span class="sxs-lookup"><span data-stu-id="7f833-110">The second command creates the folder NewFolder at the root folder.</span></span>

## <span data-ttu-id="7f833-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7f833-111">PARAMETERS</span></span>

### <span data-ttu-id="7f833-112">-Account</span><span class="sxs-lookup"><span data-stu-id="7f833-112">-Account</span></span>
<span data-ttu-id="7f833-113">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="7f833-113">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="7f833-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f833-114">-DefaultProfile</span></span>
<span data-ttu-id="7f833-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7f833-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f833-116">-Codifica</span><span class="sxs-lookup"><span data-stu-id="7f833-116">-Encoding</span></span>
<span data-ttu-id="7f833-117">Specifica la codifica per l'elemento da creare.</span><span class="sxs-lookup"><span data-stu-id="7f833-117">Specifies the encoding for the item to create.</span></span>
<span data-ttu-id="7f833-118">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="7f833-118">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="7f833-119">Sconosciuto</span><span class="sxs-lookup"><span data-stu-id="7f833-119">Unknown</span></span>
- <span data-ttu-id="7f833-120">Stringa</span><span class="sxs-lookup"><span data-stu-id="7f833-120">String</span></span>
- <span data-ttu-id="7f833-121">Unicode</span><span class="sxs-lookup"><span data-stu-id="7f833-121">Unicode</span></span>
- <span data-ttu-id="7f833-122">Byte</span><span class="sxs-lookup"><span data-stu-id="7f833-122">Byte</span></span>
- <span data-ttu-id="7f833-123">BigEndianUnicode</span><span class="sxs-lookup"><span data-stu-id="7f833-123">BigEndianUnicode</span></span>
- <span data-ttu-id="7f833-124">UTF8</span><span class="sxs-lookup"><span data-stu-id="7f833-124">UTF8</span></span>
- <span data-ttu-id="7f833-125">UTF7</span><span class="sxs-lookup"><span data-stu-id="7f833-125">UTF7</span></span>
- <span data-ttu-id="7f833-126">ASCII</span><span class="sxs-lookup"><span data-stu-id="7f833-126">Ascii</span></span>
- <span data-ttu-id="7f833-127">Predefinita</span><span class="sxs-lookup"><span data-stu-id="7f833-127">Default</span></span>
- <span data-ttu-id="7f833-128">OEM</span><span class="sxs-lookup"><span data-stu-id="7f833-128">Oem</span></span>
- <span data-ttu-id="7f833-129">BigEndianUTF32</span><span class="sxs-lookup"><span data-stu-id="7f833-129">BigEndianUTF32</span></span>

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

### <span data-ttu-id="7f833-130">-Cartella</span><span class="sxs-lookup"><span data-stu-id="7f833-130">-Folder</span></span>
<span data-ttu-id="7f833-131">Indica che questa operazione crea una cartella.</span><span class="sxs-lookup"><span data-stu-id="7f833-131">Indicates that this operation creates a folder.</span></span>

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

### <span data-ttu-id="7f833-132">-Force</span><span class="sxs-lookup"><span data-stu-id="7f833-132">-Force</span></span>
<span data-ttu-id="7f833-133">Indica che questa operazione può sovrascrivere l'elemento di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="7f833-133">Indicates that this operation can overwrite the destination item if it already exists.</span></span>

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

### <span data-ttu-id="7f833-134">-Path</span><span class="sxs-lookup"><span data-stu-id="7f833-134">-Path</span></span>
<span data-ttu-id="7f833-135">Specifica il percorso dello Store Data Lake dell'elemento da creare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="7f833-135">Specifies the Data Lake Store path of the item to create, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="7f833-136">-Valore</span><span class="sxs-lookup"><span data-stu-id="7f833-136">-Value</span></span>
<span data-ttu-id="7f833-137">Specifica il contenuto da aggiungere all'elemento creato.</span><span class="sxs-lookup"><span data-stu-id="7f833-137">Specifies the content to add to the item you create.</span></span>

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

### <span data-ttu-id="7f833-138">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7f833-138">-Confirm</span></span>
<span data-ttu-id="7f833-139">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7f833-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f833-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f833-140">-WhatIf</span></span>
<span data-ttu-id="7f833-141">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f833-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f833-142">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7f833-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f833-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f833-143">CommonParameters</span></span>
<span data-ttu-id="7f833-144">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7f833-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f833-145">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f833-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f833-146">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7f833-146">INPUTS</span></span>

### <span data-ttu-id="7f833-147">System. String</span><span class="sxs-lookup"><span data-stu-id="7f833-147">System.String</span></span>

### <span data-ttu-id="7f833-148">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="7f833-148">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="7f833-149">System. Object</span><span class="sxs-lookup"><span data-stu-id="7f833-149">System.Object</span></span>

### <span data-ttu-id="7f833-150">System. Text. Encoding</span><span class="sxs-lookup"><span data-stu-id="7f833-150">System.Text.Encoding</span></span>

### <span data-ttu-id="7f833-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7f833-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7f833-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7f833-152">OUTPUTS</span></span>

### <span data-ttu-id="7f833-153">System. String</span><span class="sxs-lookup"><span data-stu-id="7f833-153">System.String</span></span>

## <span data-ttu-id="7f833-154">Note</span><span class="sxs-lookup"><span data-stu-id="7f833-154">NOTES</span></span>

## <span data-ttu-id="7f833-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7f833-155">RELATED LINKS</span></span>

[<span data-ttu-id="7f833-156">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-156">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f833-157">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-157">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f833-158">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-158">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f833-159">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-159">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f833-160">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-160">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="7f833-161">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="7f833-161">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


