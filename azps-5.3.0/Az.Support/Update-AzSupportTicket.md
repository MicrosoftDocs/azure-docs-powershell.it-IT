---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/update-azsupportticket
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/Update-AzSupportTicket.md
ms.openlocfilehash: 160d6b4d4a8505c99d5bfcb4c535ec7bbb3b6dd3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98474575"
---
# <span data-ttu-id="6747a-101">Update-AzSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6747a-101">Update-AzSupportTicket</span></span>

## <span data-ttu-id="6747a-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="6747a-102">SYNOPSIS</span></span>
<span data-ttu-id="6747a-103">Ticket di supporto degli aggiornamenti.</span><span class="sxs-lookup"><span data-stu-id="6747a-103">Updates support ticket.</span></span>

## <span data-ttu-id="6747a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="6747a-104">SYNTAX</span></span>

### <span data-ttu-id="6747a-105">UpdateByNameWithContactDetailParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="6747a-105">UpdateByNameWithContactDetailParameterSet (Default)</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6747a-106">UpdateByNameWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6747a-106">UpdateByNameWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -Name <String> [-Severity <Severity>] [-Status <Status>] -CustomerContactDetail <PSContactProfile>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6747a-107">UpdateByInputObjectWithContactDetailParameterSet</span><span class="sxs-lookup"><span data-stu-id="6747a-107">UpdateByInputObjectWithContactDetailParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>] [-CustomerFirstName <String>]
 [-CustomerLastName <String>] [-PreferredContactMethod <ContactMethod>] [-CustomerPrimaryEmailAddress <String>]
 [-AdditionalEmailAddress <String[]>] [-CustomerPhoneNumber <String>] [-CustomerPreferredTimeZone <String>]
 [-CustomerCountry <String>] [-CustomerPreferredSupportLanguage <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6747a-108">UpdateByInputObjectWithContactObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6747a-108">UpdateByInputObjectWithContactObjectParameterSet</span></span>
```
Update-AzSupportTicket -InputObject <PSSupportTicket> [-Severity <Severity>] [-Status <Status>]
 -CustomerContactDetail <PSContactProfile> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6747a-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="6747a-109">DESCRIPTION</span></span>
<span data-ttu-id="6747a-110">Questo cmdlet consente di aggiornare il livello di gravità, lo stato o i dettagli di contatto del cliente di un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="6747a-110">Use this cmdlet to update a support ticket's severity level, status or customer contact details.</span></span> <span data-ttu-id="6747a-111">Tieni presente che l'aggiornamento del livello di gravità o dello stato di un ticket di supporto non è consentito quando il ticket viene assegnato a un tecnico del supporto.</span><span class="sxs-lookup"><span data-stu-id="6747a-111">Note that updating a support ticket's severity level or status is not allowed when the ticket is assigned to a support engineer.</span></span> <span data-ttu-id="6747a-112">Se si vuole aggiornare il livello di gravità o lo stato dopo l'assegnazione del biglietto, contattare il tecnico del supporto inviando una comunicazione sul biglietto.</span><span class="sxs-lookup"><span data-stu-id="6747a-112">If you wish to update the severity level or status after ticket assignment, contact the support engineer by sending a communication on the ticket.</span></span>

## <span data-ttu-id="6747a-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="6747a-113">EXAMPLES</span></span>

### <span data-ttu-id="6747a-114">Esempio 1: aggiornare la gravità del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="6747a-114">Example 1: Update severity of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6747a-115">Esempio 2: aggiornare lo stato del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="6747a-115">Example 2: Update status of support ticket.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6747a-116">Esempio 3: aggiornare i dettagli dei contatti del ticket di supporto per specificare l'oggetto contatto.</span><span class="sxs-lookup"><span data-stu-id="6747a-116">Example 3: Update contact details of support ticket by specify contact object.</span></span>
```powershell
PS C:\> $contactDetail = new-object Microsoft.Azure.Commands.Support.Models.PSContactProfile
PS C:\> $contactDetail.FirstName = "first name updated"
PS C:\> $contactDetail.LastName = "last name updated"
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerContactDetail $contactDetail 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6747a-117">Esempio 4: aggiornare la gravità del ticket di supporto tramite l'oggetto ticket di supporto piping.</span><span class="sxs-lookup"><span data-stu-id="6747a-117">Example 4: Update severity of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Severity "moderate"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6747a-118">Esempio 5: aggiornare i dettagli dei contatti del ticket di supporto specificando i singoli parametri di contatto.</span><span class="sxs-lookup"><span data-stu-id="6747a-118">Example 5: Update contact details of support ticket by specifying individual contact parameters.</span></span>
```powershell
PS C:\> Update-AzSupportTicket -Name "test1" -CustomerFirstName "first name updated" -CustomerLastName "last name updated" -AdditionalEmailAddress @("user2@contoso.com") 

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Open   2/5/2020 1:33:53 AM
```

### <span data-ttu-id="6747a-119">Esempio 6: aggiornare lo stato del ticket di supporto tramite l'oggetto ticket di supporto piping.</span><span class="sxs-lookup"><span data-stu-id="6747a-119">Example 6: Update status of support ticket by piping support ticket object.</span></span>
```powershell
PS C:\> Get-AzSupportTicket -Name "test1" | Update-AzSupportTicket -Status "Closed"

Name  Title                        SupportTicketId Severity ServiceDisplayName            Status CreatedDate
----  -----                        --------------- -------- ------------------            ------ -----------
test1 test title1                  150010521000317 Moderate Virtual Machine running Linux Closed   2/5/2020 1:33:53 AM
```

## <span data-ttu-id="6747a-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="6747a-120">PARAMETERS</span></span>

### <span data-ttu-id="6747a-121">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6747a-121">-AdditionalEmailAddress</span></span>
<span data-ttu-id="6747a-122">Altri indirizzi di posta elettronica.</span><span class="sxs-lookup"><span data-stu-id="6747a-122">Additional email addresses.</span></span>
<span data-ttu-id="6747a-123">Gli indirizzi di posta elettronica elencati qui verranno copiati in corrispondenza del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="6747a-123">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-124">-CustomerContactDetail</span><span class="sxs-lookup"><span data-stu-id="6747a-124">-CustomerContactDetail</span></span>
<span data-ttu-id="6747a-125">Aggiornare i dettagli di contatto in SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="6747a-125">Update Contact details on SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSContactProfile
Parameter Sets: UpdateByNameWithContactObjectParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-126">-CustomerCountry</span><span class="sxs-lookup"><span data-stu-id="6747a-126">-CustomerCountry</span></span>
<span data-ttu-id="6747a-127">Paese del cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-127">Customer country.</span></span>
<span data-ttu-id="6747a-128">Questo deve essere un codice di paese ISO alfa-3 valido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="6747a-128">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-129">-CustomerFirstName</span><span class="sxs-lookup"><span data-stu-id="6747a-129">-CustomerFirstName</span></span>
<span data-ttu-id="6747a-130">Nome cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-130">Customer first name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-131">-CustomerLastName</span><span class="sxs-lookup"><span data-stu-id="6747a-131">-CustomerLastName</span></span>
<span data-ttu-id="6747a-132">Cognome del cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-132">Customer last name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-133">-CustomerPhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6747a-133">-CustomerPhoneNumber</span></span>
<span data-ttu-id="6747a-134">Numero di telefono del cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-134">Customer phone number.</span></span>
<span data-ttu-id="6747a-135">Questo è obbligatorio se il metodo di contatto preferito è Phone.</span><span class="sxs-lookup"><span data-stu-id="6747a-135">This is required if preferred contact method is phone.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-136">-CustomerPreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="6747a-136">-CustomerPreferredSupportLanguage</span></span>
<span data-ttu-id="6747a-137">Lingua di supporto preferita dal cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-137">Customer preferred support language.</span></span>
<span data-ttu-id="6747a-138">Questo deve essere un codice contabile della lingua valido per una delle lingue supportate elencate qui https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="6747a-138">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-139">-CustomerPreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="6747a-139">-CustomerPreferredTimeZone</span></span>
<span data-ttu-id="6747a-140">Fuso orario preferito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-140">Customer preferred time zone.</span></span>
<span data-ttu-id="6747a-141">Deve essere un valore System.TimeZoneInfo.Id valido.</span><span class="sxs-lookup"><span data-stu-id="6747a-141">This must be a valid System.TimeZoneInfo.Id value.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-142">-CustomerPrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="6747a-142">-CustomerPrimaryEmailAddress</span></span>
<span data-ttu-id="6747a-143">Indirizzo di posta elettronica principale del cliente.</span><span class="sxs-lookup"><span data-stu-id="6747a-143">Customer primary email address.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-144">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6747a-144">-DefaultProfile</span></span>
<span data-ttu-id="6747a-145">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="6747a-145">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6747a-146">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6747a-146">-InputObject</span></span>
<span data-ttu-id="6747a-147">Oggetto risorsa SupportTicket che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="6747a-147">SupportTicket resource object that this cmdlet updates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: UpdateByInputObjectWithContactDetailParameterSet, UpdateByInputObjectWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-148">-Nome</span><span class="sxs-lookup"><span data-stu-id="6747a-148">-Name</span></span>
<span data-ttu-id="6747a-149">Nome della risorsa SupportTicket che questo cmdlet aggiorna.</span><span class="sxs-lookup"><span data-stu-id="6747a-149">Name of SupportTicket resource that this cmdlet updates.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByNameWithContactObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-150">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="6747a-150">-PreferredContactMethod</span></span>
<span data-ttu-id="6747a-151">Metodo di contatto preferito.</span><span class="sxs-lookup"><span data-stu-id="6747a-151">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: UpdateByNameWithContactDetailParameterSet, UpdateByInputObjectWithContactDetailParameterSet
Aliases:
Accepted values: Email, Phone

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-152">-Gravità</span><span class="sxs-lookup"><span data-stu-id="6747a-152">-Severity</span></span>
<span data-ttu-id="6747a-153">Aggiornare la gravità di SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="6747a-153">Update Severity of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Severity
Parameter Sets: (All)
Aliases:
Accepted values: Minimal, Moderate, Critical, HighestCriticalImpact

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-154">-Stato</span><span class="sxs-lookup"><span data-stu-id="6747a-154">-Status</span></span>
<span data-ttu-id="6747a-155">Aggiornare lo stato di SupportTicket.</span><span class="sxs-lookup"><span data-stu-id="6747a-155">Update Status of SupportTicket.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.Status
Parameter Sets: (All)
Aliases:
Accepted values: Open, Closed

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-156">-Confermare</span><span class="sxs-lookup"><span data-stu-id="6747a-156">-Confirm</span></span>
<span data-ttu-id="6747a-157">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6747a-157">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6747a-158">-WhatIf</span></span>
<span data-ttu-id="6747a-159">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6747a-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6747a-160">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="6747a-160">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6747a-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6747a-161">CommonParameters</span></span>
<span data-ttu-id="6747a-162">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6747a-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6747a-163">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6747a-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6747a-164">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="6747a-164">INPUTS</span></span>

### <span data-ttu-id="6747a-165">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6747a-165">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="6747a-166">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="6747a-166">OUTPUTS</span></span>

### <span data-ttu-id="6747a-167">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="6747a-167">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="6747a-168">Note</span><span class="sxs-lookup"><span data-stu-id="6747a-168">NOTES</span></span>

## <span data-ttu-id="6747a-169">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="6747a-169">RELATED LINKS</span></span>
