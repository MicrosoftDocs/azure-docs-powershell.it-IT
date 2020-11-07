---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 00CCA9B8-7C57-4FC0-9BD1-5FC16010E820
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/move-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Move-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 5e6fb437833db3f4278335f67693d084c2d6d95b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686112"
---
# <span data-ttu-id="05330-101">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-101">Move-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="05330-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="05330-102">SYNOPSIS</span></span>
<span data-ttu-id="05330-103">Consente di spostare o rinominare un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="05330-103">Moves or renames a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05330-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="05330-104">SYNTAX</span></span>

```
Move-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05330-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="05330-105">DESCRIPTION</span></span>
<span data-ttu-id="05330-106">Il cmdlet **Move-AzureRmDataLakeStoreItem** sposta o rinomina un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="05330-106">The **Move-AzureRmDataLakeStoreItem** cmdlet moves or renames a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="05330-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="05330-107">EXAMPLES</span></span>

### <span data-ttu-id="05330-108">Esempio 1: modificare e rinominare un elemento</span><span class="sxs-lookup"><span data-stu-id="05330-108">Example 1: Move and rename an item</span></span>
```
PS C:\>Move-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/Original/Path/File.txt" -Destination "/New/Path/RenamedFile.txt"
```

<span data-ttu-id="05330-109">Questo comando Rinomina l'elemento File.txt in RenamedFile.txt e lo sposta in una cartella diversa.</span><span class="sxs-lookup"><span data-stu-id="05330-109">This command renames the item File.txt to RenamedFile.txt and moves it to a different folder.</span></span>

## <span data-ttu-id="05330-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="05330-110">PARAMETERS</span></span>

### <span data-ttu-id="05330-111">-Account</span><span class="sxs-lookup"><span data-stu-id="05330-111">-Account</span></span>
<span data-ttu-id="05330-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="05330-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="05330-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05330-113">-DefaultProfile</span></span>
<span data-ttu-id="05330-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="05330-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05330-115">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="05330-115">-Destination</span></span>
<span data-ttu-id="05330-116">Specifica il percorso dello Store Data Lake a cui trasferire l'elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="05330-116">Specifies the Data Lake Store path to which to move the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05330-117">-Force</span><span class="sxs-lookup"><span data-stu-id="05330-117">-Force</span></span>
<span data-ttu-id="05330-118">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="05330-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="05330-119">-Path</span><span class="sxs-lookup"><span data-stu-id="05330-119">-Path</span></span>
<span data-ttu-id="05330-120">Specifica il percorso dello Store Data Lake dell'elemento da trasferire o rinominare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="05330-120">Specifies the Data Lake Store path of the item to move or rename, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05330-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="05330-121">-Confirm</span></span>
<span data-ttu-id="05330-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05330-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="05330-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05330-123">-WhatIf</span></span>
<span data-ttu-id="05330-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05330-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05330-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="05330-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="05330-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05330-126">CommonParameters</span></span>
<span data-ttu-id="05330-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05330-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05330-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05330-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05330-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="05330-129">INPUTS</span></span>

### <span data-ttu-id="05330-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="05330-130">None</span></span>
<span data-ttu-id="05330-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="05330-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="05330-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="05330-132">OUTPUTS</span></span>

### <span data-ttu-id="05330-133">stringa</span><span class="sxs-lookup"><span data-stu-id="05330-133">string</span></span>
<span data-ttu-id="05330-134">Percorso completo per il file o la cartella spostata.</span><span class="sxs-lookup"><span data-stu-id="05330-134">The full path to the moved file or folder.</span></span>

## <span data-ttu-id="05330-135">Note</span><span class="sxs-lookup"><span data-stu-id="05330-135">NOTES</span></span>

## <span data-ttu-id="05330-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="05330-136">RELATED LINKS</span></span>

[<span data-ttu-id="05330-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="05330-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="05330-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="05330-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="05330-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="05330-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="05330-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


