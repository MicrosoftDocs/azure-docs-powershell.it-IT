---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 96c6d80f4281b8d3e10d29a288787ff9ebcc5586
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862062"
---
# <span data-ttu-id="fe246-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fe246-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="fe246-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="fe246-102">SYNOPSIS</span></span>
<span data-ttu-id="fe246-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe246-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="fe246-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="fe246-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fe246-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="fe246-105">DESCRIPTION</span></span>
<span data-ttu-id="fe246-106">Il cmdlet **Remove-AzStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe246-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="fe246-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="fe246-107">EXAMPLES</span></span>

### <span data-ttu-id="fe246-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="fe246-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="fe246-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="fe246-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="fe246-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="fe246-110">PARAMETERS</span></span>

### <span data-ttu-id="fe246-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="fe246-111">-Context</span></span>
<span data-ttu-id="fe246-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="fe246-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="fe246-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fe246-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="fe246-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe246-114">-DefaultProfile</span></span>
<span data-ttu-id="fe246-115">comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="fe246-115">communication with Azure.</span></span>

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

### <span data-ttu-id="fe246-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fe246-116">-PassThru</span></span>
<span data-ttu-id="fe246-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="fe246-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="fe246-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="fe246-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="fe246-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="fe246-119">-Policy</span></span>
<span data-ttu-id="fe246-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe246-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="fe246-121">-Tabella</span><span class="sxs-lookup"><span data-stu-id="fe246-121">-Table</span></span>
<span data-ttu-id="fe246-122">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="fe246-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="fe246-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="fe246-123">-Confirm</span></span>
<span data-ttu-id="fe246-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fe246-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fe246-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe246-125">-WhatIf</span></span>
<span data-ttu-id="fe246-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe246-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fe246-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="fe246-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fe246-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe246-128">CommonParameters</span></span>
<span data-ttu-id="fe246-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe246-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe246-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe246-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe246-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="fe246-131">INPUTS</span></span>

### <span data-ttu-id="fe246-132">System. String</span><span class="sxs-lookup"><span data-stu-id="fe246-132">System.String</span></span>

### <span data-ttu-id="fe246-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe246-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="fe246-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="fe246-134">OUTPUTS</span></span>

### <span data-ttu-id="fe246-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fe246-135">System.Boolean</span></span>

## <span data-ttu-id="fe246-136">Note</span><span class="sxs-lookup"><span data-stu-id="fe246-136">NOTES</span></span>

## <span data-ttu-id="fe246-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="fe246-137">RELATED LINKS</span></span>

[<span data-ttu-id="fe246-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fe246-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fe246-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="fe246-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="fe246-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fe246-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="fe246-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fe246-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
