---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/test-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Test-AzDataLakeStoreItem.md
ms.openlocfilehash: 83f44ced24587340f063f24a17036184115cf299
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93865492"
---
# <span data-ttu-id="cb018-101">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-101">Test-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="cb018-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cb018-102">SYNOPSIS</span></span>
<span data-ttu-id="cb018-103">Verifica l'esistenza di un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb018-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cb018-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cb018-104">SYNTAX</span></span>

```
Test-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cb018-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cb018-105">DESCRIPTION</span></span>
<span data-ttu-id="cb018-106">Il cmdlet **test-AzDataLakeStoreItem** verifica l'esistenza di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb018-106">The **Test-AzDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="cb018-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cb018-107">EXAMPLES</span></span>

### <span data-ttu-id="cb018-108">Esempio 1: testare un file</span><span class="sxs-lookup"><span data-stu-id="cb018-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="cb018-109">Questo comando verifica se il file Test.csv esiste nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="cb018-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="cb018-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cb018-110">PARAMETERS</span></span>

### <span data-ttu-id="cb018-111">-Account</span><span class="sxs-lookup"><span data-stu-id="cb018-111">-Account</span></span>
<span data-ttu-id="cb018-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="cb018-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="cb018-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb018-113">-DefaultProfile</span></span>
<span data-ttu-id="cb018-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cb018-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb018-115">-Path</span><span class="sxs-lookup"><span data-stu-id="cb018-115">-Path</span></span>
<span data-ttu-id="cb018-116">Specifica il percorso dello Store Data Lake dell'elemento da testare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="cb018-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="cb018-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="cb018-117">-PathType</span></span>
<span data-ttu-id="cb018-118">Specifica il tipo di elemento da testare.</span><span class="sxs-lookup"><span data-stu-id="cb018-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="cb018-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="cb018-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="cb018-120">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="cb018-120">Any</span></span> 
- <span data-ttu-id="cb018-121">File</span><span class="sxs-lookup"><span data-stu-id="cb018-121">File</span></span> 
- <span data-ttu-id="cb018-122">Cartella</span><span class="sxs-lookup"><span data-stu-id="cb018-122">Folder</span></span>

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

### <span data-ttu-id="cb018-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb018-123">CommonParameters</span></span>
<span data-ttu-id="cb018-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb018-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb018-125">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb018-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb018-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cb018-126">INPUTS</span></span>

### <span data-ttu-id="cb018-127">System. String</span><span class="sxs-lookup"><span data-stu-id="cb018-127">System.String</span></span>

### <span data-ttu-id="cb018-128">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="cb018-128">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="cb018-129">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + PathType</span><span class="sxs-lookup"><span data-stu-id="cb018-129">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+PathType</span></span>

## <span data-ttu-id="cb018-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cb018-130">OUTPUTS</span></span>

### <span data-ttu-id="cb018-131">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cb018-131">System.Boolean</span></span>

## <span data-ttu-id="cb018-132">Note</span><span class="sxs-lookup"><span data-stu-id="cb018-132">NOTES</span></span>

## <span data-ttu-id="cb018-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cb018-133">RELATED LINKS</span></span>

[<span data-ttu-id="cb018-134">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-134">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="cb018-135">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-135">Get-AzDataLakeStoreItem</span></span>](./Get-AzDataLakeStoreItem.md)

[<span data-ttu-id="cb018-136">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-136">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="cb018-137">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-137">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="cb018-138">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-138">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="cb018-139">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="cb018-139">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)


