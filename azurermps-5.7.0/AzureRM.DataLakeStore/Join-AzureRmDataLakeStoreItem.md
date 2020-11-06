---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/join-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: c321c605977e09f119d19e5c4ced44261c3de0cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512616"
---
# <span data-ttu-id="67b81-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="67b81-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="67b81-102">SYNOPSIS</span></span>
<span data-ttu-id="67b81-103">Unisce uno o più file per creare un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67b81-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67b81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="67b81-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67b81-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="67b81-105">DESCRIPTION</span></span>
<span data-ttu-id="67b81-106">Il cmdlet **join-AzureRmDataLakeStoreItem** unisce uno o più file per creare un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67b81-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="67b81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="67b81-107">EXAMPLES</span></span>

### <span data-ttu-id="67b81-108">Esempio 1: unire due elementi</span><span class="sxs-lookup"><span data-stu-id="67b81-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="67b81-109">Questo comando unisce File01.txt e File02.txt per creare il file CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="67b81-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="67b81-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="67b81-110">PARAMETERS</span></span>

### <span data-ttu-id="67b81-111">-Account</span><span class="sxs-lookup"><span data-stu-id="67b81-111">-Account</span></span>
<span data-ttu-id="67b81-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="67b81-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="67b81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67b81-113">-DefaultProfile</span></span>
<span data-ttu-id="67b81-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="67b81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="67b81-115">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="67b81-115">-Destination</span></span>
<span data-ttu-id="67b81-116">Specifica il percorso dello Store Data Lake per l'elemento Unito, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="67b81-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="67b81-117">-Force</span><span class="sxs-lookup"><span data-stu-id="67b81-117">-Force</span></span>
<span data-ttu-id="67b81-118">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="67b81-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="67b81-119">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="67b81-119">-Paths</span></span>
<span data-ttu-id="67b81-120">Specifica una matrice di percorsi per l'archiviazione dei dati di un lago nei file da combinare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="67b81-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67b81-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="67b81-121">-Confirm</span></span>
<span data-ttu-id="67b81-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67b81-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67b81-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67b81-123">-WhatIf</span></span>
<span data-ttu-id="67b81-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67b81-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67b81-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="67b81-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67b81-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67b81-126">CommonParameters</span></span>
<span data-ttu-id="67b81-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67b81-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67b81-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67b81-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67b81-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="67b81-129">INPUTS</span></span>

### <span data-ttu-id="67b81-130">Nessuno</span><span class="sxs-lookup"><span data-stu-id="67b81-130">None</span></span>
<span data-ttu-id="67b81-131">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="67b81-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67b81-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="67b81-132">OUTPUTS</span></span>

### <span data-ttu-id="67b81-133">stringa</span><span class="sxs-lookup"><span data-stu-id="67b81-133">string</span></span>
<span data-ttu-id="67b81-134">Il percorso completo del file risultante dai file Uniti.</span><span class="sxs-lookup"><span data-stu-id="67b81-134">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="67b81-135">Note</span><span class="sxs-lookup"><span data-stu-id="67b81-135">NOTES</span></span>

## <span data-ttu-id="67b81-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="67b81-136">RELATED LINKS</span></span>

[<span data-ttu-id="67b81-137">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-137">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="67b81-138">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-138">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="67b81-139">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-139">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="67b81-140">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-140">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="67b81-141">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-141">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="67b81-142">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="67b81-142">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


