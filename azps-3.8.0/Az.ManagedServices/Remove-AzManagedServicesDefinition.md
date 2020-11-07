---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.dll-Help.xml
Module Name: Az.ManagedServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.managedservices/remove-azmanagedservicesdefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ManagedServices/ManagedServices/help/Remove-AzManagedServicesDefinition.md
ms.openlocfilehash: ffebb4e3fca417c896939bb54ed1c0af1c42f7fc
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/21/2020
ms.locfileid: "93864429"
---
# <span data-ttu-id="a564c-101">Remove-AzManagedServicesDefinition</span><span class="sxs-lookup"><span data-stu-id="a564c-101">Remove-AzManagedServicesDefinition</span></span>

## <span data-ttu-id="a564c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="a564c-102">SYNOPSIS</span></span>
<span data-ttu-id="a564c-103">Elimina la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a564c-103">Deletes the registration definition.</span></span>

## <span data-ttu-id="a564c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="a564c-104">SYNTAX</span></span>

### <span data-ttu-id="a564c-105">Predefinito (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="a564c-105">Default (Default)</span></span>
```
Remove-AzManagedServicesDefinition -Id <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a564c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a564c-106">ByResourceId</span></span>
```
Remove-AzManagedServicesDefinition -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a564c-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a564c-107">ByInputObject</span></span>
```
Remove-AzManagedServicesDefinition -InputObject <PSRegistrationDefinition> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a564c-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a564c-108">DESCRIPTION</span></span>
<span data-ttu-id="a564c-109">Elimina la definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a564c-109">Deletes the registration definition.</span></span>

## <span data-ttu-id="a564c-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="a564c-110">EXAMPLES</span></span>

### <span data-ttu-id="a564c-111">Esempio 1</span><span class="sxs-lookup"><span data-stu-id="a564c-111">Example 1</span></span>
```powershell
PS C:\> Remove-RegistrationDefinition -Id 0513b566-cab0-4fef-9b53-a285cd33389f
```

<span data-ttu-id="a564c-112">Rimuove la definizione di registrazione assegnata all'identificatore.</span><span class="sxs-lookup"><span data-stu-id="a564c-112">Removes the registration definition given it identifier.</span></span>

### <span data-ttu-id="a564c-113">Esempio 2</span><span class="sxs-lookup"><span data-stu-id="a564c-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzManagedServicesDefinition -ResourceId /subscriptions/38bd4bef-41ff-45b5-b3af-d03e55a4ca15/providers/Microsoft.ManagedServices/registrationDefinitions/11b7c937-c5c1-4dd1-9a77-204591f93fcd

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
11b7c937-c5c1-4dd1-9a77-204591f93fcd bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="a564c-114">Rimuove la definizione di registrazione in base all'ID risorsa completo.</span><span class="sxs-lookup"><span data-stu-id="a564c-114">Removes the registration definition given the fully qualified resource id.</span></span> 

### <span data-ttu-id="a564c-115">Esempio 3</span><span class="sxs-lookup"><span data-stu-id="a564c-115">Example 3</span></span>
```powershell
PS C:\> $def = New-AzManagedServicesDefinition -RegistrationDefinitionName 572e1807-b80b-4401-9128-1968f432a5ad -ManagedByTenantId "bab3375b-6197-4a15-a44b-16c41faa91d7" -PrincipalId "d6f6c88a-5b7a-455e-ba40-ce146d4d3671" -RoleDefinitionId "acdd72a7-3385-48ef-bd42-f606fba81ae7"
PS C:\> Remove-AzManagedServicesDefinition -InputObject $def

Name                                 ManagedByTenantId                    PrincipalId                          RoleDefinitionId
----                                 -----------------                    -----------                          ----------------
eee59839-119f-453f-adec-4a72a8687125 bab3375b-6197-4a15-a44b-16c41faa91d7 d6f6c88a-5b7a-455e-ba40-ce146d4d3671 acdd72a7-3385-48ef-bd42-f606fba81ae7
```

<span data-ttu-id="a564c-116">Elimina la definizione di registrazione in base all'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a564c-116">Deletes the registration definition given the object.</span></span>

## <span data-ttu-id="a564c-117">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="a564c-117">PARAMETERS</span></span>

### <span data-ttu-id="a564c-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a564c-118">-AsJob</span></span>
<span data-ttu-id="a564c-119">Esegui cmdlet in background</span><span class="sxs-lookup"><span data-stu-id="a564c-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a564c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a564c-120">-DefaultProfile</span></span>
<span data-ttu-id="a564c-121">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="a564c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a564c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="a564c-122">-Id</span></span>
<span data-ttu-id="a564c-123">Identificatore della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a564c-123">The registration definition identifier.</span></span>

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

### <span data-ttu-id="a564c-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a564c-124">-InputObject</span></span>
<span data-ttu-id="a564c-125">Oggetto della definizione di registrazione.</span><span class="sxs-lookup"><span data-stu-id="a564c-125">The registration definition object.</span></span>

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

### <span data-ttu-id="a564c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a564c-126">-ResourceId</span></span>
<span data-ttu-id="a564c-127">ResourceId della definizione di registrazione</span><span class="sxs-lookup"><span data-stu-id="a564c-127">ResourceId of the registration definition</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a564c-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="a564c-128">-Confirm</span></span>
<span data-ttu-id="a564c-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a564c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a564c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a564c-130">-WhatIf</span></span>
<span data-ttu-id="a564c-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a564c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a564c-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="a564c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a564c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a564c-133">CommonParameters</span></span>
<span data-ttu-id="a564c-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a564c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a564c-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a564c-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a564c-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="a564c-136">INPUTS</span></span>

### <span data-ttu-id="a564c-137">Nessuno</span><span class="sxs-lookup"><span data-stu-id="a564c-137">None</span></span>

## <span data-ttu-id="a564c-138">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="a564c-138">OUTPUTS</span></span>

### <span data-ttu-id="a564c-139">Microsoft. Azure. PowerShell. Cmdlets. ManagedServices. Models. PSRegistrationDefinition</span><span class="sxs-lookup"><span data-stu-id="a564c-139">Microsoft.Azure.PowerShell.Cmdlets.ManagedServices.Models.PSRegistrationDefinition</span></span>

## <span data-ttu-id="a564c-140">Note</span><span class="sxs-lookup"><span data-stu-id="a564c-140">NOTES</span></span>

## <span data-ttu-id="a564c-141">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="a564c-141">RELATED LINKS</span></span>
