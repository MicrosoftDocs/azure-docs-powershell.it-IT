---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: b98b0ef6e8c4d47c32cab4ee891041e0820ea3ca
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686762"
---
# <span data-ttu-id="18180-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="18180-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="18180-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="18180-102">SYNOPSIS</span></span>
<span data-ttu-id="18180-103">Rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18180-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18180-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="18180-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="18180-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="18180-105">DESCRIPTION</span></span>
<span data-ttu-id="18180-106">Il cmdlet **Remove-AzureStorageQueue** rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="18180-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="18180-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="18180-107">EXAMPLES</span></span>

### <span data-ttu-id="18180-108">Esempio 1: rimuovere una coda di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="18180-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="18180-109">Questo comando rimuove una coda denominata ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="18180-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="18180-110">Esempio 2: rimuovere più code di archiviazione</span><span class="sxs-lookup"><span data-stu-id="18180-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="18180-111">Questo comando consente di rimuovere tutte le code con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="18180-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="18180-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="18180-112">PARAMETERS</span></span>

### <span data-ttu-id="18180-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="18180-113">-Context</span></span>
<span data-ttu-id="18180-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="18180-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="18180-115">Per ottenere il contesto di archiviazione, il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="18180-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="18180-116">-Force</span><span class="sxs-lookup"><span data-stu-id="18180-116">-Force</span></span>
<span data-ttu-id="18180-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="18180-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="18180-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="18180-118">-Name</span></span>
<span data-ttu-id="18180-119">Specifica il nome della coda da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="18180-119">Specifies the name of the queue to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="18180-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="18180-120">-PassThru</span></span>
<span data-ttu-id="18180-121">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="18180-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="18180-122">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="18180-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="18180-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="18180-123">-Confirm</span></span>
<span data-ttu-id="18180-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="18180-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="18180-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="18180-125">-WhatIf</span></span>
<span data-ttu-id="18180-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18180-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="18180-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="18180-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="18180-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18180-128">CommonParameters</span></span>
<span data-ttu-id="18180-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18180-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18180-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18180-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18180-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="18180-131">INPUTS</span></span>

### <span data-ttu-id="18180-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="18180-132">IStorageContext</span></span>

<span data-ttu-id="18180-133">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="18180-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="18180-134">Stringa</span><span class="sxs-lookup"><span data-stu-id="18180-134">String</span></span>

<span data-ttu-id="18180-135">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="18180-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="18180-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="18180-136">OUTPUTS</span></span>

### <span data-ttu-id="18180-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="18180-137">System.Boolean</span></span>

## <span data-ttu-id="18180-138">Note</span><span class="sxs-lookup"><span data-stu-id="18180-138">NOTES</span></span>

## <span data-ttu-id="18180-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="18180-139">RELATED LINKS</span></span>

[<span data-ttu-id="18180-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="18180-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="18180-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="18180-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
