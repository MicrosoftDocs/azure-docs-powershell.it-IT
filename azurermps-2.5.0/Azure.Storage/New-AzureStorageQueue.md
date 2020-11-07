---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/new-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: a028d2528d74e9372bfca28ccfb085f119486ce7
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866594"
---
# <span data-ttu-id="a1b23-101">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a1b23-101">New-AzureStorageQueue</span></span>

## <span data-ttu-id="a1b23-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a1b23-102">SYNOPSIS</span></span>
<span data-ttu-id="a1b23-103">Crea una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1b23-103">Creates a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1b23-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a1b23-104">SYNTAX</span></span>

```
New-AzureStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1b23-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a1b23-105">DESCRIPTION</span></span>
<span data-ttu-id="a1b23-106">Il cmdlet **New-AzureStorageQueue** crea una coda di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b23-106">The **New-AzureStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="a1b23-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a1b23-107">EXAMPLES</span></span>

### <span data-ttu-id="a1b23-108">Esempio 1: creare una coda di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a1b23-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzureStorageQueue -Name "queueabc"
```

<span data-ttu-id="a1b23-109">Questo esempio crea una coda di archiviazione denominata queueabc.</span><span class="sxs-lookup"><span data-stu-id="a1b23-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="a1b23-110">Esempio 2: creare più code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="a1b23-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzureStorageQueue
```

<span data-ttu-id="a1b23-111">Questo esempio crea più code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="a1b23-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="a1b23-112">Usa il metodo Split della classe String .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="a1b23-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="a1b23-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a1b23-113">PARAMETERS</span></span>

### <span data-ttu-id="a1b23-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a1b23-114">-Context</span></span>
<span data-ttu-id="a1b23-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b23-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="a1b23-116">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a1b23-116">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a1b23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1b23-117">-DefaultProfile</span></span>
<span data-ttu-id="a1b23-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a1b23-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1b23-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="a1b23-119">-Name</span></span>
<span data-ttu-id="a1b23-120">Specifica un nome per la coda.</span><span class="sxs-lookup"><span data-stu-id="a1b23-120">Specifies a name for the queue.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a1b23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1b23-121">CommonParameters</span></span>
<span data-ttu-id="a1b23-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1b23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1b23-123">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1b23-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1b23-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a1b23-124">INPUTS</span></span>

### <span data-ttu-id="a1b23-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a1b23-125">System.String</span></span>

### <span data-ttu-id="a1b23-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a1b23-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a1b23-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a1b23-127">OUTPUTS</span></span>

### <span data-ttu-id="a1b23-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a1b23-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="a1b23-129">Note</span><span class="sxs-lookup"><span data-stu-id="a1b23-129">NOTES</span></span>

## <span data-ttu-id="a1b23-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a1b23-130">RELATED LINKS</span></span>

[<span data-ttu-id="a1b23-131">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a1b23-131">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="a1b23-132">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="a1b23-132">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


