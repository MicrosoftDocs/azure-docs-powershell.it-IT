---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3f2bccab190fc27b5e97ecf3af502d3488f28998
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507032"
---
# <span data-ttu-id="1a217-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1a217-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="1a217-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1a217-102">SYNOPSIS</span></span>
<span data-ttu-id="1a217-103">Elenca le tabelle di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1a217-103">Lists the storage tables.</span></span>

## <span data-ttu-id="1a217-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1a217-104">SYNTAX</span></span>

### <span data-ttu-id="1a217-105">TableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1a217-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="1a217-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="1a217-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="1a217-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1a217-107">DESCRIPTION</span></span>
<span data-ttu-id="1a217-108">Il cmdlet **Get-AzureStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="1a217-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="1a217-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1a217-109">EXAMPLES</span></span>

### <span data-ttu-id="1a217-110">Esempio 1: elencare tutte le tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="1a217-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="1a217-111">Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1a217-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="1a217-112">Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="1a217-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="1a217-113">Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="1a217-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="1a217-114">Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella</span><span class="sxs-lookup"><span data-stu-id="1a217-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="1a217-115">Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="1a217-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="1a217-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1a217-116">PARAMETERS</span></span>

### <span data-ttu-id="1a217-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1a217-117">-Context</span></span>
<span data-ttu-id="1a217-118">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1a217-118">Specifies the storage context.</span></span>
<span data-ttu-id="1a217-119">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1a217-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1a217-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="1a217-120">-Name</span></span>
<span data-ttu-id="1a217-121">Specifica il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="1a217-121">Specifies the table name.</span></span>
<span data-ttu-id="1a217-122">Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.</span><span class="sxs-lookup"><span data-stu-id="1a217-122">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="1a217-123">In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.</span><span class="sxs-lookup"><span data-stu-id="1a217-123">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

```yaml
Type: String
Parameter Sets: TableName
Aliases: N, Table

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a217-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="1a217-124">-Prefix</span></span>
<span data-ttu-id="1a217-125">Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="1a217-125">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="1a217-126">Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.</span><span class="sxs-lookup"><span data-stu-id="1a217-126">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="1a217-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a217-127">CommonParameters</span></span>
<span data-ttu-id="1a217-128">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a217-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a217-129">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a217-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a217-130">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1a217-130">INPUTS</span></span>

## <span data-ttu-id="1a217-131">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1a217-131">OUTPUTS</span></span>

## <span data-ttu-id="1a217-132">Note</span><span class="sxs-lookup"><span data-stu-id="1a217-132">NOTES</span></span>

## <span data-ttu-id="1a217-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1a217-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a217-134">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1a217-134">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="1a217-135">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="1a217-135">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


