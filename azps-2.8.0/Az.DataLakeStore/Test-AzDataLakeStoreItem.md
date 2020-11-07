---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: c79e8c225fbbc901d9c39eed85d795cf27d6d1d7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674745"
---
# <span data-ttu-id="a3466-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="a3466-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a3466-102">SYNOPSIS</span></span>
<span data-ttu-id="a3466-103">Verifica l'esistenza di un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3466-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a3466-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a3466-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3466-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a3466-105">DESCRIPTION</span></span>
<span data-ttu-id="a3466-106">Il cmdlet **test-AzDataLakeStoreItem** verifica l'esistenza di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3466-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="a3466-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a3466-107">EXAMPLES</span></span>

### <span data-ttu-id="a3466-108">Esempio 1: testare un file</span><span class="sxs-lookup"><span data-stu-id="a3466-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="a3466-109">Questo comando verifica se il file Test.csv esiste nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="a3466-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="a3466-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a3466-110">PARAMETERS</span></span>

### <span data-ttu-id="a3466-111">-Account</span><span class="sxs-lookup"><span data-stu-id="a3466-111">-Account</span></span>
<span data-ttu-id="a3466-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="a3466-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="a3466-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3466-113">-DefaultProfile</span></span>
<span data-ttu-id="a3466-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a3466-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a3466-115">-Path</span><span class="sxs-lookup"><span data-stu-id="a3466-115">-Path</span></span>
<span data-ttu-id="a3466-116">Specifica il percorso dello Store Data Lake dell'elemento da testare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="a3466-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3466-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="a3466-117">-PathType</span></span>
<span data-ttu-id="a3466-118">Specifica il tipo di elemento da testare.</span><span class="sxs-lookup"><span data-stu-id="a3466-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="a3466-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a3466-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="a3466-120">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="a3466-120">Any</span></span> 
- <span data-ttu-id="a3466-121">File</span><span class="sxs-lookup"><span data-stu-id="a3466-121">File</span></span> 
- <span data-ttu-id="a3466-122">Cartella</span><span class="sxs-lookup"><span data-stu-id="a3466-122">Folder</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType
Parameter Sets: (All)
Aliases:
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a3466-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3466-123">CommonParameters</span></span>
<span data-ttu-id="a3466-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3466-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3466-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3466-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3466-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a3466-126">INPUTS</span></span>

### <span data-ttu-id="a3466-127">System. String</span><span class="sxs-lookup"><span data-stu-id="a3466-127">System.String</span></span>

### <span data-ttu-id="a3466-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="a3466-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="a3466-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="a3466-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="a3466-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a3466-130">OUTPUTS</span></span>

### <span data-ttu-id="a3466-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3466-131">System.Boolean</span></span>

## <span data-ttu-id="a3466-132">Note</span><span class="sxs-lookup"><span data-stu-id="a3466-132">NOTES</span></span>

## <span data-ttu-id="a3466-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a3466-133">RELATED LINKS</span></span>

[<span data-ttu-id="a3466-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3466-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3466-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3466-137">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3466-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="a3466-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="a3466-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


