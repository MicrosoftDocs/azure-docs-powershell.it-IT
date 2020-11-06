---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemPermission.md
ms.openlocfilehash: f76473239661b492c95a356dfb1b381e1093f98c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93512623"
---
# <span data-ttu-id="832b5-101">Get-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="832b5-101">Get-AzureRmDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="832b5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="832b5-102">SYNOPSIS</span></span>
<span data-ttu-id="832b5-103">Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="832b5-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="832b5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="832b5-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="832b5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="832b5-105">DESCRIPTION</span></span>
<span data-ttu-id="832b5-106">Il cmdlet **Get-AzureRmDataLakeStoreItemPermission** Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="832b5-106">The **Get-AzureRmDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="832b5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="832b5-107">EXAMPLES</span></span>

### <span data-ttu-id="832b5-108">Esempio 1: impostare l'ottale delle autorizzazioni per un file</span><span class="sxs-lookup"><span data-stu-id="832b5-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="832b5-109">Questo comando ottiene l'ottale delle autorizzazioni per un file.</span><span class="sxs-lookup"><span data-stu-id="832b5-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="832b5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="832b5-110">PARAMETERS</span></span>

### <span data-ttu-id="832b5-111">-Account</span><span class="sxs-lookup"><span data-stu-id="832b5-111">-Account</span></span>
<span data-ttu-id="832b5-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="832b5-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="832b5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="832b5-113">-DefaultProfile</span></span>
<span data-ttu-id="832b5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="832b5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="832b5-115">-Path</span><span class="sxs-lookup"><span data-stu-id="832b5-115">-Path</span></span>
<span data-ttu-id="832b5-116">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="832b5-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="832b5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="832b5-117">CommonParameters</span></span>
<span data-ttu-id="832b5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="832b5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="832b5-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="832b5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="832b5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="832b5-120">INPUTS</span></span>

### <span data-ttu-id="832b5-121">Nessuno</span><span class="sxs-lookup"><span data-stu-id="832b5-121">None</span></span>
<span data-ttu-id="832b5-122">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="832b5-122">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="832b5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="832b5-123">OUTPUTS</span></span>

### <span data-ttu-id="832b5-124">stringa</span><span class="sxs-lookup"><span data-stu-id="832b5-124">string</span></span>
<span data-ttu-id="832b5-125">Rappresentazione in stringa dell'ottale di proprietà</span><span class="sxs-lookup"><span data-stu-id="832b5-125">The string representation of the ownership octal</span></span>

## <span data-ttu-id="832b5-126">Note</span><span class="sxs-lookup"><span data-stu-id="832b5-126">NOTES</span></span>
* <span data-ttu-id="832b5-127">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="832b5-127">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="832b5-128">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="832b5-128">RELATED LINKS</span></span>

[<span data-ttu-id="832b5-129">Set-AzureRmDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="832b5-129">Set-AzureRmDataLakeStoreItemPermission</span></span>](./Set-AzureRmDataLakeStoreItemPermission.md)


