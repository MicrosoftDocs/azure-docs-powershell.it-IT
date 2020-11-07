---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetablestoredaccesspolicy
schema: 2.0.0
ms.openlocfilehash: 6d32ddf53f675f2ab2897e4bb9ec85655e0fcd14
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866928"
---
# <span data-ttu-id="43f30-101">Remove-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f30-101">Remove-AzureStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="43f30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="43f30-102">SYNOPSIS</span></span>
<span data-ttu-id="43f30-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43f30-103">Removes a stored access policy from an Azure storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="43f30-104">SYNTAX</span></span>

```
Remove-AzureStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43f30-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43f30-105">DESCRIPTION</span></span>
<span data-ttu-id="43f30-106">Il cmdlet **Remove-AzureStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43f30-106">The **Remove-AzureStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="43f30-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="43f30-107">EXAMPLES</span></span>

### <span data-ttu-id="43f30-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="43f30-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzureStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="43f30-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="43f30-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="43f30-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="43f30-110">PARAMETERS</span></span>

### <span data-ttu-id="43f30-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="43f30-111">-Context</span></span>
<span data-ttu-id="43f30-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="43f30-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="43f30-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="43f30-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="43f30-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f30-114">-DefaultProfile</span></span>
<span data-ttu-id="43f30-115">comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="43f30-115">communication with Azure.</span></span>

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

### <span data-ttu-id="43f30-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="43f30-116">-PassThru</span></span>
<span data-ttu-id="43f30-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="43f30-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="43f30-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="43f30-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="43f30-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="43f30-119">-Policy</span></span>
<span data-ttu-id="43f30-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f30-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f30-121">-Tabella</span><span class="sxs-lookup"><span data-stu-id="43f30-121">-Table</span></span>
<span data-ttu-id="43f30-122">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="43f30-122">Specifies the Azure table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="43f30-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="43f30-123">-Confirm</span></span>
<span data-ttu-id="43f30-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f30-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f30-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f30-125">-WhatIf</span></span>
<span data-ttu-id="43f30-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43f30-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f30-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="43f30-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f30-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f30-128">CommonParameters</span></span>
<span data-ttu-id="43f30-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f30-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f30-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f30-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f30-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="43f30-131">INPUTS</span></span>

### <span data-ttu-id="43f30-132">System. String</span><span class="sxs-lookup"><span data-stu-id="43f30-132">System.String</span></span>

### <span data-ttu-id="43f30-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="43f30-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="43f30-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="43f30-134">OUTPUTS</span></span>

### <span data-ttu-id="43f30-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="43f30-135">System.Boolean</span></span>

## <span data-ttu-id="43f30-136">Note</span><span class="sxs-lookup"><span data-stu-id="43f30-136">NOTES</span></span>

## <span data-ttu-id="43f30-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="43f30-137">RELATED LINKS</span></span>

[<span data-ttu-id="43f30-138">Get-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f30-138">Get-AzureStorageTableStoredAccessPolicy</span></span>](./Get-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="43f30-139">New-AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="43f30-139">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="43f30-140">New-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f30-140">New-AzureStorageTableStoredAccessPolicy</span></span>](./New-AzureStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="43f30-141">Set-AzureStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="43f30-141">Set-AzureStorageTableStoredAccessPolicy</span></span>](./Set-AzureStorageTableStoredAccessPolicy.md)
