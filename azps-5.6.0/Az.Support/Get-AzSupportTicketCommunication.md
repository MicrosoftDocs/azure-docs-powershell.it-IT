---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/powershell/module/az.support/get-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Get-AzSupportTicketCommunication.md
ms.openlocfilehash: 106ee61629c1252300d63ca686848ba7cc926cea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981917"
---
# <span data-ttu-id="08233-101">Get-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="08233-101">Get-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="08233-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="08233-102">SYNOPSIS</span></span>
<span data-ttu-id="08233-103">Ricevi comunicazioni con i ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="08233-103">Get support ticket communications.</span></span>

## <span data-ttu-id="08233-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="08233-104">SYNTAX</span></span>

### <span data-ttu-id="08233-105">GetByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="08233-105">GetByNameParameterSet (Default)</span></span>
```
Get-AzSupportTicketCommunication -SupportTicketName <String> [-Name <String>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

### <span data-ttu-id="08233-106">GetByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="08233-106">GetByParentObjectParameterSet</span></span>
```
Get-AzSupportTicketCommunication [-Name <String>] -SupportTicketObject <PSSupportTicket> [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [-IncludeTotalCount] [-Skip <UInt64>] [-First <UInt64>]
 [<CommonParameters>]
```

## <span data-ttu-id="08233-107">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="08233-107">DESCRIPTION</span></span>
<span data-ttu-id="08233-108">Riceve comunicazioni per un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="08233-108">Gets communications for a support ticket.</span></span> <span data-ttu-id="08233-109">Se non si specificano altri parametri, verranno recuperate tutte le comunicazioni per un ticket.</span><span class="sxs-lookup"><span data-stu-id="08233-109">It will retrieve all the communications for a ticket if you do not specify any other parameters.</span></span> <span data-ttu-id="08233-110">È anche possibile filtrare le comunicazioni in base a CreatedDate o CommunicationType usando il parametro Filter.</span><span class="sxs-lookup"><span data-stu-id="08233-110">You can also filter the communications by CreatedDate or CommunicationType using the Filter parameter.</span></span> <span data-ttu-id="08233-111">Ecco alcuni esempi di valori di filtro che è possibile specificare.</span><span class="sxs-lookup"><span data-stu-id="08233-111">Here are some examples of filter values that you can specify.</span></span>


| <span data-ttu-id="08233-112">Scenario</span><span class="sxs-lookup"><span data-stu-id="08233-112">Scenario</span></span>                                                        | <span data-ttu-id="08233-113">Filtro</span><span class="sxs-lookup"><span data-stu-id="08233-113">Filter</span></span>                                                     |
|-----------------------------------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="08233-114">Ottieni comunicazioni Web</span><span class="sxs-lookup"><span data-stu-id="08233-114">Get Web communications</span></span>                                          | <span data-ttu-id="08233-115">"CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="08233-115">"CommunicationType eq 'Web'"</span></span>                               |
| <span data-ttu-id="08233-116">Ottieni comunicazioni telefoniche</span><span class="sxs-lookup"><span data-stu-id="08233-116">Get Phone communications</span></span>                                        | <span data-ttu-id="08233-117">"CommunicationType eq 'Phone'"</span><span class="sxs-lookup"><span data-stu-id="08233-117">"CommunicationType eq 'Phone'"</span></span>                             |
| <span data-ttu-id="08233-118">Ricevere comunicazioni create il 20 dicembre 2019 o dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="08233-118">Get communications that were created on or after 20th Dec, 2019</span></span> | <span data-ttu-id="08233-119">"CreatedDate ge 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="08233-119">"CreatedDate ge 2019-12-20"</span></span>                                |
| <span data-ttu-id="08233-120">Ricevere comunicazioni create dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="08233-120">Get communications that were created after 20th Dec, 2019</span></span>       | <span data-ttu-id="08233-121">"CreatedDate gt 2019-12-20"</span><span class="sxs-lookup"><span data-stu-id="08233-121">"CreatedDate gt 2019-12-20"</span></span>                                |
| <span data-ttu-id="08233-122">Recupera le comunicazioni Web create dopo il 20 dicembre 2019</span><span class="sxs-lookup"><span data-stu-id="08233-122">Gets Web communications created after 20th Dec, 2019</span></span>            | <span data-ttu-id="08233-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span><span class="sxs-lookup"><span data-stu-id="08233-123">"CreatedDate gt 2019-12-20 and CommunicationType eq 'Web'"</span></span> |


<span data-ttu-id="08233-124">Questo cmdlet supporta la suddivisione in pagine tramite i parametri First e Skip.</span><span class="sxs-lookup"><span data-stu-id="08233-124">This cmdlet supports paging via First and Skip parameters.</span></span>

<span data-ttu-id="08233-125">È anche possibile recuperare una singola comunicazione ticket di supporto specificando il nome della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="08233-125">You can also retrieve a single support ticket communication by specifying the communication name.</span></span> 

## <span data-ttu-id="08233-126">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="08233-126">EXAMPLES</span></span>

### <span data-ttu-id="08233-127">Esempio 1: Recuperare tutte le comunicazioni per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-127">Example 1: Retrieve all communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

### <span data-ttu-id="08233-128">Esempio 2: Recuperare una singola comunicazione con il nome di un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-128">Example 2: Retrieve a single communication by it's name for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Name "testmessage1"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage1 user@contoso.com     test message   2/4/2020 9:38:14 PM
```

### <span data-ttu-id="08233-129">Esempio 3: Recuperare le prime 2 comunicazioni per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-129">Example 3: Retrieve first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="08233-130">Esempio 4: Recuperare le prossime 2 comunicazioni dopo aver ignorato le prime 2 comunicazioni per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-130">Example 4: Retrieve next 2 communications after skipping first 2 communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Skip 2 -First 2

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage4 user@contoso.com     test message4  2/4/2020 9:38:14 PM
testmessage5 user@contoso.com     test message5  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="08233-131">Esempio 5: Recuperare tutte le comunicazioni Web per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-131">Example 5: Retrieve all Web communications for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web'"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="08233-132">Esempio 6: Recuperare tutte le comunicazioni create il 20 dicembre 2019 o dopo il 20 dicembre 2019 per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-132">Example 6: Retrieve all communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="08233-133">Esempio 7: Recuperare tutte le comunicazioni Web create il 20 dicembre 2019 o dopo il 20 dicembre 2019 per un ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-133">Example 7: Retrieve all Web communications created on or after Dec 20th, 2019 for a support ticket</span></span>
```powershell
PS C:\> Get-AzSupportTicketCommunication -SupportTicketName "test1" -Filter "CommunicationType eq 'Web' and CreatedDate ge 2019-12-20"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
```

### <span data-ttu-id="08233-134">Esempio 8: Recuperare tutte le comunicazioni per un ticket di supporto piping dell'oggetto ticket di supporto</span><span class="sxs-lookup"><span data-stu-id="08233-134">Example 8: Retrieve all communications for a support ticket by piping support ticket object</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Get-AzSupportTicketCommunication

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage3 user@contoso.com     test message3  2/4/2020 9:38:14 PM
testmessage2 user@contoso.com     test message2  2/4/2020 9:36:36 PM
testmessage1 user@contoso.com     test message   2/4/2020 9:35:42 PM
```

## <span data-ttu-id="08233-135">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="08233-135">PARAMETERS</span></span>

### <span data-ttu-id="08233-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08233-136">-DefaultProfile</span></span>
<span data-ttu-id="08233-137">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="08233-137">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="08233-138">-Filter</span><span class="sxs-lookup"><span data-stu-id="08233-138">-Filter</span></span>
<span data-ttu-id="08233-139">Filtro da applicare ai risultati di questo cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08233-139">Filter to be applied to the results of this cmdlet.</span></span>

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

### <span data-ttu-id="08233-140">-Name</span><span class="sxs-lookup"><span data-stu-id="08233-140">-Name</span></span>
<span data-ttu-id="08233-141">Nome della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="08233-141">Communication name.</span></span>

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

### <span data-ttu-id="08233-142">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="08233-142">-SupportTicketName</span></span>
<span data-ttu-id="08233-143">Nome del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="08233-143">Support ticket name.</span></span>

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

### <span data-ttu-id="08233-144">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="08233-144">-SupportTicketObject</span></span>
<span data-ttu-id="08233-145">Oggetto ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="08233-145">Support ticket object.</span></span>

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

### <span data-ttu-id="08233-146">-IncludeTotalCount</span><span class="sxs-lookup"><span data-stu-id="08233-146">-IncludeTotalCount</span></span>
<span data-ttu-id="08233-147">Segnala il numero totale di oggetti nel set di dati (un numero intero) seguito dagli oggetti selezionati.</span><span class="sxs-lookup"><span data-stu-id="08233-147">Reports the total number of objects in the data set (an integer) followed by the selected objects.</span></span>
<span data-ttu-id="08233-148">Se il cmdlet non riesce a determinare il conteggio totale, viene visualizzato "Numero totale sconosciuto".</span><span class="sxs-lookup"><span data-stu-id="08233-148">If the cmdlet cannot determine the total count, it displays "Unknown total count."</span></span> <span data-ttu-id="08233-149">Il numero intero ha una proprietà Accuracy che indica l'affidabilità del valore totale del conteggio.</span><span class="sxs-lookup"><span data-stu-id="08233-149">The integer has an Accuracy property that indicates the reliability of the total count value.</span></span>
<span data-ttu-id="08233-150">Il valore di Precisione è compreso tra 0,0 e 1,0, dove 0,0 indica che il cmdlet non è stato in grado di contare gli oggetti, 1,0 indica che il conteggio è esatto e un valore compreso tra 0,0 e 1,0 indica una stima sempre più affidabile.</span><span class="sxs-lookup"><span data-stu-id="08233-150">The value of Accuracy ranges from 0.0 to 1.0 where 0.0 means that the cmdlet could not count the objects, 1.0 means that the count is exact, and a value between 0.0 and 1.0 indicates an increasingly reliable estimate.</span></span>

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

### <span data-ttu-id="08233-151">-Skip</span><span class="sxs-lookup"><span data-stu-id="08233-151">-Skip</span></span>
<span data-ttu-id="08233-152">Ignora il numero specificato di oggetti e ottiene gli oggetti rimanenti.</span><span class="sxs-lookup"><span data-stu-id="08233-152">Ignores the specified number of objects and then gets the remaining objects.</span></span>
<span data-ttu-id="08233-153">Immettere il numero di oggetti da ignorare.</span><span class="sxs-lookup"><span data-stu-id="08233-153">Enter the number of objects to skip.</span></span>

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

### <span data-ttu-id="08233-154">-First</span><span class="sxs-lookup"><span data-stu-id="08233-154">-First</span></span>
<span data-ttu-id="08233-155">Ottiene solo il numero specificato di oggetti.</span><span class="sxs-lookup"><span data-stu-id="08233-155">Gets only the specified number of objects.</span></span>
<span data-ttu-id="08233-156">Immettere il numero di oggetti da recuperare.</span><span class="sxs-lookup"><span data-stu-id="08233-156">Enter the number of objects to get.</span></span>

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

### <span data-ttu-id="08233-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08233-157">CommonParameters</span></span>
<span data-ttu-id="08233-158">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08233-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08233-159">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="08233-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08233-160">INPUT</span><span class="sxs-lookup"><span data-stu-id="08233-160">INPUTS</span></span>

### <span data-ttu-id="08233-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="08233-161">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="08233-162">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="08233-162">OUTPUTS</span></span>

### <span data-ttu-id="08233-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="08233-163">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="08233-164">NOTE</span><span class="sxs-lookup"><span data-stu-id="08233-164">NOTES</span></span>

## <span data-ttu-id="08233-165">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="08233-165">RELATED LINKS</span></span>
