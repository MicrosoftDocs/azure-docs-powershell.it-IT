---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryCredential.md
ms.openlocfilehash: d8e5f36366df16dd7b0d03fb07f948e436c0a919
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/27/2020
ms.locfileid: "94299611"
---
# <span data-ttu-id="30a18-101">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="30a18-101">Update-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="30a18-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="30a18-102">SYNOPSIS</span></span>
<span data-ttu-id="30a18-103">Rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="30a18-103">Regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="30a18-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="30a18-104">SYNTAX</span></span>

### <span data-ttu-id="30a18-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="30a18-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="30a18-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="30a18-106">RegistryObjectParameterSet</span></span>
```
Update-AzContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30a18-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="30a18-107">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30a18-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="30a18-108">DESCRIPTION</span></span>
<span data-ttu-id="30a18-109">Il cmdlet Update-AzContainerRegistryCredential rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="30a18-109">The Update-AzContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="30a18-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="30a18-110">EXAMPLES</span></span>

### <span data-ttu-id="30a18-111">Esempio 1: rigenerare una credenziale di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="30a18-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="30a18-112">Questo comando rigenera una credenziale di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="30a18-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="30a18-113">L'utente di amministratore deve essere abilitato per il registro \` di sistema Registry \` per rigenerare le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="30a18-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="30a18-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="30a18-114">PARAMETERS</span></span>

### <span data-ttu-id="30a18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30a18-115">-DefaultProfile</span></span>
<span data-ttu-id="30a18-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="30a18-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30a18-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="30a18-117">-Name</span></span>
<span data-ttu-id="30a18-118">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="30a18-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="30a18-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="30a18-119">-PasswordName</span></span>
<span data-ttu-id="30a18-120">Nome della password da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="30a18-120">The name of password to regenerate.</span></span>
<span data-ttu-id="30a18-121">Valori consentiti: password, password2.</span><span class="sxs-lookup"><span data-stu-id="30a18-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="30a18-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="30a18-122">-Registry</span></span>
<span data-ttu-id="30a18-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="30a18-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="30a18-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30a18-124">-ResourceGroupName</span></span>
<span data-ttu-id="30a18-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="30a18-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="30a18-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="30a18-126">-ResourceId</span></span>
<span data-ttu-id="30a18-127">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="30a18-127">The container registry resource id</span></span>

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

### <span data-ttu-id="30a18-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="30a18-128">-Confirm</span></span>
<span data-ttu-id="30a18-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30a18-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30a18-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30a18-130">-WhatIf</span></span>
<span data-ttu-id="30a18-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30a18-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30a18-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="30a18-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30a18-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30a18-133">CommonParameters</span></span>
<span data-ttu-id="30a18-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30a18-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30a18-135">Per altre informazioni, Vedi [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="30a18-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30a18-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="30a18-136">INPUTS</span></span>

### <span data-ttu-id="30a18-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30a18-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="30a18-138">System. String</span><span class="sxs-lookup"><span data-stu-id="30a18-138">System.String</span></span>

## <span data-ttu-id="30a18-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="30a18-139">OUTPUTS</span></span>

### <span data-ttu-id="30a18-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="30a18-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="30a18-141">Note</span><span class="sxs-lookup"><span data-stu-id="30a18-141">NOTES</span></span>

## <span data-ttu-id="30a18-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="30a18-142">RELATED LINKS</span></span>

[<span data-ttu-id="30a18-143">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30a18-143">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="30a18-144">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="30a18-144">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="30a18-145">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="30a18-145">Get-AzContainerRegistryCredential</span></span>](Get-AzContainerRegistryCredential.md)

