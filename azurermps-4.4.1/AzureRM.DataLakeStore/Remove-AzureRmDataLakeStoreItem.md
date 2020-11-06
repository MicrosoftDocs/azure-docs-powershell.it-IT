---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: da26deb246fc90a1b83b63c47560dd5912616d62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520534"
---
# <span data-ttu-id="31b91-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="31b91-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="31b91-102">SYNOPSIS</span></span>
<span data-ttu-id="31b91-103">Elimina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31b91-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b91-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="31b91-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31b91-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="31b91-105">DESCRIPTION</span></span>
<span data-ttu-id="31b91-106">Il cmdlet **Remove-AzureRmDataLakeStoreItem** Elimina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31b91-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="31b91-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="31b91-107">EXAMPLES</span></span>

### <span data-ttu-id="31b91-108">Esempio 1: rimuovere più elementi</span><span class="sxs-lookup"><span data-stu-id="31b91-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="31b91-109">Questo comando rimuove i file File01.txt e File.csv da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31b91-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="31b91-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="31b91-110">PARAMETERS</span></span>

### <span data-ttu-id="31b91-111">-Account</span><span class="sxs-lookup"><span data-stu-id="31b91-111">-Account</span></span>
<span data-ttu-id="31b91-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31b91-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="31b91-113">-Pulisci</span><span class="sxs-lookup"><span data-stu-id="31b91-113">-Clean</span></span>
<span data-ttu-id="31b91-114">Indica che questa operazione rimuove tutto il contenuto della cartella di destinazione e mantiene la cartella.</span><span class="sxs-lookup"><span data-stu-id="31b91-114">Indicates that this operation removes all of the contents of the target folder and retains the folder.</span></span>
<span data-ttu-id="31b91-115">Usa questo parametro con il parametro *recurse* .</span><span class="sxs-lookup"><span data-stu-id="31b91-115">Use this parameter with the *Recurse* parameter.</span></span>

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

### <span data-ttu-id="31b91-116">-Force</span><span class="sxs-lookup"><span data-stu-id="31b91-116">-Force</span></span>
<span data-ttu-id="31b91-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="31b91-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="31b91-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31b91-118">-PassThru</span></span>
<span data-ttu-id="31b91-119">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="31b91-119">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="31b91-120">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="31b91-120">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b91-121">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="31b91-121">-Paths</span></span>
<span data-ttu-id="31b91-122">Specifica una matrice di percorsi di archiviazione dei dati del lago per i file da rimuovere, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="31b91-122">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b91-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="31b91-123">-Recurse</span></span>
<span data-ttu-id="31b91-124">Indica che questa operazione Elimina tutti gli elementi nella cartella di destinazione, incluse le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="31b91-124">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="31b91-125">A meno che non specifichi il parametro *Clean* , viene eliminata anche la cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="31b91-125">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31b91-126">-Confermare</span><span class="sxs-lookup"><span data-stu-id="31b91-126">-Confirm</span></span>
<span data-ttu-id="31b91-127">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31b91-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31b91-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31b91-128">-WhatIf</span></span>
<span data-ttu-id="31b91-129">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31b91-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31b91-130">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="31b91-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31b91-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b91-131">-DefaultProfile</span></span>
<span data-ttu-id="31b91-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="31b91-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b91-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b91-133">CommonParameters</span></span>
<span data-ttu-id="31b91-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31b91-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b91-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b91-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b91-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="31b91-136">INPUTS</span></span>

## <span data-ttu-id="31b91-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="31b91-137">OUTPUTS</span></span>

### <span data-ttu-id="31b91-138">bool</span><span class="sxs-lookup"><span data-stu-id="31b91-138">bool</span></span>
<span data-ttu-id="31b91-139">Se PassThru è specificato, restituisce il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="31b91-139">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="31b91-140">Note</span><span class="sxs-lookup"><span data-stu-id="31b91-140">NOTES</span></span>

## <span data-ttu-id="31b91-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="31b91-141">RELATED LINKS</span></span>

[<span data-ttu-id="31b91-142">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-142">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31b91-143">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-143">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31b91-144">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-144">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31b91-145">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-145">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31b91-146">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-146">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="31b91-147">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="31b91-147">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


