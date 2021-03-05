---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistry.md
ms.openlocfilehash: 969e37173c487b2ed3ee4ab6dad5374208f5ff27
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004446"
---
# <span data-ttu-id="f95c0-101">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f95c0-101">Get-AzContainerRegistry</span></span>

## <span data-ttu-id="f95c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f95c0-102">SYNOPSIS</span></span>
<span data-ttu-id="f95c0-103">Ottiene un registro del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f95c0-103">Gets a container registry.</span></span>

## <span data-ttu-id="f95c0-104">SINTASSI</span><span class="sxs-lookup"><span data-stu-id="f95c0-104">SYNTAX</span></span>

### <span data-ttu-id="f95c0-105">ListRegistriesParameterSet (impostazione predefinita)</span><span class="sxs-lookup"><span data-stu-id="f95c0-105">ListRegistriesParameterSet (Default)</span></span>
```
Get-AzContainerRegistry [[-ResourceGroupName] <String>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95c0-106">RegistryNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95c0-106">RegistryNameParameterSet</span></span>
```
Get-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f95c0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f95c0-107">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistry [-IncludeDetail] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f95c0-108">DESCRIZIONE</span><span class="sxs-lookup"><span data-stu-id="f95c0-108">DESCRIPTION</span></span>
<span data-ttu-id="f95c0-109">Il Get-AzContainerRegistry cmdlet ottiene un registro contenitore specificato o tutti i registri dei contenitori in un gruppo di risorse o nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f95c0-109">The Get-AzContainerRegistry cmdlet gets a specified container registry or all the container registries in a resource group or the subscription.</span></span>

## <span data-ttu-id="f95c0-110">ESEMPI</span><span class="sxs-lookup"><span data-stu-id="f95c0-110">EXAMPLES</span></span>

### <span data-ttu-id="f95c0-111">Esempio 1: Ottenere un contenitore specificato nel Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="f95c0-111">Example 1: Get a specified container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="f95c0-112">Questo comando ottiene il Registro di sistema del contenitore specificato.</span><span class="sxs-lookup"><span data-stu-id="f95c0-112">This command gets the specified container registry.</span></span>

### <span data-ttu-id="f95c0-113">Esempio 2: Ottenere tutti i registri dei contenitori in un gruppo di risorse</span><span class="sxs-lookup"><span data-stu-id="f95c0-113">Example 2: Get all the container registries in a resource group</span></span>
```powershell
PS C:\>Get-AzContainerRegistry -ResourceGroupName "MyResourceGroup"

   Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="f95c0-114">Questo comando recupera tutti i registri dei contenitori in un gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f95c0-114">This command gets all the container registries in a resource group.</span></span>

### <span data-ttu-id="f95c0-115">Esempio 3: Ottenere tutti i registri dei contenitori nella sottoscrizione</span><span class="sxs-lookup"><span data-stu-id="f95c0-115">Example 3:  Get all the container registries in the subscription</span></span>
```powershell
PS C:\>Get-AzContainerRegistry

  Container registry location: westus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True


   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry1       Premium    myregistry1.azurecr.io    10/31/2017 6:29:31 PM      Succeeded  True
```

<span data-ttu-id="f95c0-116">Questo comando recupera tutti i registri dei contenitori nella sottoscrizione.</span><span class="sxs-lookup"><span data-stu-id="f95c0-116">This command gets all the container registries in the subscription.</span></span>

## <span data-ttu-id="f95c0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f95c0-117">PARAMETERS</span></span>

### <span data-ttu-id="f95c0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f95c0-118">-DefaultProfile</span></span>
<span data-ttu-id="f95c0-119">Credenziali, account, tenant e abbonamento usati per la comunicazione con Azure</span><span class="sxs-lookup"><span data-stu-id="f95c0-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f95c0-120">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="f95c0-120">-IncludeDetail</span></span>
<span data-ttu-id="f95c0-121">Visualizzare altri dettagli sul Registro di sistema del contenitore.</span><span class="sxs-lookup"><span data-stu-id="f95c0-121">Show more details about the container registry.</span></span>

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

### <span data-ttu-id="f95c0-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f95c0-122">-Name</span></span>
<span data-ttu-id="f95c0-123">Nome del Registro di sistema contenitore.</span><span class="sxs-lookup"><span data-stu-id="f95c0-123">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95c0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f95c0-124">-ResourceGroupName</span></span>
<span data-ttu-id="f95c0-125">Nome gruppo di risorse.</span><span class="sxs-lookup"><span data-stu-id="f95c0-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListRegistriesParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: RegistryNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f95c0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f95c0-126">-ResourceId</span></span>
<span data-ttu-id="f95c0-127">ID risorsa del Registro di sistema contenitore</span><span class="sxs-lookup"><span data-stu-id="f95c0-127">The container registry resource id</span></span>

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

### <span data-ttu-id="f95c0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f95c0-128">CommonParameters</span></span>
<span data-ttu-id="f95c0-129">Questo cmdlet supporta i parametri comuni: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutAction, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f95c0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f95c0-130">Per altre informazioni, [vedere](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f95c0-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f95c0-131">INPUT</span><span class="sxs-lookup"><span data-stu-id="f95c0-131">INPUTS</span></span>

### <span data-ttu-id="f95c0-132">System.String</span><span class="sxs-lookup"><span data-stu-id="f95c0-132">System.String</span></span>

## <span data-ttu-id="f95c0-133">OUTPUT</span><span class="sxs-lookup"><span data-stu-id="f95c0-133">OUTPUTS</span></span>

### <span data-ttu-id="f95c0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f95c0-134">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f95c0-135">NOTE</span><span class="sxs-lookup"><span data-stu-id="f95c0-135">NOTES</span></span>

## <span data-ttu-id="f95c0-136">COLLEGAMENTI CORRELATI</span><span class="sxs-lookup"><span data-stu-id="f95c0-136">RELATED LINKS</span></span>

[<span data-ttu-id="f95c0-137">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f95c0-137">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="f95c0-138">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f95c0-138">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="f95c0-139">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f95c0-139">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

