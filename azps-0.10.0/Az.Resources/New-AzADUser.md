---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADUser.md
ms.openlocfilehash: 213e488dde914a8e87b76d6c3765f5dbe99a527a
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399975"
---
# <span data-ttu-id="86d88-101">New-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86d88-101">New-AzADUser</span></span>

## <span data-ttu-id="86d88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86d88-102">SYNOPSIS</span></span>
<span data-ttu-id="86d88-103">Crea un nuovo utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="86d88-103">Creates a new active directory user.</span></span>

## <span data-ttu-id="86d88-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="86d88-104">SYNTAX</span></span>

```
New-AzADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86d88-105">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="86d88-105">DESCRIPTION</span></span>
<span data-ttu-id="86d88-106">Crea un nuovo utente di Active Directory (account aziendale o dell'istituto di istruzione noto anche come org-id).</span><span class="sxs-lookup"><span data-stu-id="86d88-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="86d88-107">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="86d88-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="86d88-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="86d88-108">EXAMPLES</span></span>

### <span data-ttu-id="86d88-109">Esempio 1 - Creare un nuovo utente di Active Directory</span><span class="sxs-lookup"><span data-stu-id="86d88-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="86d88-110">Crea un nuovo utente Active Directory con il nome "MyDisplayName" e il nome dell'entità utente myemail@domain.com " " in un tenant.</span><span class="sxs-lookup"><span data-stu-id="86d88-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="86d88-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86d88-111">PARAMETERS</span></span>

### <span data-ttu-id="86d88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86d88-112">-DefaultProfile</span></span>
<span data-ttu-id="86d88-113">Le credenziali, l'account, il tenant e la sottoscrizione usati per le comunicazioni con Azure</span><span class="sxs-lookup"><span data-stu-id="86d88-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86d88-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="86d88-114">-DisplayName</span></span>
<span data-ttu-id="86d88-115">Nome da visualizzare nella rubrica dell'utente.</span><span class="sxs-lookup"><span data-stu-id="86d88-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="86d88-116">esempio "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="86d88-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="86d88-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="86d88-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="86d88-118">Deve essere specificato se l'utente deve cambiare la password al successivo accesso riuscito (true).</span><span class="sxs-lookup"><span data-stu-id="86d88-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="86d88-119">Il comportamento predefinito è (false) per non cambiare la password al successivo accesso riuscito.</span><span class="sxs-lookup"><span data-stu-id="86d88-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="86d88-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="86d88-120">-ImmutableId</span></span>
<span data-ttu-id="86d88-121">Deve essere specificato solo se si usa un dominio federato per la proprietà del nome dell'entità utente (upn) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="86d88-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="86d88-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="86d88-122">-MailNickname</span></span>
<span data-ttu-id="86d88-123">Alias di posta elettronica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="86d88-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="86d88-124">-Password</span><span class="sxs-lookup"><span data-stu-id="86d88-124">-Password</span></span>
<span data-ttu-id="86d88-125">Password dell'utente.</span><span class="sxs-lookup"><span data-stu-id="86d88-125">Password for the user.</span></span>
<span data-ttu-id="86d88-126">Deve soddisfare i requisiti di complessità della password del tenant.</span><span class="sxs-lookup"><span data-stu-id="86d88-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="86d88-127">È consigliabile impostare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="86d88-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="86d88-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="86d88-128">-UserPrincipalName</span></span>
<span data-ttu-id="86d88-129">Il nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="86d88-129">The user principal name.</span></span>
<span data-ttu-id="86d88-130">Example-' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="86d88-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="86d88-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86d88-131">-Confirm</span></span>
<span data-ttu-id="86d88-132">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86d88-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86d88-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86d88-133">-WhatIf</span></span>
<span data-ttu-id="86d88-134">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86d88-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86d88-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="86d88-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86d88-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86d88-136">CommonParameters</span></span>
<span data-ttu-id="86d88-137">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86d88-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86d88-138">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86d88-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86d88-139">INPUT</span><span class="sxs-lookup"><span data-stu-id="86d88-139">INPUTS</span></span>

### <span data-ttu-id="86d88-140">System.String</span><span class="sxs-lookup"><span data-stu-id="86d88-140">System.String</span></span>

### <span data-ttu-id="86d88-141">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="86d88-141">System.Security.SecureString</span></span>

### <span data-ttu-id="86d88-142">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="86d88-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="86d88-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="86d88-143">OUTPUTS</span></span>

### <span data-ttu-id="86d88-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span><span class="sxs-lookup"><span data-stu-id="86d88-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="86d88-145">NOTE</span><span class="sxs-lookup"><span data-stu-id="86d88-145">NOTES</span></span>

## <span data-ttu-id="86d88-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="86d88-146">RELATED LINKS</span></span>

[<span data-ttu-id="86d88-147">Get-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86d88-147">Get-AzADUser</span></span>](./Get-AzADUser.md)


[<span data-ttu-id="86d88-148">Remove-AzADUser</span><span class="sxs-lookup"><span data-stu-id="86d88-148">Remove-AzADUser</span></span>](./Remove-AzADUser.md)
