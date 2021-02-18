---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azstoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageTable.md
ms.openlocfilehash: 98ffbfe7153ba0592563b21695e1a4d1c227f99a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190742"
---
# <span data-ttu-id="6277c-101">Remove-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6277c-101">Remove-AzStorageTable</span></span>

## <span data-ttu-id="6277c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6277c-102">SYNOPSIS</span></span>
<span data-ttu-id="6277c-103">Rimuove una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="6277c-103">Removes a storage table.</span></span>

## <span data-ttu-id="6277c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6277c-104">SYNTAX</span></span>

```
Remove-AzStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6277c-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="6277c-105">DESCRIPTION</span></span>
<span data-ttu-id="6277c-106">Il cmdlet **Remove-AzStorageTable** rimuove una o più tabelle di archiviazione da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="6277c-106">The **Remove-AzStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="6277c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6277c-107">EXAMPLES</span></span>

### <span data-ttu-id="6277c-108">Esempio 1: Rimuovere una tabella</span><span class="sxs-lookup"><span data-stu-id="6277c-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzStorageTable -Name "TableABC"
```

<span data-ttu-id="6277c-109">Questo comando rimuove una tabella.</span><span class="sxs-lookup"><span data-stu-id="6277c-109">This command removes a table.</span></span>

### <span data-ttu-id="6277c-110">Esempio 2: Rimuovere più tabelle</span><span class="sxs-lookup"><span data-stu-id="6277c-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzStorageTable table* | Remove-AzStorageTable
```

<span data-ttu-id="6277c-111">Questo esempio usa un carattere jolly con il parametro *Name* per ottenere tutte le tabelle che corrispondono alla tabella dei criteri e quindi passa il risultato alla pipeline per rimuovere le tabelle.</span><span class="sxs-lookup"><span data-stu-id="6277c-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="6277c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6277c-112">PARAMETERS</span></span>

### <span data-ttu-id="6277c-113">-Context</span><span class="sxs-lookup"><span data-stu-id="6277c-113">-Context</span></span>
<span data-ttu-id="6277c-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="6277c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="6277c-115">È possibile crearla usando il cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="6277c-115">You can create it by using the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6277c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6277c-116">-DefaultProfile</span></span>
<span data-ttu-id="6277c-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6277c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6277c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="6277c-118">-Force</span></span>
<span data-ttu-id="6277c-119">Forza l'esecuzione del comando senza chiedere conferma all'utente.</span><span class="sxs-lookup"><span data-stu-id="6277c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6277c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6277c-120">-Name</span></span>
<span data-ttu-id="6277c-121">Specifica il nome della tabella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="6277c-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="6277c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6277c-122">-PassThru</span></span>
<span data-ttu-id="6277c-123">Indica che questo cmdlet restituisce un valore **booleano** che riflette l'esito dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="6277c-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="6277c-124">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="6277c-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="6277c-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6277c-125">-Confirm</span></span>
<span data-ttu-id="6277c-126">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6277c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6277c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6277c-127">-WhatIf</span></span>
<span data-ttu-id="6277c-128">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6277c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6277c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6277c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6277c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6277c-130">CommonParameters</span></span>
<span data-ttu-id="6277c-131">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6277c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6277c-132">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6277c-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6277c-133">INPUT</span><span class="sxs-lookup"><span data-stu-id="6277c-133">INPUTS</span></span>

### <span data-ttu-id="6277c-134">System.String</span><span class="sxs-lookup"><span data-stu-id="6277c-134">System.String</span></span>

### <span data-ttu-id="6277c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6277c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6277c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6277c-136">OUTPUTS</span></span>

### <span data-ttu-id="6277c-137">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6277c-137">System.Boolean</span></span>

## <span data-ttu-id="6277c-138">NOTE</span><span class="sxs-lookup"><span data-stu-id="6277c-138">NOTES</span></span>

## <span data-ttu-id="6277c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6277c-139">RELATED LINKS</span></span>

[<span data-ttu-id="6277c-140">Get-AzStorageTable</span><span class="sxs-lookup"><span data-stu-id="6277c-140">Get-AzStorageTable</span></span>](./Get-AzStorageTable.md)
