---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzADGroupMember.md
ms.openlocfilehash: 7cc64ad6d0f17666ac1e97ae00473907c53a5552
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955662"
---
# <span data-ttu-id="c4567-101">Remove-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="c4567-101">Remove-AzADGroupMember</span></span>

## <span data-ttu-id="c4567-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4567-102">SYNOPSIS</span></span>
<span data-ttu-id="c4567-103">Rimuove un utente da un gruppo active directory.</span><span class="sxs-lookup"><span data-stu-id="c4567-103">Removes a user from an AD group.</span></span>

## <span data-ttu-id="c4567-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="c4567-104">SYNTAX</span></span>

### <span data-ttu-id="c4567-105">ExplicitParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="c4567-105">ExplicitParameterSet (Default)</span></span>
```
Remove-AzADGroupMember [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c4567-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c4567-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4567-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="c4567-107">MemberObjectIdWithGroupObject</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4567-108">MemberObjectIdWithGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="c4567-108">MemberObjectIdWithGroupObjectId</span></span>
```
Remove-AzADGroupMember -MemberObjectId <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4567-109">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4567-109">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4567-110">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4567-110">MemberUPNWithGroupObjectParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4567-111">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c4567-111">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Remove-AzADGroupMember -MemberUserPrincipalName <String[]> -GroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4567-112">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="c4567-112">DESCRIPTION</span></span>
<span data-ttu-id="c4567-113">Rimuove un utente da un gruppo active directory.</span><span class="sxs-lookup"><span data-stu-id="c4567-113">Removes a user from an AD group.</span></span>

## <span data-ttu-id="c4567-114">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="c4567-114">EXAMPLES</span></span>

### <span data-ttu-id="c4567-115">Esempio 1: Rimuovere un utente da un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="c4567-115">Example 1: Remove a user from a group by object id</span></span>

```powershell
PS C:\> Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -GroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="c4567-116">Rimuove l'utente con ID oggetto 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' dal gruppo con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="c4567-116">Removes the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' from the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="c4567-117">Esempio 2: Rimuovere un utente da un gruppo tramite piping</span><span class="sxs-lookup"><span data-stu-id="c4567-117">Example 2: Remove a user from a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Remove-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="c4567-118">Ottiene il gruppo con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e lo sua pipe al cmdlet di Remove-AzADGroupMember per rimuovere l'utente al gruppo.</span><span class="sxs-lookup"><span data-stu-id="c4567-118">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Remove-AzADGroupMember cmdlet to remove the user to that group.</span></span>

## <span data-ttu-id="c4567-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4567-119">PARAMETERS</span></span>

### <span data-ttu-id="c4567-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4567-120">-DefaultProfile</span></span>
<span data-ttu-id="c4567-121">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="c4567-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4567-122">-GroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="c4567-122">-GroupDisplayName</span></span>
<span data-ttu-id="c4567-123">Nome visualizzato del gruppo da cui rimuovere i membri.</span><span class="sxs-lookup"><span data-stu-id="c4567-123">The display name of the group to remove the member(s) from.</span></span>

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

### <span data-ttu-id="c4567-124">-GroupObject</span><span class="sxs-lookup"><span data-stu-id="c4567-124">-GroupObject</span></span>
<span data-ttu-id="c4567-125">Rappresentazione dell'oggetto del gruppo da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="c4567-125">The object representation of the group to remove the member from.</span></span>

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

### <span data-ttu-id="c4567-126">-GroupObjectId</span><span class="sxs-lookup"><span data-stu-id="c4567-126">-GroupObjectId</span></span>
<span data-ttu-id="c4567-127">ID oggetto del gruppo da cui rimuovere il membro.</span><span class="sxs-lookup"><span data-stu-id="c4567-127">The object id of the group to remove the member from.</span></span>

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

### <span data-ttu-id="c4567-128">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="c4567-128">-MemberObjectId</span></span>
<span data-ttu-id="c4567-129">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="c4567-129">The object id of the member.</span></span>

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

### <span data-ttu-id="c4567-130">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="c4567-130">-MemberUserPrincipalName</span></span>
<span data-ttu-id="c4567-131">UPN dei membri da rimuovere.</span><span class="sxs-lookup"><span data-stu-id="c4567-131">The UPN of the member(s) to remove.</span></span>

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

### <span data-ttu-id="c4567-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c4567-132">-PassThru</span></span>
<span data-ttu-id="c4567-133">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="c4567-133">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="c4567-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4567-134">-Confirm</span></span>
<span data-ttu-id="c4567-135">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c4567-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4567-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4567-136">-WhatIf</span></span>
<span data-ttu-id="c4567-137">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4567-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4567-138">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="c4567-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4567-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4567-139">CommonParameters</span></span>
<span data-ttu-id="c4567-140">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c4567-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4567-141">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4567-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4567-142">INPUT</span><span class="sxs-lookup"><span data-stu-id="c4567-142">INPUTS</span></span>

### <span data-ttu-id="c4567-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="c4567-143">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="c4567-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="c4567-144">OUTPUTS</span></span>

### <span data-ttu-id="c4567-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c4567-145">System.Boolean</span></span>

## <span data-ttu-id="c4567-146">NOTE</span><span class="sxs-lookup"><span data-stu-id="c4567-146">NOTES</span></span>

## <span data-ttu-id="c4567-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="c4567-147">RELATED LINKS</span></span>
