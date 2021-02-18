---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 9df25558c752b47e41bf76f7db128bd127ad0c53
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190735"
---
# <span data-ttu-id="7b472-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b472-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="7b472-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b472-102">SYNOPSIS</span></span>
<span data-ttu-id="7b472-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b472-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="7b472-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7b472-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7b472-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="7b472-105">DESCRIPTION</span></span>
<span data-ttu-id="7b472-106">Il cmdlet **Remove-AzStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b472-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="7b472-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7b472-107">EXAMPLES</span></span>

### <span data-ttu-id="7b472-108">Esempio 1: Rimuovere criteri di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="7b472-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="7b472-109">Questo comando rimuove il criterio denominato Policy05 dalla tabella di archiviazione denominata Tabella_</span><span class="sxs-lookup"><span data-stu-id="7b472-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="7b472-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b472-110">PARAMETERS</span></span>

### <span data-ttu-id="7b472-111">-Context</span><span class="sxs-lookup"><span data-stu-id="7b472-111">-Context</span></span>
<span data-ttu-id="7b472-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b472-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="7b472-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext archiviazione.</span><span class="sxs-lookup"><span data-stu-id="7b472-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="7b472-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b472-114">-DefaultProfile</span></span>
<span data-ttu-id="7b472-115">comunicare con Azure.</span><span class="sxs-lookup"><span data-stu-id="7b472-115">communication with Azure.</span></span>

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

### <span data-ttu-id="7b472-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b472-116">-PassThru</span></span>
<span data-ttu-id="7b472-117">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="7b472-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="7b472-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="7b472-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="7b472-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="7b472-119">-Policy</span></span>
<span data-ttu-id="7b472-120">Specifica il nome dei criteri di accesso archiviato rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b472-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7b472-121">-Table</span><span class="sxs-lookup"><span data-stu-id="7b472-121">-Table</span></span>
<span data-ttu-id="7b472-122">Specifica il nome della tabella di Azure.</span><span class="sxs-lookup"><span data-stu-id="7b472-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="7b472-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b472-123">-Confirm</span></span>
<span data-ttu-id="7b472-124">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b472-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b472-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b472-125">-WhatIf</span></span>
<span data-ttu-id="7b472-126">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b472-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b472-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7b472-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b472-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b472-128">CommonParameters</span></span>
<span data-ttu-id="7b472-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b472-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b472-130">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b472-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b472-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="7b472-131">INPUTS</span></span>

### <span data-ttu-id="7b472-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7b472-132">System.String</span></span>

### <span data-ttu-id="7b472-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b472-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="7b472-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7b472-134">OUTPUTS</span></span>

### <span data-ttu-id="7b472-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b472-135">System.Boolean</span></span>

## <span data-ttu-id="7b472-136">NOTE</span><span class="sxs-lookup"><span data-stu-id="7b472-136">NOTES</span></span>

## <span data-ttu-id="7b472-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7b472-137">RELATED LINKS</span></span>

[<span data-ttu-id="7b472-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b472-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7b472-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="7b472-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="7b472-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b472-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="7b472-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="7b472-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
