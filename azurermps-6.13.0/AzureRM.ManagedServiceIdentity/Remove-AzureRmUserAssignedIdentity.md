---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 03d73ac28bc1869452ecc96b5c867fcbb8c372c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93687821"
---
# <span data-ttu-id="d1a72-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d1a72-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="d1a72-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="d1a72-102">SYNOPSIS</span></span>
<span data-ttu-id="d1a72-103">Rimuove un'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="d1a72-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1a72-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="d1a72-104">SYNTAX</span></span>

### <span data-ttu-id="d1a72-105">ResourceGroupAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="d1a72-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1a72-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a72-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1a72-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d1a72-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1a72-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="d1a72-108">DESCRIPTION</span></span>
<span data-ttu-id="d1a72-109">**Remove-AzureRmUserAssignedIdentity** Elimina l'identità assegnata dall'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="d1a72-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="d1a72-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="d1a72-110">EXAMPLES</span></span>

### <span data-ttu-id="d1a72-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="d1a72-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="d1a72-112">Questo cmdlet di esempio Elimina l'identità **ID1** in gruppo risorse **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="d1a72-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>
<span data-ttu-id="d1a72-113">True</span><span class="sxs-lookup"><span data-stu-id="d1a72-113">True</span></span>

## <span data-ttu-id="d1a72-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="d1a72-114">PARAMETERS</span></span>

### <span data-ttu-id="d1a72-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1a72-115">-AsJob</span></span>
<span data-ttu-id="d1a72-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="d1a72-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1a72-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1a72-117">-DefaultProfile</span></span>
<span data-ttu-id="d1a72-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="d1a72-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1a72-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d1a72-119">-Force</span></span>
<span data-ttu-id="d1a72-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="d1a72-120">{{Fill Force Description}}</span></span>

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

### <span data-ttu-id="d1a72-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1a72-121">-InputObject</span></span>
<span data-ttu-id="d1a72-122">Oggetto Identity.</span><span class="sxs-lookup"><span data-stu-id="d1a72-122">The Identity object.</span></span>

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

### <span data-ttu-id="d1a72-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="d1a72-123">-Name</span></span>
<span data-ttu-id="d1a72-124">Nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="d1a72-124">The Identity name.</span></span>

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

### <span data-ttu-id="d1a72-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1a72-125">-ResourceGroupName</span></span>
<span data-ttu-id="d1a72-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="d1a72-126">The resource group name.</span></span>

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

### <span data-ttu-id="d1a72-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d1a72-127">-ResourceId</span></span>
<span data-ttu-id="d1a72-128">ID risorsa dell'identità.</span><span class="sxs-lookup"><span data-stu-id="d1a72-128">The Identity's resource id.</span></span>

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

### <span data-ttu-id="d1a72-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="d1a72-129">-Confirm</span></span>
<span data-ttu-id="d1a72-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1a72-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1a72-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1a72-131">-WhatIf</span></span>
<span data-ttu-id="d1a72-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1a72-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1a72-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="d1a72-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1a72-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1a72-134">CommonParameters</span></span>
<span data-ttu-id="d1a72-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1a72-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1a72-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1a72-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1a72-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="d1a72-137">INPUTS</span></span>

### <span data-ttu-id="d1a72-138">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="d1a72-138">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>
<span data-ttu-id="d1a72-139">Parametri: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d1a72-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="d1a72-140">System. String</span><span class="sxs-lookup"><span data-stu-id="d1a72-140">System.String</span></span>

## <span data-ttu-id="d1a72-141">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="d1a72-141">OUTPUTS</span></span>

### <span data-ttu-id="d1a72-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d1a72-142">System.Boolean</span></span>

## <span data-ttu-id="d1a72-143">Note</span><span class="sxs-lookup"><span data-stu-id="d1a72-143">NOTES</span></span>

## <span data-ttu-id="d1a72-144">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="d1a72-144">RELATED LINKS</span></span>
