---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: 32bf76e80dbd088b133d4401dc51bb1f49b2593b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93857741"
---
# <span data-ttu-id="4c140-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c140-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="4c140-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c140-102">SYNOPSIS</span></span>
<span data-ttu-id="4c140-103">Rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c140-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="4c140-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c140-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4c140-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c140-105">DESCRIPTION</span></span>
<span data-ttu-id="4c140-106">Il cmdlet **Remove-AzStorageQueueStoredAccessPolicy** rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c140-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="4c140-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c140-107">EXAMPLES</span></span>

### <span data-ttu-id="4c140-108">Esempio 1: rimuovere un criterio di accesso archiviato da una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="4c140-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="4c140-109">Questo comando rimuove un criterio di accesso denominato Policy04 dalla coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="4c140-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="4c140-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c140-110">PARAMETERS</span></span>

### <span data-ttu-id="4c140-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="4c140-111">-Context</span></span>
<span data-ttu-id="4c140-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c140-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4c140-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="4c140-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4c140-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c140-114">-DefaultProfile</span></span>
<span data-ttu-id="4c140-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c140-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c140-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c140-116">-PassThru</span></span>
<span data-ttu-id="4c140-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="4c140-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="4c140-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="4c140-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4c140-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="4c140-119">-Policy</span></span>
<span data-ttu-id="4c140-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c140-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4c140-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="4c140-121">-Queue</span></span>
<span data-ttu-id="4c140-122">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="4c140-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="4c140-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c140-123">-Confirm</span></span>
<span data-ttu-id="4c140-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c140-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c140-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c140-125">-WhatIf</span></span>
<span data-ttu-id="4c140-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c140-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c140-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c140-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c140-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c140-128">CommonParameters</span></span>
<span data-ttu-id="4c140-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c140-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c140-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c140-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c140-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c140-131">INPUTS</span></span>

### <span data-ttu-id="4c140-132">System. String</span><span class="sxs-lookup"><span data-stu-id="4c140-132">System.String</span></span>

### <span data-ttu-id="4c140-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c140-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4c140-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c140-134">OUTPUTS</span></span>

### <span data-ttu-id="4c140-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c140-135">System.Boolean</span></span>

## <span data-ttu-id="4c140-136">Note</span><span class="sxs-lookup"><span data-stu-id="4c140-136">NOTES</span></span>

## <span data-ttu-id="4c140-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c140-137">RELATED LINKS</span></span>

[<span data-ttu-id="4c140-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c140-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4c140-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4c140-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="4c140-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c140-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="4c140-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4c140-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)
