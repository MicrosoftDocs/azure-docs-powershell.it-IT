---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 5bfdca4637f4d1504d8dbf18a923f8c1f0c082bd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93688483"
---
# <span data-ttu-id="36344-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36344-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="36344-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="36344-102">SYNOPSIS</span></span>
<span data-ttu-id="36344-103">Rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="36344-103">Removes a stored access policy from an Azure storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36344-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="36344-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36344-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="36344-105">DESCRIPTION</span></span>
<span data-ttu-id="36344-106">Il cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="36344-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="36344-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="36344-107">EXAMPLES</span></span>

### <span data-ttu-id="36344-108">Esempio 1: rimuovere un criterio di accesso archiviato da una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="36344-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="36344-109">Questo comando rimuove un criterio di accesso denominato Policy04 dalla coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="36344-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="36344-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="36344-110">PARAMETERS</span></span>

### <span data-ttu-id="36344-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="36344-111">-Context</span></span>
<span data-ttu-id="36344-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="36344-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="36344-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="36344-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="36344-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36344-114">-PassThru</span></span>
<span data-ttu-id="36344-115">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="36344-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="36344-116">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="36344-116">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36344-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="36344-117">-Policy</span></span>
<span data-ttu-id="36344-118">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36344-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36344-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="36344-119">-Queue</span></span>
<span data-ttu-id="36344-120">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="36344-120">Specifies the Azure storage queue name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36344-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="36344-121">-Confirm</span></span>
<span data-ttu-id="36344-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36344-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36344-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36344-123">-WhatIf</span></span>
<span data-ttu-id="36344-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36344-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36344-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="36344-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36344-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36344-126">CommonParameters</span></span>
<span data-ttu-id="36344-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36344-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36344-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36344-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36344-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="36344-129">INPUTS</span></span>

### <span data-ttu-id="36344-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="36344-130">IStorageContext</span></span>

<span data-ttu-id="36344-131">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="36344-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="36344-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="36344-132">OUTPUTS</span></span>

### <span data-ttu-id="36344-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36344-133">System.Boolean</span></span>

## <span data-ttu-id="36344-134">Note</span><span class="sxs-lookup"><span data-stu-id="36344-134">NOTES</span></span>

## <span data-ttu-id="36344-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="36344-135">RELATED LINKS</span></span>

[<span data-ttu-id="36344-136">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36344-136">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="36344-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="36344-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="36344-138">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36344-138">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="36344-139">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="36344-139">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
