---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryCredential.md
ms.openlocfilehash: e65367a94e946aee83df2087463bd0081e925862
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "93686169"
---
# <span data-ttu-id="0936c-101">Update-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0936c-101">Update-AzureRmContainerRegistryCredential</span></span>

## <span data-ttu-id="0936c-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="0936c-102">SYNOPSIS</span></span>
<span data-ttu-id="0936c-103">Rigenera una credenziale di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0936c-103">Regenerates a login credential for a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0936c-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="0936c-104">SYNTAX</span></span>

### <span data-ttu-id="0936c-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="0936c-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 -PasswordName <PasswordName> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0936c-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0936c-106">RegistryObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryCredential -Registry <PSContainerRegistry> -PasswordName <PasswordName>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0936c-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="0936c-107">DESCRIPTION</span></span>
<span data-ttu-id="0936c-108">Il cmdlet **Update-AzureRmContainerRegistryCredential** rigenera una credenziale di accesso per un registro dei contenitori.</span><span class="sxs-lookup"><span data-stu-id="0936c-108">The **Update-AzureRmContainerRegistryCredential** cmdlet regenerates a login credential for a container registry.</span></span>

## <span data-ttu-id="0936c-109">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="0936c-109">EXAMPLES</span></span>

### <span data-ttu-id="0936c-110">Esempio 1: rigenerare una credenziale di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="0936c-110">Example 1: Regenerate a login credential for a container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -PasswordName "Password"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry ++q/=K9+RH/+hwg2+3A=N+/w=J/12Ph9 //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="0936c-111">Questo comando rigenera una credenziale di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="0936c-111">This command regenerates a login credential for the specified container registry.</span></span> <span data-ttu-id="0936c-112">L'utente di amministratore deve essere abilitato per il registro `MyRegistry` di sistema contenitore per rigenerare le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="0936c-112">Admin user has to be enabled for the container registry `MyRegistry` to regenerate login credentials.</span></span>

## <span data-ttu-id="0936c-113">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="0936c-113">PARAMETERS</span></span>

### <span data-ttu-id="0936c-114">-Nome</span><span class="sxs-lookup"><span data-stu-id="0936c-114">-Name</span></span>
<span data-ttu-id="0936c-115">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0936c-115">Container Registry Name.</span></span>

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

### <span data-ttu-id="0936c-116">-Passwordname</span><span class="sxs-lookup"><span data-stu-id="0936c-116">-PasswordName</span></span>
<span data-ttu-id="0936c-117">Nome della password da rigenerare.</span><span class="sxs-lookup"><span data-stu-id="0936c-117">The name of password to regenerate.</span></span>
<span data-ttu-id="0936c-118">Valori consentiti: password, password2.</span><span class="sxs-lookup"><span data-stu-id="0936c-118">Allowed values: password, password2.</span></span>

```yaml
Type: Microsoft.Azure.Management.ContainerRegistry.Models.PasswordName
Parameter Sets: (All)
Aliases: 
Accepted values: Password, Password2

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0936c-119">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="0936c-119">-Registry</span></span>
<span data-ttu-id="0936c-120">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="0936c-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="0936c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0936c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0936c-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="0936c-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="0936c-123">-Confermare</span><span class="sxs-lookup"><span data-stu-id="0936c-123">-Confirm</span></span>
<span data-ttu-id="0936c-124">Richiede la conferma prima di eseguire il cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0936c-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0936c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0936c-125">-WhatIf</span></span>
<span data-ttu-id="0936c-126">Mostra cosa succede se il cmdlet viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0936c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0936c-127">Il cmdlet non viene eseguito.</span><span class="sxs-lookup"><span data-stu-id="0936c-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0936c-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0936c-128">-DefaultProfile</span></span>
<span data-ttu-id="0936c-129">Le credenziali, l'account, il tenant e l'abbonamento usati per la comunicazione con Azure.</span><span class="sxs-lookup"><span data-stu-id="0936c-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0936c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0936c-130">CommonParameters</span></span>
<span data-ttu-id="0936c-131">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0936c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0936c-132">Per altre informazioni, Vedi about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0936c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0936c-133">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="0936c-133">INPUTS</span></span>

### <span data-ttu-id="0936c-134">PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0936c-134">PSContainerRegistry</span></span>
<span data-ttu-id="0936c-135">Il parametro ' Registry ' accetta il valore di tipo ' PSContainerRegistry ' dalla pipeline</span><span class="sxs-lookup"><span data-stu-id="0936c-135">Parameter 'Registry' accepts value of type 'PSContainerRegistry' from the pipeline</span></span>

## <span data-ttu-id="0936c-136">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="0936c-136">OUTPUTS</span></span>

### <span data-ttu-id="0936c-137">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0936c-137">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="0936c-138">Note</span><span class="sxs-lookup"><span data-stu-id="0936c-138">NOTES</span></span>

## <span data-ttu-id="0936c-139">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="0936c-139">RELATED LINKS</span></span>

[<span data-ttu-id="0936c-140">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0936c-140">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="0936c-141">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="0936c-141">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="0936c-142">Get-AzureRmContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="0936c-142">Get-AzureRmContainerRegistryCredential</span></span>](./Get-AzureRmContainerRegistryCredential.md)

