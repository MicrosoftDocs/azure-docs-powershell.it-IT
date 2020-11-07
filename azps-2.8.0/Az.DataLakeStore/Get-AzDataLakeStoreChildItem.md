---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 828418095c7e77a7ee484d00e9d4d3f6f4a9927b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674818"
---
# <span data-ttu-id="3b232-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="3b232-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="3b232-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3b232-102">SYNOPSIS</span></span>
<span data-ttu-id="3b232-103">Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b232-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="3b232-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3b232-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b232-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3b232-105">DESCRIPTION</span></span>
<span data-ttu-id="3b232-106">Il cmdlet **Get-AzDataLakeStoreChildItem** Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b232-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="3b232-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3b232-107">EXAMPLES</span></span>

### <span data-ttu-id="3b232-108">Esempio 1: ottenere gli elementi figlio per una cartella</span><span class="sxs-lookup"><span data-stu-id="3b232-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="3b232-109">Questo comando consente di ottenere gli elementi figlio per la cartella myfiles.</span><span class="sxs-lookup"><span data-stu-id="3b232-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="3b232-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3b232-110">PARAMETERS</span></span>

### <span data-ttu-id="3b232-111">-Account</span><span class="sxs-lookup"><span data-stu-id="3b232-111">-Account</span></span>
<span data-ttu-id="3b232-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="3b232-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="3b232-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b232-113">-DefaultProfile</span></span>
<span data-ttu-id="3b232-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3b232-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3b232-115">-Path</span><span class="sxs-lookup"><span data-stu-id="3b232-115">-Path</span></span>
<span data-ttu-id="3b232-116">Specifica il percorso dello Store Data Lake della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="3b232-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="3b232-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b232-117">CommonParameters</span></span>
<span data-ttu-id="3b232-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3b232-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b232-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b232-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b232-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3b232-120">INPUTS</span></span>

### <span data-ttu-id="3b232-121">System. String</span><span class="sxs-lookup"><span data-stu-id="3b232-121">System.String</span></span>

### <span data-ttu-id="3b232-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="3b232-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="3b232-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3b232-123">OUTPUTS</span></span>

### <span data-ttu-id="3b232-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="3b232-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="3b232-125">Note</span><span class="sxs-lookup"><span data-stu-id="3b232-125">NOTES</span></span>

## <span data-ttu-id="3b232-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3b232-126">RELATED LINKS</span></span>
