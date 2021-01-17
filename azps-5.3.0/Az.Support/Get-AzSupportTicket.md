---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474584"
---
# <span data-ttu-id="23630-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="23630-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="23630-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="23630-102">SYNOPSIS</span></span>
<span data-ttu-id="23630-103">Ottenere i ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="23630-103">Get support tickets.</span></span>

## <span data-ttu-id="23630-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="23630-104">SYNTAX</span></span>

### <span data-ttu-id="23630-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="23630-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="23630-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="23630-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="23630-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="23630-107">DESCRIPTION</span></span>
<span data-ttu-id="23630-108">Ottiene l'elenco dei ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="23630-108">Gets the list of support tickets.</span></span> <span data-ttu-id="23630-109">Recupererà tutti i ticket di supporto se non specifichi alcun parametro.</span><span class="sxs-lookup"><span data-stu-id="23630-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="23630-110">Puoi anche filtrare i ticket di supporto in base allo stato o I valori CreatedDate usando il parametro Filter.</span><span class="sxs-lookup"><span data-stu-id="23630-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="23630-111">Ecco alcuni esempi di valori di filtro che puoi specificare.</span><span class="sxs-lookup"><span data-stu-id="23630-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="23630-112">Scenario</span><span class="sxs-lookup"><span data-stu-id="23630-112">Scenario</span></span>                                                         | <span data-ttu-id="23630-113">Filtro</span><span class="sxs-lookup"><span data-stu-id="23630-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="23630-114">Ottenere i ticket in stato aperto</span><span class="sxs-lookup"><span data-stu-id="23630-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="23630-115">"Stato EQ ' aperto '"</span><span class="sxs-lookup"><span data-stu-id="23630-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="23630-116">Ottenere i ticket in stato chiuso</span><span class="sxs-lookup"><span data-stu-id="23630-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="23630-117">"Stato EQ ' chiuso '"</span><span class="sxs-lookup"><span data-stu-id="23630-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="23630-118">Ottenere i biglietti creati durante o dopo il 20 dicembre, 2019</span><span class="sxs-lookup"><span data-stu-id="23630-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="23630-119">"I valori CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="23630-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="23630-120">Ottenere i biglietti creati dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="23630-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="23630-121">"I valori CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="23630-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="23630-122">Ottiene i ticket creati dopo il 20 dicembre, 2019 in stato aperto</span><span class="sxs-lookup"><span data-stu-id="23630-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="23630-123">"I valori CreatedDate gt 2019-12-20 e lo stato EQ" aperto ""</span><span class="sxs-lookup"><span data-stu-id="23630-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="23630-124">Questo cmdlet supporta il paging tramite i parametri First e Skip.</span><span class="sxs-lookup"><span data-stu-id="23630-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="23630-125">È anche possibile recuperare un singolo ticket di supporto specificando il nome del ticket.</span><span class="sxs-lookup"><span data-stu-id="23630-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="23630-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="23630-126">EXAMPLES</span></span>

### <span data-ttu-id="23630-127">Esempio 1: ottenere i primi 2 biglietti</span><span class="sxs-lookup"><span data-stu-id="23630-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="23630-128">Esempio 2: ottenere i primi 2 biglietti dopo aver saltato i primi 2</span><span class="sxs-lookup"><span data-stu-id="23630-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="23630-129">Esempio 3: ottenere un ticket di supporto per nome</span><span class="sxs-lookup"><span data-stu-id="23630-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="23630-130">Esempio 4: ottenere i primi 2 ticket di supporto filtrati in base allo stato</span><span class="sxs-lookup"><span data-stu-id="23630-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="23630-131">Esempio 5: ottenere tutti i ticket di supporto in stato aperto e creati dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="23630-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="23630-132">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="23630-132">PARAMETERS</span></span>

### <span data-ttu-id="23630-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23630-133">-DefaultProfile</span></span>
<span data-ttu-id="23630-134">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="23630-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23630-135">-Filtro</span><span class="sxs-lookup"><span data-stu-id="23630-135">-Filter</span></span>
<span data-ttu-id="23630-136">Filtro da applicare ai risultati di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23630-136">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23630-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="23630-137">-Name</span></span>
<span data-ttu-id="23630-138">Nome del ticket di supporto che viene ottenuto da questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23630-138">Name of support ticket that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23630-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="23630-139">-IncludeTotalCount</span></span>
<span data-ttu-id="23630-140">Indica il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="23630-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="23630-141">Se il cmdlet non riesce a determinare il conteggio totale, Visualizza "numero totale sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="23630-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="23630-142">Il numero intero ha una proprietà di precisione che indica l'affidabilità del valore di conteggio totale.</span><span class="sxs-lookup"><span data-stu-id="23630-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="23630-143">Il valore di precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non ha potuto contare gli oggetti, 1,0 significa che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 è una stima sempre più attendibile.</span><span class="sxs-lookup"><span data-stu-id="23630-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="23630-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="23630-144">-Skip</span></span>
<span data-ttu-id="23630-145">Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="23630-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="23630-146">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="23630-146">Enter the number of objects to skip.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23630-147">-Primo</span><span class="sxs-lookup"><span data-stu-id="23630-147">-First</span></span>
<span data-ttu-id="23630-148">Ottiene solo il numero di oggetti specificato.</span><span class="sxs-lookup"><span data-stu-id="23630-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="23630-149">Immettere il numero di oggetti da ottenere.</span><span class="sxs-lookup"><span data-stu-id="23630-149">Enter the number of objects to get.</span></span>

```yaml
Type: System.UInt64
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23630-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23630-150">CommonParameters</span></span>
<span data-ttu-id="23630-151">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23630-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23630-152">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23630-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23630-153">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="23630-153">INPUTS</span></span>

### <span data-ttu-id="23630-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="23630-154">None</span></span>

## <span data-ttu-id="23630-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="23630-155">OUTPUTS</span></span>

### <span data-ttu-id="23630-156">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="23630-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="23630-157">Note</span><span class="sxs-lookup"><span data-stu-id="23630-157">NOTES</span></span>

## <span data-ttu-id="23630-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="23630-158">RELATED LINKS</span></span>
