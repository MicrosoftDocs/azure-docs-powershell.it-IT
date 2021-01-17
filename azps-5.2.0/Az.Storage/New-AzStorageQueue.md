---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324727"
---
# <span data-ttu-id="1c4d3-101">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1c4d3-101">New-AzStorageQueue</span></span>

## <span data-ttu-id="1c4d3-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1c4d3-102">SYNOPSIS</span></span>
<span data-ttu-id="1c4d3-103">Crea una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-103">Creates a storage queue.</span></span>

## <span data-ttu-id="1c4d3-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1c4d3-104">SYNTAX</span></span>

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1c4d3-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1c4d3-105">DESCRIPTION</span></span>
<span data-ttu-id="1c4d3-106">Il cmdlet **New-AzStorageQueue** crea una coda di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-106">The **New-AzStorageQueue** cmdlet creates a storage queue in Azure.</span></span>

## <span data-ttu-id="1c4d3-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1c4d3-107">EXAMPLES</span></span>

### <span data-ttu-id="1c4d3-108">Esempio 1: creare una coda di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="1c4d3-108">Example 1: Create an Azure storage queue</span></span>
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

<span data-ttu-id="1c4d3-109">Questo esempio crea una coda di archiviazione denominata queueabc.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-109">This example creates a storage queue named queueabc.</span></span>

### <span data-ttu-id="1c4d3-110">Esempio 2: creare più code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="1c4d3-110">Example 2: Create multiple azure storage queues</span></span>
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

<span data-ttu-id="1c4d3-111">Questo esempio crea più code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-111">This example creates multiple storage queues.</span></span>
<span data-ttu-id="1c4d3-112">Usa il metodo Split della classe String .NET e quindi passa i nomi sulla pipeline.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-112">It uses the Split method of the .NET String class and then passes the names on the pipeline.</span></span>

## <span data-ttu-id="1c4d3-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1c4d3-113">PARAMETERS</span></span>

### <span data-ttu-id="1c4d3-114">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1c4d3-114">-Context</span></span>
<span data-ttu-id="1c4d3-115">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-115">Specifies the Azure storage context.</span></span>
<span data-ttu-id="1c4d3-116">Puoi crearlo usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-116">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1c4d3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c4d3-117">-DefaultProfile</span></span>
<span data-ttu-id="1c4d3-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c4d3-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="1c4d3-119">-Name</span></span>
<span data-ttu-id="1c4d3-120">Specifica un nome per la coda.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-120">Specifies a name for the queue.</span></span>

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

### <span data-ttu-id="1c4d3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c4d3-121">CommonParameters</span></span>
<span data-ttu-id="1c4d3-122">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c4d3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c4d3-123">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c4d3-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c4d3-124">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1c4d3-124">INPUTS</span></span>

### <span data-ttu-id="1c4d3-125">System. String</span><span class="sxs-lookup"><span data-stu-id="1c4d3-125">System.String</span></span>

### <span data-ttu-id="1c4d3-126">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1c4d3-126">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1c4d3-127">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1c4d3-127">OUTPUTS</span></span>

### <span data-ttu-id="1c4d3-128">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1c4d3-128">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="1c4d3-129">Note</span><span class="sxs-lookup"><span data-stu-id="1c4d3-129">NOTES</span></span>

## <span data-ttu-id="1c4d3-130">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1c4d3-130">RELATED LINKS</span></span>

[<span data-ttu-id="1c4d3-131">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1c4d3-131">Get-AzStorageQueue</span></span>](./Get-AzStorageQueue.md)

[<span data-ttu-id="1c4d3-132">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="1c4d3-132">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


