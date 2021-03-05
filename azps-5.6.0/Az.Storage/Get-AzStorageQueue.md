---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 2361196f2e8b904f2403aaf06118122931e83afd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997078"
---
# <span data-ttu-id="105ce-101">Get-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="105ce-101">Get-AzStorageQueue</span></span>

## <span data-ttu-id="105ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="105ce-102">SYNOPSIS</span></span>
<span data-ttu-id="105ce-103">Elenca le code di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="105ce-103">Lists storage queues.</span></span>

## <span data-ttu-id="105ce-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="105ce-104">SYNTAX</span></span>

### <span data-ttu-id="105ce-105">QueueName (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="105ce-105">QueueName (Default)</span></span>
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="105ce-106">QueuePrefix</span><span class="sxs-lookup"><span data-stu-id="105ce-106">QueuePrefix</span></span>
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="105ce-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="105ce-107">DESCRIPTION</span></span>
<span data-ttu-id="105ce-108">Il cmdlet **Get-AzStorageQueue** elenca le code di archiviazione associate a un account di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="105ce-108">The **Get-AzStorageQueue** cmdlet lists storage queues associated with an Azure Storage account.</span></span>

## <span data-ttu-id="105ce-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="105ce-109">EXAMPLES</span></span>

### <span data-ttu-id="105ce-110">Esempio 1: Elencare tutte le code di Archiviazione di Azure</span><span class="sxs-lookup"><span data-stu-id="105ce-110">Example 1: List all Azure Storage queues</span></span>
```
PS C:\>Get-AzStorageQueue
```

<span data-ttu-id="105ce-111">Questo comando ottiene un elenco di tutte le code di archiviazione per l'account di archiviazione corrente.</span><span class="sxs-lookup"><span data-stu-id="105ce-111">This command gets a list of all storage queues for the current Storage account.</span></span>

### <span data-ttu-id="105ce-112">Esempio 2: Elencare le code di Archiviazione di Azure usando un carattere jolly</span><span class="sxs-lookup"><span data-stu-id="105ce-112">Example 2: List Azure Storage queues using a wildcard character</span></span>
```
PS C:\>Get-AzStorageQueue -Name queue*
```

<span data-ttu-id="105ce-113">Questo comando usa un carattere jolly per ottenere un elenco delle code di archiviazione il cui nome inizia con coda.</span><span class="sxs-lookup"><span data-stu-id="105ce-113">This command uses a wildcard character to get a list of storage queues whose name starts with queue.</span></span>

### <span data-ttu-id="105ce-114">Esempio 3: Elencare le code di archiviazione di Azure usando il prefisso del nome della coda</span><span class="sxs-lookup"><span data-stu-id="105ce-114">Example 3: List Azure Storage queues using queue name prefix</span></span>
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

<span data-ttu-id="105ce-115">Questo esempio usa il *parametro Prefix* per ottenere un elenco delle code di archiviazione il cui nome inizia con coda.</span><span class="sxs-lookup"><span data-stu-id="105ce-115">This example uses the *Prefix* parameter to get a list of storage queues whose name starts with queue.</span></span>

## <span data-ttu-id="105ce-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="105ce-116">PARAMETERS</span></span>

### <span data-ttu-id="105ce-117">-Context</span><span class="sxs-lookup"><span data-stu-id="105ce-117">-Context</span></span>
<span data-ttu-id="105ce-118">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="105ce-118">Specifies the Azure storage context.</span></span>
<span data-ttu-id="105ce-119">È possibile crearla usando il cmdlet **New-AzStorageContext.**</span><span class="sxs-lookup"><span data-stu-id="105ce-119">You can create it by using the **New-AzStorageContext** cmdlet.</span></span>

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

### <span data-ttu-id="105ce-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="105ce-120">-DefaultProfile</span></span>
<span data-ttu-id="105ce-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="105ce-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="105ce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="105ce-122">-Name</span></span>
<span data-ttu-id="105ce-123">Specifica un nome.</span><span class="sxs-lookup"><span data-stu-id="105ce-123">Specifies a name.</span></span>
<span data-ttu-id="105ce-124">Se non si specifica alcun nome, il cmdlet ottiene un elenco di tutte le code.</span><span class="sxs-lookup"><span data-stu-id="105ce-124">If no name is specified, the cmdlet gets a list of all the queues.</span></span>
<span data-ttu-id="105ce-125">Se si specifica un nome completo o parziale, il cmdlet ottiene tutte le code che corrispondono al criterio del nome.</span><span class="sxs-lookup"><span data-stu-id="105ce-125">If a full or partial name is specified, the cmdlet gets all queues that match the name pattern.</span></span>

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

### <span data-ttu-id="105ce-126">-Prefix</span><span class="sxs-lookup"><span data-stu-id="105ce-126">-Prefix</span></span>
<span data-ttu-id="105ce-127">Specifica un prefisso usato nel nome delle code da ottenere.</span><span class="sxs-lookup"><span data-stu-id="105ce-127">Specifies a prefix used in the name of the queues you want to get.</span></span>

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

### <span data-ttu-id="105ce-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="105ce-128">CommonParameters</span></span>
<span data-ttu-id="105ce-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="105ce-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="105ce-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="105ce-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="105ce-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="105ce-131">INPUTS</span></span>

### <span data-ttu-id="105ce-132">System.String</span><span class="sxs-lookup"><span data-stu-id="105ce-132">System.String</span></span>

### <span data-ttu-id="105ce-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="105ce-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="105ce-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="105ce-134">OUTPUTS</span></span>

### <span data-ttu-id="105ce-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="105ce-135">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue</span></span>

## <span data-ttu-id="105ce-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="105ce-136">NOTES</span></span>

## <span data-ttu-id="105ce-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="105ce-137">RELATED LINKS</span></span>

[<span data-ttu-id="105ce-138">New-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="105ce-138">New-AzStorageQueue</span></span>](./New-AzStorageQueue.md)

[<span data-ttu-id="105ce-139">Remove-AzStorageQueue</span><span class="sxs-lookup"><span data-stu-id="105ce-139">Remove-AzStorageQueue</span></span>](./Remove-AzStorageQueue.md)


