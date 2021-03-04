---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: CC0E73BD-2063-4CA2-BBBA-1FB6AE04DADE
online version: https://docs.microsoft.com/powershell/module/az.datalakestore/get-azdatalakestorechilditem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreChildItem.md
ms.openlocfilehash: e27fde6a25fc512b898ded7d4f087ab7b344d293
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957294"
---
# <span data-ttu-id="38870-101">Get-AzDataLakeStoreChildItem</span><span class="sxs-lookup"><span data-stu-id="38870-101">Get-AzDataLakeStoreChildItem</span></span>

## <span data-ttu-id="38870-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38870-102">SYNOPSIS</span></span>
<span data-ttu-id="38870-103">Ottiene l'elenco degli elementi in una cartella di Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38870-103">Gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="38870-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="38870-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreChildItem [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38870-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="38870-105">DESCRIPTION</span></span>
<span data-ttu-id="38870-106">Il **cmdlet Get-AzDataLakeStoreItem ottiene** l'elenco degli elementi in una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38870-106">The **Get-AzDataLakeStoreChildItem** cmdlet gets the list of items in a folder in Data Lake Store.</span></span>

## <span data-ttu-id="38870-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="38870-107">EXAMPLES</span></span>

### <span data-ttu-id="38870-108">Esempio 1: Recuperare gli elementi figlio per una cartella</span><span class="sxs-lookup"><span data-stu-id="38870-108">Example 1: Get the child items for a folder</span></span>
```
PS C:\>Get-AzDataLakeStoreChildItem -AccountName "ContosoADL" -Path "/MyFiles/"
```

<span data-ttu-id="38870-109">Questo comando recupera gli elementi figlio della cartella MyFiles.</span><span class="sxs-lookup"><span data-stu-id="38870-109">This command gets the child items for the MyFiles folder.</span></span>

## <span data-ttu-id="38870-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38870-110">PARAMETERS</span></span>

### <span data-ttu-id="38870-111">-Account</span><span class="sxs-lookup"><span data-stu-id="38870-111">-Account</span></span>
<span data-ttu-id="38870-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="38870-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="38870-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38870-113">-DefaultProfile</span></span>
<span data-ttu-id="38870-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="38870-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38870-115">-Path</span><span class="sxs-lookup"><span data-stu-id="38870-115">-Path</span></span>
<span data-ttu-id="38870-116">Specifica il percorso Data Lake Store della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="38870-116">Specifies the Data Lake Store path of the folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="38870-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38870-117">CommonParameters</span></span>
<span data-ttu-id="38870-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38870-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38870-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38870-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38870-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="38870-120">INPUTS</span></span>

### <span data-ttu-id="38870-121">System.String</span><span class="sxs-lookup"><span data-stu-id="38870-121">System.String</span></span>

### <span data-ttu-id="38870-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="38870-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="38870-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="38870-123">OUTPUTS</span></span>

### <span data-ttu-id="38870-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span><span class="sxs-lookup"><span data-stu-id="38870-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItem</span></span>

## <span data-ttu-id="38870-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="38870-125">NOTES</span></span>

## <span data-ttu-id="38870-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="38870-126">RELATED LINKS</span></span>
