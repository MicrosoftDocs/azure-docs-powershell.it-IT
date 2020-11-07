---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 77e011275a7861f54d25339fe46aad36cffe5e34
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93676518"
---
# <span data-ttu-id="f2999-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f2999-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="f2999-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="f2999-102">SYNOPSIS</span></span>
<span data-ttu-id="f2999-103">Rimuove una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="f2999-103">Removes a storage table.</span></span>

## <span data-ttu-id="f2999-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f2999-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2999-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f2999-105">DESCRIPTION</span></span>
<span data-ttu-id="f2999-106">Il cmdlet **Remove-AzStorageTable** consente di rimuovere una o più tabelle di archiviazione da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="f2999-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="f2999-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f2999-107">EXAMPLES</span></span>

### <span data-ttu-id="f2999-108">Esempio 1: rimuovere una tabella</span><span class="sxs-lookup"><span data-stu-id="f2999-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="f2999-109">Questo comando rimuove una tabella.</span><span class="sxs-lookup"><span data-stu-id="f2999-109">This command removes a table.</span></span>

### <span data-ttu-id="f2999-110">Esempio 2: rimuovere più tabelle</span><span class="sxs-lookup"><span data-stu-id="f2999-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="f2999-111">Questo esempio usa un carattere jolly con il parametro *Name* per ottenere tutte le tabelle che corrispondono alla tabella pattern e quindi passa il risultato sulla pipeline per rimuovere le tabelle.</span><span class="sxs-lookup"><span data-stu-id="f2999-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="f2999-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="f2999-112">PARAMETERS</span></span>

### <span data-ttu-id="f2999-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="f2999-113">-Context</span></span>
<span data-ttu-id="f2999-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="f2999-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f2999-115">Puoi crearlo usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f2999-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f2999-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2999-116">-DefaultProfile</span></span>
<span data-ttu-id="f2999-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="f2999-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2999-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f2999-118">-Force</span></span>
<span data-ttu-id="f2999-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f2999-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f2999-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="f2999-120">-Name</span></span>
<span data-ttu-id="f2999-121">Specifica il nome della tabella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="f2999-121">Specifies the name of the table to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2999-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2999-122">-PassThru</span></span>
<span data-ttu-id="f2999-123">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="f2999-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="f2999-124">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="f2999-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="f2999-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="f2999-125">-Confirm</span></span>
<span data-ttu-id="f2999-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2999-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2999-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2999-127">-WhatIf</span></span>
<span data-ttu-id="f2999-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2999-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2999-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="f2999-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2999-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2999-130">CommonParameters</span></span>
<span data-ttu-id="f2999-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2999-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2999-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2999-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2999-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="f2999-133">INPUTS</span></span>

### <span data-ttu-id="f2999-134">System. String</span><span class="sxs-lookup"><span data-stu-id="f2999-134">System.String</span></span>

### <span data-ttu-id="f2999-135">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f2999-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f2999-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f2999-136">OUTPUTS</span></span>

### <span data-ttu-id="f2999-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f2999-137">System.Boolean</span></span>

## <span data-ttu-id="f2999-138">Note</span><span class="sxs-lookup"><span data-stu-id="f2999-138">NOTES</span></span>

## <span data-ttu-id="f2999-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f2999-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2999-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="f2999-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)