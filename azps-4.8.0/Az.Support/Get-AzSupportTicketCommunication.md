---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 07a8747f94f9c1fb93bbff06ce855363088a67a0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191130"
---
# <span data-ttu-id="2450a-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="2450a-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="2450a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="2450a-102">SYNOPSIS</span></span>
<span data-ttu-id="2450a-103">Ottenere comunicazioni di ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="2450a-103">Get support ticket communications.</span></span>

## <span data-ttu-id="2450a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="2450a-104">SYNTAX</span></span>

### <span data-ttu-id="2450a-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="2450a-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="2450a-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2450a-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="2450a-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2450a-107">DESCRIPTION</span></span>
<span data-ttu-id="2450a-108">Ottiene le comunicazioni per un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="2450a-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="2450a-109">Recupererà tutte le comunicazioni per un ticket se non specifichi altri parametri.</span><span class="sxs-lookup"><span data-stu-id="2450a-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="2450a-110">Puoi anche filtrare le comunicazioni tramite I valori CreatedDate o CommunicationType usando il parametro Filter.</span><span class="sxs-lookup"><span data-stu-id="2450a-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="2450a-111">Ecco alcuni esempi di valori di filtro che puoi specificare.</span><span class="sxs-lookup"><span data-stu-id="2450a-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="2450a-112">Scenario</span><span class="sxs-lookup"><span data-stu-id="2450a-112">Scenario</span></span>                                                        | <span data-ttu-id="2450a-113">Filtro</span><span class="sxs-lookup"><span data-stu-id="2450a-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="2450a-114">Ottenere comunicazioni Web</span><span class="sxs-lookup"><span data-stu-id="2450a-114">Get Web communications</span></span>                                          | <span data-ttu-id="2450a-115">"CommunicationType EQ" Web "</span><span class="sxs-lookup"><span data-stu-id="2450a-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="2450a-116">Ottenere comunicazioni telefoniche</span><span class="sxs-lookup"><span data-stu-id="2450a-116">Get Phone communications</span></span>                                        | <span data-ttu-id="2450a-117">"Telefono ' EQ CommunicationType '"</span><span class="sxs-lookup"><span data-stu-id="2450a-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="2450a-118">Ottenere comunicazioni create durante o dopo il 20 dicembre, 2019</span><span class="sxs-lookup"><span data-stu-id="2450a-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="2450a-119">"I valori CreatedDate GE 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="2450a-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="2450a-120">Ottenere comunicazioni create dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="2450a-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="2450a-121">"I valori CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="2450a-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="2450a-122">Ottiene le comunicazioni Web create dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="2450a-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="2450a-123">"I valori CreatedDate gt 2019-12-20 e CommunicationType EQ" Web "</span><span class="sxs-lookup"><span data-stu-id="2450a-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="2450a-124">Questo cmdlet supporta il paging tramite i parametri First e Skip.</span><span class="sxs-lookup"><span data-stu-id="2450a-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="2450a-125">È anche possibile recuperare una singola comunicazione ticket di supporto specificando il nome della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="2450a-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="2450a-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="2450a-126">EXAMPLES</span></span>

### <span data-ttu-id="2450a-127">Esempio 1: recuperare tutte le comunicazioni per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="2450a-128">Esempio 2: recuperare una singola comunicazione per il nome di un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="2450a-129">Esempio 3: recuperare le prime 2 comunicazioni per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2450a-130">Esempio 4: recuperare le 2 comunicazioni successive dopo aver saltato le prime 2 comunicazioni per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2450a-131">Esempio 5: recuperare tutte le comunicazioni Web per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2450a-132">Esempio 6: recuperare tutte le comunicazioni create in o dopo il 20 dicembre 2019 per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2450a-133">Esempio 7: recuperare tutte le comunicazioni Web create o dopo il 20 dicembre 2019 per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="2450a-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="2450a-134">Esempio 8: recuperare tutte le comunicazioni per un ticket di supporto tramite l'oggetto ticket di supporto piping</span><span class="sxs-lookup"><span data-stu-id="2450a-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="2450a-135">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="2450a-135">PARAMETERS</span></span>

### <span data-ttu-id="2450a-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2450a-136">-DefaultProfile</span></span>
<span data-ttu-id="2450a-137">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="2450a-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2450a-138">-Filtro</span><span class="sxs-lookup"><span data-stu-id="2450a-138">-Filter</span></span>
<span data-ttu-id="2450a-139">Filtro da applicare ai risultati di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2450a-139">Filter to be applied to the results of this cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2450a-140">-Nome</span><span class="sxs-lookup"><span data-stu-id="2450a-140">-Name</span></span>
<span data-ttu-id="2450a-141">Nome comunicazione.</span><span class="sxs-lookup"><span data-stu-id="2450a-141">Communication name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2450a-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="2450a-142">-SupportTicketName</span></span>
<span data-ttu-id="2450a-143">Nome del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="2450a-143">Support ticket name.</span></span>

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

### <span data-ttu-id="2450a-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="2450a-144">-SupportTicketObject</span></span>
<span data-ttu-id="2450a-145">Oggetto ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="2450a-145">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: GetByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2450a-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="2450a-146">-IncludeTotalCount</span></span>
<span data-ttu-id="2450a-147">Indica il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="2450a-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="2450a-148">Se il cmdlet non riesce a determinare il conteggio totale, Visualizza "numero totale sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="2450a-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="2450a-149">Il numero intero ha una proprietà di precisione che indica l'affidabilità del valore di conteggio totale.</span><span class="sxs-lookup"><span data-stu-id="2450a-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="2450a-150">Il valore di precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non ha potuto contare gli oggetti, 1,0 significa che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 è una stima sempre più attendibile.</span><span class="sxs-lookup"><span data-stu-id="2450a-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="2450a-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="2450a-151">-Skip</span></span>
<span data-ttu-id="2450a-152">Ignora il numero di oggetti specificato e quindi recupera gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="2450a-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="2450a-153">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="2450a-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="2450a-154">-Primo</span><span class="sxs-lookup"><span data-stu-id="2450a-154">-First</span></span>
<span data-ttu-id="2450a-155">Ottiene solo il numero di oggetti specificato.</span><span class="sxs-lookup"><span data-stu-id="2450a-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="2450a-156">Immettere il numero di oggetti da ottenere.</span><span class="sxs-lookup"><span data-stu-id="2450a-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="2450a-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2450a-157">CommonParameters</span></span>
<span data-ttu-id="2450a-158">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2450a-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2450a-159">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2450a-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2450a-160">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="2450a-160">INPUTS</span></span>

### <span data-ttu-id="2450a-161">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="2450a-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="2450a-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="2450a-162">OUTPUTS</span></span>

### <span data-ttu-id="2450a-163">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="2450a-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="2450a-164">Note</span><span class="sxs-lookup"><span data-stu-id="2450a-164">NOTES</span></span>

## <span data-ttu-id="2450a-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="2450a-165">RELATED LINKS</span></span>
