---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: 1743ee6e4d0ce1276c69bec9e3669b5d04ee3858
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93520110"
---
# <span data-ttu-id="384dc-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="384dc-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="384dc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="384dc-102">SYNOPSIS</span></span>
<span data-ttu-id="384dc-103">Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="384dc-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="384dc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="384dc-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="384dc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="384dc-105">DESCRIPTION</span></span>
<span data-ttu-id="384dc-106">Il cmdlet **Get-AzureRmDataLakeStoreItemPermission** Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="384dc-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="384dc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="384dc-107">EXAMPLES</span></span>

### <span data-ttu-id="384dc-108">Esempio 1: impostare l'ottale delle autorizzazioni per un file</span><span class="sxs-lookup"><span data-stu-id="384dc-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="384dc-109">Questo comando ottiene l'ottale delle autorizzazioni per un file.</span><span class="sxs-lookup"><span data-stu-id="384dc-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="384dc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="384dc-110">PARAMETERS</span></span>

### <span data-ttu-id="384dc-111">-Account</span><span class="sxs-lookup"><span data-stu-id="384dc-111">-Account</span></span>
<span data-ttu-id="384dc-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="384dc-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="384dc-113">-Path</span><span class="sxs-lookup"><span data-stu-id="384dc-113">-Path</span></span>
<span data-ttu-id="384dc-114">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="384dc-114">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="384dc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="384dc-115">-DefaultProfile</span></span>
<span data-ttu-id="384dc-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="384dc-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="384dc-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="384dc-117">CommonParameters</span></span>
<span data-ttu-id="384dc-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="384dc-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="384dc-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="384dc-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="384dc-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="384dc-120">INPUTS</span></span>

## <span data-ttu-id="384dc-121">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="384dc-121">OUTPUTS</span></span>

### <span data-ttu-id="384dc-122">stringa</span><span class="sxs-lookup"><span data-stu-id="384dc-122">string</span></span>
<span data-ttu-id="384dc-123">Rappresentazione in stringa dell'ottale di proprietà</span><span class="sxs-lookup"><span data-stu-id="384dc-123">The string representation of the ownership octal</span></span>

## <span data-ttu-id="384dc-124">Note</span><span class="sxs-lookup"><span data-stu-id="384dc-124">NOTES</span></span>
* <span data-ttu-id="384dc-125">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="384dc-125">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="384dc-126">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="384dc-126">RELATED LINKS</span></span>

[<span data-ttu-id="384dc-127">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="384dc-127">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


