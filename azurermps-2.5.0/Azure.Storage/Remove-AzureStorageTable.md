---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 1B29AB8C-95DD-4C4F-86E2-2F81E8020CEA
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/remove-azurestoragetable
schema: 2.0.0
ms.openlocfilehash: e33e32051c15483956d0764f5e9ddca25a083f23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93866929"
---
# <span data-ttu-id="ab629-101">Remove-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ab629-101">Remove-AzureStorageTable</span></span>

## <span data-ttu-id="ab629-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ab629-102">SYNOPSIS</span></span>
<span data-ttu-id="ab629-103">Rimuove una tabella di archiviazione.</span><span class="sxs-lookup"><span data-stu-id="ab629-103">Removes a storage table.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ab629-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ab629-104">SYNTAX</span></span>

```
Remove-AzureStorageTable [-Name] <String> [-Force] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab629-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ab629-105">DESCRIPTION</span></span>
<span data-ttu-id="ab629-106">Il cmdlet **Remove-AzureStorageTable** consente di rimuovere una o più tabelle di archiviazione da un account di archiviazione in Azure.</span><span class="sxs-lookup"><span data-stu-id="ab629-106">The **Remove-AzureStorageTable** cmdlet removes one or more storage tables from a storage account in Azure.</span></span>

## <span data-ttu-id="ab629-107">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ab629-107">EXAMPLES</span></span>

### <span data-ttu-id="ab629-108">Esempio 1: rimuovere una tabella</span><span class="sxs-lookup"><span data-stu-id="ab629-108">Example 1: Remove a table</span></span>
```
PS C:\>Remove-AzureStorageTable -Name "TableABC"
```

<span data-ttu-id="ab629-109">Questo comando rimuove una tabella.</span><span class="sxs-lookup"><span data-stu-id="ab629-109">This command removes a table.</span></span>

### <span data-ttu-id="ab629-110">Esempio 2: rimuovere più tabelle</span><span class="sxs-lookup"><span data-stu-id="ab629-110">Example 2: Remove several tables</span></span>
```
PS C:\>Get-AzureStorageTable table* | Remove-AzureStorageTable
```

<span data-ttu-id="ab629-111">Questo esempio usa un carattere jolly con il parametro *Name* per ottenere tutte le tabelle che corrispondono alla tabella pattern e quindi passa il risultato sulla pipeline per rimuovere le tabelle.</span><span class="sxs-lookup"><span data-stu-id="ab629-111">This example uses a wildcard character with the *Name* parameter to get all tables that match the pattern table and then passes the result on the pipeline to remove the tables.</span></span>

## <span data-ttu-id="ab629-112">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ab629-112">PARAMETERS</span></span>

### <span data-ttu-id="ab629-113">-Contesto</span><span class="sxs-lookup"><span data-stu-id="ab629-113">-Context</span></span>
<span data-ttu-id="ab629-114">Specifica il contesto di archiviazione di Azure.</span><span class="sxs-lookup"><span data-stu-id="ab629-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="ab629-115">Puoi crearlo usando il cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ab629-115">You can create it by using the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="ab629-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab629-116">-DefaultProfile</span></span>
<span data-ttu-id="ab629-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ab629-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ab629-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ab629-118">-Force</span></span>
<span data-ttu-id="ab629-119">Impone l'esecuzione del comando senza richiedere la conferma dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ab629-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ab629-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ab629-120">-Name</span></span>
<span data-ttu-id="ab629-121">Specifica il nome della tabella da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ab629-121">Specifies the name of the table to remove.</span></span>

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

### <span data-ttu-id="ab629-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab629-122">-PassThru</span></span>
<span data-ttu-id="ab629-123">Indica che questo cmdlet restituisce un **valore booleano** che riflette l'esito positivo dell'operazione.</span><span class="sxs-lookup"><span data-stu-id="ab629-123">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="ab629-124">Per impostazione predefinita, questo cmdlet non restituisce un valore.</span><span class="sxs-lookup"><span data-stu-id="ab629-124">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="ab629-125">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ab629-125">-Confirm</span></span>
<span data-ttu-id="ab629-126">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab629-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab629-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab629-127">-WhatIf</span></span>
<span data-ttu-id="ab629-128">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab629-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ab629-129">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ab629-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab629-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab629-130">CommonParameters</span></span>
<span data-ttu-id="ab629-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab629-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab629-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ab629-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab629-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ab629-133">INPUTS</span></span>

### <span data-ttu-id="ab629-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ab629-134">System.String</span></span>

### <span data-ttu-id="ab629-135">Microsoft. Azure. Commands. Common. Authentication. Abstracttions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="ab629-135">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="ab629-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ab629-136">OUTPUTS</span></span>

### <span data-ttu-id="ab629-137">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ab629-137">System.Boolean</span></span>

## <span data-ttu-id="ab629-138">Note</span><span class="sxs-lookup"><span data-stu-id="ab629-138">NOTES</span></span>

## <span data-ttu-id="ab629-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ab629-139">RELATED LINKS</span></span>

[<span data-ttu-id="ab629-140">Get-AzureStorageTable</span><span class="sxs-lookup"><span data-stu-id="ab629-140">Get-AzureStorageTable</span></span>](./Get-AzureStorageTable.md)
