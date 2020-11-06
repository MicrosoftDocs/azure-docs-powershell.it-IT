---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTableStoredAccessPolicy.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 7ee384fb26ed8e16b377800fc7e3912f33b81669
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511403"
---
# <span data-ttu-id="f8216-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f8216-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f8216-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f8216-102">SYNOPSIS</span></span>
<span data-ttu-id="f8216-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8216-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f8216-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f8216-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8216-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f8216-105">DESCRIPTION</span></span>
<span data-ttu-id="f8216-106">Il cmdlet **Remove-AzureStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8216-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="f8216-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f8216-107">EXAMPLES</span></span>

### <span data-ttu-id="f8216-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="f8216-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="f8216-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="f8216-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="f8216-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f8216-110">PARAMETERS</span></span>

### <span data-ttu-id="f8216-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f8216-111">-Context</span></span>
<span data-ttu-id="f8216-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f8216-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f8216-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f8216-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f8216-114">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8216-114">-PassThru</span></span>
<span data-ttu-id="f8216-115">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f8216-115">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f8216-116">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f8216-116">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f8216-117">-Policy</span><span class="sxs-lookup"><span data-stu-id="f8216-117">-Policy</span></span>
<span data-ttu-id="f8216-118">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8216-118">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="f8216-119">-Tabella</span><span class="sxs-lookup"><span data-stu-id="f8216-119">-Table</span></span>
<span data-ttu-id="f8216-120">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="f8216-120">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="f8216-121">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f8216-121">-Confirm</span></span>
<span data-ttu-id="f8216-122">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f8216-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8216-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8216-123">-WhatIf</span></span>
<span data-ttu-id="f8216-124">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8216-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8216-125">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f8216-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8216-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8216-126">CommonParameters</span></span>
<span data-ttu-id="f8216-127">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8216-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8216-128">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8216-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8216-129">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f8216-129">INPUTS</span></span>

### <span data-ttu-id="f8216-130">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8216-130">IStorageContext</span></span>

<span data-ttu-id="f8216-131">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="f8216-131">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="f8216-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f8216-132">OUTPUTS</span></span>

### <span data-ttu-id="f8216-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f8216-133">System.Boolean</span></span>

## <span data-ttu-id="f8216-134">Note</span><span class="sxs-lookup"><span data-stu-id="f8216-134">NOTES</span></span>

## <span data-ttu-id="f8216-135">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f8216-135">RELATED LINKS</span></span>

[<span data-ttu-id="f8216-136">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f8216-136">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f8216-137">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="f8216-137">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="f8216-138">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f8216-138">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f8216-139">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f8216-139">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
