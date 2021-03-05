---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 5e20ae556cba16263d8b650de869b174236ccbd5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004429"
---
# <span data-ttu-id="696d5-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="696d5-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="696d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696d5-102">SYNOPSIS</span></span>
<span data-ttu-id="696d5-103">Ottiene le credenziali di accesso per un Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="696d5-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="696d5-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="696d5-104">SYNTAX</span></span>

### <span data-ttu-id="696d5-105">NameResourceGroupParameterSet (Default)</span><span class="sxs-lookup"><span data-stu-id="696d5-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="696d5-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="696d5-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="696d5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="696d5-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="696d5-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="696d5-108">DESCRIPTION</span></span>
<span data-ttu-id="696d5-109">Il Get-AzContainerRegistryCredential cmdlet di accesso ottiene le credenziali di accesso per un registro contenitore.</span><span class="sxs-lookup"><span data-stu-id="696d5-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="696d5-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="696d5-110">EXAMPLES</span></span>

### <span data-ttu-id="696d5-111">Esempio 1: Ottenere le credenziali di accesso per un registro contenitore</span><span class="sxs-lookup"><span data-stu-id="696d5-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="696d5-112">Questo comando ottiene le credenziali di accesso per il Registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="696d5-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="696d5-113">Per ottenere le credenziali di accesso, l'utente amministratore deve essere abilitato per il contenitore Registro di sistema \` \` MyRegistry.</span><span class="sxs-lookup"><span data-stu-id="696d5-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="696d5-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="696d5-114">PARAMETERS</span></span>

### <span data-ttu-id="696d5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696d5-115">-DefaultProfile</span></span>
<span data-ttu-id="696d5-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="696d5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="696d5-117">-Name</span><span class="sxs-lookup"><span data-stu-id="696d5-117">-Name</span></span>
<span data-ttu-id="696d5-118">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="696d5-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="696d5-119">-Registry</span><span class="sxs-lookup"><span data-stu-id="696d5-119">-Registry</span></span>
<span data-ttu-id="696d5-120">Oggetto Container Registry.</span><span class="sxs-lookup"><span data-stu-id="696d5-120">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="696d5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696d5-121">-ResourceGroupName</span></span>
<span data-ttu-id="696d5-122">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="696d5-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="696d5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="696d5-123">-ResourceId</span></span>
<span data-ttu-id="696d5-124">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="696d5-124">The container registry resource id</span></span>

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

### <span data-ttu-id="696d5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696d5-125">CommonParameters</span></span>
<span data-ttu-id="696d5-126">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="696d5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696d5-127">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="696d5-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696d5-128">INPUT</span><span class="sxs-lookup"><span data-stu-id="696d5-128">INPUTS</span></span>

### <span data-ttu-id="696d5-129">System.String</span><span class="sxs-lookup"><span data-stu-id="696d5-129">System.String</span></span>

## <span data-ttu-id="696d5-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="696d5-130">OUTPUTS</span></span>

### <span data-ttu-id="696d5-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="696d5-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="696d5-132">NOTE</span><span class="sxs-lookup"><span data-stu-id="696d5-132">NOTES</span></span>

## <span data-ttu-id="696d5-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="696d5-133">RELATED LINKS</span></span>

[<span data-ttu-id="696d5-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="696d5-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="696d5-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="696d5-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="696d5-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="696d5-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)

