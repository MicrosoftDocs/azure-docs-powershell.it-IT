---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServiceIdentity.dll-Help.xml
Module Name: Az.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServiceIdentity/ManagedServiceIdentity/help/New-AzUserAssignedIdentity.md
ms.openlocfilehash: 572e3d61f4d7cf514cc44fe965a7726288806a9d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93673904"
---
# <span data-ttu-id="1dda4-101">New-AzUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1dda4-101">New-AzUserAssignedIdentity</span></span>

## <span data-ttu-id="1dda4-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1dda4-102">SYNOPSIS</span></span>
<span data-ttu-id="1dda4-103">Crea una nuova identità assegnata dall'utente o aggiorna un'identità assegnata a un utente esistente.</span><span class="sxs-lookup"><span data-stu-id="1dda4-103">Creates a new User Assigned Identity or updates an existing User Assigned Identity.</span></span>

## <span data-ttu-id="1dda4-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1dda4-104">SYNTAX</span></span>

```
New-AzUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-Location <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-Tag <Hashtable>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1dda4-105">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1dda4-105">DESCRIPTION</span></span>
<span data-ttu-id="1dda4-106">Il cmdlet **New-AzUserAssignedIdentity** crea una nuova identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="1dda4-106">The **New-AzUserAssignedIdentity** cmdlet creates a new User Assigned Identity.</span></span> <span data-ttu-id="1dda4-107">Se usato con un'identità già esistente, ha aggiornato l'identità.</span><span class="sxs-lookup"><span data-stu-id="1dda4-107">When used with an already existing identity, it updated the identity.</span></span>
<span data-ttu-id="1dda4-108">Per aggiungere tag di Azure Resource Manager all'identità, usare il cmdlet Set-AzResource.</span><span class="sxs-lookup"><span data-stu-id="1dda4-108">To add Azure Resource Manager tags to the identity, please use the Set-AzResource cmdlet.</span></span>

## <span data-ttu-id="1dda4-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1dda4-109">EXAMPLES</span></span>

### <span data-ttu-id="1dda4-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="1dda4-110">Example 1</span></span>
<span data-ttu-id="1dda4-111">Questo cmdlet di esempio crea una nuova identità assegnata dall'utente con il nome **ID1** in gruppo risorse **PSRG** nella posizione di ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1dda4-111">This example cmdlet creates a new User Assigned Identity with name **ID1** under resource group **PSRG** in the location of the ResourceGroup.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : centralus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG1/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

### <span data-ttu-id="1dda4-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="1dda4-112">Example 2</span></span>
<span data-ttu-id="1dda4-113">Questo cmdlet di esempio crea una nuova identità assegnata dall'utente con il nome **ID1** nel gruppo di risorse **PSRG** nell'area westus.</span><span class="sxs-lookup"><span data-stu-id="1dda4-113">This example cmdlet creates a new User Assigned Identity with name **ID1** under the resource group **PSRG** in the westus region.</span></span>

```powershell
PS C:\> New-AzUserAssignedIdentity -ResourceGroupName PSRG -Name ID1 -Location westus

Id                : /subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1

ResourceGroupName : PSRG

Name              : ID1

Location          : westus

TenantId          : 493b860d-2741-480b-8b34-7b1d76e33c50

PrincipalId       : e34192f9-7831-4a02-bfe2-4c6d2fb4360d

ClientId          : a5e650a2-fdfe-4652-bb3b-109b64617cfd

ClientSecretUrl   : https://control-westus.identity.azure.net/subscriptions/586d0246-0344-49dc-a790-59c916b0c309/resourcegroups/PSRG/providers/Microsoft.ManagedIdentity/userAssignedIdentities/ID1/credentials?tid=493b860d-2741-480b-8b34-7b1d76e33c50&oid=e34192f9-7831-4a02-bfe2-4c6d2fb4360d&aid=a5e650a2-fdfe-4652-bb3b-109b64617cfd

Type              : Microsoft.ManagedIdentity/userAssignedIdentities
```

## <span data-ttu-id="1dda4-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1dda4-114">PARAMETERS</span></span>

### <span data-ttu-id="1dda4-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1dda4-115">-AsJob</span></span>
<span data-ttu-id="1dda4-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="1dda4-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1dda4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1dda4-117">-DefaultProfile</span></span>
<span data-ttu-id="1dda4-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="1dda4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1dda4-119">-Posizione</span><span class="sxs-lookup"><span data-stu-id="1dda4-119">-Location</span></span>
<span data-ttu-id="1dda4-120">Nome dell'area di Azure in cui deve essere creata l'identità.</span><span class="sxs-lookup"><span data-stu-id="1dda4-120">The Azure region name where the Identity should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda4-121">-Nome</span><span class="sxs-lookup"><span data-stu-id="1dda4-121">-Name</span></span>
<span data-ttu-id="1dda4-122">Nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="1dda4-122">The Identity name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda4-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1dda4-123">-ResourceGroupName</span></span>
<span data-ttu-id="1dda4-124">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1dda4-124">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda4-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="1dda4-125">-Tag</span></span>
<span data-ttu-id="1dda4-126">Tag di gestione risorse di Azure associati all'identità.</span><span class="sxs-lookup"><span data-stu-id="1dda4-126">The Azure Resource Manager tags associated with the identity.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1dda4-127">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1dda4-127">-Confirm</span></span>
<span data-ttu-id="1dda4-128">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1dda4-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1dda4-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1dda4-129">-WhatIf</span></span>
<span data-ttu-id="1dda4-130">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dda4-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1dda4-131">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1dda4-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1dda4-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1dda4-132">CommonParameters</span></span>
<span data-ttu-id="1dda4-133">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1dda4-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1dda4-134">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1dda4-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1dda4-135">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1dda4-135">INPUTS</span></span>

### <span data-ttu-id="1dda4-136">System. String</span><span class="sxs-lookup"><span data-stu-id="1dda4-136">System.String</span></span>

### <span data-ttu-id="1dda4-137">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="1dda4-137">System.Collections.Hashtable</span></span>

## <span data-ttu-id="1dda4-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1dda4-138">OUTPUTS</span></span>

### <span data-ttu-id="1dda4-139">Microsoft. Azure. Commands. ManagedServiceIdentity. Models. PsUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="1dda4-139">Microsoft.Azure.Commands.ManagedServiceIdentity.Models.PsUserAssignedIdentity</span></span>

## <span data-ttu-id="1dda4-140">Note</span><span class="sxs-lookup"><span data-stu-id="1dda4-140">NOTES</span></span>

## <span data-ttu-id="1dda4-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1dda4-141">RELATED LINKS</span></span>