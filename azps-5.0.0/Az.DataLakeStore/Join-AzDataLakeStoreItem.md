---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94297816"
---
# <span data-ttu-id="6b8da-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="6b8da-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6b8da-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8da-103">Unisce uno o più file per creare un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b8da-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="6b8da-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6b8da-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6b8da-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6b8da-105">DESCRIPTION</span></span>
<span data-ttu-id="6b8da-106">Il cmdlet **join-AzDataLakeStoreItem** unisce uno o più file per creare un file in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b8da-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="6b8da-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6b8da-107">EXAMPLES</span></span>

### <span data-ttu-id="6b8da-108">Esempio 1: unire due elementi</span><span class="sxs-lookup"><span data-stu-id="6b8da-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="6b8da-109">Questo comando unisce File01.txt e File02.txt per creare il file CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="6b8da-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="6b8da-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6b8da-110">PARAMETERS</span></span>

### <span data-ttu-id="6b8da-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6b8da-111">-Account</span></span>
<span data-ttu-id="6b8da-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6b8da-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6b8da-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8da-113">-DefaultProfile</span></span>
<span data-ttu-id="6b8da-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8da-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b8da-115">-Destinazione</span><span class="sxs-lookup"><span data-stu-id="6b8da-115">-Destination</span></span>
<span data-ttu-id="6b8da-116">Specifica il percorso dello Store Data Lake per l'elemento Unito, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="6b8da-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6b8da-117">-Force</span><span class="sxs-lookup"><span data-stu-id="6b8da-117">-Force</span></span>
<span data-ttu-id="6b8da-118">Indica che questa operazione può sovrascrivere il file di destinazione se esiste già.</span><span class="sxs-lookup"><span data-stu-id="6b8da-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="6b8da-119">-Percorsi</span><span class="sxs-lookup"><span data-stu-id="6b8da-119">-Paths</span></span>
<span data-ttu-id="6b8da-120">Specifica una matrice di percorsi per l'archiviazione dei dati di un lago nei file da combinare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="6b8da-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6b8da-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6b8da-121">-Confirm</span></span>
<span data-ttu-id="6b8da-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8da-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b8da-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b8da-123">-WhatIf</span></span>
<span data-ttu-id="6b8da-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b8da-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b8da-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6b8da-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b8da-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8da-126">CommonParameters</span></span>
<span data-ttu-id="6b8da-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8da-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8da-128">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6b8da-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8da-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6b8da-129">INPUTS</span></span>

### <span data-ttu-id="6b8da-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6b8da-130">System.String</span></span>

### <span data-ttu-id="6b8da-131">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance []</span><span class="sxs-lookup"><span data-stu-id="6b8da-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="6b8da-132">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6b8da-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6b8da-133">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6b8da-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6b8da-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6b8da-134">OUTPUTS</span></span>

### <span data-ttu-id="6b8da-135">System. String</span><span class="sxs-lookup"><span data-stu-id="6b8da-135">System.String</span></span>

## <span data-ttu-id="6b8da-136">Note</span><span class="sxs-lookup"><span data-stu-id="6b8da-136">NOTES</span></span>

## <span data-ttu-id="6b8da-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6b8da-137">RELATED LINKS</span></span>

[<span data-ttu-id="6b8da-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b8da-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b8da-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b8da-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b8da-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="6b8da-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="6b8da-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


