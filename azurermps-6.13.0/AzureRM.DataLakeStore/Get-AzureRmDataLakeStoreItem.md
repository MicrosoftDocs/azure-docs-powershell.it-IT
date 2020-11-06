---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItem.md
ms.openlocfilehash: a1e70286364fea53062a75b7ac886834803c3674
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520643"
---
# <span data-ttu-id="8fa34-101">Get-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-101">Get-AzureRmDataLakeStoreItem</span></span>

## <span data-ttu-id="8fa34-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="8fa34-102">SYNOPSIS</span></span>
<span data-ttu-id="8fa34-103">Ottiene i dettagli di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa34-103">Gets the details of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8fa34-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8fa34-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8fa34-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="8fa34-105">DESCRIPTION</span></span>
<span data-ttu-id="8fa34-106">Il cmdlet **Get-AzureRmDataLakeStoreItem** ottiene i dettagli di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa34-106">The **Get-AzureRmDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="8fa34-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8fa34-107">EXAMPLES</span></span>

### <span data-ttu-id="8fa34-108">Esempio 1: ottenere i dettagli di un file da data Lake Store</span><span class="sxs-lookup"><span data-stu-id="8fa34-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="8fa34-109">Questo comando consente di ottenere i dettagli del file Test.csv da data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa34-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="8fa34-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="8fa34-110">PARAMETERS</span></span>

### <span data-ttu-id="8fa34-111">-Account</span><span class="sxs-lookup"><span data-stu-id="8fa34-111">-Account</span></span>
<span data-ttu-id="8fa34-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="8fa34-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="8fa34-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8fa34-113">-DefaultProfile</span></span>
<span data-ttu-id="8fa34-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8fa34-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8fa34-115">-Path</span><span class="sxs-lookup"><span data-stu-id="8fa34-115">-Path</span></span>
<span data-ttu-id="8fa34-116">Specifica il percorso di data Lake Store da cui ottenere i dettagli di un elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="8fa34-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="8fa34-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8fa34-117">CommonParameters</span></span>
<span data-ttu-id="8fa34-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8fa34-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8fa34-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8fa34-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8fa34-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="8fa34-120">INPUTS</span></span>

### <span data-ttu-id="8fa34-121">System. String</span><span class="sxs-lookup"><span data-stu-id="8fa34-121">System.String</span></span>

### <span data-ttu-id="8fa34-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="8fa34-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="8fa34-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8fa34-123">OUTPUTS</span></span>

### <span data-ttu-id="8fa34-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="8fa34-125">Note</span><span class="sxs-lookup"><span data-stu-id="8fa34-125">NOTES</span></span>

## <span data-ttu-id="8fa34-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8fa34-126">RELATED LINKS</span></span>

[<span data-ttu-id="8fa34-127">Export-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-127">Export-AzureRmDataLakeStoreItem</span></span>](./Export-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8fa34-128">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-128">Get-AzureRmDataLakeStoreChildItem</span></span>](./Get-AzureRmDataLakeStoreChildItem.md)

[<span data-ttu-id="8fa34-129">Import-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-129">Import-AzureRmDataLakeStoreItem</span></span>](./Import-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8fa34-130">Join-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-130">Join-AzureRmDataLakeStoreItem</span></span>](./Join-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8fa34-131">Move-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-131">Move-AzureRmDataLakeStoreItem</span></span>](./Move-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8fa34-132">New-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-132">New-AzureRmDataLakeStoreItem</span></span>](./New-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8fa34-133">Remove-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-133">Remove-AzureRmDataLakeStoreItem</span></span>](./Remove-AzureRmDataLakeStoreItem.md)

[<span data-ttu-id="8fa34-134">Test-AzureRmDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="8fa34-134">Test-AzureRmDataLakeStoreItem</span></span>](./Test-AzureRmDataLakeStoreItem.md)


