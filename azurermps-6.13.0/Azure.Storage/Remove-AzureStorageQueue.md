---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 22975A89-CAFF-4F18-8DCE-B695413FBAC7
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageQueue.md
ms.openlocfilehash: 544d019547616ab7fc37804e150115eacc8a0224
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93509468"
---
# <span data-ttu-id="2a9b1-101">Remove-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2a9b1-101">Remove-AzureStorageQueue</span></span>

## <span data-ttu-id="2a9b1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2a9b1-102">SYNOPSIS</span></span>
<span data-ttu-id="2a9b1-103">Rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-103">Removes a storage queue.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a9b1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2a9b1-104">SYNTAX</span></span>

```
Remove-AzureStorageQueue [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2a9b1-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2a9b1-105">DESCRIPTION</span></span>
<span data-ttu-id="2a9b1-106">Il cmdlet **Remove-AzureStorageQueue** rimuove una coda di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-106">The **Remove-AzureStorageQueue** cmdlet removes a storage queue.</span></span>

## <span data-ttu-id="2a9b1-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2a9b1-107">EXAMPLES</span></span>

### <span data-ttu-id="2a9b1-108">Esempio 1: rimuovere una coda di archiviazione per nome</span><span class="sxs-lookup"><span data-stu-id="2a9b1-108">Example 1: Remove a storage queue by name</span></span>
```
PS C:\>Remove-AzureStorageQueue "ContosoQueue01"
```

<span data-ttu-id="2a9b1-109">Questo comando rimuove una coda denominata ContosoQueue01.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-109">This command removes a queue named ContosoQueue01.</span></span>

### <span data-ttu-id="2a9b1-110">Esempio 2: rimuovere più code di archiviazione</span><span class="sxs-lookup"><span data-stu-id="2a9b1-110">Example 2: Remove multiple storage queues</span></span>
```
PS C:\>Get-AzureStorageQueue "Contoso*" | Remove-AzureStorageQueue
```

<span data-ttu-id="2a9b1-111">Questo comando consente di rimuovere tutte le code con nomi che iniziano con contoso.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-111">This command removes all queues with names that start with Contoso.</span></span>

## <span data-ttu-id="2a9b1-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2a9b1-112">PARAMETERS</span></span>

### <span data-ttu-id="2a9b1-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="2a9b1-113">-Context</span></span>
<span data-ttu-id="2a9b1-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="2a9b1-115">Per ottenere il contesto di archiviazione, il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-115">To obtain the storage context, the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="2a9b1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a9b1-116">-DefaultProfile</span></span>
<span data-ttu-id="2a9b1-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a9b1-118">-Force</span><span class="sxs-lookup"><span data-stu-id="2a9b1-118">-Force</span></span>
<span data-ttu-id="2a9b1-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="2a9b1-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="2a9b1-120">-Name</span></span>
<span data-ttu-id="2a9b1-121">Specifica il nome della coda da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-121">Specifies the name of the queue to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2a9b1-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2a9b1-122">-PassThru</span></span>
<span data-ttu-id="2a9b1-123">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="2a9b1-124">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="2a9b1-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="2a9b1-125">-Confirm</span></span>
<span data-ttu-id="2a9b1-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a9b1-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a9b1-127">-WhatIf</span></span>
<span data-ttu-id="2a9b1-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a9b1-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a9b1-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a9b1-130">CommonParameters</span></span>
<span data-ttu-id="2a9b1-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a9b1-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a9b1-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a9b1-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a9b1-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2a9b1-133">INPUTS</span></span>

### <span data-ttu-id="2a9b1-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2a9b1-134">System.String</span></span>

### <span data-ttu-id="2a9b1-135">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2a9b1-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="2a9b1-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2a9b1-136">OUTPUTS</span></span>

### <span data-ttu-id="2a9b1-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2a9b1-137">System.Boolean</span></span>

## <span data-ttu-id="2a9b1-138">Note</span><span class="sxs-lookup"><span data-stu-id="2a9b1-138">NOTES</span></span>

## <span data-ttu-id="2a9b1-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2a9b1-139">RELATED LINKS</span></span>

[<span data-ttu-id="2a9b1-140">Get-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2a9b1-140">Get-AzureStorageQueue</span></span>](./Get-AzureStorageQueue.md)

[<span data-ttu-id="2a9b1-141">New-AzureStorageQueue</span><span class="sxs-lookup"><span data-stu-id="2a9b1-141">New-AzureStorageQueue</span></span>](./New-AzureStorageQueue.md)
