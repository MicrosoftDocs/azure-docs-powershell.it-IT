---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/New-AzureStorageShare.md
gitcommit: https://github.com/Azure/azure-powershell/blob/173e94aec59d7f539b72e43e90e5e7f8ba5f62bc
ms.openlocfilehash: a1be5816427ac1aa91b9daa98701abaec044c20f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93522014"
---
# <span data-ttu-id="bf53c-101">New-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf53c-101">New-AzureStorageShare</span></span>

## <span data-ttu-id="bf53c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="bf53c-102">SYNOPSIS</span></span>
<span data-ttu-id="bf53c-103">Crea una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bf53c-103">Creates a file share.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf53c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="bf53c-104">SYNTAX</span></span>

```
New-AzureStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="bf53c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bf53c-105">DESCRIPTION</span></span>
<span data-ttu-id="bf53c-106">Il cmdlet **New-AzureStorageShare** crea una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bf53c-106">The **New-AzureStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="bf53c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="bf53c-107">EXAMPLES</span></span>

### <span data-ttu-id="bf53c-108">Esempio 1: creare una condivisione file</span><span class="sxs-lookup"><span data-stu-id="bf53c-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzureStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="bf53c-109">Questo comando crea una condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="bf53c-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="bf53c-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="bf53c-110">PARAMETERS</span></span>

### <span data-ttu-id="bf53c-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf53c-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="bf53c-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="bf53c-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="bf53c-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="bf53c-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="bf53c-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="bf53c-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="bf53c-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="bf53c-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="bf53c-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="bf53c-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="bf53c-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="bf53c-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="bf53c-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="bf53c-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="bf53c-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="bf53c-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="bf53c-120">The default value is 10.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="bf53c-121">-Context</span></span>
<span data-ttu-id="bf53c-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="bf53c-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bf53c-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzureStorageContext](./New-AzureStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="bf53c-123">To obtain a storage context, use the [New-AzureStorageContext](./New-AzureStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="bf53c-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="bf53c-124">-Name</span></span>
<span data-ttu-id="bf53c-125">Specifica il nome di una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="bf53c-125">Specifies the name of a file share.</span></span>
<span data-ttu-id="bf53c-126">Questo cmdlet crea una condivisione file con il nome specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="bf53c-126">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-127">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="bf53c-127">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="bf53c-128">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="bf53c-128">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf53c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf53c-129">CommonParameters</span></span>
<span data-ttu-id="bf53c-130">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf53c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf53c-131">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf53c-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf53c-132">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="bf53c-132">INPUTS</span></span>

### <span data-ttu-id="bf53c-133">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf53c-133">IStorageContext</span></span>

<span data-ttu-id="bf53c-134">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bf53c-134">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="bf53c-135">Stringa</span><span class="sxs-lookup"><span data-stu-id="bf53c-135">String</span></span>

<span data-ttu-id="bf53c-136">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="bf53c-136">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="bf53c-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="bf53c-137">OUTPUTS</span></span>

## <span data-ttu-id="bf53c-138">Note</span><span class="sxs-lookup"><span data-stu-id="bf53c-138">NOTES</span></span>

## <span data-ttu-id="bf53c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="bf53c-139">RELATED LINKS</span></span>

[<span data-ttu-id="bf53c-140">Get-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf53c-140">Get-AzureStorageShare</span></span>](./Get-AzureStorageShare.md)

[<span data-ttu-id="bf53c-141">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bf53c-141">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bf53c-142">Remove-AzureStorageShare</span><span class="sxs-lookup"><span data-stu-id="bf53c-142">Remove-AzureStorageShare</span></span>](./Remove-AzureStorageShare.md)
