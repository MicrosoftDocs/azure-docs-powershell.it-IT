---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54770fd564addf30e7c4ed058776857b823903e3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506952"
---
# <span data-ttu-id="cdc36-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdc36-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="cdc36-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="cdc36-102">SYNOPSIS</span></span>
<span data-ttu-id="cdc36-103">Rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdc36-103">Removes a storage queue.</span></span>

## <span data-ttu-id="cdc36-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="cdc36-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdc36-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="cdc36-105">DESCRIPTION</span></span>
<span data-ttu-id="cdc36-106">Il cmdlet **Remove-AzureStorageQueue** rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="cdc36-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="cdc36-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="cdc36-107">EXAMPLES</span></span>

### <span data-ttu-id="cdc36-108">Esempio 1: rimuovere una coda di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="cdc36-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="cdc36-109">Questo comando rimuove una coda denominata ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="cdc36-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="cdc36-110">Esempio 2: rimuovere più code di archiviazione</span><span class="sxs-lookup"><span data-stu-id="cdc36-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="cdc36-111">Questo comando consente di rimuovere tutte le code con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="cdc36-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="cdc36-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="cdc36-112">PARAMETERS</span></span>

### <span data-ttu-id="cdc36-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="cdc36-113">-Context</span></span>
<span data-ttu-id="cdc36-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="cdc36-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="cdc36-115">Per ottenere il contesto di archiviazione, il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="cdc36-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cdc36-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cdc36-116">-Force</span></span>
<span data-ttu-id="cdc36-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="cdc36-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="cdc36-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="cdc36-118">-Name</span></span>
<span data-ttu-id="cdc36-119">Specifica il nome della coda da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="cdc36-119">Specifies the name of the queue to remove.</span></span>

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

### <span data-ttu-id="cdc36-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cdc36-120">-PassThru</span></span>
<span data-ttu-id="cdc36-121">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="cdc36-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="cdc36-122">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="cdc36-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="cdc36-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="cdc36-123">-Confirm</span></span>
<span data-ttu-id="cdc36-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdc36-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdc36-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdc36-125">-WhatIf</span></span>
<span data-ttu-id="cdc36-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdc36-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdc36-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="cdc36-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdc36-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdc36-128">CommonParameters</span></span>
<span data-ttu-id="cdc36-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdc36-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdc36-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cdc36-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdc36-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="cdc36-131">INPUTS</span></span>

## <span data-ttu-id="cdc36-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="cdc36-132">OUTPUTS</span></span>

## <span data-ttu-id="cdc36-133">Note</span><span class="sxs-lookup"><span data-stu-id="cdc36-133">NOTES</span></span>

## <span data-ttu-id="cdc36-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="cdc36-134">RELATED LINKS</span></span>

[<span data-ttu-id="cdc36-135">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdc36-135">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="cdc36-136">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="cdc36-136">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
