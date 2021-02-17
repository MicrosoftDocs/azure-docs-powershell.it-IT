---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177094"
---
# <span data-ttu-id="c3e81-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c3e81-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="c3e81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3e81-102">SYNOPSIS</span></span>
<span data-ttu-id="c3e81-103">Ottiene l'ottale di autorizzazione di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c3e81-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c3e81-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3e81-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3e81-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c3e81-105">DESCRIPTION</span></span>
<span data-ttu-id="c3e81-106">Il cmdlet **Get-AzDataLakeStoreItemPermission** ottiene l'ottale di autorizzazione di un file o di una cartella in Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c3e81-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c3e81-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3e81-107">EXAMPLES</span></span>

### <span data-ttu-id="c3e81-108">Esempio 1: Impostare l'ottale di autorizzazione per un file</span><span class="sxs-lookup"><span data-stu-id="c3e81-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="c3e81-109">Questo comando ottiene l'ottale di autorizzazione per un file.</span><span class="sxs-lookup"><span data-stu-id="c3e81-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="c3e81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3e81-110">PARAMETERS</span></span>

### <span data-ttu-id="c3e81-111">-Account</span><span class="sxs-lookup"><span data-stu-id="c3e81-111">-Account</span></span>
<span data-ttu-id="c3e81-112">Specifica il nome dell'account Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="c3e81-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="c3e81-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3e81-113">-DefaultProfile</span></span>
<span data-ttu-id="c3e81-114">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c3e81-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3e81-115">-Path</span><span class="sxs-lookup"><span data-stu-id="c3e81-115">-Path</span></span>
<span data-ttu-id="c3e81-116">Specifica il percorso Data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="c3e81-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c3e81-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3e81-117">CommonParameters</span></span>
<span data-ttu-id="c3e81-118">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3e81-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3e81-119">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3e81-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3e81-120">INPUT</span><span class="sxs-lookup"><span data-stu-id="c3e81-120">INPUTS</span></span>

### <span data-ttu-id="c3e81-121">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e81-121">System.String</span></span>

### <span data-ttu-id="c3e81-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="c3e81-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="c3e81-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3e81-123">OUTPUTS</span></span>

### <span data-ttu-id="c3e81-124">System.String</span><span class="sxs-lookup"><span data-stu-id="c3e81-124">System.String</span></span>

## <span data-ttu-id="c3e81-125">NOTE</span><span class="sxs-lookup"><span data-stu-id="c3e81-125">NOTES</span></span>
* <span data-ttu-id="c3e81-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c3e81-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="c3e81-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3e81-127">RELATED LINKS</span></span>

[<span data-ttu-id="c3e81-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="c3e81-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


