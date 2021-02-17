---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 4E9EA2E9-4BE2-4530-BC2B-D369C016CD8C
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/join-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Join-AzDataLakeStoreItem.md
ms.openlocfilehash: 1d361149109b654cf3e7fa45e133b9daff84c21c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188590"
---
# <span data-ttu-id="d7c48-101">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-101">Join-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="d7c48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7c48-102">SYNOPSIS</span></span>
<span data-ttu-id="d7c48-103">Unisce uno o più file per crearne uno in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7c48-103">Joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d7c48-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d7c48-104">SYNTAX</span></span>

```
Join-AzDataLakeStoreItem [-Account] <String> [-Paths] <DataLakeStorePathInstance[]>
 [-Destination] <DataLakeStorePathInstance> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d7c48-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="d7c48-105">DESCRIPTION</span></span>
<span data-ttu-id="d7c48-106">Il cmdlet **Join-AzDataLakeStoreItem** unisce uno o più file per creare un file in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7c48-106">The **Join-AzDataLakeStoreItem** cmdlet joins one or more files to create one file in Data Lake Store.</span></span>

## <span data-ttu-id="d7c48-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d7c48-107">EXAMPLES</span></span>

### <span data-ttu-id="d7c48-108">Esempio 1: Unire due elementi</span><span class="sxs-lookup"><span data-stu-id="d7c48-108">Example 1: Join two items</span></span>
```
PS C:\>Join-AzDataLakeStoreItem -AccountName "ContosoADL" -Paths "/MyFiles/File01.txt","/MyFiles/File02.txt" -Destination "/MyFiles/CombinedFile.txt"
```

<span data-ttu-id="d7c48-109">Questo comando unisce File01.txt e File02.txt per creare il file CombinedFile.txt.</span><span class="sxs-lookup"><span data-stu-id="d7c48-109">This command joins File01.txt and File02.txt to create the file CombinedFile.txt.</span></span>

## <span data-ttu-id="d7c48-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7c48-110">PARAMETERS</span></span>

### <span data-ttu-id="d7c48-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d7c48-111">-Account</span></span>
<span data-ttu-id="d7c48-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d7c48-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d7c48-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7c48-113">-DefaultProfile</span></span>
<span data-ttu-id="d7c48-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d7c48-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d7c48-115">-Destination</span><span class="sxs-lookup"><span data-stu-id="d7c48-115">-Destination</span></span>
<span data-ttu-id="d7c48-116">Specifica il percorso Data Lake Store per l'elemento unito in join, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d7c48-116">Specifies the Data Lake Store path for the joined item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d7c48-117">-Force</span><span class="sxs-lookup"><span data-stu-id="d7c48-117">-Force</span></span>
<span data-ttu-id="d7c48-118">Indica che questa operazione può sovrascrivere il file di destinazione, se esiste già.</span><span class="sxs-lookup"><span data-stu-id="d7c48-118">Indicates that this operation can overwrite the destination file if it already exists.</span></span>

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

### <span data-ttu-id="d7c48-119">-Paths</span><span class="sxs-lookup"><span data-stu-id="d7c48-119">-Paths</span></span>
<span data-ttu-id="d7c48-120">Specifica una matrice di percorsi Data Lake Store dei file da combinare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d7c48-120">Specifies an array of Data Lake Store paths of the files to combine, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d7c48-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d7c48-121">-Confirm</span></span>
<span data-ttu-id="d7c48-122">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7c48-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7c48-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7c48-123">-WhatIf</span></span>
<span data-ttu-id="d7c48-124">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7c48-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7c48-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d7c48-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7c48-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7c48-126">CommonParameters</span></span>
<span data-ttu-id="d7c48-127">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7c48-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7c48-128">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d7c48-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7c48-129">INPUT</span><span class="sxs-lookup"><span data-stu-id="d7c48-129">INPUTS</span></span>

### <span data-ttu-id="d7c48-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d7c48-130">System.String</span></span>

### <span data-ttu-id="d7c48-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span><span class="sxs-lookup"><span data-stu-id="d7c48-131">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance[]</span></span>

### <span data-ttu-id="d7c48-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d7c48-132">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="d7c48-133">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d7c48-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7c48-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d7c48-134">OUTPUTS</span></span>

### <span data-ttu-id="d7c48-135">System.String</span><span class="sxs-lookup"><span data-stu-id="d7c48-135">System.String</span></span>

## <span data-ttu-id="d7c48-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="d7c48-136">NOTES</span></span>

## <span data-ttu-id="d7c48-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d7c48-137">RELATED LINKS</span></span>

[<span data-ttu-id="d7c48-138">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-138">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="d7c48-139">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-139">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="d7c48-140">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-140">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="d7c48-141">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-141">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="d7c48-142">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-142">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="d7c48-143">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d7c48-143">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


