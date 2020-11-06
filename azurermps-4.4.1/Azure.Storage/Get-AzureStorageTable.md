---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3ba13fb1ee18f5dcc35b81ff70ebd7c5a61d1e4d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93508892"
---
# <span data-ttu-id="6e33b-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e33b-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="6e33b-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6e33b-102">SYNOPSIS</span></span>
<span data-ttu-id="6e33b-103">Elenca le tabelle di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6e33b-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6e33b-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6e33b-104">SYNTAX</span></span>

### <span data-ttu-id="6e33b-105">TableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6e33b-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="6e33b-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="6e33b-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="6e33b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6e33b-107">DESCRIPTION</span></span>
<span data-ttu-id="6e33b-108">Il cmdlet **Get-AzureStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="6e33b-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="6e33b-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6e33b-109">EXAMPLES</span></span>

### <span data-ttu-id="6e33b-110">Esempio 1: elencare tutte le tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="6e33b-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="6e33b-111">Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6e33b-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="6e33b-112">Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="6e33b-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="6e33b-113">Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="6e33b-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="6e33b-114">Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella</span><span class="sxs-lookup"><span data-stu-id="6e33b-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="6e33b-115">Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="6e33b-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="6e33b-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6e33b-116">PARAMETERS</span></span>

### <span data-ttu-id="6e33b-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="6e33b-117">-Context</span></span>
<span data-ttu-id="6e33b-118">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6e33b-118">Specifies the storage context.</span></span>
<span data-ttu-id="6e33b-119">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6e33b-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6e33b-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="6e33b-120">-Name</span></span>
<span data-ttu-id="6e33b-121">Specifica il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="6e33b-121">Specifies the table name.</span></span>
<span data-ttu-id="6e33b-122">Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.</span><span class="sxs-lookup"><span data-stu-id="6e33b-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="6e33b-123">In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.</span><span class="sxs-lookup"><span data-stu-id="6e33b-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="6e33b-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="6e33b-124">-Prefix</span></span>
<span data-ttu-id="6e33b-125">Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="6e33b-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="6e33b-126">Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.</span><span class="sxs-lookup"><span data-stu-id="6e33b-126">You can use this to find all tables that start with the same string, such as table.</span></span>

```yaml
Type: String
Parameter Sets: TablePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e33b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e33b-127">CommonParameters</span></span>
<span data-ttu-id="6e33b-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e33b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e33b-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6e33b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e33b-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6e33b-130">INPUTS</span></span>

### <span data-ttu-id="6e33b-131">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e33b-131">IStorageContext</span></span>

<span data-ttu-id="6e33b-132">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6e33b-132">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="6e33b-133">Stringa</span><span class="sxs-lookup"><span data-stu-id="6e33b-133">String</span></span>

<span data-ttu-id="6e33b-134">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="6e33b-134">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="6e33b-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6e33b-135">OUTPUTS</span></span>

### <span data-ttu-id="6e33b-136">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e33b-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="6e33b-137">Note</span><span class="sxs-lookup"><span data-stu-id="6e33b-137">NOTES</span></span>

## <span data-ttu-id="6e33b-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6e33b-138">RELATED LINKS</span></span>

[<span data-ttu-id="6e33b-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e33b-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="6e33b-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="6e33b-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)

