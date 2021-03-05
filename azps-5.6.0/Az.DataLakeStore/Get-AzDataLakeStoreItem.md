---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: ECA70C6C-E0B0-445D-BCAD-041625FAC632
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItem.md
ms.openlocfilehash: 3a39e2f341404ac3f6dbb75c27408dd9d9ee2d47
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009150"
---
# <span data-ttu-id="aaa38-101">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-101">Get-AzDataLakeStoreItem</span></span>

## <span data-ttu-id="aaa38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaa38-102">SYNOPSIS</span></span>
<span data-ttu-id="aaa38-103">Recupera i dettagli di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aaa38-103">Gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="aaa38-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="aaa38-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aaa38-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="aaa38-105">DESCRIPTION</span></span>
<span data-ttu-id="aaa38-106">Il cmdlet **Get-AzDataLakeStoreItem** ottiene i dettagli di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aaa38-106">The **Get-AzDataLakeStoreItem** cmdlet gets the details of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="aaa38-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="aaa38-107">EXAMPLES</span></span>

### <span data-ttu-id="aaa38-108">Esempio 1: Ottenere i dettagli di un file da Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="aaa38-108">Example 1: Get details of a file from the Data Lake Store</span></span>
```
PS C:\>Get-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "/MyFiles/Test.csv"
```

<span data-ttu-id="aaa38-109">Questo comando recupera i dettagli del file Test.csv da Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aaa38-109">This command gets the details of the file Test.csv from the Data Lake Store.</span></span>

## <span data-ttu-id="aaa38-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aaa38-110">PARAMETERS</span></span>

### <span data-ttu-id="aaa38-111">-Account</span><span class="sxs-lookup"><span data-stu-id="aaa38-111">-Account</span></span>
<span data-ttu-id="aaa38-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="aaa38-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="aaa38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaa38-113">-DefaultProfile</span></span>
<span data-ttu-id="aaa38-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="aaa38-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aaa38-115">-Path</span><span class="sxs-lookup"><span data-stu-id="aaa38-115">-Path</span></span>
<span data-ttu-id="aaa38-116">Specifica il percorso data lake store da cui ottenere i dettagli di un elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="aaa38-116">Specifies the Data Lake Store path from which to get details of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="aaa38-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaa38-117">CommonParameters</span></span>
<span data-ttu-id="aaa38-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aaa38-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaa38-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aaa38-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaa38-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="aaa38-120">INPUTS</span></span>

### <span data-ttu-id="aaa38-121">System.String</span><span class="sxs-lookup"><span data-stu-id="aaa38-121">System.String</span></span>

### <span data-ttu-id="aaa38-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="aaa38-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="aaa38-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="aaa38-123">OUTPUTS</span></span>

### <span data-ttu-id="aaa38-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="aaa38-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="aaa38-125">NOTES</span></span>

## <span data-ttu-id="aaa38-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="aaa38-126">RELATED LINKS</span></span>

[<span data-ttu-id="aaa38-127">Export-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-127">Export-AzDataLakeStoreItem</span></span>](./Export-AzDataLakeStoreItem.md)

[<span data-ttu-id="aaa38-128">Get-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-128">Get-AzDataLakeStoreChildItem</span></span>](./Get-AzDataLakeStoreChildItem.md)

[<span data-ttu-id="aaa38-129">Import-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-129">Import-AzDataLakeStoreItem</span></span>](./Import-AzDataLakeStoreItem.md)

[<span data-ttu-id="aaa38-130">Join-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-130">Join-AzDataLakeStoreItem</span></span>](./Join-AzDataLakeStoreItem.md)

[<span data-ttu-id="aaa38-131">Move-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-131">Move-AzDataLakeStoreItem</span></span>](./Move-AzDataLakeStoreItem.md)

[<span data-ttu-id="aaa38-132">New-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-132">New-AzDataLakeStoreItem</span></span>](./New-AzDataLakeStoreItem.md)

[<span data-ttu-id="aaa38-133">Remove-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-133">Remove-AzDataLakeStoreItem</span></span>](./Remove-AzDataLakeStoreItem.md)

[<span data-ttu-id="aaa38-134">Test-AzDataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="aaa38-134">Test-AzDataLakeStoreItem</span></span>](./Test-AzDataLakeStoreItem.md)


