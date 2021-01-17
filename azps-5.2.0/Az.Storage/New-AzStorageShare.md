---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: FCDCEF0B-6E2C-480E-9841-EF4E64D61D54
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageshare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShare.md
ms.openlocfilehash: 4fa89a13f9b4124232d9459d7d3eff54a6f55a5c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324685"
---
# <span data-ttu-id="21ddd-101">New-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="21ddd-101">New-AzStorageShare</span></span>

## <span data-ttu-id="21ddd-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="21ddd-102">SYNOPSIS</span></span>
<span data-ttu-id="21ddd-103">Crea una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="21ddd-103">Creates a file share.</span></span>

## <span data-ttu-id="21ddd-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="21ddd-104">SYNTAX</span></span>

```
New-AzStorageShare [-Name] <String> [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [<CommonParameters>]
```

## <span data-ttu-id="21ddd-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="21ddd-105">DESCRIPTION</span></span>
<span data-ttu-id="21ddd-106">Il cmdlet **New-AzStorageShare** crea una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="21ddd-106">The **New-AzStorageShare** cmdlet creates a file share.</span></span>

## <span data-ttu-id="21ddd-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="21ddd-107">EXAMPLES</span></span>

### <span data-ttu-id="21ddd-108">Esempio 1: creare una condivisione file</span><span class="sxs-lookup"><span data-stu-id="21ddd-108">Example 1: Create a file share</span></span>
```
PS C:\>New-AzStorageShare -Name "ContosoShare06"
```

<span data-ttu-id="21ddd-109">Questo comando crea una condivisione file denominata ContosoShare06.</span><span class="sxs-lookup"><span data-stu-id="21ddd-109">This command creates a file share named ContosoShare06.</span></span>

## <span data-ttu-id="21ddd-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="21ddd-110">PARAMETERS</span></span>

### <span data-ttu-id="21ddd-111">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="21ddd-111">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="21ddd-112">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="21ddd-112">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="21ddd-113">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="21ddd-113">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="21ddd-114">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="21ddd-114">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ddd-115">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="21ddd-115">-ConcurrentTaskCount</span></span>
<span data-ttu-id="21ddd-116">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="21ddd-116">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="21ddd-117">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="21ddd-117">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="21ddd-118">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="21ddd-118">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="21ddd-119">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="21ddd-119">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="21ddd-120">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="21ddd-120">The default value is 10.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ddd-121">-Contesto</span><span class="sxs-lookup"><span data-stu-id="21ddd-121">-Context</span></span>
<span data-ttu-id="21ddd-122">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="21ddd-122">Specifies an Azure storage context.</span></span>
<span data-ttu-id="21ddd-123">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="21ddd-123">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

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

### <span data-ttu-id="21ddd-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ddd-124">-DefaultProfile</span></span>
<span data-ttu-id="21ddd-125">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="21ddd-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="21ddd-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="21ddd-126">-Name</span></span>
<span data-ttu-id="21ddd-127">Specifica il nome di una condivisione file.</span><span class="sxs-lookup"><span data-stu-id="21ddd-127">Specifies the name of a file share.</span></span>
<span data-ttu-id="21ddd-128">Questo cmdlet crea una condivisione file con il nome specificato da questo parametro.</span><span class="sxs-lookup"><span data-stu-id="21ddd-128">This cmdlet creates a file share that has the name that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21ddd-129">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="21ddd-129">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="21ddd-130">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="21ddd-130">Specifies the length of the time-out period for the server part of a request.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21ddd-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ddd-131">CommonParameters</span></span>
<span data-ttu-id="21ddd-132">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ddd-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ddd-133">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ddd-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ddd-134">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="21ddd-134">INPUTS</span></span>

### <span data-ttu-id="21ddd-135">System. String</span><span class="sxs-lookup"><span data-stu-id="21ddd-135">System.String</span></span>

### <span data-ttu-id="21ddd-136">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="21ddd-136">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="21ddd-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="21ddd-137">OUTPUTS</span></span>

### <span data-ttu-id="21ddd-138">Microsoft. WindowsAzure. Commands. Common. storage. ResourceModel. AzureStorageFileShare</span><span class="sxs-lookup"><span data-stu-id="21ddd-138">Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageFileShare</span></span>

## <span data-ttu-id="21ddd-139">Note</span><span class="sxs-lookup"><span data-stu-id="21ddd-139">NOTES</span></span>

## <span data-ttu-id="21ddd-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="21ddd-140">RELATED LINKS</span></span>

[<span data-ttu-id="21ddd-141">Get-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="21ddd-141">Get-AzStorageShare</span></span>](./Get-AzStorageShare.md)

[<span data-ttu-id="21ddd-142">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="21ddd-142">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="21ddd-143">Remove-AzStorageShare</span><span class="sxs-lookup"><span data-stu-id="21ddd-143">Remove-AzStorageShare</span></span>](./Remove-AzStorageShare.md)
