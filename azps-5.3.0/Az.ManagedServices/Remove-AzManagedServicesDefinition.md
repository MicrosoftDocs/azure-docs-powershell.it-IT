---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: 2b81a1983bb89af48115ead85c3392cc3d762734
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/05/2021
ms.locfileid: "98476848"
---
# <span data-ttu-id="4c326-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="4c326-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="4c326-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="4c326-102">SYNOPSIS</span></span>
<span data-ttu-id="4c326-103">Elimina la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4c326-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="4c326-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="4c326-104">SYNTAX</span></span>

### <span data-ttu-id="4c326-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="4c326-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition [-Scope <String>] -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c326-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="4c326-106">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c326-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="4c326-107">DESCRIPTION</span></span>
<span data-ttu-id="4c326-108">Elimina la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4c326-108">Deletes the registration definition.</span></span>

## <span data-ttu-id="4c326-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="4c326-109">EXAMPLES</span></span>

### <span data-ttu-id="4c326-110">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="4c326-110">Example 1</span></span>
```
PS C:\> Remove-AzManagedServicesDefinition -Name 0c146106-c927-4098-a7ca-30bbcf44a502
PS C:\>
```

<span data-ttu-id="4c326-111">Rimuove la definizione di registrazione per nome nell'ambito predefinito.</span><span class="sxs-lookup"><span data-stu-id="4c326-111">Removes the registration definition by name at the default scope.</span></span>

### <span data-ttu-id="4c326-112">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="4c326-112">Example 2</span></span>
```
PS C:\> $definition = New-AzManagedServicesDefinition -DisplayName "MyTestDefinition" -ManagedByTenantId 72f9acbf-86f1-41af-91ab-2d7ef011db47 -RoleDefinitionId acdd72a7-3385-48ef-bd42-f606fba81ae7 -PrincipalId 714160ec-87d5-42bb-8b17-287c0dd7417d
PS C:\> Remove-AzManagedServicesDefinition -InputObject $definition
PS C:\>
```

<span data-ttu-id="4c326-113">Elimina la definizione di registrazione in base all'oggetto di input.</span><span class="sxs-lookup"><span data-stu-id="4c326-113">Deletes the registration definition given the input object.</span></span>

## <span data-ttu-id="4c326-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="4c326-114">PARAMETERS</span></span>

### <span data-ttu-id="4c326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c326-115">-DefaultProfile</span></span>
<span data-ttu-id="4c326-116">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="4c326-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c326-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c326-117">-InputObject</span></span>
<span data-ttu-id="4c326-118">Oggetto della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4c326-118">The registration definition object.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c326-119">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c326-119">-Name</span></span>
<span data-ttu-id="4c326-120">Nome univoco della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4c326-120">The unique name of the Registration Definition.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c326-121">-Ambito</span><span class="sxs-lookup"><span data-stu-id="4c326-121">-Scope</span></span>
<span data-ttu-id="4c326-122">Ambito in cui è stata creata la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="4c326-122">The scope where the registration definition created.</span></span>

```yaml
Type: System.String
Parameter Sets: Default
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c326-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="4c326-123">-Confirm</span></span>
<span data-ttu-id="4c326-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c326-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c326-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c326-125">-WhatIf</span></span>
<span data-ttu-id="4c326-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c326-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c326-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="4c326-127">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c326-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c326-128">CommonParameters</span></span>
<span data-ttu-id="4c326-129">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c326-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c326-130">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c326-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c326-131">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="4c326-131">INPUTS</span></span>

### <span data-ttu-id="4c326-132">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="4c326-132">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>
## <span data-ttu-id="4c326-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="4c326-133">OUTPUTS</span></span>

### <span data-ttu-id="4c326-134">System. void</span><span class="sxs-lookup"><span data-stu-id="4c326-134">System.Void</span></span>
## <span data-ttu-id="4c326-135">Note</span><span class="sxs-lookup"><span data-stu-id="4c326-135">NOTES</span></span>

## <span data-ttu-id="4c326-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="4c326-136">RELATED LINKS</span></span>
