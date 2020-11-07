---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 0937A390-6AC2-4611-AA6C-99936AC0ABFD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/test-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Test-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: bf754e335753efc5350d3c0979db9f0f7057f010
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687495"
---
# <span data-ttu-id="f4815-101">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-101">Test-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="f4815-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f4815-102">SYNOPSIS</span></span>
<span data-ttu-id="f4815-103">Verifica l'esistenza di un file o una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4815-103">Tests the existence of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4815-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f4815-104">SYNTAX</span></span>

```
Test-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance> [[-PathType] <PathType>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4815-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f4815-105">DESCRIPTION</span></span>
<span data-ttu-id="f4815-106">Il cmdlet **test-AzureRmDataLakeStoreItem** verifica l'esistenza di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4815-106">The **Test-AzureRmDataLakeStoreItem** cmdlet tests the existence of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="f4815-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f4815-107">EXAMPLES</span></span>

### <span data-ttu-id="f4815-108">Esempio 1: testare un file</span><span class="sxs-lookup"><span data-stu-id="f4815-108">Example 1: Test a file</span></span>
```
PS C:\>Test-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="f4815-109">Questo comando verifica se il file Test.csv esiste nell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="f4815-109">This command tests whether the file Test.csv exists in the ContosoADL account.</span></span>

## <span data-ttu-id="f4815-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f4815-110">PARAMETERS</span></span>

### <span data-ttu-id="f4815-111">-Account</span><span class="sxs-lookup"><span data-stu-id="f4815-111">-Account</span></span>
<span data-ttu-id="f4815-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="f4815-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="f4815-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4815-113">-DefaultProfile</span></span>
<span data-ttu-id="f4815-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f4815-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4815-115">-Path</span><span class="sxs-lookup"><span data-stu-id="f4815-115">-Path</span></span>
<span data-ttu-id="f4815-116">Specifica il percorso dello Store Data Lake dell'elemento da testare, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="f4815-116">Specifies the Data Lake Store path of the item to test, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="f4815-117">-PathType</span><span class="sxs-lookup"><span data-stu-id="f4815-117">-PathType</span></span>
<span data-ttu-id="f4815-118">Specifica il tipo di elemento da testare.</span><span class="sxs-lookup"><span data-stu-id="f4815-118">Specifies the type of item to test.</span></span>
<span data-ttu-id="f4815-119">I valori accettabili per questo parametro sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="f4815-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="f4815-120">Qualsiasi</span><span class="sxs-lookup"><span data-stu-id="f4815-120">Any</span></span> 
- <span data-ttu-id="f4815-121">File</span><span class="sxs-lookup"><span data-stu-id="f4815-121">File</span></span> 
- <span data-ttu-id="f4815-122">Cartella</span><span class="sxs-lookup"><span data-stu-id="f4815-122">Folder</span></span>

```yaml
Type: PathType
Parameter Sets: (All)
Aliases: 
Accepted values: Any, File, Folder

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f4815-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4815-123">CommonParameters</span></span>
<span data-ttu-id="f4815-124">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4815-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4815-125">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4815-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4815-126">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f4815-126">INPUTS</span></span>

### <span data-ttu-id="f4815-127">Nessuno</span><span class="sxs-lookup"><span data-stu-id="f4815-127">None</span></span>
<span data-ttu-id="f4815-128">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="f4815-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="f4815-129">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f4815-129">OUTPUTS</span></span>

### <span data-ttu-id="f4815-130">bool</span><span class="sxs-lookup"><span data-stu-id="f4815-130">bool</span></span>
<span data-ttu-id="f4815-131">Vero o falso che indica l'esistenza del file o della cartella specificata.</span><span class="sxs-lookup"><span data-stu-id="f4815-131">True or false indicating the existence of the specified file or folder.</span></span>

## <span data-ttu-id="f4815-132">Note</span><span class="sxs-lookup"><span data-stu-id="f4815-132">NOTES</span></span>

## <span data-ttu-id="f4815-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f4815-133">RELATED LINKS</span></span>

[<span data-ttu-id="f4815-134">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-134">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f4815-135">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-135">Get-AzureRmDataLakeStoreItem</span></span>](./Get-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f4815-136">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-136">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f4815-137">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-137">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f4815-138">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-138">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="f4815-139">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="f4815-139">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)


