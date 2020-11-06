---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: ''
schema: 2.0.0
ms.openlocfilehash: 116dcc8967ab18d0b67cd3e4eeea91190c38930f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93506947"
---
# <span data-ttu-id="f09f6-101">Remove-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09f6-101">Remove-AzureStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="f09f6-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f09f6-102">SYNOPSIS</span></span>
<span data-ttu-id="f09f6-103">Rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f09f6-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="f09f6-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f09f6-104">SYNTAX</span></span>

```
Remove-AzureStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f09f6-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f09f6-105">DESCRIPTION</span></span>
<span data-ttu-id="f09f6-106">Il cmdlet **Remove-AzureStorageQueueStoredAccessPolicy** rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f09f6-106">The **Remove-AzureStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="f09f6-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f09f6-107">EXAMPLES</span></span>

### <span data-ttu-id="f09f6-108">Esempio 1: rimuovere un criterio di accesso archiviato da una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f09f6-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzureStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="f09f6-109">Questo comando rimuove un criterio di accesso denominato Policy04 dalla coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="f09f6-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="f09f6-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f09f6-110">PARAMETERS</span></span>

### <span data-ttu-id="f09f6-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f09f6-111">-Context</span></span>
<span data-ttu-id="f09f6-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f09f6-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f09f6-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f09f6-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f09f6-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f09f6-114">-PassThru</span></span>
<span data-ttu-id="f09f6-115">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f09f6-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f09f6-116">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f09f6-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f09f6-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="f09f6-117">-Policy</span></span>
<span data-ttu-id="f09f6-118">Specifica i criteri di accesso archiviati, che includono le autorizzazioni per il token SAS (Shared Access Signature).</span><span class="sxs-lookup"><span data-stu-id="f09f6-118">Specifies the stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

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

### <span data-ttu-id="f09f6-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="f09f6-119">-Queue</span></span>
<span data-ttu-id="f09f6-120">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f09f6-120">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="f09f6-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f09f6-121">-Confirm</span></span>
<span data-ttu-id="f09f6-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f09f6-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f09f6-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f09f6-123">-WhatIf</span></span>
<span data-ttu-id="f09f6-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f09f6-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f09f6-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f09f6-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f09f6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f09f6-126">CommonParameters</span></span>
<span data-ttu-id="f09f6-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f09f6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f09f6-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f09f6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f09f6-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f09f6-129">INPUTS</span></span>

## <span data-ttu-id="f09f6-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f09f6-130">OUTPUTS</span></span>

## <span data-ttu-id="f09f6-131">Note</span><span class="sxs-lookup"><span data-stu-id="f09f6-131">NOTES</span></span>

## <span data-ttu-id="f09f6-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f09f6-132">RELATED LINKS</span></span>

[<span data-ttu-id="f09f6-133">Get-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09f6-133">Get-AzureStorageQueueStoredAccessPolicy</span></span>](./Get-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f09f6-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f09f6-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f09f6-135">New-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09f6-135">New-AzureStorageQueueStoredAccessPolicy</span></span>](./New-AzureStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="f09f6-136">Set-AzureStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f09f6-136">Set-AzureStorageQueueStoredAccessPolicy</span></span>](./Set-AzureStorageQueueStoredAccessPolicy.md)
