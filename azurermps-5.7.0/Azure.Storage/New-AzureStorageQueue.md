---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageQueue.md
ms.openlocfilehash: 6363b8030571d6cf3e89b30229395b16cdb5f44b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93515887"
---
# <span data-ttu-id="c3978-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c3978-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="c3978-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c3978-102">SYNOPSIS</span></span>
<span data-ttu-id="c3978-103">Crea una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3978-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3978-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c3978-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="c3978-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c3978-105">DESCRIPTION</span></span>
<span data-ttu-id="c3978-106">Il cmdlet **New-AzureStorageQueue** crea una coda di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="c3978-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="c3978-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c3978-107">EXAMPLES</span></span>

### <span data-ttu-id="c3978-108">Esempio 1: creare una coda di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="c3978-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="c3978-109">Questo esempio crea una coda di archiviazione denominata queueabc.</span><span class="sxs-lookup"><span data-stu-id="c3978-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="c3978-110">Esempio 2: creare più code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="c3978-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="c3978-111">Questo esempio crea più code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c3978-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="c3978-112">Usa il metodo Split della classe String .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="c3978-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="c3978-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c3978-113">PARAMETERS</span></span>

### <span data-ttu-id="c3978-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c3978-114">-Context</span></span>
<span data-ttu-id="c3978-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c3978-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c3978-116">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c3978-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c3978-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="c3978-117">-Name</span></span>
<span data-ttu-id="c3978-118">Specifica un nome per la coda.</span><span class="sxs-lookup"><span data-stu-id="c3978-118">Specifies a name for the queue.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3978-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3978-119">CommonParameters</span></span>
<span data-ttu-id="c3978-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3978-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3978-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3978-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3978-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c3978-122">INPUTS</span></span>

### <span data-ttu-id="c3978-123">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c3978-123">IStorageContext</span></span>

<span data-ttu-id="c3978-124">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c3978-124">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c3978-125">Stringa</span><span class="sxs-lookup"><span data-stu-id="c3978-125">String</span></span>

<span data-ttu-id="c3978-126">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c3978-126">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c3978-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c3978-127">OUTPUTS</span></span>

### <span data-ttu-id="c3978-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c3978-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="c3978-129">Note</span><span class="sxs-lookup"><span data-stu-id="c3978-129">NOTES</span></span>

## <span data-ttu-id="c3978-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c3978-130">RELATED LINKS</span></span>

[<span data-ttu-id="c3978-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c3978-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="c3978-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c3978-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


