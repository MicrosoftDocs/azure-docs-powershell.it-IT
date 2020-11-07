---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryCredential.md
ms.openlocfilehash: 89b3f47953c4074088c1ae5e2cf8e5f51ff383e9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/29/2020
ms.locfileid: "93675092"
---
# <span data-ttu-id="e2a35-101">Get-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e2a35-101">Get-AzContainerRegistryCredential</span></span>

## <span data-ttu-id="e2a35-102">Sinossi</span><span class="sxs-lookup"><span data-stu-id="e2a35-102">SYNOPSIS</span></span>
<span data-ttu-id="e2a35-103">Ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a35-103">Gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="e2a35-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="e2a35-104">SYNTAX</span></span>

### <span data-ttu-id="e2a35-105">NameResourceGroupParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="e2a35-105">NameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryCredential [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e2a35-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a35-106">RegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryCredential -Registry <PSContainerRegistry> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e2a35-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2a35-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryCredential -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e2a35-108">Descrizione</span><span class="sxs-lookup"><span data-stu-id="e2a35-108">DESCRIPTION</span></span>
<span data-ttu-id="e2a35-109">Il cmdlet Get-AzContainerRegistryCredential ottiene le credenziali di accesso per un registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a35-109">The Get-AzContainerRegistryCredential cmdlet gets the login credentials for a container registry.</span></span>

## <span data-ttu-id="e2a35-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="e2a35-110">EXAMPLES</span></span>

### <span data-ttu-id="e2a35-111">Esempio 1: ottenere le credenziali di accesso per un registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="e2a35-111">Example 1: Get the login credentials for a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryCredential -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

Username   Password                         Password2
--------   --------                         ---------
MyRegistry +Y+==B==KdT=YV=ZgH=p/zQ/e1sNQq/d //JRPkgxx+r+z/ztU=R//E==vum=pRKL
```

<span data-ttu-id="e2a35-112">Questo comando ottiene le credenziali di accesso per il registro di sistema contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="e2a35-112">This command gets the login credentials for the specified container registry.</span></span>
<span data-ttu-id="e2a35-113">L'utente di amministratore deve essere abilitato per il registro \` di sistema Registry \` per ottenere le credenziali di accesso.</span><span class="sxs-lookup"><span data-stu-id="e2a35-113">Admin user has to be enabled for the container registry \`MyRegistry\` to get login credentials.</span></span>

## <span data-ttu-id="e2a35-114">PARAMETRI</span><span class="sxs-lookup"><span data-stu-id="e2a35-114">PARAMETERS</span></span>

### <span data-ttu-id="e2a35-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2a35-115">-DefaultProfile</span></span>
<span data-ttu-id="e2a35-116">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="e2a35-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e2a35-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="e2a35-117">-Name</span></span>
<span data-ttu-id="e2a35-118">Nome del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a35-118">Container Registry Name.</span></span>

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

### <span data-ttu-id="e2a35-119">-Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="e2a35-119">-Registry</span></span>
<span data-ttu-id="e2a35-120">Oggetto del registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="e2a35-120">Container Registry Object.</span></span>

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

### <span data-ttu-id="e2a35-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2a35-121">-ResourceGroupName</span></span>
<span data-ttu-id="e2a35-122">Nome del gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="e2a35-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="e2a35-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2a35-123">-ResourceId</span></span>
<span data-ttu-id="e2a35-124">ID risorsa del registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="e2a35-124">The container registry resource id</span></span>

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

### <span data-ttu-id="e2a35-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2a35-125">CommonParameters</span></span>
<span data-ttu-id="e2a35-126">Questo cmdlet supporta i parametri comuni:-debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e2a35-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2a35-127">Per altre informazioni, Vedi [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e2a35-127">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2a35-128">INGRESSI</span><span class="sxs-lookup"><span data-stu-id="e2a35-128">INPUTS</span></span>

### <span data-ttu-id="e2a35-129">System. String</span><span class="sxs-lookup"><span data-stu-id="e2a35-129">System.String</span></span>

## <span data-ttu-id="e2a35-130">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="e2a35-130">OUTPUTS</span></span>

### <span data-ttu-id="e2a35-131">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e2a35-131">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryCredential</span></span>

## <span data-ttu-id="e2a35-132">Note</span><span class="sxs-lookup"><span data-stu-id="e2a35-132">NOTES</span></span>

## <span data-ttu-id="e2a35-133">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="e2a35-133">RELATED LINKS</span></span>

[<span data-ttu-id="e2a35-134">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a35-134">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="e2a35-135">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="e2a35-135">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="e2a35-136">Update-AzContainerRegistryCredential</span><span class="sxs-lookup"><span data-stu-id="e2a35-136">Update-AzContainerRegistryCredential</span></span>](Update-AzContainerRegistryCredential.md)
