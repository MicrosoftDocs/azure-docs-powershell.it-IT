---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 3B4F32F3-51ED-4851-B38F-172658186C96
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageTable.md
ms.openlocfilehash: 53bb5f3a34cddf9e74bfb9d9c9f1bd1d109d8f6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515868"
---
# <span data-ttu-id="d6eaa-101">New-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d6eaa-101">New-AzureStorageTable</span></span>

## <span data-ttu-id="d6eaa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d6eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="d6eaa-103">Crea una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-103">Creates a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6eaa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d6eaa-104">SYNTAX</span></span>

```
New-AzureStorageTable [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="d6eaa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d6eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="d6eaa-106">Il cmdlet **New-AzureStorageTable** crea una tabella di archiviazione associata all'account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-106">The **New-AzureStorageTable** cmdlet creates a storage table associated with the storage account in Azure.</span></span>

## <span data-ttu-id="d6eaa-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d6eaa-107">EXAMPLES</span></span>

### <span data-ttu-id="d6eaa-108">Esempio 1: creare una tabella di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="d6eaa-108">Example 1: Create an azure storage table</span></span>
```
PS C:\>New-AzureStorageTable -Name "tableabc"
```

<span data-ttu-id="d6eaa-109">Questo comando crea una tabella di archiviazione con il nome tableabc.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-109">This command creates a storage table with a name of tableabc.</span></span>

### <span data-ttu-id="d6eaa-110">Esempio 2: creare più tabelle di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="d6eaa-110">Example 2: Create multiple azure storage tables</span></span>
```
PS C:\>"table1 table2 table3".split() | New-AzureStorageTable
```

<span data-ttu-id="d6eaa-111">Questo comando crea più tabelle.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-111">This command creates multiple tables.</span></span>
<span data-ttu-id="d6eaa-112">Usa il metodo **Split** della classe **String** .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-112">It uses the **Split** method of the .NET **String** class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="d6eaa-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d6eaa-113">PARAMETERS</span></span>

### <span data-ttu-id="d6eaa-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="d6eaa-114">-Context</span></span>
<span data-ttu-id="d6eaa-115">Specifica il contesto di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-115">Specifies the storage context.</span></span>
<span data-ttu-id="d6eaa-116">Per crearlo, puoi usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-116">To create it, you can use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="d6eaa-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="d6eaa-117">-Name</span></span>
<span data-ttu-id="d6eaa-118">Specifica un nome per la nuova tabella.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-118">Specifies a name for the new table.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6eaa-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6eaa-119">CommonParameters</span></span>
<span data-ttu-id="d6eaa-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6eaa-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6eaa-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6eaa-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6eaa-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d6eaa-122">INPUTS</span></span>

### <span data-ttu-id="d6eaa-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="d6eaa-123">IStorageContext</span></span>

<span data-ttu-id="d6eaa-124">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d6eaa-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="d6eaa-125">Stringa</span><span class="sxs-lookup"><span data-stu-id="d6eaa-125">String</span></span>

<span data-ttu-id="d6eaa-126">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="d6eaa-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="d6eaa-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d6eaa-127">OUTPUTS</span></span>

### <span data-ttu-id="d6eaa-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d6eaa-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageTable</span></span>

## <span data-ttu-id="d6eaa-129">Note</span><span class="sxs-lookup"><span data-stu-id="d6eaa-129">NOTES</span></span>

## <span data-ttu-id="d6eaa-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d6eaa-130">RELATED LINKS</span></span>

[<span data-ttu-id="d6eaa-131">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d6eaa-131">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)

[<span data-ttu-id="d6eaa-132">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="d6eaa-132">Remove-AzureStorageTable</span></span>](./Remove-AzureStorageTable.md)


