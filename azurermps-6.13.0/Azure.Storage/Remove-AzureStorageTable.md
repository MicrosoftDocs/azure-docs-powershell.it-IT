---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Remove-AzureStorageTable.md
ms.openlocfilehash: a4083920e935077658d218663e0a0255f6566ff8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686281"
---
# <span data-ttu-id="3fd2c-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3fd2c-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="3fd2c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="3fd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd2c-103">Rimuove una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd2c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="3fd2c-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd2c-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3fd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd2c-106">Il cmdlet **Remove-AzureStorageTable** consente di rimuovere una o più tabelle di archiviazione da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="3fd2c-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="3fd2c-107">EXAMPLES</span></span>

### <span data-ttu-id="3fd2c-108">Esempio 1: rimuovere una tabella</span><span class="sxs-lookup"><span data-stu-id="3fd2c-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="3fd2c-109">Questo comando rimuove una tabella.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-109">This command removes a table.</span></span>

### <span data-ttu-id="3fd2c-110">Esempio 2: rimuovere più tabelle</span><span class="sxs-lookup"><span data-stu-id="3fd2c-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="3fd2c-111">Questo esempio usa un carattere jolly con il parametro *Name* per ottenere tutte le tabelle che corrispondono alla tabella pattern e quindi passa il risultato sulla pipeline per rimuovere le tabelle.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="3fd2c-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="3fd2c-112">PARAMETERS</span></span>

### <span data-ttu-id="3fd2c-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="3fd2c-113">-Context</span></span>
<span data-ttu-id="3fd2c-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="3fd2c-115">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="3fd2c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd2c-116">-DefaultProfile</span></span>
<span data-ttu-id="3fd2c-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3fd2c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="3fd2c-118">-Force</span></span>
<span data-ttu-id="3fd2c-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3fd2c-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3fd2c-120">-Name</span></span>
<span data-ttu-id="3fd2c-121">Specifica il nome della tabella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="3fd2c-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3fd2c-122">-PassThru</span></span>
<span data-ttu-id="3fd2c-123">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="3fd2c-124">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="3fd2c-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="3fd2c-125">-Confirm</span></span>
<span data-ttu-id="3fd2c-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3fd2c-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd2c-127">-WhatIf</span></span>
<span data-ttu-id="3fd2c-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3fd2c-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3fd2c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd2c-130">CommonParameters</span></span>
<span data-ttu-id="3fd2c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd2c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd2c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd2c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd2c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="3fd2c-133">INPUTS</span></span>

### <span data-ttu-id="3fd2c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd2c-134">System.String</span></span>

### <span data-ttu-id="3fd2c-135">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="3fd2c-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="3fd2c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="3fd2c-136">OUTPUTS</span></span>

### <span data-ttu-id="3fd2c-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3fd2c-137">System.Boolean</span></span>

## <span data-ttu-id="3fd2c-138">Note</span><span class="sxs-lookup"><span data-stu-id="3fd2c-138">NOTES</span></span>

## <span data-ttu-id="3fd2c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="3fd2c-139">RELATED LINKS</span></span>

[<span data-ttu-id="3fd2c-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="3fd2c-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
