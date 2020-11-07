---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 476E889F-C763-4EFA-AFD6-B037BA6BA0A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitempermission
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemPermission.md
ms.openlocfilehash: 5270d77a9f9cd05b8075011e3fc002ac47d5c3a6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93674799"
---
# <span data-ttu-id="0d1a5-101">Get-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0d1a5-101">Get-AzDataLakeStoreItemPermission</span></span>

## <span data-ttu-id="0d1a5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0d1a5-102">SYNOPSIS</span></span>
<span data-ttu-id="0d1a5-103">Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-103">Gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0d1a5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0d1a5-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemPermission [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0d1a5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0d1a5-105">DESCRIPTION</span></span>
<span data-ttu-id="0d1a5-106">Il cmdlet **Get-AzDataLakeStoreItemPermission** Ottiene l'ottale delle autorizzazioni di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-106">The **Get-AzDataLakeStoreItemPermission** cmdlet gets the permission octal of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="0d1a5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0d1a5-107">EXAMPLES</span></span>

### <span data-ttu-id="0d1a5-108">Esempio 1: impostare l'ottale delle autorizzazioni per un file</span><span class="sxs-lookup"><span data-stu-id="0d1a5-108">Example 1: Set the permission octal for a file</span></span>
```
PS C:\>Get-AzDataLakeStoreItemPermission -AccountName "ContosoADL" -Path "/file.txt"
```

<span data-ttu-id="0d1a5-109">Questo comando ottiene l'ottale delle autorizzazioni per un file.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-109">This command gets the permission octal for a file.</span></span>

## <span data-ttu-id="0d1a5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0d1a5-110">PARAMETERS</span></span>

### <span data-ttu-id="0d1a5-111">-Account</span><span class="sxs-lookup"><span data-stu-id="0d1a5-111">-Account</span></span>
<span data-ttu-id="0d1a5-112">Specifica il nome dell'account Store Data Lake.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-112">Specifies the Data Lake Store account name.</span></span>

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

### <span data-ttu-id="0d1a5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d1a5-113">-DefaultProfile</span></span>
<span data-ttu-id="0d1a5-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0d1a5-115">-Path</span><span class="sxs-lookup"><span data-stu-id="0d1a5-115">-Path</span></span>
<span data-ttu-id="0d1a5-116">Specifica il percorso di data Lake Store del file o della cartella, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="0d1a5-116">Specifies the Data Lake Store path of the file or folder, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="0d1a5-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d1a5-117">CommonParameters</span></span>
<span data-ttu-id="0d1a5-118">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0d1a5-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d1a5-119">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0d1a5-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d1a5-120">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0d1a5-120">INPUTS</span></span>

### <span data-ttu-id="0d1a5-121">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1a5-121">System.String</span></span>

### <span data-ttu-id="0d1a5-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="0d1a5-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="0d1a5-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0d1a5-123">OUTPUTS</span></span>

### <span data-ttu-id="0d1a5-124">System. String</span><span class="sxs-lookup"><span data-stu-id="0d1a5-124">System.String</span></span>

## <span data-ttu-id="0d1a5-125">Note</span><span class="sxs-lookup"><span data-stu-id="0d1a5-125">NOTES</span></span>
* <span data-ttu-id="0d1a5-126">Alias: Get-AdlStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0d1a5-126">Alias: Get-AdlStoreItemPermission</span></span>

## <span data-ttu-id="0d1a5-127">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0d1a5-127">RELATED LINKS</span></span>

[<span data-ttu-id="0d1a5-128">Set-AzDataLakeStoreItemPermission</span><span class="sxs-lookup"><span data-stu-id="0d1a5-128">Set-AzDataLakeStoreItemPermission</span></span>](./Set-AzDataLakeStoreItemPermission.md)


