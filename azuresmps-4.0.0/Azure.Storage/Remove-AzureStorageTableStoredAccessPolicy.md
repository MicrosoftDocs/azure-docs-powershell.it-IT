---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
ms.openlocfilehash: c3276a23869633238ebc6b84dfa01934e5ad9896
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93490993"
---
# <span data-ttu-id="4b2f5-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b2f5-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="4b2f5-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4b2f5-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2f5-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="4b2f5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4b2f5-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4b2f5-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4b2f5-105">DESCRIPTION</span></span>
<span data-ttu-id="4b2f5-106">Il cmdlet **Remove-AzureStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="4b2f5-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4b2f5-107">EXAMPLES</span></span>

### <span data-ttu-id="4b2f5-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4b2f5-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="4b2f5-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="4b2f5-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4b2f5-110">PARAMETERS</span></span>

### <span data-ttu-id="4b2f5-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4b2f5-111">-Context</span></span>
<span data-ttu-id="4b2f5-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4b2f5-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4b2f5-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4b2f5-114">-PassThru</span></span>
<span data-ttu-id="4b2f5-115">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4b2f5-116">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4b2f5-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="4b2f5-117">-Policy</span></span>
<span data-ttu-id="4b2f5-118">Specifica i criteri di accesso archiviati, che includono le autorizzazioni per il token SAS.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-118">Specifies the stored access policy, which includes the permissions for this SAS token.</span></span>

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

### <span data-ttu-id="4b2f5-119">-Tabella</span><span class="sxs-lookup"><span data-stu-id="4b2f5-119">-Table</span></span>
<span data-ttu-id="4b2f5-120">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="4b2f5-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4b2f5-121">-Confirm</span></span>
<span data-ttu-id="4b2f5-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4b2f5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4b2f5-123">-WhatIf</span></span>
<span data-ttu-id="4b2f5-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4b2f5-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4b2f5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2f5-126">CommonParameters</span></span>
<span data-ttu-id="4b2f5-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b2f5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2f5-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4b2f5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2f5-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4b2f5-129">INPUTS</span></span>

## <span data-ttu-id="4b2f5-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4b2f5-130">OUTPUTS</span></span>

## <span data-ttu-id="4b2f5-131">Note</span><span class="sxs-lookup"><span data-stu-id="4b2f5-131">NOTES</span></span>

## <span data-ttu-id="4b2f5-132">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4b2f5-132">RELATED LINKS</span></span>

[<span data-ttu-id="4b2f5-133">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b2f5-133">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4b2f5-134">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="4b2f5-134">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="4b2f5-135">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b2f5-135">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="4b2f5-136">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4b2f5-136">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
