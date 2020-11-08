---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193753"
---
# <span data-ttu-id="faacc-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faacc-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="faacc-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="faacc-102">SYNOPSIS</span></span>
<span data-ttu-id="faacc-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="faacc-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="faacc-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="faacc-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="faacc-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="faacc-105">DESCRIPTION</span></span>
<span data-ttu-id="faacc-106">Il cmdlet **Remove-AzStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="faacc-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="faacc-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="faacc-107">EXAMPLES</span></span>

### <span data-ttu-id="faacc-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="faacc-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="faacc-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="faacc-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="faacc-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="faacc-110">PARAMETERS</span></span>

### <span data-ttu-id="faacc-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="faacc-111">-Context</span></span>
<span data-ttu-id="faacc-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="faacc-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="faacc-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="faacc-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="faacc-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faacc-114">-DefaultProfile</span></span>
<span data-ttu-id="faacc-115">comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="faacc-115">communication with Azure.</span></span>

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

### <span data-ttu-id="faacc-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="faacc-116">-PassThru</span></span>
<span data-ttu-id="faacc-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="faacc-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="faacc-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="faacc-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="faacc-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="faacc-119">-Policy</span></span>
<span data-ttu-id="faacc-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faacc-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="faacc-121">-Tabella</span><span class="sxs-lookup"><span data-stu-id="faacc-121">-Table</span></span>
<span data-ttu-id="faacc-122">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="faacc-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="faacc-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="faacc-123">-Confirm</span></span>
<span data-ttu-id="faacc-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="faacc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="faacc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="faacc-125">-WhatIf</span></span>
<span data-ttu-id="faacc-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faacc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="faacc-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="faacc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="faacc-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faacc-128">CommonParameters</span></span>
<span data-ttu-id="faacc-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="faacc-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faacc-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="faacc-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faacc-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="faacc-131">INPUTS</span></span>

### <span data-ttu-id="faacc-132">System. String</span><span class="sxs-lookup"><span data-stu-id="faacc-132">System.String</span></span>

### <span data-ttu-id="faacc-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="faacc-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="faacc-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="faacc-134">OUTPUTS</span></span>

### <span data-ttu-id="faacc-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="faacc-135">System.Boolean</span></span>

## <span data-ttu-id="faacc-136">Note</span><span class="sxs-lookup"><span data-stu-id="faacc-136">NOTES</span></span>

## <span data-ttu-id="faacc-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="faacc-137">RELATED LINKS</span></span>

[<span data-ttu-id="faacc-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faacc-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="faacc-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="faacc-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="faacc-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faacc-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="faacc-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="faacc-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
