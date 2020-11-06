---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 27b52e6b3cf58f530e15b2ddd2ff3873087dfc2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93511515"
---
# <span data-ttu-id="ec4a0-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ec4a0-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="ec4a0-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec4a0-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4a0-103">Crea un nuovo utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec4a0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec4a0-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-MailNickname <String>] [-ForceChangePasswordNextLogin]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4a0-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec4a0-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4a0-106">Crea un nuovo utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="ec4a0-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="ec4a0-107">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="ec4a0-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="ec4a0-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec4a0-108">EXAMPLES</span></span>

### <span data-ttu-id="ec4a0-109">Esempio 1-creare un nuovo utente di Active Directory</span><span class="sxs-lookup"><span data-stu-id="ec4a0-109">Example 1 - Create a new AD user</span></span>
```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADUser -DisplayName "MyDisplayName" -UserPrincipalName "myemail@domain.com" -Password $SecureStringPassword -MailNickname "MyMailNickName"
```

<span data-ttu-id="ec4a0-110">Crea un nuovo utente di Active Directory con il nome "DisplayName" e il nome dell'entità utente " myemail@domain.com " in un tenant.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-110">Creates a new AD user with the name "MyDisplayName" and user principal name "myemail@domain.com" in a tenant.</span></span>

## <span data-ttu-id="ec4a0-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec4a0-111">PARAMETERS</span></span>

### <span data-ttu-id="ec4a0-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4a0-112">-DefaultProfile</span></span>
<span data-ttu-id="ec4a0-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="ec4a0-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4a0-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ec4a0-114">-DisplayName</span></span>
<span data-ttu-id="ec4a0-115">Nome da visualizzare nella rubrica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="ec4a0-116">esempio "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="ec4a0-116">example 'Alex Wu'.</span></span>

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

### <span data-ttu-id="ec4a0-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="ec4a0-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="ec4a0-118">Deve essere specificato se l'utente deve cambiare la password nel successivo accesso riuscito (vero).</span><span class="sxs-lookup"><span data-stu-id="ec4a0-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="ec4a0-119">Il comportamento predefinito è (false) per non modificare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="ec4a0-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="ec4a0-120">-ImmutableId</span></span>
<span data-ttu-id="ec4a0-121">Deve essere specificato solo se si usa un dominio federato per la proprietà nome dell'entità utente (UPN) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

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

### <span data-ttu-id="ec4a0-122">-MailNickname</span><span class="sxs-lookup"><span data-stu-id="ec4a0-122">-MailNickname</span></span>
<span data-ttu-id="ec4a0-123">Alias di posta per l'utente.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-123">The mail alias for the user.</span></span>

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

### <span data-ttu-id="ec4a0-124">-Password</span><span class="sxs-lookup"><span data-stu-id="ec4a0-124">-Password</span></span>
<span data-ttu-id="ec4a0-125">Password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-125">Password for the user.</span></span>
<span data-ttu-id="ec4a0-126">Deve soddisfare i requisiti di complessità della password del tenant.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="ec4a0-127">È consigliabile impostare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-127">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="ec4a0-128">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ec4a0-128">-UserPrincipalName</span></span>
<span data-ttu-id="ec4a0-129">Nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-129">The user principal name.</span></span>
<span data-ttu-id="ec4a0-130">Esempio:' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-130">Example-'someuser@contoso.com'.</span></span>

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

### <span data-ttu-id="ec4a0-131">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec4a0-131">-Confirm</span></span>
<span data-ttu-id="ec4a0-132">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec4a0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4a0-133">-WhatIf</span></span>
<span data-ttu-id="ec4a0-134">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4a0-135">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec4a0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4a0-136">CommonParameters</span></span>
<span data-ttu-id="ec4a0-137">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4a0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4a0-138">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec4a0-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4a0-139">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec4a0-139">INPUTS</span></span>

### <span data-ttu-id="ec4a0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ec4a0-140">System.String</span></span>

### <span data-ttu-id="ec4a0-141">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="ec4a0-141">System.Security.SecureString</span></span>

### <span data-ttu-id="ec4a0-142">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ec4a0-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ec4a0-143">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec4a0-143">OUTPUTS</span></span>

### <span data-ttu-id="ec4a0-144">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="ec4a0-144">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="ec4a0-145">Note</span><span class="sxs-lookup"><span data-stu-id="ec4a0-145">NOTES</span></span>

## <span data-ttu-id="ec4a0-146">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec4a0-146">RELATED LINKS</span></span>

[<span data-ttu-id="ec4a0-147">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ec4a0-147">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="ec4a0-148">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ec4a0-148">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="ec4a0-149">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="ec4a0-149">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
