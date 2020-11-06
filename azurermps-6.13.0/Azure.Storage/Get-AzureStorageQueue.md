---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
ms.openlocfilehash: 077d8139817c3998e27300d8c86c809b4da9e630
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514016"
---
# <span data-ttu-id="941ee-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="941ee-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="941ee-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="941ee-102">SYNOPSIS</span></span>
<span data-ttu-id="941ee-103">Elenca le code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="941ee-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="941ee-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="941ee-104">SYNTAX</span></span>

### <span data-ttu-id="941ee-105">QueueName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="941ee-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="941ee-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="941ee-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="941ee-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="941ee-107">DESCRIPTION</span></span>
<span data-ttu-id="941ee-108">Il cmdlet **Get-AzureStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="941ee-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="941ee-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="941ee-109">EXAMPLES</span></span>

### <span data-ttu-id="941ee-110">Esempio 1: elencare tutte le code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="941ee-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="941ee-111">Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="941ee-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="941ee-112">Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="941ee-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="941ee-113">Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="941ee-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="941ee-114">Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda</span><span class="sxs-lookup"><span data-stu-id="941ee-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="941ee-115">Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="941ee-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="941ee-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="941ee-116">PARAMETERS</span></span>

### <span data-ttu-id="941ee-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="941ee-117">-Context</span></span>
<span data-ttu-id="941ee-118">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="941ee-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="941ee-119">Puoi crearlo usando il cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="941ee-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="941ee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="941ee-120">-DefaultProfile</span></span>
<span data-ttu-id="941ee-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="941ee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="941ee-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="941ee-122">-Name</span></span>
<span data-ttu-id="941ee-123">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="941ee-123">Specifies a name.</span></span>
<span data-ttu-id="941ee-124">Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.</span><span class="sxs-lookup"><span data-stu-id="941ee-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="941ee-125">Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.</span><span class="sxs-lookup"><span data-stu-id="941ee-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="941ee-126">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="941ee-126">-Prefix</span></span>
<span data-ttu-id="941ee-127">Specifica un prefisso usato nel nome delle code che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="941ee-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="941ee-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="941ee-128">CommonParameters</span></span>
<span data-ttu-id="941ee-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="941ee-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="941ee-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="941ee-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="941ee-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="941ee-131">INPUTS</span></span>

### <span data-ttu-id="941ee-132">System. String</span><span class="sxs-lookup"><span data-stu-id="941ee-132">System.String</span></span>

### <span data-ttu-id="941ee-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="941ee-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="941ee-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="941ee-134">OUTPUTS</span></span>

### <span data-ttu-id="941ee-135">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="941ee-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="941ee-136">Note</span><span class="sxs-lookup"><span data-stu-id="941ee-136">NOTES</span></span>

## <span data-ttu-id="941ee-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="941ee-137">RELATED LINKS</span></span>

[<span data-ttu-id="941ee-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="941ee-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="941ee-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="941ee-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


