---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Support.dll-Help.xml
Module Name: Az.Support
online version: https://docs.microsoft.com/en-us/powershell/module/az.support/new-azsupportcontactprofileobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Support/Support/help/New-AzSupportContactProfileObject.md
ms.openlocfilehash: 312fa24c8805664867d86bdaf38a01d287a3c499
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182831"
---
# <span data-ttu-id="e1cd5-101">New-AzSupportContactProfileObject</span><span class="sxs-lookup"><span data-stu-id="e1cd5-101">New-AzSupportContactProfileObject</span></span>

## <span data-ttu-id="e1cd5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e1cd5-102">SYNOPSIS</span></span>
<span data-ttu-id="e1cd5-103">Crea un oggetto profilo contatto di supporto.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-103">Creates a support contact profile object.</span></span>

## <span data-ttu-id="e1cd5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e1cd5-104">SYNTAX</span></span>

```
New-AzSupportContactProfileObject -FirstName <String> -LastName <String>
 -PreferredContactMethod <ContactMethod> -PrimaryEmailAddress <String> [-AdditionalEmailAddress <String[]>]
 [-PhoneNumber <String>] -PreferredTimeZone <String> -Country <String> -PreferredSupportLanguage <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1cd5-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="e1cd5-105">DESCRIPTION</span></span>
<span data-ttu-id="e1cd5-106">Si tratta di un cmdlet che consente di creare un oggetto profilo contatto di supporto durante la creazione o l'aggiornamento di un ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-106">This is a helper cmdlet that you can use to create a support contact profile object when creating or updating a support ticket.</span></span> <span data-ttu-id="e1cd5-107">È necessario specificare i parametri seguenti obbligatori per la creazione di un ticket di supporto:</span><span class="sxs-lookup"><span data-stu-id="e1cd5-107">You must specify the following parameters which are mandatory for creating a support ticket:</span></span> 

    • FirstName
    • LastName
    • PrimaryEmailAddress
    • PreferredContactMethod
    • Country
    • PreferredSupportLanguage
    • PreferredTimeZone

## <span data-ttu-id="e1cd5-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e1cd5-108">EXAMPLES</span></span>

### <span data-ttu-id="e1cd5-109">Esempio 1: Creare un oggetto contatto</span><span class="sxs-lookup"><span data-stu-id="e1cd5-109">Example 1: Create a contact object</span></span>
```powershell
PS C:\> New-AzSupportContactProfileObject -FirstName "First" -LastName "Last" -PreferredContactMethod "Email" -PrimaryEmailAddress "user@contoso.com" -PreferredTimeZone "Pacific Standard Time" -PreferredSupportLanguage "en-US" -Country "USA"             

