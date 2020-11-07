---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/remove-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/Remove-AzUserAssignedIdentity.md
ms.openlocfilehash: 7b3a231af55bfc16584426fe16c5cedcec50b8b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673903"
---
# <span data-ttu-id="a9213-101">Remove-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a9213-101">Remove-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="a9213-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a9213-102">SYNOPSIS</span></span>
<span data-ttu-id="a9213-103">Rimuove un'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="a9213-103">Removes a User Assigned Identity.</span></span>

## <span data-ttu-id="a9213-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a9213-104">SYNTAX</span></span>

### <span data-ttu-id="a9213-105">ResourceGroupAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a9213-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9213-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9213-106">InputObjectParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a9213-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a9213-107">ResourceIdParameterSet</span></span>
```
Remove-AzUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9213-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a9213-108">DESCRIPTION</span></span>
<span data-ttu-id="a9213-109">**Remove-AzUserAssignedIdentity** Elimina l'identità assegnata dall'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="a9213-109">The **Remove-AzUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="a9213-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a9213-110">EXAMPLES</span></span>

### <span data-ttu-id="a9213-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a9213-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="a9213-112">Questo cmdlet di esempio Elimina l'identità **ID1** in gruppo risorse **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="a9213-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="a9213-113">True</span><span class="sxs-lookup"><span data-stu-id="a9213-113">True</span></span>

## <span data-ttu-id="a9213-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a9213-114">PARAMETERS</span></span>

### <span data-ttu-id="a9213-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a9213-115">-AsJob</span></span>
<span data-ttu-id="a9213-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a9213-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a9213-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9213-117">-DefaultProfile</span></span>
<span data-ttu-id="a9213-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a9213-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9213-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a9213-119">-Force</span></span>
<span data-ttu-id="a9213-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="a9213-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="a9213-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a9213-121">-InputObject</span></span>
<span data-ttu-id="a9213-122">Oggetto Identity.</span><span class="sxs-lookup"><span data-stu-id="a9213-122">The Identity object.</span></span>

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

### <span data-ttu-id="a9213-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="a9213-123">-Name</span></span>
<span data-ttu-id="a9213-124">Nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="a9213-124">The Identity name.</span></span>

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

### <span data-ttu-id="a9213-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9213-125">-ResourceGroupName</span></span>
<span data-ttu-id="a9213-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="a9213-126">The resource group name.</span></span>

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

### <span data-ttu-id="a9213-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a9213-127">-ResourceId</span></span>
<span data-ttu-id="a9213-128">ID risorsa dell'identità.</span><span class="sxs-lookup"><span data-stu-id="a9213-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="a9213-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a9213-129">-Confirm</span></span>
<span data-ttu-id="a9213-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9213-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9213-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9213-131">-WhatIf</span></span>
<span data-ttu-id="a9213-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9213-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9213-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a9213-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9213-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9213-134">CommonParameters</span></span>
<span data-ttu-id="a9213-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9213-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9213-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9213-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9213-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a9213-137">INPUTS</span></span>

### <span data-ttu-id="a9213-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="a9213-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

### <span data-ttu-id="a9213-139">System. String</span><span class="sxs-lookup"><span data-stu-id="a9213-139">System.String</span></span>

## <span data-ttu-id="a9213-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a9213-140">OUTPUTS</span></span>

### <span data-ttu-id="a9213-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a9213-141">System.Boolean</span></span>

## <span data-ttu-id="a9213-142">Note</span><span class="sxs-lookup"><span data-stu-id="a9213-142">NOTES</span></span>

## <span data-ttu-id="a9213-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a9213-143">RELATED LINKS</span></span>
