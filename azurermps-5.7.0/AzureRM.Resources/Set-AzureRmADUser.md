---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/set-azurermaduser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 325f134baf860b728aec3f144d9c9cf455c6b4ce
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93507992"
---
# <span data-ttu-id="adad7-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="adad7-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="adad7-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="adad7-102">SYNOPSIS</span></span>
<span data-ttu-id="adad7-103">Aggiorna un utente di Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="adad7-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="adad7-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="adad7-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <SecureString>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="adad7-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="adad7-105">DESCRIPTION</span></span>
<span data-ttu-id="adad7-106">Aggiorna un utente di Active Directory esistente (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="adad7-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="adad7-107">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="adad7-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="adad7-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="adad7-108">EXAMPLES</span></span>

### <span data-ttu-id="adad7-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="adad7-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="adad7-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="adad7-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="adad7-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="adad7-111">PARAMETERS</span></span>

### <span data-ttu-id="adad7-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adad7-112">-DefaultProfile</span></span>
<span data-ttu-id="adad7-113">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="adad7-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="adad7-114">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="adad7-114">-DisplayName</span></span>
<span data-ttu-id="adad7-115">Nuovo nome da visualizzare in Rubrica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="adad7-115">New name to display in the address book for the user.</span></span>
<span data-ttu-id="adad7-116">Esempio-'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="adad7-116">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="adad7-117">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="adad7-117">-EnableAccount</span></span>
<span data-ttu-id="adad7-118">True per l'abilitazione dell'account; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="adad7-118">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adad7-119">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="adad7-119">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="adad7-120">Deve essere specificato solo quando si aggiorna la password.</span><span class="sxs-lookup"><span data-stu-id="adad7-120">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="adad7-121">In caso contrario, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="adad7-121">Otherwise it will be ignored.</span></span>
<span data-ttu-id="adad7-122">Deve essere specificato se l'utente deve cambiare la password nel successivo accesso riuscito (vero).</span><span class="sxs-lookup"><span data-stu-id="adad7-122">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="adad7-123">Il comportamento predefinito è (false) per non modificare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="adad7-123">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="adad7-124">-Password</span><span class="sxs-lookup"><span data-stu-id="adad7-124">-Password</span></span>
<span data-ttu-id="adad7-125">Nuova password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="adad7-125">New password for the user.</span></span>
<span data-ttu-id="adad7-126">Deve soddisfare i requisiti di complessità della password del tenant.</span><span class="sxs-lookup"><span data-stu-id="adad7-126">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="adad7-127">È consigliabile impostare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="adad7-127">It is recommended to set a strong password.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="adad7-128">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="adad7-128">-UPNOrObjectId</span></span>
<span data-ttu-id="adad7-129">Nome dell'entità utente (ad esempio ' someuser@contoso.com ') o ObjectID dell'utente per cui devono essere aggiornate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="adad7-129">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="adad7-130">-Confermare</span><span class="sxs-lookup"><span data-stu-id="adad7-130">-Confirm</span></span>
<span data-ttu-id="adad7-131">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="adad7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="adad7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="adad7-132">-WhatIf</span></span>
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

### <span data-ttu-id="adad7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adad7-133">CommonParameters</span></span>
<span data-ttu-id="adad7-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="adad7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adad7-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adad7-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adad7-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="adad7-136">INPUTS</span></span>

### <span data-ttu-id="adad7-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="adad7-137">None</span></span>
<span data-ttu-id="adad7-138">Questo cmdlet non accetta alcun input.</span><span class="sxs-lookup"><span data-stu-id="adad7-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="adad7-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="adad7-139">OUTPUTS</span></span>

### <span data-ttu-id="adad7-140">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="adad7-140">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="adad7-141">Note</span><span class="sxs-lookup"><span data-stu-id="adad7-141">NOTES</span></span>

## <span data-ttu-id="adad7-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="adad7-142">RELATED LINKS</span></span>

[<span data-ttu-id="adad7-143">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="adad7-143">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="adad7-144">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="adad7-144">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="adad7-145">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="adad7-145">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

