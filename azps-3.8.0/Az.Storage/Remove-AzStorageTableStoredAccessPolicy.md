---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "94019973"
---
# <span data-ttu-id="1b9ec-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b9ec-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="1b9ec-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1b9ec-102">SYNOPSIS</span></span>
<span data-ttu-id="1b9ec-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="1b9ec-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1b9ec-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1b9ec-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1b9ec-105">DESCRIPTION</span></span>
<span data-ttu-id="1b9ec-106">Il cmdlet **Remove-AzStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="1b9ec-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1b9ec-107">EXAMPLES</span></span>

### <span data-ttu-id="1b9ec-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="1b9ec-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="1b9ec-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="1b9ec-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1b9ec-110">PARAMETERS</span></span>

### <span data-ttu-id="1b9ec-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="1b9ec-111">-Context</span></span>
<span data-ttu-id="1b9ec-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1b9ec-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1b9ec-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b9ec-114">-DefaultProfile</span></span>
<span data-ttu-id="1b9ec-115">comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-115">communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b9ec-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b9ec-116">-PassThru</span></span>
<span data-ttu-id="1b9ec-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="1b9ec-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1b9ec-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="1b9ec-119">-Policy</span></span>
<span data-ttu-id="1b9ec-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="1b9ec-121">-Tabella</span><span class="sxs-lookup"><span data-stu-id="1b9ec-121">-Table</span></span>
<span data-ttu-id="1b9ec-122">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="1b9ec-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1b9ec-123">-Confirm</span></span>
<span data-ttu-id="1b9ec-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b9ec-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b9ec-125">-WhatIf</span></span>
<span data-ttu-id="1b9ec-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b9ec-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b9ec-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b9ec-128">CommonParameters</span></span>
<span data-ttu-id="1b9ec-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b9ec-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b9ec-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b9ec-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b9ec-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1b9ec-131">INPUTS</span></span>

### <span data-ttu-id="1b9ec-132">System. String</span><span class="sxs-lookup"><span data-stu-id="1b9ec-132">System.String</span></span>

### <span data-ttu-id="1b9ec-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b9ec-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1b9ec-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1b9ec-134">OUTPUTS</span></span>

### <span data-ttu-id="1b9ec-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1b9ec-135">System.Boolean</span></span>

## <span data-ttu-id="1b9ec-136">Note</span><span class="sxs-lookup"><span data-stu-id="1b9ec-136">NOTES</span></span>

## <span data-ttu-id="1b9ec-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1b9ec-137">RELATED LINKS</span></span>

[<span data-ttu-id="1b9ec-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b9ec-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1b9ec-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b9ec-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1b9ec-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b9ec-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1b9ec-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b9ec-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
