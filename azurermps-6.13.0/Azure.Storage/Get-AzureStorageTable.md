---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 4631D36F-926A-4279-AA4D-5F694C18081E
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageTable.md
ms.openlocfilehash: 1d31bff44bb93db1022a88a464c2942a2a3fadbb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687395"
---
# <span data-ttu-id="0f560-101">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0f560-101">Get-AzureStorageTable</span></span>

## <span data-ttu-id="0f560-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0f560-102">SYNOPSIS</span></span>
<span data-ttu-id="0f560-103">Elenca le tabelle di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0f560-103">Lists the storage tables.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f560-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f560-104">SYNTAX</span></span>

### <span data-ttu-id="0f560-105">TableName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0f560-105">TableName (Default)</span></span>
```
Get-AzureStorageTable [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f560-106">TablePrefix</span><span class="sxs-lookup"><span data-stu-id="0f560-106">TablePrefix</span></span>
```
Get-AzureStorageTable -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0f560-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0f560-107">DESCRIPTION</span></span>
<span data-ttu-id="0f560-108">Il cmdlet **Get-AzureStorageTable** elenca le tabelle di archiviazione associate all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="0f560-108">The **Get-AzureStorageTable** cmdlet lists the storage tables associated with the storage account in Azure.</span></span>

## <span data-ttu-id="0f560-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f560-109">EXAMPLES</span></span>

### <span data-ttu-id="0f560-110">Esempio 1: elencare tutte le tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="0f560-110">Example 1: List all Azure Storage tables</span></span>
```
PS C:\>Get-AzureStorageTable
```

<span data-ttu-id="0f560-111">Questo comando consente di ottenere tutte le tabelle di archiviazione per un account di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0f560-111">This command gets all storage tables for a Storage account.</span></span>

### <span data-ttu-id="0f560-112">Esempio 2: elencare le tabelle di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="0f560-112">Example 2: List Azure Storage tables using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageTable -Name table*
```

<span data-ttu-id="0f560-113">Questo comando usa un carattere jolly per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="0f560-113">This command uses a wildcard character to get storage tables whose name starts with table.</span></span>

### <span data-ttu-id="0f560-114">Esempio 3: elenca tabelle di archiviazione di Azure con prefisso di nome di tabella</span><span class="sxs-lookup"><span data-stu-id="0f560-114">Example 3: List Azure Storage tables using table name prefix</span></span>
```
PS C:\>Get-AzureStorageTable -Prefix "table"
```

<span data-ttu-id="0f560-115">Questo comando usa il parametro *Prefix* per ottenere le tabelle di archiviazione il cui nome inizia con la tabella.</span><span class="sxs-lookup"><span data-stu-id="0f560-115">This command uses the *Prefix* parameter to get storage tables whose name starts with table.</span></span>

## <span data-ttu-id="0f560-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0f560-116">PARAMETERS</span></span>

### <span data-ttu-id="0f560-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="0f560-117">-Context</span></span>
<span data-ttu-id="0f560-118">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="0f560-118">Specifies the storage context.</span></span>
<span data-ttu-id="0f560-119">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="0f560-119">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0f560-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f560-120">-DefaultProfile</span></span>
<span data-ttu-id="0f560-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0f560-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f560-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="0f560-122">-Name</span></span>
<span data-ttu-id="0f560-123">Specifica il nome della tabella.</span><span class="sxs-lookup"><span data-stu-id="0f560-123">Specifies the table name.</span></span>
<span data-ttu-id="0f560-124">Se il nome della tabella è vuoto, il cmdlet elenca tutte le tabelle.</span><span class="sxs-lookup"><span data-stu-id="0f560-124">If the table name is empty, the cmdlet lists all the tables.</span></span>
<span data-ttu-id="0f560-125">In caso contrario, elenca tutte le tabelle che corrispondono al nome specificato o al modello di nome normale.</span><span class="sxs-lookup"><span data-stu-id="0f560-125">Otherwise, it lists all tables that match the specified name or the regular name pattern.</span></span>

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

### <span data-ttu-id="0f560-126">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="0f560-126">-Prefix</span></span>
<span data-ttu-id="0f560-127">Specifica un prefisso usato nel nome della tabella o delle tabelle che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="0f560-127">Specifies a prefix used in the name of the table or tables you want to get.</span></span>
<span data-ttu-id="0f560-128">Puoi usare questa procedura per trovare tutte le tabelle che iniziano con la stessa stringa, ad esempio tabella.</span><span class="sxs-lookup"><span data-stu-id="0f560-128">You can use this to find all tables that start with the same string, such as table.</span></span>

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

### <span data-ttu-id="0f560-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f560-129">CommonParameters</span></span>
<span data-ttu-id="0f560-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f560-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f560-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f560-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f560-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0f560-132">INPUTS</span></span>

### <span data-ttu-id="0f560-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0f560-133">System.String</span></span>

### <span data-ttu-id="0f560-134">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0f560-134">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0f560-135">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f560-135">OUTPUTS</span></span>

### <span data-ttu-id="0f560-136">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0f560-136">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="0f560-137">Note</span><span class="sxs-lookup"><span data-stu-id="0f560-137">NOTES</span></span>

## <span data-ttu-id="0f560-138">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f560-138">RELATED LINKS</span></span>

[<span data-ttu-id="0f560-139">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0f560-139">New-AzureStorageTable</span></span>](./New-AzureStorageTable.md)

[<span data-ttu-id="0f560-140">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="0f560-140">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


