---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 40477ad0635f1b832e7d95e459b27102dc68f8db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508179"
---
# <span data-ttu-id="16541-101">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-101">Remove-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="16541-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="16541-102">SYNOPSIS</span></span>
<span data-ttu-id="16541-103">Elimina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16541-103">Deletes a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16541-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="16541-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Clean]
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16541-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="16541-105">DESCRIPTION</span></span>
<span data-ttu-id="16541-106">Il cmdlet **Remove-AzureRmDataLakeStoreItem** Elimina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16541-106">The **Remove-AzureRmDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="16541-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="16541-107">EXAMPLES</span></span>

### <span data-ttu-id="16541-108">Esempio 1: rimuovere più elementi</span><span class="sxs-lookup"><span data-stu-id="16541-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="16541-109">Questo comando rimuove i file File01.txt e File.csv da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16541-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="16541-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="16541-110">PARAMETERS</span></span>

### <span data-ttu-id="16541-111">-Account</span><span class="sxs-lookup"><span data-stu-id="16541-111">-Account</span></span>
<span data-ttu-id="16541-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="16541-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="16541-113">-Pulisci</span><span class="sxs-lookup"><span data-stu-id="16541-113">-Clean</span></span>
<span data-ttu-id="16541-114">Indica che l'utente vuole rimuovere tutto il contenuto della cartella, ma non la cartella stessa</span><span class="sxs-lookup"><span data-stu-id="16541-114">Indicates the user wants to remove all of the contents of the folder, but not the folder itself</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16541-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16541-115">-DefaultProfile</span></span>
<span data-ttu-id="16541-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="16541-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16541-117">-Force</span><span class="sxs-lookup"><span data-stu-id="16541-117">-Force</span></span>
<span data-ttu-id="16541-118">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="16541-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16541-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="16541-119">-PassThru</span></span>
<span data-ttu-id="16541-120">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="16541-120">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="16541-121">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="16541-121">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16541-122">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="16541-122">-Paths</span></span>
<span data-ttu-id="16541-123">Specifica una matrice di percorsi di archiviazione dei dati del lago per i file da rimuovere, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="16541-123">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16541-124">-Recurse</span><span class="sxs-lookup"><span data-stu-id="16541-124">-Recurse</span></span>
<span data-ttu-id="16541-125">Indica che questa operazione Elimina tutti gli elementi nella cartella di destinazione, incluse le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="16541-125">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>
<span data-ttu-id="16541-126">A meno che non specifichi il parametro *Clean* , viene eliminata anche la cartella di destinazione.</span><span class="sxs-lookup"><span data-stu-id="16541-126">Unless you specify the *Clean* parameter, the target folder is also deleted.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16541-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="16541-127">-Confirm</span></span>
<span data-ttu-id="16541-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16541-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16541-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16541-129">-WhatIf</span></span>
<span data-ttu-id="16541-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16541-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16541-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="16541-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="16541-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16541-132">CommonParameters</span></span>
<span data-ttu-id="16541-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16541-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16541-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16541-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16541-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="16541-135">INPUTS</span></span>

### <span data-ttu-id="16541-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="16541-136">None</span></span>
<span data-ttu-id="16541-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="16541-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="16541-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="16541-138">OUTPUTS</span></span>

### <span data-ttu-id="16541-139">bool</span><span class="sxs-lookup"><span data-stu-id="16541-139">bool</span></span>
<span data-ttu-id="16541-140">Se PassThru è specificato, restituisce il risultato dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="16541-140">If PassThru is specified, returns the result of the operation.</span></span>

## <span data-ttu-id="16541-141">Note</span><span class="sxs-lookup"><span data-stu-id="16541-141">NOTES</span></span>

## <span data-ttu-id="16541-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="16541-142">RELATED LINKS</span></span>

[<span data-ttu-id="16541-143">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-143">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="16541-144">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-144">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="16541-145">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-145">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="16541-146">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-146">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="16541-147">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-147">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="16541-148">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="16541-148">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


