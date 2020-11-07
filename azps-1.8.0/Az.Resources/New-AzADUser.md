---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: ac2dfb864733d7bcb2b46e17d557fca57c7bb4b4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677353"
---
# <span data-ttu-id="245fa-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="245fa-101">New-AzADUser</span></span>

## <span data-ttu-id="245fa-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="245fa-102">SYNOPSIS</span></span>
<span data-ttu-id="245fa-103">Crea un nuovo utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="245fa-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="245fa-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="245fa-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString> [-ImmutableId <String>]
 -MailNickname <String> [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="245fa-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="245fa-105">DESCRIPTION</span></span>
<span data-ttu-id="245fa-106">Crea un nuovo utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="245fa-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="245fa-107">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="245fa-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="245fa-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="245fa-108">EXAMPLES</span></span>

### <span data-ttu-id="245fa-109">Esempio 1-creare un nuovo utente di Active Directory</span><span class="sxs-lookup"><span data-stu-id="245fa-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="245fa-110">Crea un nuovo utente di Active Directory con il nome "DisplayName" e il nome dell'entità utente " myemail@domain.com " in un tenant.</span><span class="sxs-lookup"><span data-stu-id="245fa-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="245fa-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="245fa-111">PARAMETERS</span></span>

### <span data-ttu-id="245fa-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="245fa-112">-DefaultProfile</span></span>
<span data-ttu-id="245fa-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="245fa-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="245fa-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="245fa-114">-DisplayName</span></span>
<span data-ttu-id="245fa-115">Nome da visualizzare nella rubrica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="245fa-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="245fa-116">esempio "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="245fa-116">example 'Alex Wu'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="245fa-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="245fa-118">Deve essere specificato se l'utente deve cambiare la password nel successivo accesso riuscito (vero).</span><span class="sxs-lookup"><span data-stu-id="245fa-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="245fa-119">Il comportamento predefinito è (false) per non modificare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="245fa-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="245fa-120">-ImmutableId</span></span>
<span data-ttu-id="245fa-121">Deve essere specificato solo se si usa un dominio federato per la proprietà nome dell'entità utente (UPN) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="245fa-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="245fa-122">-MailNickname</span></span>
<span data-ttu-id="245fa-123">Alias di posta per l'utente.</span><span class="sxs-lookup"><span data-stu-id="245fa-123">The mail alias for the user.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-124">-Password</span><span class="sxs-lookup"><span data-stu-id="245fa-124">-Password</span></span>
<span data-ttu-id="245fa-125">Password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="245fa-125">Password for the user.</span></span>
<span data-ttu-id="245fa-126">Deve soddisfare i requisiti di complessità della password del tenant.</span><span class="sxs-lookup"><span data-stu-id="245fa-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="245fa-127">È consigliabile impostare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="245fa-127">It is recommended to set a strong password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="245fa-128">-UserPrincipalName</span></span>
<span data-ttu-id="245fa-129">Nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="245fa-129">The user principal name.</span></span>
<span data-ttu-id="245fa-130">Esempio:' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="245fa-130">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="245fa-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="245fa-131">-Confirm</span></span>
<span data-ttu-id="245fa-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="245fa-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="245fa-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="245fa-133">-WhatIf</span></span>
<span data-ttu-id="245fa-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="245fa-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="245fa-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="245fa-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="245fa-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="245fa-136">CommonParameters</span></span>
<span data-ttu-id="245fa-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="245fa-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="245fa-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="245fa-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="245fa-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="245fa-139">INPUTS</span></span>

### <span data-ttu-id="245fa-140">System. String</span><span class="sxs-lookup"><span data-stu-id="245fa-140">System.String</span></span>

### <span data-ttu-id="245fa-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="245fa-141">System.Security.SecureString</span></span>

### <span data-ttu-id="245fa-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="245fa-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="245fa-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="245fa-143">OUTPUTS</span></span>

### <span data-ttu-id="245fa-144">Microsoft. Azure. Commands. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="245fa-144">Microsoft.Azure.Commands.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="245fa-145">Note</span><span class="sxs-lookup"><span data-stu-id="245fa-145">NOTES</span></span>

## <span data-ttu-id="245fa-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="245fa-146">RELATED LINKS</span></span>

[<span data-ttu-id="245fa-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="245fa-147">Get-AzADUser</span></span>](./Get-AzADUser.md)

[<span data-ttu-id="245fa-148">Set-AzADUser</span><span class="sxs-lookup"><span data-stu-id="245fa-148">Set-AzADUser</span></span>](./Set-AzADUser.md)

[<span data-ttu-id="245fa-149">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="245fa-149">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
