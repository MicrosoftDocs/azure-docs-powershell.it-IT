---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352879"
---
# <span data-ttu-id="d1a14-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="d1a14-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="d1a14-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1a14-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a14-103">Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d1a14-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d1a14-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1a14-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1a14-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1a14-105">DESCRIPTION</span></span>
<span data-ttu-id="d1a14-106">Il cmdlet **Get-AzDataLakeStoreChildItem** Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d1a14-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="d1a14-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1a14-107">EXAMPLES</span></span>

### <span data-ttu-id="d1a14-108">Esempio 1: ottenere gli elementi figlio per una cartella</span><span class="sxs-lookup"><span data-stu-id="d1a14-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="d1a14-109">Questo comando consente di ottenere gli elementi figlio per la cartella myfiles.</span><span class="sxs-lookup"><span data-stu-id="d1a14-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="d1a14-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1a14-110">PARAMETERS</span></span>

### <span data-ttu-id="d1a14-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d1a14-111">-Account</span></span>
<span data-ttu-id="d1a14-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d1a14-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="d1a14-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a14-113">-DefaultProfile</span></span>
<span data-ttu-id="d1a14-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a14-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1a14-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d1a14-115">-Path</span></span>
<span data-ttu-id="d1a14-116">Specifica il percorso dello Store Data Lake della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d1a14-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d1a14-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a14-117">CommonParameters</span></span>
<span data-ttu-id="d1a14-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a14-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a14-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a14-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a14-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1a14-120">INPUTS</span></span>

### <span data-ttu-id="d1a14-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d1a14-121">System.String</span></span>

### <span data-ttu-id="d1a14-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d1a14-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d1a14-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1a14-123">OUTPUTS</span></span>

### <span data-ttu-id="d1a14-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="d1a14-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="d1a14-125">Note</span><span class="sxs-lookup"><span data-stu-id="d1a14-125">NOTES</span></span>

## <span data-ttu-id="d1a14-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1a14-126">RELATED LINKS</span></span>
