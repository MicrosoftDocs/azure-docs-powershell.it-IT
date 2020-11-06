---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 335588D4-4D2C-4DBD-B6B2-B1227C4AF9A9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/get-azurermdatalakestoreitemowner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemOwner.md
ms.openlocfilehash: 4276b9477e51165e01c716095d5f4e2a4ea6ca69
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511732"
---
# <span data-ttu-id="6fc7b-101">Get-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6fc7b-101">Get-AzureRmDataLakeStoreItemOwner</span></span>

## <span data-ttu-id="6fc7b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6fc7b-102">SYNOPSIS</span></span>
<span data-ttu-id="6fc7b-103">Ottiene il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-103">Gets the owner of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fc7b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6fc7b-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemOwner [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Type] <Owner>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6fc7b-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6fc7b-105">DESCRIPTION</span></span>
<span data-ttu-id="6fc7b-106">Il cmdlet **Get-AzureRmDataLakeStoreItemOwner** ottiene il proprietario di un file o di una cartella in data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-106">The **Get-AzureRmDataLakeStoreItemOwner** cmdlet gets the owner of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="6fc7b-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6fc7b-107">EXAMPLES</span></span>

### <span data-ttu-id="6fc7b-108">Esempio 1: ottenere il proprietario per una directory</span><span class="sxs-lookup"><span data-stu-id="6fc7b-108">Example 1: Get the owner for a directory</span></span>
```
PS C:\>Get-AzureRmDataLakeStoreItemOwner -AccountName "ContosoADL" -Path / -Type User
```

<span data-ttu-id="6fc7b-109">Questo comando consente di ottenere il proprietario dell'utente per la directory radice dell'account ContosoADL.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-109">This command gets the user owner for the root directory of the ContosoADL account.</span></span>

## <span data-ttu-id="6fc7b-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6fc7b-110">PARAMETERS</span></span>

### <span data-ttu-id="6fc7b-111">-Account</span><span class="sxs-lookup"><span data-stu-id="6fc7b-111">-Account</span></span>
<span data-ttu-id="6fc7b-112">Specifica il nome dell'account di data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="6fc7b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fc7b-113">-DefaultProfile</span></span>
<span data-ttu-id="6fc7b-114">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6fc7b-115">-Path</span><span class="sxs-lookup"><span data-stu-id="6fc7b-115">-Path</span></span>
<span data-ttu-id="6fc7b-116">Specifica il percorso di data Lake Store di un elemento, a partire dalla directory radice (/).</span><span class="sxs-lookup"><span data-stu-id="6fc7b-116">Specifies the Data Lake Store path of an item, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="6fc7b-117">-Digitare</span><span class="sxs-lookup"><span data-stu-id="6fc7b-117">-Type</span></span>
<span data-ttu-id="6fc7b-118">Specifica il tipo di proprietario da ottenere.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-118">Specifies the type of owner to get.</span></span>
<span data-ttu-id="6fc7b-119">I valori accettabili per questo parametro sono: utente e gruppo.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-119">The acceptable values for this parameter are: User and Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner
Parameter Sets: (All)
Aliases:
Accepted values: User, Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6fc7b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fc7b-120">CommonParameters</span></span>
<span data-ttu-id="6fc7b-121">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fc7b-122">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fc7b-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fc7b-123">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6fc7b-123">INPUTS</span></span>

### <span data-ttu-id="6fc7b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc7b-124">System.String</span></span>

### <span data-ttu-id="6fc7b-125">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="6fc7b-125">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

### <span data-ttu-id="6fc7b-126">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreEnums + Owner</span><span class="sxs-lookup"><span data-stu-id="6fc7b-126">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreEnums+Owner</span></span>

## <span data-ttu-id="6fc7b-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6fc7b-127">OUTPUTS</span></span>

### <span data-ttu-id="6fc7b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6fc7b-128">System.String</span></span>
<span data-ttu-id="6fc7b-129">Il proprietario dell'elemento specificato.</span><span class="sxs-lookup"><span data-stu-id="6fc7b-129">The owner of the specified item.</span></span>

## <span data-ttu-id="6fc7b-130">Note</span><span class="sxs-lookup"><span data-stu-id="6fc7b-130">NOTES</span></span>

## <span data-ttu-id="6fc7b-131">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6fc7b-131">RELATED LINKS</span></span>

[<span data-ttu-id="6fc7b-132">Set-AzureRmDataLakeStoreItemOwner</span><span class="sxs-lookup"><span data-stu-id="6fc7b-132">Set-AzureRmDataLakeStoreItemOwner</span></span>](./Set-AzureRmDataLakeStoreItemOwner.md)


