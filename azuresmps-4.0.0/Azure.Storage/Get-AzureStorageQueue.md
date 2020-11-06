---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: 11a8ffe26a65bf2ecabab7807d8e54bc23b629fc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93507060"
---
# <span data-ttu-id="ceb10-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ceb10-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="ceb10-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ceb10-102">SYNOPSIS</span></span>
<span data-ttu-id="ceb10-103">Elenca le code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ceb10-103">Lists storage queues.</span></span>

## <span data-ttu-id="ceb10-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ceb10-104">SYNTAX</span></span>

### <span data-ttu-id="ceb10-105">QueueName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ceb10-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [<CommonParameters>]
```

### <span data-ttu-id="ceb10-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="ceb10-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="ceb10-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ceb10-107">DESCRIPTION</span></span>
<span data-ttu-id="ceb10-108">Il cmdlet **Get-AzureStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb10-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="ceb10-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ceb10-109">EXAMPLES</span></span>

### <span data-ttu-id="ceb10-110">Esempio 1: elencare tutte le code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="ceb10-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="ceb10-111">Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="ceb10-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="ceb10-112">Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="ceb10-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="ceb10-113">Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="ceb10-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="ceb10-114">Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda</span><span class="sxs-lookup"><span data-stu-id="ceb10-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="ceb10-115">Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="ceb10-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="ceb10-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ceb10-116">PARAMETERS</span></span>

### <span data-ttu-id="ceb10-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ceb10-117">-Context</span></span>
<span data-ttu-id="ceb10-118">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ceb10-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ceb10-119">Puoi crearlo usando il cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="ceb10-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="ceb10-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ceb10-120">-Name</span></span>
<span data-ttu-id="ceb10-121">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="ceb10-121">Specifies a name.</span></span>
<span data-ttu-id="ceb10-122">Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.</span><span class="sxs-lookup"><span data-stu-id="ceb10-122">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="ceb10-123">Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.</span><span class="sxs-lookup"><span data-stu-id="ceb10-123">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

```yaml
Type: String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ceb10-124">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="ceb10-124">-Prefix</span></span>
<span data-ttu-id="ceb10-125">Specifica un prefisso usato nel nome delle code che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="ceb10-125">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="ceb10-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceb10-126">CommonParameters</span></span>
<span data-ttu-id="ceb10-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceb10-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceb10-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ceb10-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceb10-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ceb10-129">INPUTS</span></span>

## <span data-ttu-id="ceb10-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ceb10-130">OUTPUTS</span></span>

## <span data-ttu-id="ceb10-131">Note</span><span class="sxs-lookup"><span data-stu-id="ceb10-131">NOTES</span></span>

## <span data-ttu-id="ceb10-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ceb10-132">RELATED LINKS</span></span>

[<span data-ttu-id="ceb10-133">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ceb10-133">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="ceb10-134">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="ceb10-134">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


