---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3AC3F8DE-E25D-41AE-9083-5C459A4C8CD0
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/stop-azstoragefilecopy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Stop-AzStorageFileCopy.md
ms.openlocfilehash: 9a2449299c6c4a6d87ee7c4b0403a35a0b7c3683
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676475"
---
# <span data-ttu-id="09492-101">Stop-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="09492-101">Stop-AzStorageFileCopy</span></span>

## <span data-ttu-id="09492-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="09492-102">SYNOPSIS</span></span>
<span data-ttu-id="09492-103">Interrompe un'operazione di copia nel file di destinazione specificato.</span><span class="sxs-lookup"><span data-stu-id="09492-103">Stops a copy operation to the specified destination file.</span></span>

## <span data-ttu-id="09492-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="09492-104">SYNTAX</span></span>

### <span data-ttu-id="09492-105">Nomecondivisione</span><span class="sxs-lookup"><span data-stu-id="09492-105">ShareName</span></span>
```
Stop-AzStorageFileCopy [-ShareName] <String> [-FilePath] <String> [-CopyId <String>] [-Force]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="09492-106">File</span><span class="sxs-lookup"><span data-stu-id="09492-106">File</span></span>
```
Stop-AzStorageFileCopy [-File] <CloudFile> [-CopyId <String>] [-Force] [-ServerTimeoutPerRequest <Int32>]
 [-ClientTimeoutPerRequest <Int32>] [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="09492-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="09492-107">DESCRIPTION</span></span>
<span data-ttu-id="09492-108">Il cmdlet **Stop-AzStorageFileCopy** interrompe la copia di un file in un file di destinazione.</span><span class="sxs-lookup"><span data-stu-id="09492-108">The **Stop-AzStorageFileCopy** cmdlet stops copying a file to a destination file.</span></span>

## <span data-ttu-id="09492-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="09492-109">EXAMPLES</span></span>

### <span data-ttu-id="09492-110">Esempio 1: interrompere un'operazione di copia</span><span class="sxs-lookup"><span data-stu-id="09492-110">Example 1: Stop a copy operation</span></span>
```
PS C:\>Stop-AzStorageFileCopy -ShareName "ContosoShare" -FilePath "FilePath" -CopyId "CopyId"
```

<span data-ttu-id="09492-111">Questo comando interrompe la copia di un file con il nome specificato.</span><span class="sxs-lookup"><span data-stu-id="09492-111">This command stops copying a file that has the specified name.</span></span>

## <span data-ttu-id="09492-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="09492-112">PARAMETERS</span></span>

### <span data-ttu-id="09492-113">-ClientTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09492-113">-ClientTimeoutPerRequest</span></span>
<span data-ttu-id="09492-114">Specifica l'intervallo di timeout lato client, in secondi, per una richiesta di servizio.</span><span class="sxs-lookup"><span data-stu-id="09492-114">Specifies the client-side time-out interval, in seconds, for one service request.</span></span>
<span data-ttu-id="09492-115">Se la chiamata precedente non riesce nell'intervallo specificato, questo cmdlet ritenta la richiesta.</span><span class="sxs-lookup"><span data-stu-id="09492-115">If the previous call fails in the specified interval, this cmdlet retries the request.</span></span>
<span data-ttu-id="09492-116">Se questo cmdlet non riceve una risposta corretta prima che l'intervallo venga trascorso, questo cmdlet restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="09492-116">If this cmdlet does not receive a successful response before the interval elapses, this cmdlet returns an error.</span></span>

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

### <span data-ttu-id="09492-117">-ConcurrentTaskCount</span><span class="sxs-lookup"><span data-stu-id="09492-117">-ConcurrentTaskCount</span></span>
<span data-ttu-id="09492-118">Specifica le chiamate di rete simultanee massime.</span><span class="sxs-lookup"><span data-stu-id="09492-118">Specifies the maximum concurrent network calls.</span></span>
<span data-ttu-id="09492-119">Puoi usare questo parametro per limitare la concorrenza per accelerare l'uso della CPU locale e della larghezza di banda specificando il numero massimo di chiamate di rete simultanee.</span><span class="sxs-lookup"><span data-stu-id="09492-119">You can use this parameter to limit the concurrency to throttle local CPU and bandwidth usage by specifying the maximum number of concurrent network calls.</span></span>
<span data-ttu-id="09492-120">Il valore specificato è un conteggio assoluto e non viene moltiplicato per il numero di base.</span><span class="sxs-lookup"><span data-stu-id="09492-120">The specified value is an absolute count and is not multiplied by the core count.</span></span>
<span data-ttu-id="09492-121">Questo parametro può aiutare a ridurre i problemi di connessione di rete in ambienti con larghezza di banda ridotta, ad esempio 100 kilobit al secondo.</span><span class="sxs-lookup"><span data-stu-id="09492-121">This parameter can help reduce network connection problems in low bandwidth environments, such as 100 kilobits per second.</span></span>
<span data-ttu-id="09492-122">Il valore predefinito è 10.</span><span class="sxs-lookup"><span data-stu-id="09492-122">The default value is 10.</span></span>

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

### <span data-ttu-id="09492-123">-Contesto</span><span class="sxs-lookup"><span data-stu-id="09492-123">-Context</span></span>
<span data-ttu-id="09492-124">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="09492-124">Specifies an Azure storage context.</span></span>
<span data-ttu-id="09492-125">Per ottenere un contesto di archiviazione, usare il cmdlet [New-AzStorageContext](./New-AzStorageContext.md) .</span><span class="sxs-lookup"><span data-stu-id="09492-125">To obtain a storage context, use the [New-AzStorageContext](./New-AzStorageContext.md) cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: ShareName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09492-126">-CopyId</span><span class="sxs-lookup"><span data-stu-id="09492-126">-CopyId</span></span>
<span data-ttu-id="09492-127">Specifica l'ID dell'operazione di copia.</span><span class="sxs-lookup"><span data-stu-id="09492-127">Specifies the ID of the copy operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09492-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09492-128">-DefaultProfile</span></span>
<span data-ttu-id="09492-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="09492-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09492-130">-File</span><span class="sxs-lookup"><span data-stu-id="09492-130">-File</span></span>
<span data-ttu-id="09492-131">Specifica un oggetto **CloudFile** .</span><span class="sxs-lookup"><span data-stu-id="09492-131">Specifies a **CloudFile** object.</span></span>
<span data-ttu-id="09492-132">È possibile creare un file cloud o ottenerne uno usando il cmdlet Get-AzStorageFile.</span><span class="sxs-lookup"><span data-stu-id="09492-132">You can create a cloud file or obtain one by using the Get-AzStorageFile cmdlet.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.File.CloudFile
Parameter Sets: File
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09492-133">-FilePath</span><span class="sxs-lookup"><span data-stu-id="09492-133">-FilePath</span></span>
<span data-ttu-id="09492-134">Specifica il percorso di un file.</span><span class="sxs-lookup"><span data-stu-id="09492-134">Specifies the path of a file.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09492-135">-Force</span><span class="sxs-lookup"><span data-stu-id="09492-135">-Force</span></span>
<span data-ttu-id="09492-136">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="09492-136">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09492-137">-ServerTimeoutPerRequest</span><span class="sxs-lookup"><span data-stu-id="09492-137">-ServerTimeoutPerRequest</span></span>
<span data-ttu-id="09492-138">Specifica la lunghezza del periodo di timeout per la parte server di una richiesta.</span><span class="sxs-lookup"><span data-stu-id="09492-138">Specifies the length of the time-out period for the server part of a request.</span></span>

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

### <span data-ttu-id="09492-139">-ShareName</span><span class="sxs-lookup"><span data-stu-id="09492-139">-ShareName</span></span>
<span data-ttu-id="09492-140">Specifica il nome di una condivisione.</span><span class="sxs-lookup"><span data-stu-id="09492-140">Specifies the name of a share.</span></span>

```yaml
Type: System.String
Parameter Sets: ShareName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09492-141">-Confermare</span><span class="sxs-lookup"><span data-stu-id="09492-141">-Confirm</span></span>
<span data-ttu-id="09492-142">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09492-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09492-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="09492-143">-WhatIf</span></span>
<span data-ttu-id="09492-144">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09492-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="09492-145">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="09492-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09492-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09492-146">CommonParameters</span></span>
<span data-ttu-id="09492-147">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09492-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09492-148">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09492-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09492-149">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="09492-149">INPUTS</span></span>

### <span data-ttu-id="09492-150">Microsoft. WindowsAzure. storage. file. CloudFile</span><span class="sxs-lookup"><span data-stu-id="09492-150">Microsoft.WindowsAzure.Storage.File.CloudFile</span></span>

### <span data-ttu-id="09492-151">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="09492-151">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="09492-152">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="09492-152">OUTPUTS</span></span>

### <span data-ttu-id="09492-153">System. void</span><span class="sxs-lookup"><span data-stu-id="09492-153">System.Void</span></span>

## <span data-ttu-id="09492-154">Note</span><span class="sxs-lookup"><span data-stu-id="09492-154">NOTES</span></span>

## <span data-ttu-id="09492-155">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="09492-155">RELATED LINKS</span></span>

[<span data-ttu-id="09492-156">Get-AzStorageFile</span><span class="sxs-lookup"><span data-stu-id="09492-156">Get-AzStorageFile</span></span>](./Get-AzStorageFile.md)

[<span data-ttu-id="09492-157">Get-AzStorageFileCopyState</span><span class="sxs-lookup"><span data-stu-id="09492-157">Get-AzStorageFileCopyState</span></span>](./Get-AzStorageFileCopyState.md)

[<span data-ttu-id="09492-158">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="09492-158">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="09492-159">Start-AzStorageFileCopy</span><span class="sxs-lookup"><span data-stu-id="09492-159">Start-AzStorageFileCopy</span></span>](./Start-AzStorageFileCopy.md)
