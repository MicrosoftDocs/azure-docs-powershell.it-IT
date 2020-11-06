---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: 46eb802b4a91aa7ee7d370ed9ca93805497f21d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93516835"
---
# <span data-ttu-id="1e091-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1e091-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="1e091-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="1e091-102">SYNOPSIS</span></span>
<span data-ttu-id="1e091-103">Rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e091-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e091-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="1e091-104">SYNTAX</span></span>

### <span data-ttu-id="1e091-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="1e091-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1e091-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e091-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1e091-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1e091-107">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -PasswordName <PasswordName> -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e091-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1e091-108">DESCRIPTION</span></span>
<span data-ttu-id="1e091-109">Il cmdlet Update-AzureRmContainerRegistryCredential rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e091-109">The Update-AzureRmContainerRegistryCredential cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="1e091-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="1e091-110">EXAMPLES</span></span>

### <span data-ttu-id="1e091-111">Esempio 1: rigenerare una credenziale di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="1e091-111">Example 1: Regenerate a login credential for a container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="1e091-112">Questo comando rigenera una credenziale di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="1e091-112">This command regenerates a login credential for the specified container registry.</span></span>
<span data-ttu-id="1e091-113">L'utente di amministratore deve essere abilitato per il registro \` di sistema Registry \` per rigenerare le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="1e091-113">Admin user has to be enabled for the container registry \`MyRegistry\` to regenerate login credentials.</span></span>

## <span data-ttu-id="1e091-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="1e091-114">PARAMETERS</span></span>

### <span data-ttu-id="1e091-115">-Nome</span><span class="sxs-lookup"><span data-stu-id="1e091-115">-Name</span></span>
<span data-ttu-id="1e091-116">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e091-116">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-117">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="1e091-117">-PasswordName</span></span>
<span data-ttu-id="1e091-118">Nome della password da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="1e091-118">The name of password to regenerate.</span></span>
<span data-ttu-id="1e091-119">Valori consentiti: password, password2.</span><span class="sxs-lookup"><span data-stu-id="1e091-119">Allowed values: password, password2.</span></span>

```yaml
Type: PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-120">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="1e091-120">-Registry</span></span>
<span data-ttu-id="1e091-121">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="1e091-121">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e091-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e091-123">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="1e091-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-124">-Confermare</span><span class="sxs-lookup"><span data-stu-id="1e091-124">-Confirm</span></span>
<span data-ttu-id="1e091-125">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e091-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e091-126">-WhatIf</span></span>
<span data-ttu-id="1e091-127">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e091-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e091-128">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="1e091-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e091-129">-DefaultProfile</span></span>
<span data-ttu-id="1e091-130">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="1e091-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1e091-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1e091-131">-ResourceId</span></span>
<span data-ttu-id="1e091-132">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="1e091-132">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e091-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e091-133">CommonParameters</span></span>
<span data-ttu-id="1e091-134">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e091-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e091-135">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e091-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e091-136">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="1e091-136">INPUTS</span></span>

### <span data-ttu-id="1e091-137">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e091-137">PSContainerRegistry</span></span>
<span data-ttu-id="1e091-138">Il parametro ' Registry ' accetta il valore di tipo ' PSContainerRegistry ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="1e091-138">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="1e091-139">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="1e091-139">OUTPUTS</span></span>

### <span data-ttu-id="1e091-140">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1e091-140">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="1e091-141">Note</span><span class="sxs-lookup"><span data-stu-id="1e091-141">NOTES</span></span>

## <span data-ttu-id="1e091-142">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="1e091-142">RELATED LINKS</span></span>

[<span data-ttu-id="1e091-143">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e091-143">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="1e091-144">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="1e091-144">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="1e091-145">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="1e091-145">Get-AzureRmContainerRegistryCredential</span></span>](Get-AzureRmContainerRegistryCredential.md)

