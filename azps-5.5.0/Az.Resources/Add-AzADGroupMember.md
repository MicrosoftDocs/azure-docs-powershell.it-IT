---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192790"
---
# <span data-ttu-id="60e0d-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="60e0d-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="60e0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="60e0d-103">Aggiunge un utente a un gruppo Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="60e0d-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="60e0d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="60e0d-104">SYNTAX</span></span>

### <span data-ttu-id="60e0d-105">MemberObjectIdWithGroupObjectId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="60e0d-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0d-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="60e0d-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0d-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="60e0d-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0d-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="60e0d-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0d-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="60e0d-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="60e0d-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="60e0d-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="60e0d-111">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="60e0d-111">DESCRIPTION</span></span>
<span data-ttu-id="60e0d-112">Aggiunge un utente a un gruppo Active Directory esistente.</span><span class="sxs-lookup"><span data-stu-id="60e0d-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="60e0d-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="60e0d-113">EXAMPLES</span></span>

### <span data-ttu-id="60e0d-114">Esempio 1: Aggiungere un utente a un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="60e0d-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="60e0d-115">Aggiunge l'utente con ID oggetto 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' al gruppo con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span><span class="sxs-lookup"><span data-stu-id="60e0d-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="60e0d-116">Esempio 2: Aggiungere un utente a un gruppo tramite piping</span><span class="sxs-lookup"><span data-stu-id="60e0d-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="60e0d-117">Ottiene il gruppo con ID oggetto '85F89C90-780E-4AA6-9F4F-6F268D322EEE' e lo aggiunge al cmdlet di Add-AzADGroupMember per aggiungere l'utente al gruppo.</span><span class="sxs-lookup"><span data-stu-id="60e0d-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="60e0d-118">Esempio 3: Aggiungere un utente a un gruppo in base al nome dell'entità</span><span class="sxs-lookup"><span data-stu-id="60e0d-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="60e0d-119">Aggiunge un utente a un gruppo ed elenca i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="60e0d-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="60e0d-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60e0d-120">PARAMETERS</span></span>

### <span data-ttu-id="60e0d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60e0d-121">-DefaultProfile</span></span>
<span data-ttu-id="60e0d-122">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="60e0d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60e0d-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="60e0d-123">-MemberObjectId</span></span>
<span data-ttu-id="60e0d-124">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="60e0d-124">The object id of the member.</span></span>

```yaml
Type: System.String[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60e0d-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="60e0d-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="60e0d-126">UPN dei membri da aggiungere al gruppo.</span><span class="sxs-lookup"><span data-stu-id="60e0d-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="60e0d-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="60e0d-127">-PassThru</span></span>
<span data-ttu-id="60e0d-128">Se si specifica questo valore, viene restituito true se il comando ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="60e0d-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="60e0d-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="60e0d-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="60e0d-130">Nome visualizzato del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="60e0d-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="60e0d-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="60e0d-131">-TargetGroupObject</span></span>
<span data-ttu-id="60e0d-132">Rappresentazione dell'oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="60e0d-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="60e0d-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="60e0d-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="60e0d-134">ID oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="60e0d-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="60e0d-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60e0d-135">-Confirm</span></span>
<span data-ttu-id="60e0d-136">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="60e0d-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60e0d-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="60e0d-137">-WhatIf</span></span>
<span data-ttu-id="60e0d-138">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e0d-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60e0d-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="60e0d-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60e0d-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60e0d-140">CommonParameters</span></span>
<span data-ttu-id="60e0d-141">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60e0d-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60e0d-142">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="60e0d-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60e0d-143">INPUT</span><span class="sxs-lookup"><span data-stu-id="60e0d-143">INPUTS</span></span>

### <span data-ttu-id="60e0d-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span><span class="sxs-lookup"><span data-stu-id="60e0d-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="60e0d-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="60e0d-145">OUTPUTS</span></span>

### <span data-ttu-id="60e0d-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="60e0d-146">System.Boolean</span></span>

## <span data-ttu-id="60e0d-147">NOTE</span><span class="sxs-lookup"><span data-stu-id="60e0d-147">NOTES</span></span>

## <span data-ttu-id="60e0d-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="60e0d-148">RELATED LINKS</span></span>
