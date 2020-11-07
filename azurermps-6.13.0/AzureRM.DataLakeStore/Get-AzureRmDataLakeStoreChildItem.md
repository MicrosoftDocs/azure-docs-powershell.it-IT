---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreChildItem.md
ms.openlocfilehash: 64cf2a14791796e2796f15e446e6ceb29b5b24cc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686419"
---
# <span data-ttu-id="0f148-101">Get-AzureRmDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="0f148-101">Get-AzureRmDataLakeStoreChildItem</span></span>

## <span data-ttu-id="0f148-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f148-102">SYNOPSIS</span></span>
<span data-ttu-id="0f148-103">Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f148-103">Gets the list of items in a folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f148-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f148-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f148-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f148-105">DESCRIPTION</span></span>
<span data-ttu-id="0f148-106">Il cmdlet **Get-AzureRmDataLakeStoreChildItem** Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f148-106">The **Get-AzureRmDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="0f148-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f148-107">EXAMPLES</span></span>

### <span data-ttu-id="0f148-108">Esempio 1: ottenere gli elementi figlio per una cartella</span><span class="sxs-lookup"><span data-stu-id="0f148-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="0f148-109">Questo comando consente di ottenere gli elementi figlio per la cartella myfiles.</span><span class="sxs-lookup"><span data-stu-id="0f148-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="0f148-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f148-110">PARAMETERS</span></span>

### <span data-ttu-id="0f148-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0f148-111">-Account</span></span>
<span data-ttu-id="0f148-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0f148-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="0f148-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f148-113">-DefaultProfile</span></span>
<span data-ttu-id="0f148-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f148-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f148-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0f148-115">-Path</span></span>
<span data-ttu-id="0f148-116">Specifica il percorso dello Store Data Lake della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="0f148-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0f148-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f148-117">CommonParameters</span></span>
<span data-ttu-id="0f148-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f148-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f148-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f148-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f148-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f148-120">INPUTS</span></span>

### <span data-ttu-id="0f148-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0f148-121">System.String</span></span>

### <span data-ttu-id="0f148-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0f148-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0f148-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f148-123">OUTPUTS</span></span>

### <span data-ttu-id="0f148-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="0f148-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="0f148-125">Note</span><span class="sxs-lookup"><span data-stu-id="0f148-125">NOTES</span></span>

## <span data-ttu-id="0f148-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f148-126">RELATED LINKS</span></span>