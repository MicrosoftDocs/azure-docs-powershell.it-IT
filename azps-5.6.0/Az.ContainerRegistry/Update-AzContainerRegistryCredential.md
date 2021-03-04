---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: 71eb25c99197513bead7cb400b8a5648c137442d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956302"
---
# <span data-ttu-id="0f29d-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0f29d-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="0f29d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f29d-102">SYNOPSIS</span></span>
<span data-ttu-id="0f29d-103">Rigenera le credenziali di accesso per un Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0f29d-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="0f29d-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0f29d-104">SYNTAX</span></span>

### <span data-ttu-id="0f29d-105">NameResourceGroupParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="0f29d-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0f29d-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f29d-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0f29d-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f29d-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f29d-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="0f29d-108">DESCRIPTION</span></span>
<span data-ttu-id="0f29d-109">Il cmdlet Update-AzContainerRegistryCredential rigenera le credenziali di accesso per un Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="0f29d-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="0f29d-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0f29d-110">EXAMPLES</span></span>

### <span data-ttu-id="0f29d-111">Esempio 1: Rigenerare le credenziali di accesso per un Registro di sistema del contenitore</span><span class="sxs-lookup"><span data-stu-id="0f29d-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="0f29d-112">Questo comando rigenera le credenziali di accesso per il Registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="0f29d-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="0f29d-113">L'utente amministratore deve essere abilitato per il registro del contenitore \` MyRegistry \` per rigenerare le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="0f29d-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="0f29d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0f29d-114">PARAMETERS</span></span>

### <span data-ttu-id="0f29d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f29d-115">-DefaultProfile</span></span>
<span data-ttu-id="0f29d-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="0f29d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0f29d-117">-Name</span><span class="sxs-lookup"><span data-stu-id="0f29d-117">-Name</span></span>
<span data-ttu-id="0f29d-118">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0f29d-118">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f29d-119">-PasswordName</span><span class="sxs-lookup"><span data-stu-id="0f29d-119">-PasswordName</span></span>
<span data-ttu-id="0f29d-120">Nome della password da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="0f29d-120">The name of password to regenerate.</span></span>
<span data-ttu-id="0f29d-121">Valori consentiti: password, password2.</span><span class="sxs-lookup"><span data-stu-id="0f29d-121">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases:
Accepted values: password, password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f29d-122">-Registry</span><span class="sxs-lookup"><span data-stu-id="0f29d-122">-Registry</span></span>
<span data-ttu-id="0f29d-123">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="0f29d-123">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f29d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f29d-124">-ResourceGroupName</span></span>
<span data-ttu-id="0f29d-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0f29d-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0f29d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0f29d-126">-ResourceId</span></span>
<span data-ttu-id="0f29d-127">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="0f29d-127">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f29d-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0f29d-128">-Confirm</span></span>
<span data-ttu-id="0f29d-129">Chiede conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f29d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f29d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f29d-130">-WhatIf</span></span>
<span data-ttu-id="0f29d-131">Mostra cosa accadrebbe se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f29d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f29d-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0f29d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f29d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f29d-133">CommonParameters</span></span>
<span data-ttu-id="0f29d-134">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f29d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f29d-135">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0f29d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f29d-136">INPUT</span><span class="sxs-lookup"><span data-stu-id="0f29d-136">INPUTS</span></span>

### <span data-ttu-id="0f29d-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f29d-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="0f29d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0f29d-138">System.String</span></span>

## <span data-ttu-id="0f29d-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0f29d-139">OUTPUTS</span></span>

### <span data-ttu-id="0f29d-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0f29d-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="0f29d-141">NOTE</span><span class="sxs-lookup"><span data-stu-id="0f29d-141">NOTES</span></span>

## <span data-ttu-id="0f29d-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0f29d-142">RELATED LINKS</span></span>

[<span data-ttu-id="0f29d-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f29d-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="0f29d-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0f29d-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="0f29d-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0f29d-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

