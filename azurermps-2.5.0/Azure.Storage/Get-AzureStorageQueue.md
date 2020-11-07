---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestoragequeue
schema: 2.0.0
ms.openlocfilehash: 59a035a7af56a333a1ef91b5ce4aa2d1afbe5086
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93867185"
---
# <span data-ttu-id="cfe31-101">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cfe31-101">Get-AzureStorageQueue</span></span>

## <span data-ttu-id="cfe31-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cfe31-102">SYNOPSIS</span></span>
<span data-ttu-id="cfe31-103">Elenca le code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cfe31-103">Lists storage queues.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cfe31-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cfe31-104">SYNTAX</span></span>

### <span data-ttu-id="cfe31-105">QueueName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="cfe31-105">QueueName (Default)</span></span>
```
Get-AzureStorageQueue [[-Name] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cfe31-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="cfe31-106">QueuePrefix</span></span>
```
Get-AzureStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cfe31-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cfe31-107">DESCRIPTION</span></span>
<span data-ttu-id="cfe31-108">Il cmdlet **Get-AzureStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe31-108">The **Get-AzureStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="cfe31-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cfe31-109">EXAMPLES</span></span>

### <span data-ttu-id="cfe31-110">Esempio 1: elencare tutte le code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="cfe31-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue
```

<span data-ttu-id="cfe31-111">Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="cfe31-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="cfe31-112">Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="cfe31-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzureStorageQueue -Name queue*
```

<span data-ttu-id="cfe31-113">Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="cfe31-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="cfe31-114">Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda</span><span class="sxs-lookup"><span data-stu-id="cfe31-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzureStorageQueue -Prefix "queue"
```

<span data-ttu-id="cfe31-115">Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="cfe31-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="cfe31-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cfe31-116">PARAMETERS</span></span>

### <span data-ttu-id="cfe31-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cfe31-117">-Context</span></span>
<span data-ttu-id="cfe31-118">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe31-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cfe31-119">Puoi crearlo usando il cmdlet **New-AzureStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="cfe31-119">You can create it by using the **New-AzureStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="cfe31-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cfe31-120">-DefaultProfile</span></span>
<span data-ttu-id="cfe31-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="cfe31-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cfe31-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="cfe31-122">-Name</span></span>
<span data-ttu-id="cfe31-123">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="cfe31-123">Specifies a name.</span></span>
<span data-ttu-id="cfe31-124">Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.</span><span class="sxs-lookup"><span data-stu-id="cfe31-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="cfe31-125">Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.</span><span class="sxs-lookup"><span data-stu-id="cfe31-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="cfe31-126">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="cfe31-126">-Prefix</span></span>
<span data-ttu-id="cfe31-127">Specifica un prefisso usato nel nome delle code che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="cfe31-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="cfe31-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cfe31-128">CommonParameters</span></span>
<span data-ttu-id="cfe31-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cfe31-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cfe31-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cfe31-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cfe31-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cfe31-131">INPUTS</span></span>

### <span data-ttu-id="cfe31-132">System. String</span><span class="sxs-lookup"><span data-stu-id="cfe31-132">System.String</span></span>

### <span data-ttu-id="cfe31-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cfe31-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="cfe31-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cfe31-134">OUTPUTS</span></span>

### <span data-ttu-id="cfe31-135">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cfe31-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="cfe31-136">Note</span><span class="sxs-lookup"><span data-stu-id="cfe31-136">NOTES</span></span>

## <span data-ttu-id="cfe31-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cfe31-137">RELATED LINKS</span></span>

[<span data-ttu-id="cfe31-138">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cfe31-138">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)

[<span data-ttu-id="cfe31-139">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cfe31-139">Remove-AzureStorageQueue</span></span>](./Remove-AzureStorageQueue.md)


