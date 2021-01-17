---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: 6123cacd35eb0a683ec2103ea00e2e06a2d80cd2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98473597"
---
# <span data-ttu-id="9d930-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="9d930-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="9d930-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9d930-102">SYNOPSIS</span></span>
<span data-ttu-id="9d930-103">Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9d930-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="9d930-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9d930-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d930-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9d930-105">DESCRIPTION</span></span>
<span data-ttu-id="9d930-106">Il cmdlet **Get-AzDataLakeStoreChildItem** Ottiene l'elenco di elementi in una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9d930-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="9d930-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9d930-107">EXAMPLES</span></span>

### <span data-ttu-id="9d930-108">Esempio 1: ottenere gli elementi figlio per una cartella</span><span class="sxs-lookup"><span data-stu-id="9d930-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="9d930-109">Questo comando consente di ottenere gli elementi figlio per la cartella myfiles.</span><span class="sxs-lookup"><span data-stu-id="9d930-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="9d930-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9d930-110">PARAMETERS</span></span>

### <span data-ttu-id="9d930-111">-Account</span><span class="sxs-lookup"><span data-stu-id="9d930-111">-Account</span></span>
<span data-ttu-id="9d930-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="9d930-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="9d930-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d930-113">-DefaultProfile</span></span>
<span data-ttu-id="9d930-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9d930-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d930-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9d930-115">-Path</span></span>
<span data-ttu-id="9d930-116">Specifica il percorso dello Store Data Lake della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="9d930-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="9d930-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d930-117">CommonParameters</span></span>
<span data-ttu-id="9d930-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d930-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d930-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d930-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d930-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9d930-120">INPUTS</span></span>

### <span data-ttu-id="9d930-121">System. String</span><span class="sxs-lookup"><span data-stu-id="9d930-121">System.String</span></span>

### <span data-ttu-id="9d930-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="9d930-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="9d930-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9d930-123">OUTPUTS</span></span>

### <span data-ttu-id="9d930-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="9d930-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="9d930-125">Note</span><span class="sxs-lookup"><span data-stu-id="9d930-125">NOTES</span></span>

## <span data-ttu-id="9d930-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9d930-126">RELATED LINKS</span></span>
