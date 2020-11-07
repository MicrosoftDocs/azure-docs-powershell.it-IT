---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: d674376325c103f6e3e8e0368f0db6c64422c97b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93684516"
---
# <span data-ttu-id="cbd77-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="cbd77-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="cbd77-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cbd77-102">SYNOPSIS</span></span>
<span data-ttu-id="cbd77-103">Ripristinare un file o una cartella eliminata in Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="cbd77-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="cbd77-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cbd77-104">SYNTAX</span></span>

### <span data-ttu-id="cbd77-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cbd77-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="cbd77-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="cbd77-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cbd77-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cbd77-107">DESCRIPTION</span></span>
<span data-ttu-id="cbd77-108">Il cmdlet **Restore-AzDataLakeStoreDeletedItem** ripristina un file o una cartella eliminata in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cbd77-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="cbd77-109">Richiede il percorso dell'elemento eliminato nel cestino retunred da Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="cbd77-109">Requires the path of deleted item in trash retunred by Get-AzDataLakeStoreDeletedItem.</span></span>

## <span data-ttu-id="cbd77-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cbd77-110">EXAMPLES</span></span>

### <span data-ttu-id="cbd77-111">Esempio 1: ripristinare un file dall'opzione data Lake store using-Force</span><span class="sxs-lookup"><span data-stu-id="cbd77-111">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
```
PS > Restore-AzDataLakeStoreDeletedItem -Account ml1ptrashtest -Path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -Destination adl://ml1ptrashtest.azuredatalake.com/test0/file_1230 -Type "file" -Force
PS >

### Example 2: Restore a file from Data Lake Store using user confirmation

PS > restore-azdatalakestoredeleteditem -account ml1ptrashtest -path 927e8fb1-a287-4353-b50e-3b4a39ae4088 -destination adl://ml1ptrashtest.azuredatalake.com/test4/file_1115 -type file

Restore user data ?
From - 927e8fb1-a287-4353-b50e-3b4a39ae4088
To   - adl://ml1ptrashtest.azuredatalake.com/test4/file_1115
Type - file
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y
PS >
```

## <span data-ttu-id="cbd77-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cbd77-112">PARAMETERS</span></span>

### <span data-ttu-id="cbd77-113">-Account</span><span class="sxs-lookup"><span data-stu-id="cbd77-113">-Account</span></span>
<span data-ttu-id="cbd77-114">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cbd77-114">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cbd77-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cbd77-115">-DefaultProfile</span></span>
<span data-ttu-id="cbd77-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cbd77-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cbd77-117">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="cbd77-117">-DeletedItem</span></span>
<span data-ttu-id="cbd77-118">Oggetto elemento eliminato.</span><span class="sxs-lookup"><span data-stu-id="cbd77-118">The deleted item object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreDeletedItem
Parameter Sets: InputObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-119">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="cbd77-119">-Destination</span></span>
<span data-ttu-id="cbd77-120">Percorso di destinazione in cui deve essere ripristinato il file o la cartella eliminata.</span><span class="sxs-lookup"><span data-stu-id="cbd77-120">The destination path to where the deleted file or folder should be restored.</span></span> 

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-121">-Force</span><span class="sxs-lookup"><span data-stu-id="cbd77-121">-Force</span></span>
<span data-ttu-id="cbd77-122">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cbd77-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cbd77-123">-PassThru</span></span>
<span data-ttu-id="cbd77-124">Restituisce un valore booleano true per Success.</span><span class="sxs-lookup"><span data-stu-id="cbd77-124">Return boolean true on success.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-125">-Path</span><span class="sxs-lookup"><span data-stu-id="cbd77-125">-Path</span></span>
<span data-ttu-id="cbd77-126">Percorso del file o della cartella eliminata nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="cbd77-126">The path of the deleted file or folder in trash.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-127">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="cbd77-127">-RestoreAction</span></span>
<span data-ttu-id="cbd77-128">Azione da eseguire in conflitto di nomi di destinazione-"copia" o "Sovrascrivi"</span><span class="sxs-lookup"><span data-stu-id="cbd77-128">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-129">-Digitare</span><span class="sxs-lookup"><span data-stu-id="cbd77-129">-Type</span></span>
<span data-ttu-id="cbd77-130">Tipo di voce da ripristinare: "file" o "cartella"</span><span class="sxs-lookup"><span data-stu-id="cbd77-130">The type of entry being restored - "file" or "folder"</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cbd77-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cbd77-131">CommonParameters</span></span>
<span data-ttu-id="cbd77-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cbd77-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cbd77-133">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cbd77-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cbd77-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cbd77-134">INPUTS</span></span>

### <span data-ttu-id="cbd77-135">System. String</span><span class="sxs-lookup"><span data-stu-id="cbd77-135">System.String</span></span>

## <span data-ttu-id="cbd77-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cbd77-136">OUTPUTS</span></span>

### <span data-ttu-id="cbd77-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="cbd77-137">None</span></span>

## <span data-ttu-id="cbd77-138">Note</span><span class="sxs-lookup"><span data-stu-id="cbd77-138">NOTES</span></span>

## <span data-ttu-id="cbd77-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cbd77-139">RELATED LINKS</span></span>

[<span data-ttu-id="cbd77-140">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="cbd77-140">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)