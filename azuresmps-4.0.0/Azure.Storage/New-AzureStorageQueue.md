---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 76876cb76e65c913401d62fc7f08b3cb8b5626c0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93491434"
---
# <span data-ttu-id="74554-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="74554-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="74554-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="74554-102">SYNOPSIS</span></span>
<span data-ttu-id="74554-103">Crea una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="74554-103">Creates a storage queue.</span></span>

## <span data-ttu-id="74554-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="74554-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="74554-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="74554-105">DESCRIPTION</span></span>
<span data-ttu-id="74554-106">Il cmdlet **New-AzureStorageQueue** crea una coda di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="74554-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="74554-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="74554-107">EXAMPLES</span></span>

### <span data-ttu-id="74554-108">Esempio 1: creare una coda di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="74554-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="74554-109">Questo esempio crea una coda di archiviazione denominata queueabc.</span><span class="sxs-lookup"><span data-stu-id="74554-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="74554-110">Esempio 2: creare più code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="74554-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="74554-111">Questo esempio crea più code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="74554-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="74554-112">Usa il metodo Split della classe String .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="74554-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="74554-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="74554-113">PARAMETERS</span></span>

### <span data-ttu-id="74554-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="74554-114">-Context</span></span>
<span data-ttu-id="74554-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="74554-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="74554-116">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="74554-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="74554-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="74554-117">-Name</span></span>
<span data-ttu-id="74554-118">Specifica un nome per la coda.</span><span class="sxs-lookup"><span data-stu-id="74554-118">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="74554-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74554-119">CommonParameters</span></span>
<span data-ttu-id="74554-120">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74554-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74554-121">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74554-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74554-122">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="74554-122">INPUTS</span></span>

## <span data-ttu-id="74554-123">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="74554-123">OUTPUTS</span></span>

## <span data-ttu-id="74554-124">Note</span><span class="sxs-lookup"><span data-stu-id="74554-124">NOTES</span></span>

## <span data-ttu-id="74554-125">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="74554-125">RELATED LINKS</span></span>

[<span data-ttu-id="74554-126">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="74554-126">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="74554-127">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="74554-127">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


