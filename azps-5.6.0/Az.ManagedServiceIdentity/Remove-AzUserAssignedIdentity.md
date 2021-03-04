---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 83280df19363285ab23ca1e27441a491a783b03a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962910"
---
# <span data-ttu-id="8004a-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8004a-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="8004a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8004a-102">SYNOPSIS</span></span>
<span data-ttu-id="8004a-103">Rimuove un'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="8004a-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="8004a-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="8004a-104">SYNTAX</span></span>

### <span data-ttu-id="8004a-105">ResourceGroupAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="8004a-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8004a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8004a-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8004a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8004a-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8004a-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="8004a-108">DESCRIPTION</span></span>
<span data-ttu-id="8004a-109">**Remove-AzUserAssignedIdentity** elimina l'identità assegnata dall'utente specificata.</span><span class="sxs-lookup"><span data-stu-id="8004a-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="8004a-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="8004a-110">EXAMPLES</span></span>

### <span data-ttu-id="8004a-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="8004a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="8004a-112">Questo cmdlet di esempio elimina **l'id di identità1** nel gruppo di risorse **PSRG.**</span><span class="sxs-lookup"><span data-stu-id="8004a-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="8004a-113">True</span><span class="sxs-lookup"><span data-stu-id="8004a-113">True</span></span>

## <span data-ttu-id="8004a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8004a-114">PARAMETERS</span></span>

### <span data-ttu-id="8004a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8004a-115">-AsJob</span></span>
<span data-ttu-id="8004a-116">Eseguire il cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="8004a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8004a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8004a-117">-DefaultProfile</span></span>
<span data-ttu-id="8004a-118">Le credenziali, l'account, il tenant e la sottoscrizione usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="8004a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8004a-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8004a-119">-Force</span></span>
<span data-ttu-id="8004a-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="8004a-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="8004a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8004a-121">-InputObject</span></span>
<span data-ttu-id="8004a-122">Oggetto Identity.</span><span class="sxs-lookup"><span data-stu-id="8004a-122">The Identity object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8004a-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8004a-123">-Name</span></span>
<span data-ttu-id="8004a-124">Nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="8004a-124">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8004a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8004a-125">-ResourceGroupName</span></span>
<span data-ttu-id="8004a-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="8004a-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8004a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8004a-127">-ResourceId</span></span>
<span data-ttu-id="8004a-128">ID risorsa dell'identità.</span><span class="sxs-lookup"><span data-stu-id="8004a-128">The Identity's resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8004a-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8004a-129">-Confirm</span></span>
<span data-ttu-id="8004a-130">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8004a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8004a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8004a-131">-WhatIf</span></span>
<span data-ttu-id="8004a-132">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8004a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8004a-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="8004a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8004a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8004a-134">CommonParameters</span></span>
<span data-ttu-id="8004a-135">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8004a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8004a-136">Per altre informazioni, vedere about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8004a-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8004a-137">INPUT</span><span class="sxs-lookup"><span data-stu-id="8004a-137">INPUTS</span></span>

### <span data-ttu-id="8004a-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="8004a-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="8004a-139">System.String</span><span class="sxs-lookup"><span data-stu-id="8004a-139">System.String</span></span>

## <span data-ttu-id="8004a-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="8004a-140">OUTPUTS</span></span>

### <span data-ttu-id="8004a-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8004a-141">System.Boolean</span></span>

## <span data-ttu-id="8004a-142">NOTE</span><span class="sxs-lookup"><span data-stu-id="8004a-142">NOTES</span></span>

## <span data-ttu-id="8004a-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="8004a-143">RELATED LINKS</span></span>
