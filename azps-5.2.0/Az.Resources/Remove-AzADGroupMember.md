---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7450588905deeb900efbffffa253f5c06ae63272
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363016"
---
# <span data-ttu-id="ec336-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="ec336-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="ec336-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ec336-102">SYNOPSIS</span></span>
<span data-ttu-id="ec336-103">Rimuove un utente da un gruppo di annunci.</span><span class="sxs-lookup"><span data-stu-id="ec336-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="ec336-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ec336-104">SYNTAX</span></span>

### <span data-ttu-id="ec336-105">ExplicitParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ec336-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ec336-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="ec336-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec336-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="ec336-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec336-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="ec336-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec336-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec336-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec336-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec336-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ec336-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ec336-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec336-112">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ec336-112">DESCRIPTION</span></span>
<span data-ttu-id="ec336-113">Rimuove un utente da un gruppo di annunci.</span><span class="sxs-lookup"><span data-stu-id="ec336-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="ec336-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ec336-114">EXAMPLES</span></span>

### <span data-ttu-id="ec336-115">Esempio 1: rimuovere un utente da un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="ec336-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="ec336-116">Rimuove l'utente con l'ID oggetto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" dal gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="ec336-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="ec336-117">Esempio 2: rimuovere un utente da un gruppo per piping</span><span class="sxs-lookup"><span data-stu-id="ec336-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="ec336-118">Ottiene il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Remove-AzADGroupMember per rimuovere l'utente in tale gruppo.</span><span class="sxs-lookup"><span data-stu-id="ec336-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="ec336-119">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ec336-119">PARAMETERS</span></span>

### <span data-ttu-id="ec336-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec336-120">-DefaultProfile</span></span>
<span data-ttu-id="ec336-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ec336-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec336-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="ec336-122">-GroupDisplayName</span></span>
<span data-ttu-id="ec336-123">Il nome visualizzato del gruppo da cui rimuovere il membro o i membri.</span><span class="sxs-lookup"><span data-stu-id="ec336-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="ec336-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="ec336-124">-GroupObject</span></span>
<span data-ttu-id="ec336-125">Rappresentazione dell'oggetto del gruppo da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="ec336-125">The object representation of the group to remove the member from.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADGroup
Parameter Sets: MemberObjectIdWithGroupObject, MemberUPNWithGroupObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ec336-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="ec336-126">-GroupObjectId</span></span>
<span data-ttu-id="ec336-127">ID oggetto del gruppo da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="ec336-127">The object id of the group to remove the member from.</span></span>

```yaml
Type: System.String
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberUPNWithGroupObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec336-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="ec336-128">-MemberObjectId</span></span>
<span data-ttu-id="ec336-129">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="ec336-129">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject, MemberObjectIdWithGroupObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec336-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="ec336-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="ec336-131">L'UPN del membro o dei membri da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="ec336-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="ec336-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ec336-132">-PassThru</span></span>
<span data-ttu-id="ec336-133">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="ec336-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="ec336-134">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ec336-134">-Confirm</span></span>
<span data-ttu-id="ec336-135">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec336-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec336-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec336-136">-WhatIf</span></span>
<span data-ttu-id="ec336-137">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec336-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec336-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ec336-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec336-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec336-139">CommonParameters</span></span>
<span data-ttu-id="ec336-140">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec336-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec336-141">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec336-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec336-142">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ec336-142">INPUTS</span></span>

### <span data-ttu-id="ec336-143">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="ec336-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="ec336-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ec336-144">OUTPUTS</span></span>

### <span data-ttu-id="ec336-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ec336-145">System.Boolean</span></span>

## <span data-ttu-id="ec336-146">Note</span><span class="sxs-lookup"><span data-stu-id="ec336-146">NOTES</span></span>

## <span data-ttu-id="ec336-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ec336-147">RELATED LINKS</span></span>
