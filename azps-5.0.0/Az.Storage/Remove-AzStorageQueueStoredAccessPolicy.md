---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 80DE5D60-93F8-4509-AA9C-F54E4AB70013
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragequeuestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageQueueStoredAccessPolicy.md
ms.openlocfilehash: f5620baf0cbd2f5c195b981787ac9def98851fe2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94193760"
---
# <span data-ttu-id="a5162-101">Remove-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5162-101">Remove-AzStorageQueueStoredAccessPolicy</span></span>

## <span data-ttu-id="a5162-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a5162-102">SYNOPSIS</span></span>
<span data-ttu-id="a5162-103">Rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5162-103">Removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="a5162-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a5162-104">SYNTAX</span></span>

```
Remove-AzStorageQueueStoredAccessPolicy [-Queue] <String> [-Policy] <String> [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a5162-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a5162-105">DESCRIPTION</span></span>
<span data-ttu-id="a5162-106">Il cmdlet **Remove-AzStorageQueueStoredAccessPolicy** rimuove un criterio di accesso archiviato da una coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5162-106">The **Remove-AzStorageQueueStoredAccessPolicy** cmdlet removes a stored access policy from an Azure storage queue.</span></span>

## <span data-ttu-id="a5162-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a5162-107">EXAMPLES</span></span>

### <span data-ttu-id="a5162-108">Esempio 1: rimuovere un criterio di accesso archiviato da una coda di archiviazione</span><span class="sxs-lookup"><span data-stu-id="a5162-108">Example 1: Remove a stored access policy from a storage queue</span></span>
```
PS C:\>Remove-AzStorageQueueStoredAccessPolicy -Queue "MyQueue" -Policy "Policy04"
```

<span data-ttu-id="a5162-109">Questo comando rimuove un criterio di accesso denominato Policy04 dalla coda di archiviazione denominata Queue.</span><span class="sxs-lookup"><span data-stu-id="a5162-109">This command removes an access policy named Policy04 from the storage queue named MyQueue.</span></span>

## <span data-ttu-id="a5162-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a5162-110">PARAMETERS</span></span>

### <span data-ttu-id="a5162-111">-Contesto</span><span class="sxs-lookup"><span data-stu-id="a5162-111">-Context</span></span>
<span data-ttu-id="a5162-112">Specifica un contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5162-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="a5162-113">Per ottenere un contesto di archiviazione, usare il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="a5162-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="a5162-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5162-114">-DefaultProfile</span></span>
<span data-ttu-id="a5162-115">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a5162-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5162-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5162-116">-PassThru</span></span>
<span data-ttu-id="a5162-117">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="a5162-117">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="a5162-118">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="a5162-118">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="a5162-119">-Policy</span><span class="sxs-lookup"><span data-stu-id="a5162-119">-Policy</span></span>
<span data-ttu-id="a5162-120">Specifica il nome dei criteri di accesso archiviati rimossi dal cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5162-120">Specifies the name of the stored access policy that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a5162-121">-Queue</span><span class="sxs-lookup"><span data-stu-id="a5162-121">-Queue</span></span>
<span data-ttu-id="a5162-122">Specifica il nome della coda di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="a5162-122">Specifies the Azure storage queue name.</span></span>

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

### <span data-ttu-id="a5162-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a5162-123">-Confirm</span></span>
<span data-ttu-id="a5162-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5162-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5162-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5162-125">-WhatIf</span></span>
<span data-ttu-id="a5162-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5162-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5162-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a5162-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5162-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5162-128">CommonParameters</span></span>
<span data-ttu-id="a5162-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5162-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5162-130">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5162-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5162-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a5162-131">INPUTS</span></span>

### <span data-ttu-id="a5162-132">System. String</span><span class="sxs-lookup"><span data-stu-id="a5162-132">System.String</span></span>

### <span data-ttu-id="a5162-133">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5162-133">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="a5162-134">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a5162-134">OUTPUTS</span></span>

### <span data-ttu-id="a5162-135">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5162-135">System.Boolean</span></span>

## <span data-ttu-id="a5162-136">Note</span><span class="sxs-lookup"><span data-stu-id="a5162-136">NOTES</span></span>

## <span data-ttu-id="a5162-137">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a5162-137">RELATED LINKS</span></span>

[<span data-ttu-id="a5162-138">Get-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5162-138">Get-AzStorageQueueStoredAccessPolicy</span></span>](./Get-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a5162-139">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="a5162-139">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="a5162-140">New-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5162-140">New-AzStorageQueueStoredAccessPolicy</span></span>](./New-AzStorageQueueStoredAccessPolicy.md)

[<span data-ttu-id="a5162-141">Set-AzStorageQueueStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5162-141">Set-AzStorageQueueStoredAccessPolicy</span></span>](./Set-AzStorageQueueStoredAccessPolicy.md)