FirstName LastName PreferredContactMethod PrimaryEmailAddress  PhoneNumber PreferredTimeZone     Country PreferredSupportLanguage
--------- -------- ---------------------- -------------------  ----------- -----------------     ------- ------------------------
First     Last     Email                  user@contoso.com                 Pacific Standard Time USA     en-US
```

## <span data-ttu-id="e1cd5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e1cd5-110">PARAMETERS</span></span>

### <span data-ttu-id="e1cd5-111">-AdditionalEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e1cd5-111">-AdditionalEmailAddress</span></span>
<span data-ttu-id="e1cd5-112">Gli indirizzi e-mail qui elencati verranno copiati in qualsiasi corrispondenza del ticket di supporto.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-112">Email addresses listed here will be copied on any correspondence about the support ticket.</span></span>

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

### <span data-ttu-id="e1cd5-113">-Paese</span><span class="sxs-lookup"><span data-stu-id="e1cd5-113">-Country</span></span>
<span data-ttu-id="e1cd5-114">Paese del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-114">Customer country.</span></span>
<span data-ttu-id="e1cd5-115">Deve essere un codice paese ISO Alfa-3 valido (ISO 3166).</span><span class="sxs-lookup"><span data-stu-id="e1cd5-115">This must be a valid ISO Alpha-3 country code (ISO 3166).</span></span>

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

### <span data-ttu-id="e1cd5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1cd5-116">-DefaultProfile</span></span>
<span data-ttu-id="e1cd5-117">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1cd5-118">-FirstName</span><span class="sxs-lookup"><span data-stu-id="e1cd5-118">-FirstName</span></span>
<span data-ttu-id="e1cd5-119">Nome del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-119">Customer first name.</span></span>

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

### <span data-ttu-id="e1cd5-120">-LastName</span><span class="sxs-lookup"><span data-stu-id="e1cd5-120">-LastName</span></span>
<span data-ttu-id="e1cd5-121">Cognome del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-121">Customer last name.</span></span>

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

### <span data-ttu-id="e1cd5-122">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="e1cd5-122">-PhoneNumber</span></span>
<span data-ttu-id="e1cd5-123">Numero di telefono del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-123">Customer phone number.</span></span>
<span data-ttu-id="e1cd5-124">È obbligatorio se il metodo di contatto preferito è il telefono.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-124">This is required if preferred contact method is phone.</span></span>

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

### <span data-ttu-id="e1cd5-125">-PreferredContactMethod</span><span class="sxs-lookup"><span data-stu-id="e1cd5-125">-PreferredContactMethod</span></span>
<span data-ttu-id="e1cd5-126">Metodo di contatto preferito.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-126">Preferred contact method.</span></span>

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

### <span data-ttu-id="e1cd5-127">-PreferredSupportLanguage</span><span class="sxs-lookup"><span data-stu-id="e1cd5-127">-PreferredSupportLanguage</span></span>
<span data-ttu-id="e1cd5-128">Lingua preferita del supporto tecnico.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-128">Customer preferred support language.</span></span>
<span data-ttu-id="e1cd5-129">Deve essere un codice di lingua valido per una delle lingue supportate elencate https://azure.microsoft.com/support/faq/ qui.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-129">This must be a valid language-contry code for one of the supported languages listed here https://azure.microsoft.com/support/faq/.</span></span>

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

### <span data-ttu-id="e1cd5-130">-PreferredTimeZone</span><span class="sxs-lookup"><span data-stu-id="e1cd5-130">-PreferredTimeZone</span></span>
<span data-ttu-id="e1cd5-131">Fuso orario preferito del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-131">Customer preferred time zone.</span></span>
<span data-ttu-id="e1cd5-132">Deve essere un valore System.TimeZoneInfo.Id valido.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-132">This must be a valid System.TimeZoneInfo.Id value.</span></span>

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

### <span data-ttu-id="e1cd5-133">-PrimaryEmailAddress</span><span class="sxs-lookup"><span data-stu-id="e1cd5-133">-PrimaryEmailAddress</span></span>
<span data-ttu-id="e1cd5-134">Indirizzo e-mail principale del cliente.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-134">Customer primary email address.</span></span>

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

### <span data-ttu-id="e1cd5-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e1cd5-135">-Confirm</span></span>
<span data-ttu-id="e1cd5-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1cd5-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1cd5-137">-WhatIf</span></span>
<span data-ttu-id="e1cd5-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1cd5-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1cd5-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1cd5-140">CommonParameters</span></span>
<span data-ttu-id="e1cd5-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1cd5-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e1cd5-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1cd5-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="e1cd5-143">INPUTS</span></span>

### <span data-ttu-id="e1cd5-144">Nessuno</span><span class="sxs-lookup"><span data-stu-id="e1cd5-144">None</span></span>

## <span data-ttu-id="e1cd5-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e1cd5-145">OUTPUTS</span></span>

### <span data-ttu-id="e1cd5-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span><span class="sxs-lookup"><span data-stu-id="e1cd5-146">Microsoft.Azure.Commands.Support.Models.PSContactProfile</span></span>

## <span data-ttu-id="e1cd5-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="e1cd5-147">NOTES</span></span>

## <span data-ttu-id="e1cd5-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e1cd5-148">RELATED LINKS</span></span>
