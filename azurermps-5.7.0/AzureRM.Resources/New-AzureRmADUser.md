---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 86D8965D-D999-48A4-A4EE-9E054E5486EE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADUser.md
ms.openlocfilehash: 80a35ac1a1087d9e74cb47c3297af3ded491e701
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93514127"
---
# <span data-ttu-id="68887-101">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="68887-101">New-AzureRmADUser</span></span>

## <span data-ttu-id="68887-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="68887-102">SYNOPSIS</span></span>
<span data-ttu-id="68887-103">Crea un nuovo utente di Active Directory.</span><span class="sxs-lookup"><span data-stu-id="68887-103">Creates a new active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68887-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="68887-104">SYNTAX</span></span>

```
New-AzureRmADUser -DisplayName <String> -UserPrincipalName <String> -Password <SecureString>
 [-ImmutableId <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="68887-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="68887-105">DESCRIPTION</span></span>
<span data-ttu-id="68887-106">Crea un nuovo utente di Active Directory (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="68887-106">Creates a new active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="68887-107">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span><span class="sxs-lookup"><span data-stu-id="68887-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#CreateUser</span></span>

## <span data-ttu-id="68887-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="68887-108">EXAMPLES</span></span>

### <span data-ttu-id="68887-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="68887-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="68887-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="68887-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="68887-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="68887-111">PARAMETERS</span></span>

### <span data-ttu-id="68887-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68887-112">-DefaultProfile</span></span>
<span data-ttu-id="68887-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="68887-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68887-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="68887-114">-DisplayName</span></span>
<span data-ttu-id="68887-115">Nome da visualizzare nella rubrica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="68887-115">The name to display in the address book for the user.</span></span>
<span data-ttu-id="68887-116">esempio "Alex Wu".</span><span class="sxs-lookup"><span data-stu-id="68887-116">example 'Alex Wu'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68887-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="68887-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="68887-118">Deve essere specificato se l'utente deve cambiare la password nel successivo accesso riuscito (vero).</span><span class="sxs-lookup"><span data-stu-id="68887-118">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="68887-119">Il comportamento predefinito è (false) per non modificare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="68887-119">Default behavior is (false) to not change the password on the next successful login.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68887-120">-ImmutableId</span><span class="sxs-lookup"><span data-stu-id="68887-120">-ImmutableId</span></span>
<span data-ttu-id="68887-121">Deve essere specificato solo se si usa un dominio federato per la proprietà nome dell'entità utente (UPN) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="68887-121">It needs to be specified only if you are using a federated domain for the user's user principal name (upn) property.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68887-122">-Password</span><span class="sxs-lookup"><span data-stu-id="68887-122">-Password</span></span>
<span data-ttu-id="68887-123">Password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="68887-123">Password for the user.</span></span>
<span data-ttu-id="68887-124">Deve soddisfare i requisiti di complessità della password del tenant.</span><span class="sxs-lookup"><span data-stu-id="68887-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="68887-125">È consigliabile impostare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="68887-125">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68887-126">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="68887-126">-UserPrincipalName</span></span>
<span data-ttu-id="68887-127">Nome dell'entità utente.</span><span class="sxs-lookup"><span data-stu-id="68887-127">The user principal name.</span></span>
<span data-ttu-id="68887-128">Esempio:' someuser@contoso.com '.</span><span class="sxs-lookup"><span data-stu-id="68887-128">Example-'someuser@contoso.com'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68887-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="68887-129">-Confirm</span></span>
<span data-ttu-id="68887-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="68887-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68887-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68887-131">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68887-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68887-132">CommonParameters</span></span>
<span data-ttu-id="68887-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68887-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68887-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68887-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68887-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="68887-135">INPUTS</span></span>

### <span data-ttu-id="68887-136">Nessuno</span><span class="sxs-lookup"><span data-stu-id="68887-136">None</span></span>
<span data-ttu-id="68887-137">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="68887-137">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68887-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="68887-138">OUTPUTS</span></span>

### <span data-ttu-id="68887-139">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="68887-139">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="68887-140">Note</span><span class="sxs-lookup"><span data-stu-id="68887-140">NOTES</span></span>

## <span data-ttu-id="68887-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="68887-141">RELATED LINKS</span></span>

[<span data-ttu-id="68887-142">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="68887-142">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="68887-143">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="68887-143">Set-AzureRmADUser</span></span>](./Set-AzureRmADUser.md)

[<span data-ttu-id="68887-144">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="68887-144">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)
