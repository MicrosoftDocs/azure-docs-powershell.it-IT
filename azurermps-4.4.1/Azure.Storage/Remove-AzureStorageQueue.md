---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 51ea3111b5010b0e29f7bfd69ed5a8e66e596113
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511412"
---
# <span data-ttu-id="c9d89-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c9d89-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="c9d89-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c9d89-102">SYNOPSIS</span></span>
<span data-ttu-id="c9d89-103">Rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9d89-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9d89-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c9d89-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9d89-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c9d89-105">DESCRIPTION</span></span>
<span data-ttu-id="c9d89-106">Il cmdlet **Remove-AzureStorageQueue** rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c9d89-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="c9d89-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c9d89-107">EXAMPLES</span></span>

### <span data-ttu-id="c9d89-108">Esempio 1: rimuovere una coda di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="c9d89-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="c9d89-109">Questo comando rimuove una coda denominata ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="c9d89-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="c9d89-110">Esempio 2: rimuovere più code di archiviazione</span><span class="sxs-lookup"><span data-stu-id="c9d89-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="c9d89-111">Questo comando consente di rimuovere tutte le code con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="c9d89-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="c9d89-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c9d89-112">PARAMETERS</span></span>

### <span data-ttu-id="c9d89-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c9d89-113">-Context</span></span>
<span data-ttu-id="c9d89-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c9d89-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c9d89-115">Per ottenere il contesto di archiviazione, il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c9d89-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c9d89-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c9d89-116">-Force</span></span>
<span data-ttu-id="c9d89-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c9d89-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c9d89-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c9d89-118">-Name</span></span>
<span data-ttu-id="c9d89-119">Specifica il nome della coda da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c9d89-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="c9d89-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c9d89-120">-PassThru</span></span>
<span data-ttu-id="c9d89-121">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c9d89-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c9d89-122">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c9d89-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c9d89-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c9d89-123">-Confirm</span></span>
<span data-ttu-id="c9d89-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c9d89-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9d89-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9d89-125">-WhatIf</span></span>
<span data-ttu-id="c9d89-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9d89-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9d89-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c9d89-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9d89-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9d89-128">CommonParameters</span></span>
<span data-ttu-id="c9d89-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9d89-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9d89-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9d89-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9d89-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c9d89-131">INPUTS</span></span>

### <span data-ttu-id="c9d89-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="c9d89-132">IStorageContext</span></span>

<span data-ttu-id="c9d89-133">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c9d89-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="c9d89-134">Stringa</span><span class="sxs-lookup"><span data-stu-id="c9d89-134">String</span></span>

<span data-ttu-id="c9d89-135">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="c9d89-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="c9d89-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c9d89-136">OUTPUTS</span></span>

### <span data-ttu-id="c9d89-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c9d89-137">System.Boolean</span></span>

## <span data-ttu-id="c9d89-138">Note</span><span class="sxs-lookup"><span data-stu-id="c9d89-138">NOTES</span></span>

## <span data-ttu-id="c9d89-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c9d89-139">RELATED LINKS</span></span>

[<span data-ttu-id="c9d89-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c9d89-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="c9d89-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="c9d89-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
