---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Join-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: 1f09d1da5ab4ad88ff16be56affaa582ad1e24d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519592"
---
# <span data-ttu-id="56d76-101">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-101">Join-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="56d76-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="56d76-102">SYNOPSIS</span></span>
<span data-ttu-id="56d76-103">Unisce uno o più file per creare un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="56d76-103">Joins one or more files to create one file in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56d76-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="56d76-104">SYNTAX</span></span>

```
Join-AzureRmDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56d76-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="56d76-105">DESCRIPTION</span></span>
<span data-ttu-id="56d76-106">Il cmdlet **join-AzureRmDataLakeStoreItem** unisce uno o più file per creare un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="56d76-106">The **Join-AzureRmDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="56d76-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="56d76-107">EXAMPLES</span></span>

### <span data-ttu-id="56d76-108">Esempio 1: unire due elementi</span><span class="sxs-lookup"><span data-stu-id="56d76-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="56d76-109">Questo comando unisce File01.txt e File02.txt per creare il file CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="56d76-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="56d76-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="56d76-110">PARAMETERS</span></span>

### <span data-ttu-id="56d76-111">-Account</span><span class="sxs-lookup"><span data-stu-id="56d76-111">-Account</span></span>
<span data-ttu-id="56d76-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="56d76-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="56d76-113">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="56d76-113">-Destination</span></span>
<span data-ttu-id="56d76-114">Specifica il percorso dello Store Data Lake per l'elemento Unito, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="56d76-114">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d76-115">-Force</span><span class="sxs-lookup"><span data-stu-id="56d76-115">-Force</span></span>
<span data-ttu-id="56d76-116">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="56d76-116">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="56d76-117">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="56d76-117">-Paths</span></span>
<span data-ttu-id="56d76-118">Specifica una matrice di percorsi per l'archiviazione dei dati di un lago nei file da combinare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="56d76-118">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]
Parameter Sets: (All)
Aliases: Path

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56d76-119">-Confermare</span><span class="sxs-lookup"><span data-stu-id="56d76-119">-Confirm</span></span>
<span data-ttu-id="56d76-120">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="56d76-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56d76-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56d76-121">-WhatIf</span></span>
<span data-ttu-id="56d76-122">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56d76-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56d76-123">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="56d76-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56d76-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56d76-124">-DefaultProfile</span></span>
<span data-ttu-id="56d76-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="56d76-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56d76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56d76-126">CommonParameters</span></span>
<span data-ttu-id="56d76-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56d76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56d76-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56d76-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56d76-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="56d76-129">INPUTS</span></span>

## <span data-ttu-id="56d76-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="56d76-130">OUTPUTS</span></span>

### <span data-ttu-id="56d76-131">stringa</span><span class="sxs-lookup"><span data-stu-id="56d76-131">string</span></span>
<span data-ttu-id="56d76-132">Il percorso completo del file risultante dai file Uniti.</span><span class="sxs-lookup"><span data-stu-id="56d76-132">The full path to the resulting file from the joined files.</span></span>

## <span data-ttu-id="56d76-133">Note</span><span class="sxs-lookup"><span data-stu-id="56d76-133">NOTES</span></span>

## <span data-ttu-id="56d76-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="56d76-134">RELATED LINKS</span></span>

[<span data-ttu-id="56d76-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="56d76-136">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-136">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="56d76-137">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-137">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="56d76-138">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-138">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="56d76-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="56d76-140">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="56d76-140">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


