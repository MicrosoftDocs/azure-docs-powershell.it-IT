---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicket.md
ms.openlocfilehash: 368ae4ad814c9414ea211ea6e44c2d3fbda005f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182838"
---
# <span data-ttu-id="03550-101">Get-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="03550-101">Get-AzSupportTicket</span></span>

## <span data-ttu-id="03550-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="03550-102">SYNOPSIS</span></span>
<span data-ttu-id="03550-103">Ottieni ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="03550-103">Get support tickets.</span></span>

## <span data-ttu-id="03550-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="03550-104">SYNTAX</span></span>

### <span data-ttu-id="03550-105">ListParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="03550-105">ListParameterSet (Default)</span></span>
```
Get-AzSupportTicket [-Filter <String>] [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

### <span data-ttu-id="03550-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="03550-106">GetByNameParameterSet</span></span>
```
Get-AzSupportTicket -Name <String> [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount]
 [-Skip <UInt64>] [-First <UInt64>] [<CommonParameters>]
```

## <span data-ttu-id="03550-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="03550-107">DESCRIPTION</span></span>
<span data-ttu-id="03550-108">Ottiene l'elenco dei ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="03550-108">Gets the list of support tickets.</span></span> <span data-ttu-id="03550-109">Se non si specifica alcun parametro, verranno recuperati tutti i ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="03550-109">It will retrieve all the support tickets if you do not specify any parameters.</span></span> <span data-ttu-id="03550-110">È anche possibile filtrare i ticket di supporto in base a Status o CreatedDate usando il parametro Filter.</span><span class="sxs-lookup"><span data-stu-id="03550-110">You can also filter the support tickets by Status or CreatedDate using the Filter parameter.</span></span> <span data-ttu-id="03550-111">Ecco alcuni esempi di valori di filtro che è possibile specificare.</span><span class="sxs-lookup"><span data-stu-id="03550-111">Here are some examples of filter values that you can specify.</span></span>

| <span data-ttu-id="03550-112">Scenario</span><span class="sxs-lookup"><span data-stu-id="03550-112">Scenario</span></span>                                                         | <span data-ttu-id="03550-113">Filtro</span><span class="sxs-lookup"><span data-stu-id="03550-113">Filter</span></span>                                           |
|------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="03550-114">Ottenere i ticket in stato aperto</span><span class="sxs-lookup"><span data-stu-id="03550-114">Get tickets that are in open state</span></span>                               | <span data-ttu-id="03550-115">"Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="03550-115">"Status eq 'Open'"</span></span>                               |
| <span data-ttu-id="03550-116">Ottenere i ticket in stato chiuso</span><span class="sxs-lookup"><span data-stu-id="03550-116">Get tickets that are in closed state</span></span>                             | <span data-ttu-id="03550-117">"Status eq 'Closed'"</span><span class="sxs-lookup"><span data-stu-id="03550-117">"Status eq 'Closed'"</span></span>                             |
| <span data-ttu-id="03550-118">Ottenere i biglietti creati il 20 dicembre 2019 o dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="03550-118">Get tickets that were created on or after 20th Dec, 2019</span></span>         | <span data-ttu-id="03550-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="03550-119">"CreatedDate ge 2019-12-20"</span></span>                      |
| <span data-ttu-id="03550-120">Ottenere i biglietti creati dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="03550-120">Get tickets that were created after 20th Dec, 2019</span></span>               | <span data-ttu-id="03550-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="03550-121">"CreatedDate gt 2019-12-20"</span></span>                      |
| <span data-ttu-id="03550-122">Ottiene i ticket creati dopo il 20 dicembre 2019 in stato aperto</span><span class="sxs-lookup"><span data-stu-id="03550-122">Gets tickets created after 20th Dec, 2019 that are in open state</span></span> | <span data-ttu-id="03550-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span><span class="sxs-lookup"><span data-stu-id="03550-123">"CreatedDate gt 2019-12-20 and Status eq 'Open'"</span></span> |


<span data-ttu-id="03550-124">Questo cmdlet supporta la suddivisione in pagine tramite i parametri First e Skip.</span><span class="sxs-lookup"><span data-stu-id="03550-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="03550-125">È anche possibile recuperare un singolo ticket di supporto specificando il nome del ticket.</span><span class="sxs-lookup"><span data-stu-id="03550-125">You can also retrieve a single support ticket by specifying the ticket name.</span></span> 

## <span data-ttu-id="03550-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="03550-126">EXAMPLES</span></span>

### <span data-ttu-id="03550-127">Esempio 1: Ottenere i primi 2 biglietti</span><span class="sxs-lookup"><span data-stu-id="03550-127">Example 1: Get first 2 tickets</span></span>
```powershell
PS C:\> Get-AzSupportTicket -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="03550-128">Esempio 2: Ottenere i primi 2 ticket dopo aver ignorato i primi 2</span><span class="sxs-lookup"><span data-stu-id="03550-128">Example 2: Get first 2 tickets after skipping the first 2</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Skip 2 -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test3 test title3                  150010521000314 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test4 test title4                  150010521000315 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="03550-129">Esempio 3: Ottenere un ticket di supporto in base al nome</span><span class="sxs-lookup"><span data-stu-id="03550-129">Example 3: Get a support ticket by name</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="03550-130">Esempio 4: Ottenere i primi 2 ticket di supporto filtrati in base allo stato</span><span class="sxs-lookup"><span data-stu-id="03550-130">Example 4: Get first 2 support tickets filtered by status</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Closed'" -First 2

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Minimal  Virtual Machine running Linux Closed 2/5/2020 1:33:53 AM
test2 test title2                  150010521000318 Minimal  Billing                       Closed 2/5/2020 1:33:53 AM
```

### <span data-ttu-id="03550-131">Esempio 5: Ottenere tutti i ticket di supporto nello stato Aperto e creati dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="03550-131">Example 5: Get all support tickets that are in Open state and created after Dec 20th, 2019</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Filter "Status eq 'Open' and CreatedDate gt 2019-12-20"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test6 test title6                  150010521000311 Minimal  Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
test7 test title7                  150010521000312 Minimal  Billing                       Open   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="03550-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="03550-132">PARAMETERS</span></span>

### <span data-ttu-id="03550-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03550-133">-DefaultProfile</span></span>
<span data-ttu-id="03550-134">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="03550-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03550-135">-Filter</span><span class="sxs-lookup"><span data-stu-id="03550-135">-Filter</span></span>
<span data-ttu-id="03550-136">Filtro da applicare ai risultati di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03550-136">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="03550-137">-Name</span><span class="sxs-lookup"><span data-stu-id="03550-137">-Name</span></span>
<span data-ttu-id="03550-138">Nome del ticket di supporto che riceve questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="03550-138">Name of support ticket that this cmdlet gets.</span></span>

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

### <span data-ttu-id="03550-139">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="03550-139">-IncludeTotalCount</span></span>
<span data-ttu-id="03550-140">Segnala il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="03550-140">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="03550-141">Se il cmdlet non riesce a determinare il conteggio totale, viene visualizzato "Numero totale sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="03550-141">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="03550-142">Il numero intero ha una proprietà Accuracy che indica l'affidabilità del valore totale del conteggio.</span><span class="sxs-lookup"><span data-stu-id="03550-142">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="03550-143">Il valore di Precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non è stato in grado di contare gli oggetti, 1,0 indica che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 indica una stima sempre più affidabile.</span><span class="sxs-lookup"><span data-stu-id="03550-143">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="03550-144">-Skip</span><span class="sxs-lookup"><span data-stu-id="03550-144">-Skip</span></span>
<span data-ttu-id="03550-145">Ignora il numero specificato di oggetti e ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="03550-145">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="03550-146">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="03550-146">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="03550-147">-First</span><span class="sxs-lookup"><span data-stu-id="03550-147">-First</span></span>
<span data-ttu-id="03550-148">Ottiene solo il numero specificato di oggetti.</span><span class="sxs-lookup"><span data-stu-id="03550-148">Gets only the specified number of objects.</span></span>
<span data-ttu-id="03550-149">Immettere il numero di oggetti da recuperare.</span><span class="sxs-lookup"><span data-stu-id="03550-149">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="03550-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03550-150">CommonParameters</span></span>
<span data-ttu-id="03550-151">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03550-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03550-152">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="03550-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03550-153">INPUT</span><span class="sxs-lookup"><span data-stu-id="03550-153">INPUTS</span></span>

### <span data-ttu-id="03550-154">Nessuno</span><span class="sxs-lookup"><span data-stu-id="03550-154">None</span></span>

## <span data-ttu-id="03550-155">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="03550-155">OUTPUTS</span></span>

### <span data-ttu-id="03550-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="03550-156">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="03550-157">NOTE</span><span class="sxs-lookup"><span data-stu-id="03550-157">NOTES</span></span>

## <span data-ttu-id="03550-158">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="03550-158">RELATED LINKS</span></span>
