---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: D231E9A0-DC1E-411B-A87A-56A8C767F6C5
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/restore-azdatalakestoredeleteditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Restore-AzDataLakeStoreDeletedItem.md
ms.openlocfilehash: 9dcc45f8f082ce59a6082ad71c2084c5df10064c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94022995"
---
# <span data-ttu-id="35347-101">Restore-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="35347-101">Restore-AzDataLakeStoreDeletedItem</span></span>

## <span data-ttu-id="35347-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="35347-102">SYNOPSIS</span></span>
<span data-ttu-id="35347-103">Ripristinare un file o una cartella eliminata in Azure Data Lake.</span><span class="sxs-lookup"><span data-stu-id="35347-103">Restore a deleted file or folder in Azure Data Lake.</span></span>

## <span data-ttu-id="35347-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="35347-104">SYNTAX</span></span>

### <span data-ttu-id="35347-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="35347-105">Default (Default)</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-Path] <String> [-Destination] <String>
 [-Type] <String> [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="35347-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="35347-106">InputObject</span></span>
```
Restore-AzDataLakeStoreDeletedItem [-Account] <String> [-DeletedItem] <DataLakeStoreDeletedItem>
 [-RestoreAction <String>] [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="35347-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="35347-107">DESCRIPTION</span></span>
<span data-ttu-id="35347-108">Il cmdlet **Restore-AzDataLakeStoreDeletedItem** ripristina un file o una cartella eliminata in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="35347-108">The **Restore-AzDataLakeStoreDeletedItem** cmdlet restores a deleted file or folder in Data Lake Store.</span></span> <span data-ttu-id="35347-109">Richiede il percorso dell'elemento eliminato nel cestino restituito da Get-AzDataLakeStoreDeletedItem.</span><span class="sxs-lookup"><span data-stu-id="35347-109">Requires the path of deleted item in trash returned by Get-AzDataLakeStoreDeletedItem.</span></span>
<span data-ttu-id="35347-110">Attenzione: l'eliminazione dei file è un'operazione ottimale.</span><span class="sxs-lookup"><span data-stu-id="35347-110">Caution: Undeleting files is a best effort operation.</span></span> <span data-ttu-id="35347-111">Non sono disponibili garanzie che un file possa essere ripristinato dopo l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="35347-111">There are no guarantees that a file can be restored once it is deleted.</span></span> <span data-ttu-id="35347-112">L'uso di questa API è abilitato tramite whitelist.</span><span class="sxs-lookup"><span data-stu-id="35347-112">The use of this API is enabled via whitelisting.</span></span> <span data-ttu-id="35347-113">Se l'account ADL non è in whitelist, quindi l'uso di questa API genera un'eccezione non implementata.</span><span class="sxs-lookup"><span data-stu-id="35347-113">If your ADL account is not whitelisted, then using this api will throw Not implemented exception.</span></span> <span data-ttu-id="35347-114">Per altre informazioni e assistenza, contattare il supporto tecnico Microsoft.</span><span class="sxs-lookup"><span data-stu-id="35347-114">For further information and assistance please contact Microsoft support.</span></span>

## <span data-ttu-id="35347-115">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="35347-115">EXAMPLES</span></span>

### <span data-ttu-id="35347-116">Esempio 1: ripristinare un file dall'opzione data Lake store using-Force</span><span class="sxs-lookup"><span data-stu-id="35347-116">Example 1: Restore a file from the Data Lake Store using -force option</span></span>
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

## <span data-ttu-id="35347-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="35347-117">PARAMETERS</span></span>

### <span data-ttu-id="35347-118">-Account</span><span class="sxs-lookup"><span data-stu-id="35347-118">-Account</span></span>
<span data-ttu-id="35347-119">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="35347-119">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="35347-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35347-120">-DefaultProfile</span></span>
<span data-ttu-id="35347-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="35347-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35347-122">-DeletedItem</span><span class="sxs-lookup"><span data-stu-id="35347-122">-DeletedItem</span></span>
<span data-ttu-id="35347-123">Oggetto elemento eliminato.</span><span class="sxs-lookup"><span data-stu-id="35347-123">The deleted item object.</span></span>

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

### <span data-ttu-id="35347-124">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="35347-124">-Destination</span></span>
<span data-ttu-id="35347-125">Percorso di destinazione in cui deve essere ripristinato il file o la cartella eliminata.</span><span class="sxs-lookup"><span data-stu-id="35347-125">The destination path to where the deleted file or folder should be restored.</span></span> 

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

### <span data-ttu-id="35347-126">-Force</span><span class="sxs-lookup"><span data-stu-id="35347-126">-Force</span></span>
<span data-ttu-id="35347-127">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="35347-127">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="35347-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="35347-128">-PassThru</span></span>
<span data-ttu-id="35347-129">Restituisce un valore booleano true per Success.</span><span class="sxs-lookup"><span data-stu-id="35347-129">Return boolean true on success.</span></span>

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

### <span data-ttu-id="35347-130">-Path</span><span class="sxs-lookup"><span data-stu-id="35347-130">-Path</span></span>
<span data-ttu-id="35347-131">Percorso del file o della cartella eliminata nel Cestino.</span><span class="sxs-lookup"><span data-stu-id="35347-131">The path of the deleted file or folder in trash.</span></span>

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

### <span data-ttu-id="35347-132">-RestoreAction</span><span class="sxs-lookup"><span data-stu-id="35347-132">-RestoreAction</span></span>
<span data-ttu-id="35347-133">Azione da eseguire in conflitto di nomi di destinazione-"copia" o "Sovrascrivi"</span><span class="sxs-lookup"><span data-stu-id="35347-133">Action to take on destination name conflicts - "copy" or "overwrite"</span></span>

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

### <span data-ttu-id="35347-134">-Digitare</span><span class="sxs-lookup"><span data-stu-id="35347-134">-Type</span></span>
<span data-ttu-id="35347-135">Tipo di voce da ripristinare: "file" o "cartella"</span><span class="sxs-lookup"><span data-stu-id="35347-135">The type of entry being restored - "file" or "folder"</span></span>

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

### <span data-ttu-id="35347-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35347-136">CommonParameters</span></span>
<span data-ttu-id="35347-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35347-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35347-138">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="35347-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35347-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="35347-139">INPUTS</span></span>

### <span data-ttu-id="35347-140">System. String</span><span class="sxs-lookup"><span data-stu-id="35347-140">System.String</span></span>

## <span data-ttu-id="35347-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="35347-141">OUTPUTS</span></span>

### <span data-ttu-id="35347-142">Nessuno</span><span class="sxs-lookup"><span data-stu-id="35347-142">None</span></span>

## <span data-ttu-id="35347-143">Note</span><span class="sxs-lookup"><span data-stu-id="35347-143">NOTES</span></span>

## <span data-ttu-id="35347-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="35347-144">RELATED LINKS</span></span>

[<span data-ttu-id="35347-145">Get-AzDataLakeStoreDeletedItem</span><span class="sxs-lookup"><span data-stu-id="35347-145">Get-AzDataLakeStoreDeletedItem</span></span>](./Get-AzDataLakeStoreDeletedItem.md)