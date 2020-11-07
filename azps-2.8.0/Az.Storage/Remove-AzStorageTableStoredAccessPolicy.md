---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 30CC0D80-505A-4988-B4EC-3B7BC5B76F5D
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 76f36fa6cc7b2ab51604f59fb40170734f5ce99f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93858250"
---
# <span data-ttu-id="50108-101">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="50108-101">Remove-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="50108-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="50108-102">SYNOPSIS</span></span>
<span data-ttu-id="50108-103">Rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="50108-103">Removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="50108-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="50108-104">SYNTAX</span></span>

```
Remove-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="50108-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="50108-105">DESCRIPTION</span></span>
<span data-ttu-id="50108-106">Il cmdlet **Remove-AzStorageTableStoredAccessPolicy** rimuove un criterio di accesso archiviato da una tabella di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="50108-106">The **Remove-AzStorageTableStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage table.</span></span>

## <span data-ttu-id="50108-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="50108-107">EXAMPLES</span></span>

### <span data-ttu-id="50108-108">Esempio 1: rimuovere un criterio di accesso archiviato da una tabella di archiviazione</span><span class="sxs-lookup"><span data-stu-id="50108-108">Example 1: Remove a stored access policy from a storage table</span></span>
```
PS C:\>Remove-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy05"
```

<span data-ttu-id="50108-109">Questo comando rimuove i criteri denominati Policy05 dalla tabella di archiviazione denominata MyTable.</span><span class="sxs-lookup"><span data-stu-id="50108-109">This command removes policy named Policy05 from storage table named MyTable.</span></span>

## <span data-ttu-id="50108-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="50108-110">PARAMETERS</span></span>

### <span data-ttu-id="50108-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="50108-111">-Context</span></span>
<span data-ttu-id="50108-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="50108-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="50108-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="50108-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="50108-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50108-114">-DefaultProfile</span></span>
<span data-ttu-id="50108-115">comunicazioni con Azure.</span><span class="sxs-lookup"><span data-stu-id="50108-115">communication with Azure.</span></span>

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

### <span data-ttu-id="50108-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="50108-116">-PassThru</span></span>
<span data-ttu-id="50108-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="50108-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="50108-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="50108-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="50108-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="50108-119">-Policy</span></span>
<span data-ttu-id="50108-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50108-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="50108-121">-Tabella</span><span class="sxs-lookup"><span data-stu-id="50108-121">-Table</span></span>
<span data-ttu-id="50108-122">Specifica il nome della tabella Azure.</span><span class="sxs-lookup"><span data-stu-id="50108-122">Specifies the Azure table name.</span></span>

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

### <span data-ttu-id="50108-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="50108-123">-Confirm</span></span>
<span data-ttu-id="50108-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="50108-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="50108-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50108-125">-WhatIf</span></span>
<span data-ttu-id="50108-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50108-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50108-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="50108-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="50108-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50108-128">CommonParameters</span></span>
<span data-ttu-id="50108-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50108-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50108-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50108-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50108-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="50108-131">INPUTS</span></span>

### <span data-ttu-id="50108-132">System. String</span><span class="sxs-lookup"><span data-stu-id="50108-132">System.String</span></span>

### <span data-ttu-id="50108-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="50108-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="50108-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="50108-134">OUTPUTS</span></span>

### <span data-ttu-id="50108-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="50108-135">System.Boolean</span></span>

## <span data-ttu-id="50108-136">Note</span><span class="sxs-lookup"><span data-stu-id="50108-136">NOTES</span></span>

## <span data-ttu-id="50108-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="50108-137">RELATED LINKS</span></span>

[<span data-ttu-id="50108-138">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="50108-138">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="50108-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="50108-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="50108-140">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="50108-140">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="50108-141">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="50108-141">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)
