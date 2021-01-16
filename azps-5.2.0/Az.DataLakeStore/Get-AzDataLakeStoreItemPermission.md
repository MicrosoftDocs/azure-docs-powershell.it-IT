---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: f435715c4c9361fcd396c751ea6956bfcffe1c1d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98343855"
---
# <span data-ttu-id="78f2a-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="78f2a-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="78f2a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="78f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="78f2a-103">Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="78f2a-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="78f2a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="78f2a-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78f2a-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="78f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="78f2a-106">Il cmdlet **Get-AzDataLakeStoreItemPermission** Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="78f2a-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="78f2a-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="78f2a-107">EXAMPLES</span></span>

### <span data-ttu-id="78f2a-108">Esempio 1: impostare l'ottale delle autorizzazioni per un file</span><span class="sxs-lookup"><span data-stu-id="78f2a-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="78f2a-109">Questo comando ottiene l'ottale delle autorizzazioni per un file.</span><span class="sxs-lookup"><span data-stu-id="78f2a-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="78f2a-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="78f2a-110">PARAMETERS</span></span>

### <span data-ttu-id="78f2a-111">-Account</span><span class="sxs-lookup"><span data-stu-id="78f2a-111">-Account</span></span>
<span data-ttu-id="78f2a-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="78f2a-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="78f2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78f2a-113">-DefaultProfile</span></span>
<span data-ttu-id="78f2a-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="78f2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="78f2a-115">-Path</span><span class="sxs-lookup"><span data-stu-id="78f2a-115">-Path</span></span>
<span data-ttu-id="78f2a-116">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="78f2a-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="78f2a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78f2a-117">CommonParameters</span></span>
<span data-ttu-id="78f2a-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78f2a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78f2a-119">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78f2a-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78f2a-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="78f2a-120">INPUTS</span></span>

### <span data-ttu-id="78f2a-121">System. String</span><span class="sxs-lookup"><span data-stu-id="78f2a-121">System.String</span></span>

### <span data-ttu-id="78f2a-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="78f2a-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="78f2a-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="78f2a-123">OUTPUTS</span></span>

### <span data-ttu-id="78f2a-124">System. String</span><span class="sxs-lookup"><span data-stu-id="78f2a-124">System.String</span></span>

## <span data-ttu-id="78f2a-125">Note</span><span class="sxs-lookup"><span data-stu-id="78f2a-125">NOTES</span></span>
* <span data-ttu-id="78f2a-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="78f2a-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="78f2a-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="78f2a-127">RELATED LINKS</span></span>

[<span data-ttu-id="78f2a-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="78f2a-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


