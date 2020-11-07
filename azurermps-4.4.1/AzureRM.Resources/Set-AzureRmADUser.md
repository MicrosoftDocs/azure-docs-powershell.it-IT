---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 388D4173-A937-42FA-81CB-C4A27F9D0B04
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmADUser.md
ms.openlocfilehash: 9d65ed2f6bbc2e26c4e91916cc42bf2954c08252
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93685657"
---
# <span data-ttu-id="7d563-101">Set-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7d563-101">Set-AzureRmADUser</span></span>

## <span data-ttu-id="7d563-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7d563-102">SYNOPSIS</span></span>
<span data-ttu-id="7d563-103">Aggiorna un utente di Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="7d563-103">Updates an existing active directory user.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d563-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7d563-104">SYNTAX</span></span>

```
Set-AzureRmADUser -UPNOrObjectId <String> [-DisplayName <String>] [-EnableAccount <Boolean>]
 [-Password <String>] [-ForceChangePasswordNextLogin] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7d563-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7d563-105">DESCRIPTION</span></span>
<span data-ttu-id="7d563-106">Aggiorna un utente di Active Directory esistente (account aziendale o dell'Istituto di istruzione noto anche come org-ID).</span><span class="sxs-lookup"><span data-stu-id="7d563-106">Updates an existing active directory user (work/school account also popularly known as org-id).</span></span>
<span data-ttu-id="7d563-107">Per altre informazioni: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span><span class="sxs-lookup"><span data-stu-id="7d563-107">For more information: https://msdn.microsoft.com/en-us/library/azure/ad/graph/api/users-operations#UpdateUser</span></span>

## <span data-ttu-id="7d563-108">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7d563-108">EXAMPLES</span></span>

### <span data-ttu-id="7d563-109">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="7d563-109">Example 1</span></span>
```
PS C:\> {{ Add example code here }}
```

<span data-ttu-id="7d563-110">{{Add Example description here}}</span><span class="sxs-lookup"><span data-stu-id="7d563-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="7d563-111">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7d563-111">PARAMETERS</span></span>

### <span data-ttu-id="7d563-112">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7d563-112">-DisplayName</span></span>
<span data-ttu-id="7d563-113">Nuovo nome da visualizzare in Rubrica per l'utente.</span><span class="sxs-lookup"><span data-stu-id="7d563-113">New name to display in the address book for the user.</span></span>
<span data-ttu-id="7d563-114">Esempio-'Alex Wu '.</span><span class="sxs-lookup"><span data-stu-id="7d563-114">Example-'Alex Wu'.</span></span>

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

### <span data-ttu-id="7d563-115">-EnableAccount</span><span class="sxs-lookup"><span data-stu-id="7d563-115">-EnableAccount</span></span>
<span data-ttu-id="7d563-116">True per l'abilitazione dell'account; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="7d563-116">True for enabling the account; otherwise, false.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d563-117">-ForceChangePasswordNextLogin</span><span class="sxs-lookup"><span data-stu-id="7d563-117">-ForceChangePasswordNextLogin</span></span>
<span data-ttu-id="7d563-118">Deve essere specificato solo quando si aggiorna la password.</span><span class="sxs-lookup"><span data-stu-id="7d563-118">It must be specified only when you are updating the password.</span></span>
<span data-ttu-id="7d563-119">In caso contrario, verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="7d563-119">Otherwise it will be ignored.</span></span>
<span data-ttu-id="7d563-120">Deve essere specificato se l'utente deve cambiare la password nel successivo accesso riuscito (vero).</span><span class="sxs-lookup"><span data-stu-id="7d563-120">It must be specified if the user must change the password on the next successful login (true).</span></span>
<span data-ttu-id="7d563-121">Il comportamento predefinito è (false) per non modificare la password nell'accesso successivo riuscito.</span><span class="sxs-lookup"><span data-stu-id="7d563-121">Default behavior is (false) to not change the password on the next successful login.</span></span>

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

### <span data-ttu-id="7d563-122">-Password</span><span class="sxs-lookup"><span data-stu-id="7d563-122">-Password</span></span>
<span data-ttu-id="7d563-123">Nuova password per l'utente.</span><span class="sxs-lookup"><span data-stu-id="7d563-123">New password for the user.</span></span>
<span data-ttu-id="7d563-124">Deve soddisfare i requisiti di complessità della password del tenant.</span><span class="sxs-lookup"><span data-stu-id="7d563-124">It must meet the tenant's password complexity requirements.</span></span>
<span data-ttu-id="7d563-125">È consigliabile impostare una password complessa.</span><span class="sxs-lookup"><span data-stu-id="7d563-125">It is recommended to set a strong password.</span></span>

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

### <span data-ttu-id="7d563-126">-UPNOrObjectId</span><span class="sxs-lookup"><span data-stu-id="7d563-126">-UPNOrObjectId</span></span>
<span data-ttu-id="7d563-127">Nome dell'entità utente (ad esempio ' someuser@contoso.com ') o ObjectID dell'utente per cui devono essere aggiornate le proprietà.</span><span class="sxs-lookup"><span data-stu-id="7d563-127">The user principal name (e.g. 'someuser@contoso.com') or the objectId of the user for which the properties need to be updated.</span></span>

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

### <span data-ttu-id="7d563-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7d563-128">-Confirm</span></span>
<span data-ttu-id="7d563-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7d563-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7d563-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7d563-130">-WhatIf</span></span>
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

### <span data-ttu-id="7d563-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d563-131">-DefaultProfile</span></span>
<span data-ttu-id="7d563-132">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7d563-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d563-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d563-133">CommonParameters</span></span>
<span data-ttu-id="7d563-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d563-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d563-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d563-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d563-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7d563-136">INPUTS</span></span>

## <span data-ttu-id="7d563-137">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7d563-137">OUTPUTS</span></span>

### <span data-ttu-id="7d563-138">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADUser</span><span class="sxs-lookup"><span data-stu-id="7d563-138">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADUser</span></span>

## <span data-ttu-id="7d563-139">Note</span><span class="sxs-lookup"><span data-stu-id="7d563-139">NOTES</span></span>

## <span data-ttu-id="7d563-140">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7d563-140">RELATED LINKS</span></span>

[<span data-ttu-id="7d563-141">Get-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7d563-141">Get-AzureRmADUser</span></span>](./Get-AzureRmADUser.md)

[<span data-ttu-id="7d563-142">New-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7d563-142">New-AzureRmADUser</span></span>](./New-AzureRmADUser.md)

[<span data-ttu-id="7d563-143">Remove-AzureRmADUser</span><span class="sxs-lookup"><span data-stu-id="7d563-143">Remove-AzureRmADUser</span></span>](./Remove-AzureRmADUser.md)

