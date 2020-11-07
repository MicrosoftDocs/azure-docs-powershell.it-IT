---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fcb08eb9e63917d072630f81a2026d961a70dd27
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93685174"
---
# <span data-ttu-id="c041e-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c041e-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="c041e-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="c041e-102">SYNOPSIS</span></span>
<span data-ttu-id="c041e-103">Rimuove una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="c041e-103">Removes a storage table.</span></span>

## <span data-ttu-id="c041e-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c041e-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c041e-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="c041e-105">DESCRIPTION</span></span>
<span data-ttu-id="c041e-106">Il cmdlet **Remove-AzureStorageTable** consente di rimuovere una o più tabelle di archiviazione da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="c041e-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="c041e-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c041e-107">EXAMPLES</span></span>

### <span data-ttu-id="c041e-108">Esempio 1: rimuovere una tabella</span><span class="sxs-lookup"><span data-stu-id="c041e-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="c041e-109">Questo comando rimuove una tabella.</span><span class="sxs-lookup"><span data-stu-id="c041e-109">This command removes a table.</span></span>

### <span data-ttu-id="c041e-110">Esempio 2: rimuovere più tabelle</span><span class="sxs-lookup"><span data-stu-id="c041e-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="c041e-111">Questo esempio usa un carattere jolly con il parametro *Name* per ottenere tutte le tabelle che corrispondono alla tabella pattern e quindi passa il risultato sulla pipeline per rimuovere le tabelle.</span><span class="sxs-lookup"><span data-stu-id="c041e-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="c041e-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="c041e-112">PARAMETERS</span></span>

### <span data-ttu-id="c041e-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="c041e-113">-Context</span></span>
<span data-ttu-id="c041e-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="c041e-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="c041e-115">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="c041e-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="c041e-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c041e-116">-Force</span></span>
<span data-ttu-id="c041e-117">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="c041e-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="c041e-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="c041e-118">-Name</span></span>
<span data-ttu-id="c041e-119">Specifica il nome della tabella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c041e-119">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="c041e-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c041e-120">-PassThru</span></span>
<span data-ttu-id="c041e-121">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="c041e-121">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="c041e-122">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="c041e-122">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="c041e-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="c041e-123">-Confirm</span></span>
<span data-ttu-id="c041e-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c041e-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c041e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c041e-125">-WhatIf</span></span>
<span data-ttu-id="c041e-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c041e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c041e-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c041e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c041e-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c041e-128">CommonParameters</span></span>
<span data-ttu-id="c041e-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c041e-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c041e-130">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c041e-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c041e-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="c041e-131">INPUTS</span></span>

## <span data-ttu-id="c041e-132">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c041e-132">OUTPUTS</span></span>

## <span data-ttu-id="c041e-133">Note</span><span class="sxs-lookup"><span data-stu-id="c041e-133">NOTES</span></span>

## <span data-ttu-id="c041e-134">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c041e-134">RELATED LINKS</span></span>

[<span data-ttu-id="c041e-135">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="c041e-135">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
