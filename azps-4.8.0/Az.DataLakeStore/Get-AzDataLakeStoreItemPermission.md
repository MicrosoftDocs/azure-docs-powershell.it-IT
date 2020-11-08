---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94192530"
---
# <span data-ttu-id="d3277-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d3277-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="d3277-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3277-102">SYNOPSIS</span></span>
<span data-ttu-id="d3277-103">Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3277-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d3277-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3277-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3277-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3277-105">DESCRIPTION</span></span>
<span data-ttu-id="d3277-106">Il cmdlet **Get-AzDataLakeStoreItemPermission** Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="d3277-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="d3277-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3277-107">EXAMPLES</span></span>

### <span data-ttu-id="d3277-108">Esempio 1: impostare l'ottale delle autorizzazioni per un file</span><span class="sxs-lookup"><span data-stu-id="d3277-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="d3277-109">Questo comando ottiene l'ottale delle autorizzazioni per un file.</span><span class="sxs-lookup"><span data-stu-id="d3277-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="d3277-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3277-110">PARAMETERS</span></span>

### <span data-ttu-id="d3277-111">-Account</span><span class="sxs-lookup"><span data-stu-id="d3277-111">-Account</span></span>
<span data-ttu-id="d3277-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="d3277-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="d3277-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3277-113">-DefaultProfile</span></span>
<span data-ttu-id="d3277-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3277-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3277-115">-Path</span><span class="sxs-lookup"><span data-stu-id="d3277-115">-Path</span></span>
<span data-ttu-id="d3277-116">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="d3277-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="d3277-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3277-117">CommonParameters</span></span>
<span data-ttu-id="d3277-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3277-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3277-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3277-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3277-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3277-120">INPUTS</span></span>

### <span data-ttu-id="d3277-121">System. String</span><span class="sxs-lookup"><span data-stu-id="d3277-121">System.String</span></span>

### <span data-ttu-id="d3277-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="d3277-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="d3277-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3277-123">OUTPUTS</span></span>

### <span data-ttu-id="d3277-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d3277-124">System.String</span></span>

## <span data-ttu-id="d3277-125">Note</span><span class="sxs-lookup"><span data-stu-id="d3277-125">NOTES</span></span>
* <span data-ttu-id="d3277-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d3277-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="d3277-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3277-127">RELATED LINKS</span></span>

[<span data-ttu-id="d3277-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="d3277-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


