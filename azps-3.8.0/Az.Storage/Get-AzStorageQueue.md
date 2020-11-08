---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94020241"
---
# <span data-ttu-id="9e583-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e583-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="9e583-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="9e583-102">SYNOPSIS</span></span>
<span data-ttu-id="9e583-103">Elenca le code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="9e583-103">Lists storage queues.</span></span>

## <span data-ttu-id="9e583-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="9e583-104">SYNTAX</span></span>

### <span data-ttu-id="9e583-105">QueueName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="9e583-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9e583-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="9e583-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e583-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9e583-107">DESCRIPTION</span></span>
<span data-ttu-id="9e583-108">Il cmdlet **Get-AzStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e583-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="9e583-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="9e583-109">EXAMPLES</span></span>

### <span data-ttu-id="9e583-110">Esempio 1: elencare tutte le code di archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="9e583-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="9e583-111">Questo comando consente di ottenere un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="9e583-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="9e583-112">Esempio 2: elencare le code di archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="9e583-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="9e583-113">Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="9e583-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="9e583-114">Esempio 3: code di archiviazione di elenchi di Azure tramite il prefisso del nome della coda</span><span class="sxs-lookup"><span data-stu-id="9e583-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="9e583-115">Questo esempio usa il parametro *Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con Queue.</span><span class="sxs-lookup"><span data-stu-id="9e583-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="9e583-116">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="9e583-116">PARAMETERS</span></span>

### <span data-ttu-id="9e583-117">-Contesto</span><span class="sxs-lookup"><span data-stu-id="9e583-117">-Context</span></span>
<span data-ttu-id="9e583-118">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="9e583-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="9e583-119">Puoi crearlo usando il cmdlet **New-AzStorageContext** .</span><span class="sxs-lookup"><span data-stu-id="9e583-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="9e583-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9e583-120">-DefaultProfile</span></span>
<span data-ttu-id="9e583-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="9e583-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9e583-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="9e583-122">-Name</span></span>
<span data-ttu-id="9e583-123">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="9e583-123">Specifies a name.</span></span>
<span data-ttu-id="9e583-124">Se non viene specificato alcun nome, il cmdlet riceve un elenco di tutte le code.</span><span class="sxs-lookup"><span data-stu-id="9e583-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="9e583-125">Se viene specificato un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al modello di nome.</span><span class="sxs-lookup"><span data-stu-id="9e583-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="9e583-126">-Prefisso</span><span class="sxs-lookup"><span data-stu-id="9e583-126">-Prefix</span></span>
<span data-ttu-id="9e583-127">Specifica un prefisso usato nel nome delle code che vuoi ottenere.</span><span class="sxs-lookup"><span data-stu-id="9e583-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="9e583-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e583-128">CommonParameters</span></span>
<span data-ttu-id="9e583-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9e583-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e583-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e583-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e583-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="9e583-131">INPUTS</span></span>

### <span data-ttu-id="9e583-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9e583-132">System.String</span></span>

### <span data-ttu-id="9e583-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e583-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="9e583-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="9e583-134">OUTPUTS</span></span>

### <span data-ttu-id="9e583-135">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e583-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="9e583-136">Note</span><span class="sxs-lookup"><span data-stu-id="9e583-136">NOTES</span></span>

## <span data-ttu-id="9e583-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="9e583-137">RELATED LINKS</span></span>

[<span data-ttu-id="9e583-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e583-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="9e583-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="9e583-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


