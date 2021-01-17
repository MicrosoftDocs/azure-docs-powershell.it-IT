---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 164DC871-0F0C-4E71-A37A-2B85CE65C2C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/remove-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Remove-AzDataLakeStoreItem.md
ms.openlocfilehash: 5f927bd9ef64cc22eda7669e9b0d60127cf503ac
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473559"
---
# <span data-ttu-id="81c45-101">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-101">Remove-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="81c45-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="81c45-102">SYNOPSIS</span></span>
<span data-ttu-id="81c45-103">Elimina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81c45-103">Deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="81c45-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="81c45-104">SYNTAX</span></span>

```
Remove-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]> [-Recurse] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="81c45-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="81c45-105">DESCRIPTION</span></span>
<span data-ttu-id="81c45-106">Il cmdlet **Remove-AzDataLakeStoreItem** Elimina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81c45-106">The **Remove-AzDataLakeStoreItem** cmdlet deletes a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="81c45-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="81c45-107">EXAMPLES</span></span>

### <span data-ttu-id="81c45-108">Esempio 1: rimuovere più elementi</span><span class="sxs-lookup"><span data-stu-id="81c45-108">Example 1: Remove multiple items</span></span>
```
PS C:\>Remove-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/File01.txt","/MyFiles/File.csv"
```

<span data-ttu-id="81c45-109">Questo comando rimuove i file File01.txt e File.csv da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81c45-109">This command removes the files File01.txt and File.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="81c45-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="81c45-110">PARAMETERS</span></span>

### <span data-ttu-id="81c45-111">-Account</span><span class="sxs-lookup"><span data-stu-id="81c45-111">-Account</span></span>
<span data-ttu-id="81c45-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="81c45-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="81c45-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81c45-113">-DefaultProfile</span></span>
<span data-ttu-id="81c45-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="81c45-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81c45-115">-Force</span><span class="sxs-lookup"><span data-stu-id="81c45-115">-Force</span></span>
<span data-ttu-id="81c45-116">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="81c45-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="81c45-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="81c45-117">-PassThru</span></span>
<span data-ttu-id="81c45-118">Restituisce un oggetto che rappresenta l'elemento con cui si sta lavorando.</span><span class="sxs-lookup"><span data-stu-id="81c45-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="81c45-119">Per impostazione predefinita, questo cmdlet non genera alcun output.</span><span class="sxs-lookup"><span data-stu-id="81c45-119">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="81c45-120">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="81c45-120">-Paths</span></span>
<span data-ttu-id="81c45-121">Specifica una matrice di percorsi di archiviazione dei dati del lago per i file da rimuovere, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="81c45-121">Specifies an array of Data Lake Store paths of the files to remove, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="81c45-122">-Recurse</span><span class="sxs-lookup"><span data-stu-id="81c45-122">-Recurse</span></span>
<span data-ttu-id="81c45-123">Indica che questa operazione Elimina tutti gli elementi nella cartella di destinazione, incluse le sottocartelle.</span><span class="sxs-lookup"><span data-stu-id="81c45-123">Indicates that this operation deletes all items in the target folder, including subfolders.</span></span>

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

### <span data-ttu-id="81c45-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="81c45-124">-Confirm</span></span>
<span data-ttu-id="81c45-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="81c45-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="81c45-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="81c45-126">-WhatIf</span></span>
<span data-ttu-id="81c45-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81c45-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="81c45-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="81c45-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="81c45-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c45-129">CommonParameters</span></span>
<span data-ttu-id="81c45-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81c45-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c45-131">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c45-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c45-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="81c45-132">INPUTS</span></span>

### <span data-ttu-id="81c45-133">System. String</span><span class="sxs-lookup"><span data-stu-id="81c45-133">System.String</span></span>

### <span data-ttu-id="81c45-134">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="81c45-134">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="81c45-135">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="81c45-135">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="81c45-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="81c45-136">OUTPUTS</span></span>

### <span data-ttu-id="81c45-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="81c45-137">System.Boolean</span></span>

## <span data-ttu-id="81c45-138">Note</span><span class="sxs-lookup"><span data-stu-id="81c45-138">NOTES</span></span>

## <span data-ttu-id="81c45-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="81c45-139">RELATED LINKS</span></span>

[<span data-ttu-id="81c45-140">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-140">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="81c45-141">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-141">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="81c45-142">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-142">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="81c45-143">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-143">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="81c45-144">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-144">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="81c45-145">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="81c45-145">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


