---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: 7423cbb6995430523beb137ef10eb6f1a53c959c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686531"
---
# <span data-ttu-id="97db7-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="97db7-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="97db7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="97db7-102">SYNOPSIS</span></span>
<span data-ttu-id="97db7-103">Rimuove una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="97db7-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97db7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="97db7-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97db7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97db7-105">DESCRIPTION</span></span>
<span data-ttu-id="97db7-106">Il cmdlet **Remove-AzureStorageTable** consente di rimuovere una o più tabelle di archiviazione da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="97db7-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="97db7-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="97db7-107">EXAMPLES</span></span>

### <span data-ttu-id="97db7-108">Esempio 1: rimuovere una tabella</span><span class="sxs-lookup"><span data-stu-id="97db7-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="97db7-109">Questo comando rimuove una tabella.</span><span class="sxs-lookup"><span data-stu-id="97db7-109">This command removes a table.</span></span>

### <span data-ttu-id="97db7-110">Esempio 2: rimuovere più tabelle</span><span class="sxs-lookup"><span data-stu-id="97db7-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="97db7-111">Questo esempio usa un carattere jolly con il parametro *Name* per ottenere tutte le tabelle che corrispondono alla tabella pattern e quindi passa il risultato sulla pipeline per rimuovere le tabelle.</span><span class="sxs-lookup"><span data-stu-id="97db7-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="97db7-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="97db7-112">PARAMETERS</span></span>

### <span data-ttu-id="97db7-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="97db7-113">-Context</span></span>
<span data-ttu-id="97db7-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="97db7-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="97db7-115">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="97db7-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97db7-116">-Force</span><span class="sxs-lookup"><span data-stu-id="97db7-116">-Force</span></span>
<span data-ttu-id="97db7-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="97db7-117">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db7-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="97db7-118">-Name</span></span>
<span data-ttu-id="97db7-119">Specifica il nome della tabella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="97db7-119">Specifies the name of the table to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, Table

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="97db7-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="97db7-120">-PassThru</span></span>
<span data-ttu-id="97db7-121">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="97db7-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="97db7-122">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="97db7-122">By default, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db7-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="97db7-123">-Confirm</span></span>
<span data-ttu-id="97db7-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="97db7-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db7-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97db7-125">-WhatIf</span></span>
<span data-ttu-id="97db7-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97db7-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97db7-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="97db7-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97db7-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97db7-128">CommonParameters</span></span>
<span data-ttu-id="97db7-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97db7-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97db7-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97db7-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97db7-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="97db7-131">INPUTS</span></span>

### <span data-ttu-id="97db7-132">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="97db7-132">IStorageContext</span></span>

<span data-ttu-id="97db7-133">Il parametro "context" accetta il valore di tipo "IStorageContext" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="97db7-133">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

### <span data-ttu-id="97db7-134">Stringa</span><span class="sxs-lookup"><span data-stu-id="97db7-134">String</span></span>

<span data-ttu-id="97db7-135">Il parametro "Name" accetta il valore di tipo "String" dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="97db7-135">Parameter 'Name' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="97db7-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="97db7-136">OUTPUTS</span></span>

### <span data-ttu-id="97db7-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="97db7-137">System.Boolean</span></span>

## <span data-ttu-id="97db7-138">Note</span><span class="sxs-lookup"><span data-stu-id="97db7-138">NOTES</span></span>

## <span data-ttu-id="97db7-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="97db7-139">RELATED LINKS</span></span>

[<span data-ttu-id="97db7-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="97db7-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
