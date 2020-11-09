---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: bf64c2fd139a4174496ba48cdb94aab89486a62a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302479"
---
# <span data-ttu-id="88c26-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="88c26-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="88c26-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="88c26-102">SYNOPSIS</span></span>
<span data-ttu-id="88c26-103">Aggiunge un utente a un gruppo di annunci esistente.</span><span class="sxs-lookup"><span data-stu-id="88c26-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="88c26-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="88c26-104">SYNTAX</span></span>

### <span data-ttu-id="88c26-105">MemberObjectIdWithGroupObjectId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="88c26-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c26-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="88c26-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c26-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="88c26-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c26-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="88c26-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c26-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="88c26-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88c26-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88c26-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88c26-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="88c26-111">DESCRIPTION</span></span>
<span data-ttu-id="88c26-112">Aggiunge un utente a un gruppo di annunci esistente.</span><span class="sxs-lookup"><span data-stu-id="88c26-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="88c26-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="88c26-113">EXAMPLES</span></span>

### <span data-ttu-id="88c26-114">Esempio 1: aggiungere un utente a un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="88c26-114">Example 1: Add a user to a group by object id</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="88c26-115">Aggiunge l'utente con l'ID oggetto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" al gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="88c26-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="88c26-116">Esempio 2: aggiungere un utente a un gruppo per piping</span><span class="sxs-lookup"><span data-stu-id="88c26-116">Example 2: Add a user to a group by piping</span></span>

```powershell
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="88c26-117">Ottiene il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Add-AzADGroupMember per aggiungere l'utente al gruppo.</span><span class="sxs-lookup"><span data-stu-id="88c26-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="88c26-118">Esempio 3: aggiungere un utente a un gruppo in base al nome dell'entità</span><span class="sxs-lookup"><span data-stu-id="88c26-118">Example 3: Add a user to a group by principal name</span></span>

```powershell
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="88c26-119">Aggiunge un utente a un gruppo ed elenca i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="88c26-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="88c26-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="88c26-120">PARAMETERS</span></span>

### <span data-ttu-id="88c26-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88c26-121">-DefaultProfile</span></span>
<span data-ttu-id="88c26-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="88c26-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88c26-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="88c26-123">-MemberObjectId</span></span>
<span data-ttu-id="88c26-124">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="88c26-124">The object id of the member.</span></span>

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

### <span data-ttu-id="88c26-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="88c26-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="88c26-126">L'UPN del membro o dei membri da aggiungere al gruppo.</span><span class="sxs-lookup"><span data-stu-id="88c26-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="88c26-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="88c26-127">-PassThru</span></span>
<span data-ttu-id="88c26-128">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="88c26-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="88c26-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="88c26-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="88c26-130">Il nome visualizzato del gruppo a cui aggiungere il membro o i membri.</span><span class="sxs-lookup"><span data-stu-id="88c26-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="88c26-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="88c26-131">-TargetGroupObject</span></span>
<span data-ttu-id="88c26-132">Rappresentazione dell'oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="88c26-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="88c26-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="88c26-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="88c26-134">ID oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="88c26-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="88c26-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="88c26-135">-Confirm</span></span>
<span data-ttu-id="88c26-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88c26-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88c26-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88c26-137">-WhatIf</span></span>
<span data-ttu-id="88c26-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88c26-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88c26-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="88c26-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88c26-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88c26-140">CommonParameters</span></span>
<span data-ttu-id="88c26-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88c26-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88c26-142">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88c26-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88c26-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="88c26-143">INPUTS</span></span>

### <span data-ttu-id="88c26-144">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="88c26-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="88c26-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="88c26-145">OUTPUTS</span></span>

### <span data-ttu-id="88c26-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="88c26-146">System.Boolean</span></span>

## <span data-ttu-id="88c26-147">Note</span><span class="sxs-lookup"><span data-stu-id="88c26-147">NOTES</span></span>

## <span data-ttu-id="88c26-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="88c26-148">RELATED LINKS</span></span>
