---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportticketcommunication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportTicketCommunication.md
ms.openlocfilehash: 3a0191e1df223427ec7d60dfd92f7607e2c171b0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98384187"
---
# <span data-ttu-id="e6692-101">New-AzSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="e6692-101">New-AzSupportTicketCommunication</span></span>

## <span data-ttu-id="e6692-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6692-102">SYNOPSIS</span></span>
<span data-ttu-id="e6692-103">Crea una nuova comunicazione ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e6692-103">Creates a new support ticket communication.</span></span>

## <span data-ttu-id="e6692-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6692-104">SYNTAX</span></span>

### <span data-ttu-id="e6692-105">CreateByNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e6692-105">CreateByNameParameterSet (Default)</span></span>
```
New-AzSupportTicketCommunication -SupportTicketName <String> -Name <String> -Subject <String> -Body <String>
 [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e6692-106">CreateByParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e6692-106">CreateByParentObjectParameterSet</span></span>
```
New-AzSupportTicketCommunication -SupportTicketObject <PSSupportTicket> -Name <String> -Subject <String>
 -Body <String> [-Sender <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e6692-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6692-107">DESCRIPTION</span></span>
<span data-ttu-id="e6692-108">Aggiunge una nuova comunicazione del cliente a un ticket di supporto di Azure.</span><span class="sxs-lookup"><span data-stu-id="e6692-108">Adds a new customer communication to an Azure support ticket.</span></span>

## <span data-ttu-id="e6692-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6692-109">EXAMPLES</span></span>

### <span data-ttu-id="e6692-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="e6692-110">Example 1</span></span>
```powershell
PS C:\> New-AzSupportTicketCommunication -Name "testmessage" -SupportTicketName "testticket" -Subject "test subject" -Body "test body" -Sender "user@contoso.com"

Name         Sender               Subject        CreatedDate
----         ------               -------        -----------
testmessage  user@contoso.com     test subject   2/4/2020 9:38:14 PM
```

## <span data-ttu-id="e6692-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6692-111">PARAMETERS</span></span>

### <span data-ttu-id="e6692-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e6692-112">-AsJob</span></span>
<span data-ttu-id="e6692-113">Esegui cmdlet in background.</span><span class="sxs-lookup"><span data-stu-id="e6692-113">Run cmdlet in the background.</span></span>

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

### <span data-ttu-id="e6692-114">-Body</span><span class="sxs-lookup"><span data-stu-id="e6692-114">-Body</span></span>
<span data-ttu-id="e6692-115">Corpo della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="e6692-115">Body of the communication.</span></span>

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

### <span data-ttu-id="e6692-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6692-116">-DefaultProfile</span></span>
<span data-ttu-id="e6692-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6692-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6692-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="e6692-118">-Name</span></span>
<span data-ttu-id="e6692-119">Nome della risorsa di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="e6692-119">Name of the communication resource.</span></span>

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

### <span data-ttu-id="e6692-120">-Mittente</span><span class="sxs-lookup"><span data-stu-id="e6692-120">-Sender</span></span>
<span data-ttu-id="e6692-121">Indirizzo di posta elettronica del mittente.</span><span class="sxs-lookup"><span data-stu-id="e6692-121">Email address of the sender.</span></span>

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

### <span data-ttu-id="e6692-122">-Oggetto</span><span class="sxs-lookup"><span data-stu-id="e6692-122">-Subject</span></span>
<span data-ttu-id="e6692-123">Oggetto della comunicazione.</span><span class="sxs-lookup"><span data-stu-id="e6692-123">Subject of the communication.</span></span>

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

### <span data-ttu-id="e6692-124">-SupportTicketName</span><span class="sxs-lookup"><span data-stu-id="e6692-124">-SupportTicketName</span></span>
<span data-ttu-id="e6692-125">Nome del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e6692-125">Support ticket name.</span></span>

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

### <span data-ttu-id="e6692-126">-SupportTicketObject</span><span class="sxs-lookup"><span data-stu-id="e6692-126">-SupportTicketObject</span></span>
<span data-ttu-id="e6692-127">Oggetto ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e6692-127">Support ticket object.</span></span>

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

### <span data-ttu-id="e6692-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6692-128">-Confirm</span></span>
<span data-ttu-id="e6692-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6692-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6692-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6692-130">-WhatIf</span></span>
<span data-ttu-id="e6692-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6692-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6692-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6692-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6692-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6692-133">CommonParameters</span></span>
<span data-ttu-id="e6692-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6692-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6692-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6692-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6692-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6692-136">INPUTS</span></span>

### <span data-ttu-id="e6692-137">Microsoft. Azure. Commands. support. Models. PSSupportTicket</span><span class="sxs-lookup"><span data-stu-id="e6692-137">Microsoft.Azure.Commands.Support.Models.PSSupportTicket</span></span>

## <span data-ttu-id="e6692-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6692-138">OUTPUTS</span></span>

### <span data-ttu-id="e6692-139">Microsoft. Azure. Commands. support. Models. PSSupportTicketCommunication</span><span class="sxs-lookup"><span data-stu-id="e6692-139">Microsoft.Azure.Commands.Support.Models.PSSupportTicketCommunication</span></span>

## <span data-ttu-id="e6692-140">Note</span><span class="sxs-lookup"><span data-stu-id="e6692-140">NOTES</span></span>

## <span data-ttu-id="e6692-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6692-141">RELATED LINKS</span></span>
