---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a7b47425aad152d8851ff90717698b4c25ef026d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687217"
---
# <span data-ttu-id="c805b-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="c805b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c805b-102">SYNOPSIS</span></span>
<span data-ttu-id="c805b-103">Ottiene i dettagli di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c805b-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c805b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c805b-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c805b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c805b-105">DESCRIPTION</span></span>
<span data-ttu-id="c805b-106">Il cmdlet **Get-AzureRmDataLakeStoreItem** ottiene i dettagli di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c805b-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c805b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c805b-107">EXAMPLES</span></span>

### <span data-ttu-id="c805b-108">Esempio 1: ottenere i dettagli di un file da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="c805b-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="c805b-109">Questo comando consente di ottenere i dettagli del file Test.csv da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c805b-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="c805b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c805b-110">PARAMETERS</span></span>

### <span data-ttu-id="c805b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c805b-111">-Account</span></span>
<span data-ttu-id="c805b-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c805b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c805b-113">-Path</span><span class="sxs-lookup"><span data-stu-id="c805b-113">-Path</span></span>
<span data-ttu-id="c805b-114">Specifica il percorso di data Lake Store da cui ottenere i dettagli di un elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="c805b-114">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c805b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c805b-115">-DefaultProfile</span></span>
<span data-ttu-id="c805b-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c805b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c805b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c805b-117">CommonParameters</span></span>
<span data-ttu-id="c805b-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c805b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c805b-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c805b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c805b-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c805b-120">INPUTS</span></span>

## <span data-ttu-id="c805b-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c805b-121">OUTPUTS</span></span>

### <span data-ttu-id="c805b-122">DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-122">DataLakeStoreItem</span></span>
<span data-ttu-id="c805b-123">Il file o la cartella nel percorso specificato.</span><span class="sxs-lookup"><span data-stu-id="c805b-123">The file or folder at the path specified.</span></span>

## <span data-ttu-id="c805b-124">Note</span><span class="sxs-lookup"><span data-stu-id="c805b-124">NOTES</span></span>

## <span data-ttu-id="c805b-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c805b-125">RELATED LINKS</span></span>

[<span data-ttu-id="c805b-126">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-126">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c805b-127">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="c805b-127">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="c805b-128">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-128">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c805b-129">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-129">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c805b-130">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-130">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c805b-131">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-131">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c805b-132">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-132">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="c805b-133">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="c805b-133">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


