---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 836e8983a9d2e6c7ff21444f0da7b3bf85c1b1d4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93521387"
---
# <span data-ttu-id="27c30-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="27c30-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="27c30-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="27c30-102">SYNOPSIS</span></span>
<span data-ttu-id="27c30-103">Rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="27c30-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="27c30-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="27c30-104">SYNTAX</span></span>

### <span data-ttu-id="27c30-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="27c30-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27c30-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27c30-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27c30-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="27c30-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27c30-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="27c30-108">DESCRIPTION</span></span>
<span data-ttu-id="27c30-109">Il cmdlet Update-AzureRmContainerRegistryCredential rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="27c30-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="27c30-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="27c30-110">EXAMPLES</span></span>

### <span data-ttu-id="27c30-111">Esempio 1: rigenerare una credenziale di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="27c30-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="27c30-112">Questo comando rigenera una credenziale di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="27c30-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="27c30-113">L'utente di amministratore deve essere abilitato per il registro \` di sistema Registry \` per rigenerare le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="27c30-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="27c30-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="27c30-114">PARAMETERS</span></span>

### <span data-ttu-id="27c30-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27c30-115">-DefaultProfile</span></span>
<span data-ttu-id="27c30-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="27c30-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="27c30-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="27c30-117">-Name</span></span>
<span data-ttu-id="27c30-118">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="27c30-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="27c30-119">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="27c30-119">-PasswordName</span></span>
<span data-ttu-id="27c30-120">Nome della password da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="27c30-120">The name of password to regenerate.</span></span>
<span data-ttu-id="27c30-121">Valori consentiti: password, password2.</span><span class="sxs-lookup"><span data-stu-id="27c30-121">Allowed values: password, password2.</span></span>

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

### <span data-ttu-id="27c30-122">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="27c30-122">-Registry</span></span>
<span data-ttu-id="27c30-123">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="27c30-123">Container Registry Object.</span></span>

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

### <span data-ttu-id="27c30-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27c30-124">-ResourceGroupName</span></span>
<span data-ttu-id="27c30-125">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="27c30-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="27c30-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="27c30-126">-ResourceId</span></span>
<span data-ttu-id="27c30-127">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="27c30-127">The container registry resource id</span></span>

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

### <span data-ttu-id="27c30-128">-Confermare</span><span class="sxs-lookup"><span data-stu-id="27c30-128">-Confirm</span></span>
<span data-ttu-id="27c30-129">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="27c30-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27c30-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27c30-130">-WhatIf</span></span>
<span data-ttu-id="27c30-131">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27c30-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="27c30-132">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="27c30-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27c30-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27c30-133">CommonParameters</span></span>
<span data-ttu-id="27c30-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="27c30-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27c30-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="27c30-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27c30-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="27c30-136">INPUTS</span></span>

### <span data-ttu-id="27c30-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27c30-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="27c30-138">Parametri: Registro di sistema (ByValue)</span><span class="sxs-lookup"><span data-stu-id="27c30-138">Parameters: Registry (ByValue)</span></span>

### <span data-ttu-id="27c30-139">System. String</span><span class="sxs-lookup"><span data-stu-id="27c30-139">System.String</span></span>

## <span data-ttu-id="27c30-140">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="27c30-140">OUTPUTS</span></span>

### <span data-ttu-id="27c30-141">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="27c30-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="27c30-142">Note</span><span class="sxs-lookup"><span data-stu-id="27c30-142">NOTES</span></span>

## <span data-ttu-id="27c30-143">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="27c30-143">RELATED LINKS</span></span>

[<span data-ttu-id="27c30-144">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27c30-144">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="27c30-145">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="27c30-145">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="27c30-146">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="27c30-146">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

