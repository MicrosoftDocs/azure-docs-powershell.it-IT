---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermadgroupmember
schema: 2.0.0
ms.openlocfilehash: 3b1af5134147ad099547d95fdf5dbf79850e464a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/15/2020
ms.locfileid: "93865729"
---
# <span data-ttu-id="7ac79-101">Remove-AzureRmADGroupMember</span><span class="sxs-lookup"><span data-stu-id="7ac79-101">Remove-AzureRmADGroupMember</span></span>

## <span data-ttu-id="7ac79-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="7ac79-102">SYNOPSIS</span></span>
<span data-ttu-id="7ac79-103">Rimuove un utente da un gruppo di annunci.</span><span class="sxs-lookup"><span data-stu-id="7ac79-103">Removes a user from an AD group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ac79-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="7ac79-104">SYNTAX</span></span>

### <span data-ttu-id="7ac79-105">ExplicitParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="7ac79-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzureRmADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7ac79-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7ac79-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac79-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="7ac79-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac79-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7ac79-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzureRmADGroupMember -MemberObjectId <Guid[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac79-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ac79-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac79-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ac79-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ac79-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7ac79-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzureRmADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7ac79-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ac79-112">DESCRIPTION</span></span>
<span data-ttu-id="7ac79-113">Rimuove un utente da un gruppo di annunci.</span><span class="sxs-lookup"><span data-stu-id="7ac79-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="7ac79-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="7ac79-114">EXAMPLES</span></span>

### <span data-ttu-id="7ac79-115">Esempio 1-rimuovere un utente da un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="7ac79-115">Example 1 - Remove a user from a group by object id</span></span>

```
PS C:\> Remove-AzureRmADGroup -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="7ac79-116">Rimuove l'utente con l'ID oggetto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" dal gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="7ac79-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="7ac79-117">Esempio 2-rimuovere un utente da un gruppo per piping</span><span class="sxs-lookup"><span data-stu-id="7ac79-117">Example 2 - Remove a user from a group by piping</span></span>

```
PS C:\> Get-AzureRmADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzureRmADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="7ac79-118">Ottiene il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Remove-AzureRmADGroupMember per rimuovere l'utente in tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="7ac79-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzureRmADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="7ac79-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="7ac79-119">PARAMETERS</span></span>

### <span data-ttu-id="7ac79-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ac79-120">-DefaultProfile</span></span>
<span data-ttu-id="7ac79-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="7ac79-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7ac79-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="7ac79-122">-GroupDisplayName</span></span>
<span data-ttu-id="7ac79-123">Il nome visualizzato del gruppo da cui rimuovere il membro o i membri.</span><span class="sxs-lookup"><span data-stu-id="7ac79-123">The display name of the group to remove the member(s) from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberUPNWithGroupDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac79-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="7ac79-124">-GroupObject</span></span>
<span data-ttu-id="7ac79-125">Rappresentazione dell'oggetto del gruppo da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="7ac79-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7ac79-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="7ac79-126">-GroupObjectId</span></span>
<span data-ttu-id="7ac79-127">ID oggetto del gruppo da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="7ac79-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.Guid
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac79-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="7ac79-128">-MemberObjectId</span></span>
<span data-ttu-id="7ac79-129">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="7ac79-129">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac79-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="7ac79-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="7ac79-131">L'UPN del membro o dei membri da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="7ac79-131">The UPN of the member(s) to remove.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberUPNWithGroupDisplayNameParameterSet, MemberUPNWithGroupObjectParameterSet, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ac79-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7ac79-132">-PassThru</span></span>
<span data-ttu-id="7ac79-133">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="7ac79-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="7ac79-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="7ac79-134">-Confirm</span></span>
<span data-ttu-id="7ac79-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7ac79-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ac79-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ac79-136">-WhatIf</span></span>
<span data-ttu-id="7ac79-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ac79-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7ac79-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="7ac79-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ac79-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ac79-139">CommonParameters</span></span>
<span data-ttu-id="7ac79-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ac79-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ac79-141">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ac79-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ac79-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="7ac79-142">INPUTS</span></span>

### <span data-ttu-id="7ac79-143">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="7ac79-143">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="7ac79-144">Parametri: GroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ac79-144">Parameters: GroupObject (ByValue)</span></span>

## <span data-ttu-id="7ac79-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="7ac79-145">OUTPUTS</span></span>

### <span data-ttu-id="7ac79-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7ac79-146">System.Boolean</span></span>

## <span data-ttu-id="7ac79-147">Note</span><span class="sxs-lookup"><span data-stu-id="7ac79-147">NOTES</span></span>

## <span data-ttu-id="7ac79-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="7ac79-148">RELATED LINKS</span></span>
