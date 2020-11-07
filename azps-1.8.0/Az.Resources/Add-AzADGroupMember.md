---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 876bc41e1faf1d830a247a56f9917f22023e5a6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93677423"
---
# <span data-ttu-id="d3f47-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="d3f47-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="d3f47-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d3f47-102">SYNOPSIS</span></span>
<span data-ttu-id="d3f47-103">Aggiunge un utente a un gruppo di annunci esistente.</span><span class="sxs-lookup"><span data-stu-id="d3f47-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="d3f47-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d3f47-104">SYNTAX</span></span>

### <span data-ttu-id="d3f47-105">MemberObjectIdWithGroupObjectId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d3f47-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f47-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="d3f47-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f47-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="d3f47-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f47-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f47-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f47-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f47-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3f47-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3f47-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3f47-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d3f47-111">DESCRIPTION</span></span>
<span data-ttu-id="d3f47-112">Aggiunge un utente a un gruppo di annunci esistente.</span><span class="sxs-lookup"><span data-stu-id="d3f47-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="d3f47-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d3f47-113">EXAMPLES</span></span>

### <span data-ttu-id="d3f47-114">Esempio 1-aggiungere un utente a un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="d3f47-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="d3f47-115">Aggiunge l'utente con l'ID oggetto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" al gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="d3f47-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="d3f47-116">Esempio 2: aggiungere un utente a un gruppo per piping</span><span class="sxs-lookup"><span data-stu-id="d3f47-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="d3f47-117">Ottiene il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Add-AzADGroupMember per aggiungere l'utente al gruppo.</span><span class="sxs-lookup"><span data-stu-id="d3f47-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

### <span data-ttu-id="d3f47-118">Esempio 3-aggiungere un utente a un gruppo in base al nome dell'entità</span><span class="sxs-lookup"><span data-stu-id="d3f47-118">Example 3 - Add a user to a group by principal name</span></span>

```
PS C:\> Add-AzADGroupMember -MemberUserPrincipalName "myemail@domain.com" -TargetGroupDisplayName "MyGroupDisplayName" 
PS C:\> Get-AzADGroupMember -GroupDisplayName "MyGroupDisplayName"
```

<span data-ttu-id="d3f47-119">Aggiunge un utente a un gruppo ed elenca i membri del gruppo.</span><span class="sxs-lookup"><span data-stu-id="d3f47-119">Adds an user to a group and list the members of the group.</span></span>

## <span data-ttu-id="d3f47-120">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d3f47-120">PARAMETERS</span></span>

### <span data-ttu-id="d3f47-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3f47-121">-DefaultProfile</span></span>
<span data-ttu-id="d3f47-122">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d3f47-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3f47-123">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="d3f47-123">-MemberObjectId</span></span>
<span data-ttu-id="d3f47-124">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="d3f47-124">The object id of the member.</span></span>

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

### <span data-ttu-id="d3f47-125">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="d3f47-125">-MemberUserPrincipalName</span></span>
<span data-ttu-id="d3f47-126">L'UPN del membro o dei membri da aggiungere al gruppo.</span><span class="sxs-lookup"><span data-stu-id="d3f47-126">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="d3f47-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3f47-127">-PassThru</span></span>
<span data-ttu-id="d3f47-128">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="d3f47-128">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="d3f47-129">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="d3f47-129">-TargetGroupDisplayName</span></span>
<span data-ttu-id="d3f47-130">Il nome visualizzato del gruppo a cui aggiungere il membro o i membri.</span><span class="sxs-lookup"><span data-stu-id="d3f47-130">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="d3f47-131">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="d3f47-131">-TargetGroupObject</span></span>
<span data-ttu-id="d3f47-132">Rappresentazione dell'oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="d3f47-132">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="d3f47-133">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="d3f47-133">-TargetGroupObjectId</span></span>
<span data-ttu-id="d3f47-134">ID oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="d3f47-134">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="d3f47-135">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d3f47-135">-Confirm</span></span>
<span data-ttu-id="d3f47-136">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d3f47-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3f47-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3f47-137">-WhatIf</span></span>
<span data-ttu-id="d3f47-138">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3f47-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3f47-139">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d3f47-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3f47-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3f47-140">CommonParameters</span></span>
<span data-ttu-id="d3f47-141">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3f47-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3f47-142">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3f47-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3f47-143">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d3f47-143">INPUTS</span></span>

### <span data-ttu-id="d3f47-144">Microsoft. Azure. Commands. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="d3f47-144">Microsoft.Azure.Commands.ActiveDirectory.PSADGroup</span></span>

## <span data-ttu-id="d3f47-145">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d3f47-145">OUTPUTS</span></span>

### <span data-ttu-id="d3f47-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d3f47-146">System.Boolean</span></span>

## <span data-ttu-id="d3f47-147">Note</span><span class="sxs-lookup"><span data-stu-id="d3f47-147">NOTES</span></span>

## <span data-ttu-id="d3f47-148">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d3f47-148">RELATED LINKS</span></span>
