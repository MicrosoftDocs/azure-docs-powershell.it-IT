---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/add-Azadgroupmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Add-AzADGroupMember.md
ms.openlocfilehash: 069705ffc119fae964e931164f97bfbae72eca35
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/16/2020
ms.locfileid: "93862650"
---
# <span data-ttu-id="a86e1-101">Add-AzADGroupMember</span><span class="sxs-lookup"><span data-stu-id="a86e1-101">Add-AzADGroupMember</span></span>

## <span data-ttu-id="a86e1-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a86e1-102">SYNOPSIS</span></span>
<span data-ttu-id="a86e1-103">Aggiunge un utente a un gruppo di annunci esistente.</span><span class="sxs-lookup"><span data-stu-id="a86e1-103">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="a86e1-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a86e1-104">SYNTAX</span></span>

### <span data-ttu-id="a86e1-105">MemberObjectIdWithGroupObjectId (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a86e1-105">MemberObjectIdWithGroupObjectId (Default)</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86e1-106">MemberObjectIdWithGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="a86e1-106">MemberObjectIdWithGroupDisplayName</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86e1-107">MemberObjectIdWithGroupObject</span><span class="sxs-lookup"><span data-stu-id="a86e1-107">MemberObjectIdWithGroupObject</span></span>
```
Add-AzADGroupMember -MemberObjectId <Guid[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86e1-108">MemberUPNWithGroupDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a86e1-108">MemberUPNWithGroupDisplayNameParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupDisplayName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86e1-109">MemberUPNWithGroupObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a86e1-109">MemberUPNWithGroupObjectParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObject <PSADGroup> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a86e1-110">MemberUPNWithGroupObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a86e1-110">MemberUPNWithGroupObjectIdParameterSet</span></span>
```
Add-AzADGroupMember -MemberUserPrincipalName <String[]> -TargetGroupObjectId <Guid> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a86e1-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a86e1-111">DESCRIPTION</span></span>
<span data-ttu-id="a86e1-112">Aggiunge un utente a un gruppo di annunci esistente.</span><span class="sxs-lookup"><span data-stu-id="a86e1-112">Adds a user to an existing AD group.</span></span>

## <span data-ttu-id="a86e1-113">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a86e1-113">EXAMPLES</span></span>

### <span data-ttu-id="a86e1-114">Esempio 1-aggiungere un utente a un gruppo per ID oggetto</span><span class="sxs-lookup"><span data-stu-id="a86e1-114">Example 1 - Add a user to a group by object id</span></span>

```
PS C:\> Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405 -TargetGroupObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE
```

<span data-ttu-id="a86e1-115">Aggiunge l'utente con l'ID oggetto "D9076BBC-D62C-4105-9C78-A7F5BC4A3405" al gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE".</span><span class="sxs-lookup"><span data-stu-id="a86e1-115">Adds the user with object id 'D9076BBC-D62C-4105-9C78-A7F5BC4A3405' to the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE'.</span></span>

### <span data-ttu-id="a86e1-116">Esempio 2: aggiungere un utente a un gruppo per piping</span><span class="sxs-lookup"><span data-stu-id="a86e1-116">Example 2 - Add a user to a group by piping</span></span>

```
PS C:\> Get-AzADGroup -ObjectId 85F89C90-780E-4AA6-9F4F-6F268D322EEE | Add-AzADGroupMember -MemberObjectId D9076BBC-D62C-4105-9C78-A7F5BC4A3405
```

<span data-ttu-id="a86e1-117">Ottiene il gruppo con l'ID oggetto "85F89C90-780E-4AA6-9F4F-6F268D322EEE" e lo convoglia al cmdlet Add-AzADGroupMember per aggiungere l'utente al gruppo.</span><span class="sxs-lookup"><span data-stu-id="a86e1-117">Gets the group with object id '85F89C90-780E-4AA6-9F4F-6F268D322EEE' and pipes it to the Add-AzADGroupMember cmdlet to add the user to that group.</span></span>

## <span data-ttu-id="a86e1-118">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a86e1-118">PARAMETERS</span></span>

### <span data-ttu-id="a86e1-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a86e1-119">-DefaultProfile</span></span>
<span data-ttu-id="a86e1-120">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a86e1-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86e1-121">-MemberObjectId</span><span class="sxs-lookup"><span data-stu-id="a86e1-121">-MemberObjectId</span></span>
<span data-ttu-id="a86e1-122">ID oggetto del membro.</span><span class="sxs-lookup"><span data-stu-id="a86e1-122">The object id of the member.</span></span>

```yaml
Type: System.Guid[]
Parameter Sets: MemberObjectIdWithGroupObjectId, MemberObjectIdWithGroupDisplayName, MemberObjectIdWithGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a86e1-123">-MemberUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a86e1-123">-MemberUserPrincipalName</span></span>
<span data-ttu-id="a86e1-124">L'UPN del membro o dei membri da aggiungere al gruppo.</span><span class="sxs-lookup"><span data-stu-id="a86e1-124">The UPN of the member(s) to add to the group.</span></span>

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

### <span data-ttu-id="a86e1-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a86e1-125">-PassThru</span></span>
<span data-ttu-id="a86e1-126">Se il comando ha avuto esito positivo, la specifica restituirà true.</span><span class="sxs-lookup"><span data-stu-id="a86e1-126">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="a86e1-127">-TargetGroupDisplayName</span><span class="sxs-lookup"><span data-stu-id="a86e1-127">-TargetGroupDisplayName</span></span>
<span data-ttu-id="a86e1-128">Il nome visualizzato del gruppo a cui aggiungere il membro o i membri.</span><span class="sxs-lookup"><span data-stu-id="a86e1-128">The display name of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="a86e1-129">-TargetGroupObject</span><span class="sxs-lookup"><span data-stu-id="a86e1-129">-TargetGroupObject</span></span>
<span data-ttu-id="a86e1-130">Rappresentazione dell'oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="a86e1-130">The object representation of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="a86e1-131">-TargetGroupObjectId</span><span class="sxs-lookup"><span data-stu-id="a86e1-131">-TargetGroupObjectId</span></span>
<span data-ttu-id="a86e1-132">ID oggetto del gruppo a cui aggiungere i membri.</span><span class="sxs-lookup"><span data-stu-id="a86e1-132">The object id of the group to add the member(s) to.</span></span>

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

### <span data-ttu-id="a86e1-133">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a86e1-133">-Confirm</span></span>
<span data-ttu-id="a86e1-134">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a86e1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a86e1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a86e1-135">-WhatIf</span></span>
<span data-ttu-id="a86e1-136">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a86e1-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a86e1-137">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a86e1-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a86e1-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a86e1-138">CommonParameters</span></span>
<span data-ttu-id="a86e1-139">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a86e1-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a86e1-140">Per altre informazioni, Vedi about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a86e1-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a86e1-141">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a86e1-141">INPUTS</span></span>

### <span data-ttu-id="a86e1-142">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADGroup</span><span class="sxs-lookup"><span data-stu-id="a86e1-142">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADGroup</span></span>
<span data-ttu-id="a86e1-143">Parametri: TargetGroupObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="a86e1-143">Parameters: TargetGroupObject (ByValue)</span></span>

## <span data-ttu-id="a86e1-144">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a86e1-144">OUTPUTS</span></span>

### <span data-ttu-id="a86e1-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a86e1-145">System.Boolean</span></span>

## <span data-ttu-id="a86e1-146">Note</span><span class="sxs-lookup"><span data-stu-id="a86e1-146">NOTES</span></span>

## <span data-ttu-id="a86e1-147">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a86e1-147">RELATED LINKS</span></span>
