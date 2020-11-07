---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: 834400893dc3d2065a8ca3f0b27783e0a4d5604e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866607"
---
# <span data-ttu-id="0ad0e-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0ad0e-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="0ad0e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0ad0e-102">SYNOPSIS</span></span>
<span data-ttu-id="0ad0e-103">Elenca le tabelle di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ad0e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0ad0e-104">SYNTAX</span></span>

### <span data-ttu-id="0ad0e-105">TableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0ad0e-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0ad0e-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="0ad0e-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0ad0e-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0ad0e-107">DESCRIPTION</span></span>
<span data-ttu-id="0ad0e-108">Il cmdlet **Get-AzureStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="0ad0e-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0ad0e-109">EXAMPLES</span></span>

### <span data-ttu-id="0ad0e-110">Esempio 1: elencare tutte le tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0ad0e-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="0ad0e-111">Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="0ad0e-112">Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="0ad0e-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="0ad0e-113">Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="0ad0e-114">Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella</span><span class="sxs-lookup"><span data-stu-id="0ad0e-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="0ad0e-115">Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="0ad0e-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0ad0e-116">PARAMETERS</span></span>

### <span data-ttu-id="0ad0e-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0ad0e-117">-Context</span></span>
<span data-ttu-id="0ad0e-118">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-118">Specifies the storage context.</span></span>
<span data-ttu-id="0ad0e-119">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad0e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ad0e-120">-DefaultProfile</span></span>
<span data-ttu-id="0ad0e-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ad0e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0ad0e-122">-Name</span></span>
<span data-ttu-id="0ad0e-123">Specifica il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-123">Specifies the table name.</span></span>
<span data-ttu-id="0ad0e-124">Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="0ad0e-125">In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0ad0e-126">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="0ad0e-126">-Prefix</span></span>
<span data-ttu-id="0ad0e-127">Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="0ad0e-128">Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-128">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: System.String
Parameter Sets: TablePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0ad0e-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ad0e-129">CommonParameters</span></span>
<span data-ttu-id="0ad0e-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ad0e-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ad0e-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ad0e-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ad0e-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0ad0e-132">INPUTS</span></span>

### <span data-ttu-id="0ad0e-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0ad0e-133">System.String</span></span>

### <span data-ttu-id="0ad0e-134">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0ad0e-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0ad0e-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0ad0e-135">OUTPUTS</span></span>

### <span data-ttu-id="0ad0e-136">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0ad0e-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="0ad0e-137">Note</span><span class="sxs-lookup"><span data-stu-id="0ad0e-137">NOTES</span></span>

## <span data-ttu-id="0ad0e-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0ad0e-138">RELATED LINKS</span></span>

[<span data-ttu-id="0ad0e-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0ad0e-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="0ad0e-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0ad0e-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


