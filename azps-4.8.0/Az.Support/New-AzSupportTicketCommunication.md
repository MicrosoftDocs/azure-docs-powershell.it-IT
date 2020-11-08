---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94189993"
---
# <span data-ttu-id="be029-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="be029-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="be029-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="be029-102">SYNOPSIS</span></span>
<span data-ttu-id="be029-103">Crea una nuova comunicazione ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="be029-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="be029-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="be029-104">SYNTAX</span></span>

### <span data-ttu-id="be029-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="be029-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="be029-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="be029-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="be029-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="be029-107">DESCRIPTION</span></span>
<span data-ttu-id="be029-108">Aggiunge una nuova comunicazione del cliente a un ticket di supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="be029-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="be029-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="be029-109">EXAMPLES</span></span>

### <span data-ttu-id="be029-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="be029-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="be029-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="be029-111">PARAMETERS</span></span>

### <span data-ttu-id="be029-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="be029-112">-AsJob</span></span>
<span data-ttu-id="be029-113">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="be029-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="be029-114">-Body</span><span class="sxs-lookup"><span data-stu-id="be029-114">-Body</span></span>
<span data-ttu-id="be029-115">Corpo della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="be029-115">Body of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be029-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be029-116">-DefaultProfile</span></span>
<span data-ttu-id="be029-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="be029-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="be029-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="be029-118">-Name</span></span>
<span data-ttu-id="be029-119">Nome della risorsa di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="be029-119">Name of the communication resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be029-120">-Mittente</span><span class="sxs-lookup"><span data-stu-id="be029-120">-Sender</span></span>
<span data-ttu-id="be029-121">Indirizzo di posta elettronica del mittente.</span><span class="sxs-lookup"><span data-stu-id="be029-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="be029-122">-Oggetto</span><span class="sxs-lookup"><span data-stu-id="be029-122">-Subject</span></span>
<span data-ttu-id="be029-123">Oggetto della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="be029-123">Subject of the communication.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be029-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="be029-124">-SupportTicketName</span></span>
<span data-ttu-id="be029-125">Nome del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="be029-125">Support ticket name.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="be029-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="be029-126">-SupportTicketObject</span></span>
<span data-ttu-id="be029-127">Oggetto ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="be029-127">Support ticket object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.PSSupportTicket
Parameter Sets: CreateByParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="be029-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="be029-128">-Confirm</span></span>
<span data-ttu-id="be029-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="be029-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="be029-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="be029-130">-WhatIf</span></span>
<span data-ttu-id="be029-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be029-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="be029-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="be029-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="be029-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be029-133">CommonParameters</span></span>
<span data-ttu-id="be029-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be029-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be029-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="be029-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be029-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="be029-136">INPUTS</span></span>

### <span data-ttu-id="be029-137">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="be029-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="be029-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="be029-138">OUTPUTS</span></span>

### <span data-ttu-id="be029-139">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="be029-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="be029-140">Note</span><span class="sxs-lookup"><span data-stu-id="be029-140">NOTES</span></span>

## <span data-ttu-id="be029-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="be029-141">RELATED LINKS</span></span>
