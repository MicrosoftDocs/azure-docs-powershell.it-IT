---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3fe38645f4903e2020199b10b277da856046ac59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519658"
---
# <span data-ttu-id="601b0-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="601b0-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="601b0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="601b0-102">SYNOPSIS</span></span>
<span data-ttu-id="601b0-103">Elenca le code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="601b0-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="601b0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="601b0-104">SYNTAX</span></span>

### <span data-ttu-id="601b0-105">QueueName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="601b0-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="601b0-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="601b0-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="601b0-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="601b0-107">DESCRIPTION</span></span>
<span data-ttu-id="601b0-108">Il cmdlet **Get-AzureStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="601b0-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="601b0-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="601b0-109">EXAMPLES</span></span>

### <span data-ttu-id="601b0-110">Esempio 1: elencare tutte le code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="601b0-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="601b0-111">Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="601b0-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="601b0-112">Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="601b0-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="601b0-113">Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="601b0-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="601b0-114">Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda</span><span class="sxs-lookup"><span data-stu-id="601b0-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="601b0-115">Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="601b0-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="601b0-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="601b0-116">PARAMETERS</span></span>

### <span data-ttu-id="601b0-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="601b0-117">-Context</span></span>
<span data-ttu-id="601b0-118">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="601b0-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="601b0-119">Puoi crearlo usando il cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="601b0-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="601b0-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="601b0-120">-Name</span></span>
<span data-ttu-id="601b0-121">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="601b0-121">Specifies a name.</span></span>
<span data-ttu-id="601b0-122">Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.</span><span class="sxs-lookup"><span data-stu-id="601b0-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="601b0-123">Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.</span><span class="sxs-lookup"><span data-stu-id="601b0-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: True
```

### <span data-ttu-id="601b0-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="601b0-124">-Prefix</span></span>
<span data-ttu-id="601b0-125">Specifica un prefisso usato nel nome delle code che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="601b0-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

```yaml
Type: String
Parameter Sets: QueuePrefix
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="601b0-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601b0-126">CommonParameters</span></span>
<span data-ttu-id="601b0-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="601b0-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601b0-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="601b0-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601b0-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="601b0-129">INPUTS</span></span>

### <span data-ttu-id="601b0-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="601b0-130">IStorageContext</span></span>

<span data-ttu-id="601b0-131">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="601b0-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="601b0-132">Stringa</span><span class="sxs-lookup"><span data-stu-id="601b0-132">String</span></span>

<span data-ttu-id="601b0-133">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="601b0-133">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="601b0-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="601b0-134">OUTPUTS</span></span>

### <span data-ttu-id="601b0-135">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="601b0-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="601b0-136">Note</span><span class="sxs-lookup"><span data-stu-id="601b0-136">NOTES</span></span>

## <span data-ttu-id="601b0-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="601b0-137">RELATED LINKS</span></span>

[<span data-ttu-id="601b0-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="601b0-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="601b0-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="601b0-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


