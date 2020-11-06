---
external help file: Microsoft.Azure.Commands.ManagedServiceIdentity.dll-Help.xml
Module Name: AzureRM.ManagedServiceIdentity
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.managedserviceidentity/remove-azurermuserassignedidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ManagedServiceIdentity/Commands.ManagedServiceIdentity/help/Remove-AzureRmUserAssignedIdentity.md
ms.openlocfilehash: 8b533f26b7fa947a185ee0be2dc5a395e77ebbbd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516771"
---
# <span data-ttu-id="ae121-101">Remove-AzureRmUserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="ae121-101">Remove-AzureRmUserAssignedIdentity</span></span>

## <span data-ttu-id="ae121-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="ae121-102">SYNOPSIS</span></span>
<span data-ttu-id="ae121-103">Rimuove un'identità assegnata dall'utente.</span><span class="sxs-lookup"><span data-stu-id="ae121-103">Removes a User Assigned Identity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae121-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="ae121-104">SYNTAX</span></span>

### <span data-ttu-id="ae121-105">ResourceGroupAndNameParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="ae121-105">ResourceGroupAndNameParameterSet (Default)</span></span>
```
Remove-AzureRmUserAssignedIdentity [-ResourceGroupName] <String> [-Name] <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae121-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae121-106">InputObjectParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -InputObject <PsUserAssignedIdentity> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae121-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae121-107">ResourceIdParameterSet</span></span>
```
Remove-AzureRmUserAssignedIdentity -ResourceId <String> [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae121-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ae121-108">DESCRIPTION</span></span>
<span data-ttu-id="ae121-109">**Remove-AzureRmUserAssignedIdentity** Elimina l'identità assegnata dall'utente specificato.</span><span class="sxs-lookup"><span data-stu-id="ae121-109">The **Remove-AzureRmUserAssignedIdentity** deletes the specified User Assigned Identity.</span></span>

## <span data-ttu-id="ae121-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="ae121-110">EXAMPLES</span></span>

### <span data-ttu-id="ae121-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="ae121-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzurRmUserAssignedIdentity -ResourceGroupName PSRG -Name ID1
```

<span data-ttu-id="ae121-112">Questo cmdlet di esempio Elimina l'identità **ID1** in gruppo risorse **PSRG**.</span><span class="sxs-lookup"><span data-stu-id="ae121-112">This example cmdlet deletes the identity **ID1** under resource group **PSRG**.</span></span>

<span data-ttu-id="ae121-113">True</span><span class="sxs-lookup"><span data-stu-id="ae121-113">True</span></span>

## <span data-ttu-id="ae121-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="ae121-114">PARAMETERS</span></span>

### <span data-ttu-id="ae121-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae121-115">-AsJob</span></span>
<span data-ttu-id="ae121-116">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="ae121-116">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae121-117">-DefaultProfile</span></span>
<span data-ttu-id="ae121-118">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="ae121-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ae121-119">-Force</span></span>
<span data-ttu-id="ae121-120">{{Fill Force Description}}</span><span class="sxs-lookup"><span data-stu-id="ae121-120">{{Fill Force Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae121-121">-InputObject</span></span>
<span data-ttu-id="ae121-122">Oggetto Identity.</span><span class="sxs-lookup"><span data-stu-id="ae121-122">The Identity object.</span></span>

```yaml
Type: PsUserAssignedIdentity
Parameter Sets: InputObjectParameterSet
Aliases: Identity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae121-123">-Name</span></span>
<span data-ttu-id="ae121-124">Nome dell'identità.</span><span class="sxs-lookup"><span data-stu-id="ae121-124">The Identity name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae121-125">-ResourceGroupName</span></span>
<span data-ttu-id="ae121-126">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="ae121-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae121-127">-ResourceId</span></span>
<span data-ttu-id="ae121-128">ID risorsa dell'identità.</span><span class="sxs-lookup"><span data-stu-id="ae121-128">The Identity's resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-129">-Confermare</span><span class="sxs-lookup"><span data-stu-id="ae121-129">-Confirm</span></span>
<span data-ttu-id="ae121-130">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae121-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae121-131">-WhatIf</span></span>
<span data-ttu-id="ae121-132">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae121-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae121-133">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="ae121-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae121-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae121-134">CommonParameters</span></span>
<span data-ttu-id="ae121-135">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae121-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae121-136">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae121-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae121-137">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="ae121-137">INPUTS</span></span>

### <span data-ttu-id="ae121-138">System. String</span><span class="sxs-lookup"><span data-stu-id="ae121-138">System.String</span></span>

## <span data-ttu-id="ae121-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="ae121-139">OUTPUTS</span></span>

### <span data-ttu-id="ae121-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ae121-140">System.Boolean</span></span>

## <span data-ttu-id="ae121-141">Note</span><span class="sxs-lookup"><span data-stu-id="ae121-141">NOTES</span></span>

## <span data-ttu-id="ae121-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="ae121-142">RELATED LINKS</span></span>
