---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/13/2020
ms.locfileid: "94191127"
---
# <span data-ttu-id="e6375-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="e6375-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="e6375-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e6375-102">SYNOPSIS</span></span>
<span data-ttu-id="e6375-103">Crea un oggetto del profilo del contatto di supporto.</span><span class="sxs-lookup"><span data-stu-id="e6375-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="e6375-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e6375-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e6375-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e6375-105">DESCRIPTION</span></span>
<span data-ttu-id="e6375-106">Questo è un cmdlet helper che puoi usare per creare un oggetto profilo di contatto di supporto durante la creazione o l'aggiornamento di un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e6375-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="e6375-107">È necessario specificare i parametri seguenti obbligatori per la creazione di un ticket di supporto:</span><span class="sxs-lookup"><span data-stu-id="e6375-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="e6375-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e6375-108">EXAMPLES</span></span>

### <span data-ttu-id="e6375-109">Esempio 1: creare un oggetto contatto</span><span class="sxs-lookup"><span data-stu-id="e6375-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="e6375-110">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e6375-110">PARAMETERS</span></span>

### <span data-ttu-id="e6375-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e6375-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="e6375-112">Gli indirizzi di posta elettronica elencati qui verranno copiati in corrispondenza del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e6375-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6375-113">-Paese</span><span class="sxs-lookup"><span data-stu-id="e6375-113">-Country</span></span>
<span data-ttu-id="e6375-114">Paese del cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-114">Customer country.</span></span>
<span data-ttu-id="e6375-115">Questo deve essere un codice di paese ISO alfa-3 valido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="e6375-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="e6375-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6375-116">-DefaultProfile</span></span>
<span data-ttu-id="e6375-117">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e6375-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e6375-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e6375-118">-FirstName</span></span>
<span data-ttu-id="e6375-119">Nome cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-119">Customer first name.</span></span>

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

### <span data-ttu-id="e6375-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="e6375-120">-LastName</span></span>
<span data-ttu-id="e6375-121">Cognome del cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-121">Customer last name.</span></span>

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

### <span data-ttu-id="e6375-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e6375-122">-PhoneNumber</span></span>
<span data-ttu-id="e6375-123">Numero di telefono del cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-123">Customer phone number.</span></span>
<span data-ttu-id="e6375-124">Questo è obbligatorio se il metodo di contatto preferito è Phone.</span><span class="sxs-lookup"><span data-stu-id="e6375-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="e6375-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="e6375-125">-PreferredContactMethod</span></span>
<span data-ttu-id="e6375-126">Metodo di contatto preferito.</span><span class="sxs-lookup"><span data-stu-id="e6375-126">Preferred contact method.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Support.Models.ContactMethod
Parameter Sets: (All)
Aliases:
Accepted values: Email, Phone

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e6375-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="e6375-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="e6375-128">Lingua di supporto preferita dal cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-128">Customer preferred support language.</span></span>
<span data-ttu-id="e6375-129">Questo deve essere un codice contabile della lingua valido per una delle lingue supportate elencate qui https://azure.microsoft.com/support/faq/ .</span><span class="sxs-lookup"><span data-stu-id="e6375-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="e6375-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="e6375-130">-PreferredTimeZone</span></span>
<span data-ttu-id="e6375-131">Fuso orario preferito dal cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-131">Customer preferred time zone.</span></span>
<span data-ttu-id="e6375-132">Deve essere un valore System.TimeZoneInfo.Id valido.</span><span class="sxs-lookup"><span data-stu-id="e6375-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="e6375-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e6375-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="e6375-134">Indirizzo di posta elettronica principale del cliente.</span><span class="sxs-lookup"><span data-stu-id="e6375-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="e6375-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="e6375-135">-Confirm</span></span>
<span data-ttu-id="e6375-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e6375-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e6375-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e6375-137">-WhatIf</span></span>
<span data-ttu-id="e6375-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6375-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e6375-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e6375-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e6375-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6375-140">CommonParameters</span></span>
<span data-ttu-id="e6375-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6375-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6375-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6375-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6375-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e6375-143">INPUTS</span></span>

### <span data-ttu-id="e6375-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e6375-144">None</span></span>

## <span data-ttu-id="e6375-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e6375-145">OUTPUTS</span></span>

### <span data-ttu-id="e6375-146">Microsoft. Azure. Commands. support. Models. PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="e6375-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="e6375-147">Note</span><span class="sxs-lookup"><span data-stu-id="e6375-147">NOTES</span></span>

## <span data-ttu-id="e6375-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e6375-148">RELATED LINKS</span></span>