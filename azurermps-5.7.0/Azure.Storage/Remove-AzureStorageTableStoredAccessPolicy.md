---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
ms.openlocfilehash: a9e1290c5933d54481c57b051e170568653eee5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93519055"
---
# <span data-ttu-id="5e192-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e192-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="5e192-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="5e192-102">SYNOPSIS</span></span>
<span data-ttu-id="5e192-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e192-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e192-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="5e192-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e192-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="5e192-105">DESCRIPTION</span></span>
<span data-ttu-id="5e192-106">Il cmdlet **Remove-AzureStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e192-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="5e192-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="5e192-107">EXAMPLES</span></span>

### <span data-ttu-id="5e192-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="5e192-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="5e192-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="5e192-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="5e192-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="5e192-110">PARAMETERS</span></span>

### <span data-ttu-id="5e192-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="5e192-111">-Context</span></span>
<span data-ttu-id="5e192-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="5e192-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="5e192-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="5e192-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="5e192-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e192-114">-PassThru</span></span>
<span data-ttu-id="5e192-115">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="5e192-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5e192-116">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="5e192-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5e192-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="5e192-117">-Policy</span></span>
<span data-ttu-id="5e192-118">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e192-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5e192-119">-Tabella</span><span class="sxs-lookup"><span data-stu-id="5e192-119">-Table</span></span>
<span data-ttu-id="5e192-120">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="5e192-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="5e192-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="5e192-121">-Confirm</span></span>
<span data-ttu-id="5e192-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e192-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e192-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e192-123">-WhatIf</span></span>
<span data-ttu-id="5e192-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e192-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e192-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="5e192-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e192-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e192-126">CommonParameters</span></span>
<span data-ttu-id="5e192-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e192-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e192-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e192-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e192-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="5e192-129">INPUTS</span></span>

### <span data-ttu-id="5e192-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e192-130">IStorageContext</span></span>

<span data-ttu-id="5e192-131">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="5e192-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="5e192-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="5e192-132">OUTPUTS</span></span>

### <span data-ttu-id="5e192-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e192-133">System.Boolean</span></span>

## <span data-ttu-id="5e192-134">Note</span><span class="sxs-lookup"><span data-stu-id="5e192-134">NOTES</span></span>

## <span data-ttu-id="5e192-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="5e192-135">RELATED LINKS</span></span>

[<span data-ttu-id="5e192-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e192-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5e192-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="5e192-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="5e192-138">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e192-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="5e192-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="5e192-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
